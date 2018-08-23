---
title: Syntaxe XAML en détail
ms.date: 03/30/2017
helpviewer_keywords:
- XML [WPF], namespaces
- XAML [WPF], parsing of attributes
- parsing of attributes [WPF]
- XAML [WPF], markup extensions
- attached properties [WPF]
- tag syntax [XAML]
- markup extensions [WPF]
- XAML [WPF], object element syntax
- XAML [WPF], syntax terminology
- attached events [WPF]
- lookup semantics [WPF]
- XAML [WPF], attached events
- XAML [WPF], content syntax
- XAML [WPF], lookup semantics
- content syntax [WPF]
- object element syntax [WPF]
- syntax terminology [XAML]
- XAML [WPF], attached properties
- attributes [XAML], parsing
- XAML [WPF], tag syntax
- XAML [WPF], attribute syntax
- property element syntax [WPF]
- terminology [XAML]
- namespaces [WPF], XML
- attribute syntax [XAML]
- XAML [WPF], property element syntax
ms.assetid: 67cce290-ca26-4c41-a797-b68aabc45479
ms.openlocfilehash: f2c3aab20dc5bcf9b0f9f7053323ccd7a04443cc
ms.sourcegitcommit: bd4fa78f5a46133efdead1bc692a9aa2811d7868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "42755049"
---
# <a name="xaml-syntax-in-detail"></a>Syntaxe XAML en détail
Cette rubrique définit les termes qui sont utilisés pour décrire les éléments de syntaxe XAML. Ces termes sont utilisés fréquemment dans le reste de cette documentation, à la fois pour la documentation WPF spécifiquement et pour les autres infrastructures qui utilisent XAML ou les concepts XAML de base activées par la prise en charge du langage XAML au niveau de System.Xaml. Cette rubrique s’appuie sur la terminologie de base introduite dans la rubrique [vue d’ensemble de XAML (WPF)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md).  
  

  
<a name="the_xaml_language_specification"></a>   
## <a name="the-xaml-language-specification"></a>La spécification du langage XAML  
 La terminologie de syntaxe XAML définie ici est également définie ou référencée dans la spécification du langage XAML. XAML est un langage basé sur XML et suit ou développe des règles de structure XML. La terminologie est partagé à partir d’ou repose sur la terminologie utilisée couramment lorsque vous décrivez le langage XML ou le modèle d’objet de document XML.  
  
 Pour plus d’informations sur la spécification du langage XAML, téléchargez [ \[MS-XAML\] ](http://go.microsoft.com/fwlink/?LinkId=114525) à partir du Microsoft Download Center.  
  
<a name="xaml_and_clr"></a>   
## <a name="xaml-and-clr"></a>XAML et CLR  
 XAML est un langage de balisage. Le [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)], comme son nom, permet l’exécution du runtime. XAML n’est pas en soi un des langages courants directement utilisable par le runtime CLR. Au lieu de cela, vous pouvez considérer XAML comme prenant en charge son propre système de type. Le système d’analyse XAML particulier qui est utilisé par WPF repose sur le CLR et le système de type CLR. Les types XAML sont mappés aux types CLR pour instancier une représentation sous forme de l’exécution lorsque le XAML pour WPF est analysé. Pour cette raison, le reste de la présentation de la syntaxe dans ce document comprend des références au système de type CLR, bien que les discussions de syntaxe équivalente dans la spécification du langage XAML ne le faites pas. (Par niveau de la spécification du langage XAML, les types XAML peuvent être mappés à n’importe quel autre système de type, qui ne devra pas être le CLR, mais qui nécessiterait la création et l’utilisation d’un analyseur XAML différent.)  
  
#### <a name="members-of-types-and-class-inheritance"></a>Membres de Types et de l’héritage de classes  
 Propriétés et événements dès qu’elles apparaissent en tant que membres XAML d’un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] type sont souvent hérités de types de base. Par exemple, prenons l’exemple suivant : `<Button Background="Blue" .../>`. Le <xref:System.Windows.Controls.Control.Background%2A> propriété n’est pas une propriété déclarée immédiatement sur le <xref:System.Windows.Controls.Button> classe, si vous deviez examiner la définition de classe, les résultats de la réflexion ou la documentation. Au lieu de cela, <xref:System.Windows.Controls.Control.Background%2A> est héritée de la base de <xref:System.Windows.Controls.Control> classe.  
  
 Le comportement d’héritage de classe de [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] les éléments XAML est une divergence importante par rapport à partir d’une interprétation schéma du balisage XML. L’héritage de classe peut s’avérer complexe, en particulier lorsque les classes de base intermédiaires sont abstraites, ou lorsque des interfaces sont impliquées. Il s’agit d’une seule raison pour laquelle l’ensemble des éléments XAML et leurs attributs autorisés est difficile de représenter précisément et complètement l’utilisation des types de schéma qui est généralement utilisé pour [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] de programmation, telles que format DTD ou XSD. Une autre raison est qu’extensibilité et les fonctionnalités de mappage de type du langage XAML lui-même excluent l’exhaustivité de toute représentation fixe pour les types et membres autorisés.  
  
<a name="object_element_syntax"></a>   
## <a name="object-element-syntax"></a>Syntaxe de l’élément objet  
 *Syntaxe d’élément de l’objet* est la syntaxe de balisage XAML qui instancie une structure ou une classe CLR en déclarant un élément XML. Cette syntaxe ressemble à la syntaxe d’élément d’autres langages de balisage tels que HTML. Syntaxe d’élément objet commence par un crochet pointu (\<), suivi immédiatement par le nom de type de la classe ou structure en cours d’instanciation. Zéro ou plusieurs espaces peuvent suivre le nom de type, et zéro ou plusieurs attributs peuvent également être déclarées sur l’élément objet, avec un ou plusieurs espaces séparant chaque nom d’attribut = paire « valeur ». Enfin, il se peut que parmi les options suivantes doit être remplie :  
  
-   L’élément et la balise doivent être fermées par une barre oblique (/) suivie immédiatement par un crochet angulaire à droite (>).  
  
-   La balise d’ouverture doit être complétée par un crochet angulaire à droite (>). Autres éléments objet, éléments de propriété ou texte interne, pouvez suivre la balise d’ouverture. Exactement le contenu qui peut-être être contenu ici est généralement limité par le modèle objet de l’élément. L’équivalent de balise de fermeture pour l’élément objet doit également exister dans une imbrication correcte et équilibre avec d’autres paires de balises d’ouverture et de fermeture.  
  
 XAML tel qu’implémenté par .NET possède un ensemble de règles qui mappent des éléments object en types, les attributs dans des propriétés ou des événements et des espaces de noms XAML pour les espaces de noms CLR et assembly. Mappent les éléments d’objet XAML pour WPF et .NET Framework, à [!INCLUDE[TLA#tla_net](../../../../includes/tlasharptla-net-md.md)] types, comme défini dans les assemblys référencés et les attributs sont mappés aux membres de ces types. Lorsque vous référencez un type CLR dans XAML, vous avez accès aux membres hérités de ce type.  
  
 Par exemple, l’exemple suivant est la syntaxe d’élément objet qui instancie une nouvelle instance de la <xref:System.Windows.Controls.Button> classe et spécifie également un <xref:System.Windows.FrameworkElement.Name%2A> attribut et une valeur pour cet attribut :  
  
 [!code-xaml[XAMLOvwSupport#SyntaxOE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/XAMLOvwSupport/CSharp/Page1.xaml#syntaxoe)]  
  
 L’exemple suivant est la syntaxe d’élément objet qui inclut également la syntaxe de propriété de contenu XAML. Le texte interne contenu dans permet de définir le <xref:System.Windows.Controls.TextBox> propriété de contenu XAML, <xref:System.Windows.Controls.TextBox.Text%2A>.  
  
 [!code-xaml[XAMLOvwSupport#ThisIsATextBox](../../../../samples/snippets/csharp/VS_Snippets_Wpf/XAMLOvwSupport/CSharp/Page1.xaml#thisisatextbox)]  
  
### <a name="content-models"></a>Modèles de contenu  
 Une classe peut prendre en charge une utilisation comme un élément d’objet XAML en termes de la syntaxe, mais cet élément fonctionnera correctement dans une application ou d’une page lorsqu’il est placé dans un emplacement attendu d’une arborescence de modèle ou d’élément de contenu global. Par exemple, un <xref:System.Windows.Controls.MenuItem> ne peut généralement être placé en tant qu’enfant d’un <xref:System.Windows.Controls.Primitives.MenuBase> classe dérivée comme <xref:System.Windows.Controls.Menu>. Contenu des modèles pour des éléments spécifiques sont documentés dans le cadre des notes sur les pages de la classe de contrôles et d’autres [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] classes qui peuvent être utilisées en tant qu’éléments XAML.  
  
<a name="properties_of_object_elements"></a>   
## <a name="properties-of-object-elements"></a>Propriétés des éléments de l’objet  
 Propriétés dans XAML sont définies par diverses syntaxes possibles. La syntaxe peut être utilisée pour une propriété particulière varie, selon les caractéristiques de système de type sous-jacent de la propriété que vous définissez.  
  
 En définissant les valeurs des propriétés, vous ajoutez des fonctionnalités ou des caractéristiques aux objets tels qu’ils existent dans le graphique d’objet moment de l’exécution. L’état initial de l’objet créé à partir d’un élément objet est basé sur le comportement du constructeur par défaut. En règle générale, votre application utilisera autre chose qu’une instance entièrement par défaut d’un objet donné.  
  
<a name="attribute_syntax_properties"></a>   
## <a name="attribute-syntax-properties"></a>Syntaxe d’attribut (Propriétés)  
 Syntaxe d’attribut est la syntaxe de balisage XAML qui définit une valeur pour une propriété en déclarant un attribut sur un élément objet existant. Le nom d’attribut doit correspondre au nom de membre CLR de la propriété de la classe qui stocke l’élément objet appropriée. Le nom d’attribut est suivi d’un opérateur d’assignation (=). La valeur d’attribut doit être une chaîne placée entre guillemets.  
  
> [!NOTE]
>  Vous pouvez utiliser des guillemets doubles en alternance pour placer un guillemet littéral au sein d’un attribut. Par exemple, vous pouvez utiliser les guillemets simples comme un moyen pour déclarer une chaîne qui contient un caractère de guillemet double qu’il contient. Si vous utilisez des guillemets simples ou doubles, vous devez utiliser une paire correspondante pour l’ouverture et fermeture de la chaîne de valeur d’attribut. Il existe également les séquences d’échappement ou autres techniques disponibles pour contourner les restrictions de caractères imposées par toute syntaxe XAML particulière. Consultez [entités de caractères XML et XAML](../../../../docs/framework/xaml-services/xml-character-entities-and-xaml.md).  
  
 Pour pouvoir être définie via la syntaxe d’attribut, une propriété doit être publique et doit être accessible en écriture. La valeur de la propriété dans le système de type de stockage doit être un type valeur, ou doit être un type référence qui peut être instancié ou référencé par un processeur XAML lors de l’accès au type de stockage.  
  
 Pour les événements de WPF XAML, l’événement qui est référencé en tant que le nom d’attribut doit être publique et avoir un délégué public.  
  
 La propriété ou l’événement doit être un membre de la classe ou structure qui est instancié par l’élément objet contenant.  
  
### <a name="processing-of-attribute-values"></a>Traitement des valeurs d’attribut  
 La valeur de chaîne contenue dans l’ouverture et le guillemet anglais fermant est traitée par un processeur XAML. Pour les propriétés, le comportement de traitement par défaut est déterminée par le type de la propriété CLR sous-jacente.  
  
 La valeur d’attribut est renseignée par l’une des opérations suivantes, à l’aide de cet ordre de traitement :  
  
1.  Si le processeur XAML rencontre une accolade, ou un élément objet qui dérive de <xref:System.Windows.Markup.MarkupExtension>, puis l’extension de balisage référencée est évaluée en premier au lieu de la valeur sous forme de chaîne de traitement et l’objet retourné par l’extension de balisage est utilisé comme le valeur. Dans de nombreux cas, l’objet retourné par une extension de balisage sera une référence à un objet existant, ou une expression qui diffère l’évaluation jusqu’au moment de l’exécution et n’est pas un objet qui vient d’être instancié.  
  
2.  Si la propriété est déclarée avec un <xref:System.ComponentModel.TypeConverter>, ou le type de valeur de cette propriété est déclaré avec un <xref:System.ComponentModel.TypeConverter>, la valeur de chaîne de l’attribut est envoyée au convertisseur de type en tant qu’entrée de conversion et le convertisseur retourne un nouvelle instance d’objet.  
  
3.  S’il existe aucune <xref:System.ComponentModel.TypeConverter>, une conversion directe pour le type de propriété est tentée. Ce dernier niveau est une conversion directe à la valeur de l’analyseur natif entre les types primitifs du langage XAML, ou d’une vérification pour les noms de constantes nommées dans une énumération (l’analyseur accède ensuite aux valeurs correspondantes).  
  
#### <a name="enumeration-attribute-values"></a>Valeurs d’attribut énumération  
 Énumérations dans XAML sont traitées intrinsèquement par les analyseurs XAML, et les membres d’une énumération doivent être spécifiés en spécifiant le nom de chaîne de l’une des constantes nommées de l’énumération.  
  
 Pour les valeurs d’énumération nonflag, le comportement natif doit traiter la chaîne d’une valeur d’attribut et de le résoudre à une des valeurs d’énumération. Vous ne spécifiez pas l’énumération au format *énumération*. *Valeur*, comme vous le feriez dans le code. Au lieu de cela, vous spécifiez uniquement *valeur*, et *énumération* est déduit par le type de la propriété que vous définissez. Si vous spécifiez un attribut dans le *énumération*. *Valeur* , il ne sera pas correctement résolu.  
  
 Pour les énumérations, le comportement est basé sur le <xref:System.Enum.Parse%2A?displayProperty=nameWithType> (méthode). Vous pouvez spécifier plusieurs valeurs pour une énumération d’indicateurs en séparant chaque valeur par une virgule. Toutefois, vous ne pouvez pas combiner des valeurs d’énumération qui ne sont pas flagwise. Par exemple, vous ne pouvez pas utiliser la syntaxe de virgule pour tenter de créer un <xref:System.Windows.Trigger> qui agit sur plusieurs conditions d’une énumération nonflag :  
  
```  
<!--This will not compile, because Visibility is not a flagwise enumeration.-->  
...  
<Trigger Property="Visibility" Value="Collapsed,Hidden">  
  <Setter ... />  
</Trigger>  
...  
```  
  
 Les énumérations qui prennent en charge les attributs qui peuvent être définies dans XAML sont rares dans WPF. Toutefois, une telle énumération est <xref:System.Windows.Media.StyleSimulations>. Vous pouvez, par exemple, utiliser la syntaxe d’attribut de comportant des indicateurs délimitée par des virgules pour modifier l’exemple fourni dans la section Notes pour la <xref:System.Windows.Documents.Glyphs> classe ; `StyleSimulations = "BoldSimulation"` peut devenir `StyleSimulations = "BoldSimulation,ItalicSimulation"`. <xref:System.Windows.Input.KeyBinding.Modifiers%2A?displayProperty=nameWithType> est une autre propriété où vous pouvez spécifier plusieurs valeurs d’énumération. Toutefois, cette propriété se trouve être un cas spécial, car le <xref:System.Windows.Input.ModifierKeys> énumération prend en charge son propre convertisseur de type. Le convertisseur de type pour les modificateurs utilise un signe plus (+) comme séparateur au lieu d’une virgule (,). Cette conversion prend en charge la syntaxe plus traditionnelle pour représenter des combinaisons de touches dans la programmation de Microsoft Windows, tels que « Ctrl + Alt ».  
  
### <a name="properties-and-event-member-name-references"></a>Propriétés et événements les références de nom de membre  
 Lorsque vous spécifiez un attribut, vous pouvez référencer une propriété ou un événement qui existe en tant que membre du type CLR instancié pour l’élément objet contenant.  
  
 Ou bien, vous pouvez référencer une propriété jointe ou événement attaché, indépendamment de l’élément objet contenant. (Les propriétés jointes sont présentées dans une section à venir.)  
  
 Vous pouvez également nommer un événement à partir de n’importe quel objet qui est accessible via l’espace de noms par défaut en utilisant un *typeName*. *événement* nom partiellement qualifié ; cette syntaxe prend en charge l’attachement des gestionnaires d’événements routés où le gestionnaire doit gérer les événements de routage à partir des éléments enfants, mais l’élément parent ne dispose pas de cet événement dans la table de membres. Cette syntaxe ressemble à une syntaxe d’événement attaché, mais l’événement ici n’est pas un événement attaché true. Au lieu de cela, vous faites référence à un événement avec un nom qualifié. Pour plus d’informations, consultez [vue d’ensemble des événements routés](../../../../docs/framework/wpf/advanced/routed-events-overview.md).  
  
 Dans certains scénarios, les noms de propriété sont parfois fournies en tant que la valeur d’un attribut, plutôt que le nom d’attribut. Nom de cette propriété peut également inclure des qualificateurs, tels que la propriété spécifiée sous la forme *TypePropriétaire*. *dependencyPropertyName*. Ce scénario est courant lors de l’écriture des styles ou les modèles dans XAML. Les règles de traitement pour les noms de propriété fournies comme valeur d’attribut sont différentes et sont régis par le type de la propriété qui est définie ou par les comportements de sous-systèmes WPF particuliers. Pour plus d’informations, consultez [Styling and Templating](../../../../docs/framework/wpf/controls/styling-and-templating.md).  
  
 Une autre utilisation des noms de propriétés est lorsqu’une valeur d’attribut décrit une relation de propriété de la propriété. Cette fonctionnalité est utilisée pour la liaison de données et pour les cibles de la table de montage séquentiel et est activée par le <xref:System.Windows.PropertyPath> classe et son convertisseur de type. Pour obtenir une description plus complète de la sémantique de recherche, consultez [syntaxe XAML de PropertyPath](../../../../docs/framework/wpf/advanced/propertypath-xaml-syntax.md).  
  
<a name="property_element_syntax"></a>   
## <a name="property-element-syntax"></a>Syntaxe des éléments de propriété  
 *Syntaxe d’élément de propriété* est une syntaxe qui diffère quelque peu les règles de syntaxe de base XML pour les éléments. Dans XML, la valeur d’un attribut est une chaîne de facto, la seule variante possible étant le format d’encodage de chaîne est utilisé. Dans XAML, vous pouvez affecter les autres éléments de l’objet sur la valeur d’une propriété. Cette fonctionnalité est activée par la syntaxe d’élément de propriété. Au lieu de la propriété qui est spécifiée en tant qu’attribut au sein de la balise d’élément, la propriété est spécifiée à l’aide d’un élément d’ouverture de balise dans *format elementTypeName*. *propertyName* formulaire, la valeur de la propriété est spécifiée et ensuite l’élément de propriété est fermé.  
  
 Plus précisément, la syntaxe commence par un crochet pointu (\<), suivi immédiatement par le nom de type de la classe ou structure contenue dans la syntaxe d’élément de propriété. Cela est immédiatement suivi par un point (.), puis le nom d’une propriété, puis par un crochet angulaire à droite (>). Comme avec la syntaxe d’attribut, cette propriété doit exister dans les membres déclarés publics du type spécifié. La valeur à assigner à la propriété est contenue dans l’élément de propriété. En règle générale, la valeur est fournie à une ou plusieurs éléments objet, car la spécification d’objets en tant que valeurs est le scénario de cette syntaxe d’élément de propriété est destinée à aborder. Enfin, une balise de fermeture équivalent en spécifiant les mêmes *format elementTypeName*. *propertyName* combinaison doit être fournie, dans l’imbrication appropriée et le solde avec d’autres balises d’élément.  
  
 Par exemple, ce qui suit est la syntaxe d’élément de propriété pour le <xref:System.Windows.FrameworkElement.ContextMenu%2A> propriété d’un <xref:System.Windows.Controls.Button>.  
  
 [!code-xaml[XAMLOvwSupport#ContextMenu](../../../../samples/snippets/csharp/VS_Snippets_Wpf/XAMLOvwSupport/CSharp/Page1.xaml#contextmenu)]  
  
 La valeur dans un élément de propriété peut également être indiquée en tant que texte interne, dans les cas où le type de propriété spécifié est un type valeur primitif, tel que <xref:System.String>, ou une énumération dans laquelle un nom est spécifié. Ces deux utilisations sont quelque peu rares, étant donné que chacun de ces cas peut également utiliser une syntaxe d’attribut plus simple. Un scénario de remplissage d’un élément de propriété avec une chaîne est pour les propriétés qui ne sont pas la propriété de contenu XAML, mais qui sont toujours utilisées pour la représentation sous forme de texte de l’interface utilisateur, et certains éléments d’espaces blancs tels que les sauts de ligne sont nécessaires pour apparaître dans ce texte de l’interface utilisateur. Syntaxe d’attribut ne peut pas conserver les sauts de ligne, contrairement à la syntaxe d’élément de propriété, tant que conservation de l’espace blanc significative est active (pour plus d’informations, consultez [traitement dans XAML des espaces blancs](../../../../docs/framework/xaml-services/whitespace-processing-in-xaml.md)). Un autre scénario est afin que [Directive x : Uid](../../../../docs/framework/xaml-services/x-uid-directive.md) peut être appliqué à l’élément de propriété et marque donc la valeur comme une valeur qui doit être localisée dans WPF sortie BAML ou par d’autres techniques.  
  
 Un élément de propriété n’est pas représenté dans l’arborescence logique WPF. Un élément de propriété est simplement une syntaxe particulière pour la définition d’une propriété et n’est pas un élément qui possède une instance ou un objet. (Pour plus d’informations sur le concept d’arborescence logique, consultez [arborescences dans WPF](../../../../docs/framework/wpf/advanced/trees-in-wpf.md).)  
  
 Pour les propriétés où attribut et propriété de syntaxe d’élément sont prises en charge, les deux syntaxes ont généralement le même résultat, même si les subtilités telle que la gestion de l’espace blanc peuvent varier légèrement entre les syntaxes.  
  
<a name="collection_syntax"></a>   
## <a name="collection-syntax"></a>Syntaxe des collections  
 La spécification de XAML requiert des implémentations de processeur XAML pour identifier les propriétés dont le type de valeur est une collection. L’implémentation du processeur XAML générale dans .NET est basée sur du code managé et le CLR, et il identifie les types de collections via une des opérations suivantes :  
  
-   Type implémente <xref:System.Collections.IList>.  
  
-   Type implémente <xref:System.Collections.IDictionary>.  
  
-   Type dérive <xref:System.Array> (pour plus d’informations sur les tableaux en XAML, consultez [x : Array Markup Extension](../../../../docs/framework/xaml-services/x-array-markup-extension.md).)  
  
 Si le type d’une propriété est une collection, le type de collection déduit doit-elle pas être spécifié dans le balisage en tant qu’objet élément. Au lieu de cela, les éléments qui sont destinés à devenir des éléments de la collection sont spécifiés comme un ou plusieurs éléments enfants de l’élément de propriété. Chacun de ces éléments est évaluée à un objet pendant le chargement et ajouté à la collection en appelant le `Add` méthode de la collection implicite. Par exemple, le <xref:System.Windows.Style.Triggers%2A> propriété du <xref:System.Windows.Style> prend le type de collection spécialisée <xref:System.Windows.TriggerCollection>, qui implémente <xref:System.Collections.IList>. Il n’est pas nécessaire instancier un <xref:System.Windows.TriggerCollection> élément objet dans le balisage. Au lieu de cela, vous spécifiez un ou plusieurs <xref:System.Windows.Trigger> éléments en tant qu’éléments dans le `Style.Triggers` élément de propriété, où <xref:System.Windows.Trigger> (ou une classe dérivée) est le type attendu comme type d’élément pour fortement typé et implicite <xref:System.Windows.TriggerCollection>.  
  
 [!code-xaml[XAMLOvwSupport#SyntaxPECollection](../../../../samples/snippets/csharp/VS_Snippets_Wpf/XAMLOvwSupport/CSharp/Page1.xaml#syntaxpecollection)]  
  
 Une propriété peut être un type de collection et la propriété de contenu XAML pour ce type et types dérivés, qui est abordé dans la section suivante de cette rubrique.  
  
 Un élément de collection implicite crée un membre dans la représentation sous forme de l’arborescence logique, même si elle n’apparaît pas dans le balisage en tant qu’élément. En général le constructeur du type parent effectue l’instanciation de la collection qui est une de ses propriétés, et la collection initialement vide devient partie intégrante de l’arborescence d’objets.  
  
> [!NOTE]
>  Les interfaces génériques de liste et dictionnaire (<xref:System.Collections.Generic.IList%601> et <xref:System.Collections.Generic.IDictionary%602>) ne sont pas pris en charge pour la détection de la collection. Toutefois, vous pouvez utiliser la <xref:System.Collections.Generic.List%601> classe comme classe de base, car il implémente <xref:System.Collections.IList> directement, ou <xref:System.Collections.Generic.Dictionary%602> comme classe de base, car il implémente <xref:System.Collections.IDictionary> directement.  
  
 Dans les pages de référence .NET pour les types de collection, cette syntaxe avec omission délibérée de l’élément objet pour une collection est parfois indiquée dans les sections de syntaxe XAML en tant que la syntaxe de Collection implicite.  
  
 À l’exception de l’élément racine, chaque objet dans un fichier XAML qui est imbriqué en tant qu’un élément enfant d’un autre élément est vraiment un élément qui est un ou les deux cas suivants : un membre d’une propriété de collection implicite de son élément parent , ou un élément qui spécifie la valeur de la propriété de contenu XAML pour l’élément parent (XAML contenu propriétés seront abordées dans une section à venir). En d’autres termes, la relation parent et éléments enfants dans une page de balisage est réellement un objet unique à la racine, et chaque élément d’objet sous la racine est une instance unique qui fournit une valeur de propriété du parent, ou un des éléments au sein d’une colonne LEXION est également une valeur de propriété de type de collection du parent. Ce concept de racine unique est courant avec XML et est fréquemment renforcé dans le comportement des API qui chargent XAML tel que <xref:System.Windows.Markup.XamlReader.Load%2A>.  
  
 L’exemple suivant est une syntaxe avec l’élément objet pour une collection (<xref:System.Windows.Media.GradientStopCollection>) spécifié explicitement.  
  
```xaml  
<LinearGradientBrush>  
  <LinearGradientBrush.GradientStops>  
    <GradientStopCollection>  
      <GradientStop Offset="0.0" Color="Red" />  
      <GradientStop Offset="1.0" Color="Blue" />  
    </GradientStopCollection>  
  </LinearGradientBrush.GradientStops>  
</LinearGradientBrush>  
```  
  
 Notez qu’il n’est pas toujours possible de déclarer explicitement la collection. Par exemple, essaie de déclarer <xref:System.Windows.TriggerCollection> explicitement dans présenté précédemment <xref:System.Windows.Style.Triggers%2A> exemple échouerait. La déclaration explicite de la collection nécessite que la classe de collection doit prendre en charge un constructeur par défaut, et <xref:System.Windows.TriggerCollection> n’a pas de constructeur par défaut.  
  
<a name="xaml_content_properties"></a>   
## <a name="xaml-content-properties"></a>Propriétés de contenu XAML  
 Syntaxe de contenu XAML est une syntaxe qui est activée uniquement sur les classes qui spécifient le <xref:System.Windows.Markup.ContentPropertyAttribute> dans le cadre de leur déclaration de classe. Le <xref:System.Windows.Markup.ContentPropertyAttribute> fait référence au nom de propriété qui est la propriété de contenu pour ce type d’élément (y compris les classes dérivées). Lors du traitement par un processeur XAML, les éléments enfants ou le texte interne qui se trouvent entre les balises d’ouverture et fermeture de l’élément objet sera affecté à la valeur de la propriété de contenu XAML pour cet objet. Vous êtes autorisé à spécifier les éléments de propriété explicite de la propriété de contenu, mais cette utilisation n’est pas généralement affichée dans les sections de syntaxe XAML dans la référence .NET. La technique explicite/détaillée a la valeur occasionnel pour clarifier le balisage ou une question de style de balisage, mais généralement une propriété de contenu vise à rationaliser le balisage afin que les éléments qui sont intuitivement un lien parent-enfant peuvent être imbriqués directement. Balises d’élément de propriété pour les autres propriétés sur un élément ne sont pas affectés en tant que « contenu » par une définition de langage XAML strict ; ils sont traités précédemment dans l’ordre de traitement de l’analyseur XAML et ne sont pas considérés comme « contenu ».  
  
### <a name="xaml-content-property-values-must-be-contiguous"></a>Les valeurs de propriété de contenu XAML doivent être contiguës  
 La valeur d’une propriété de contenu XAML doit figurer soit entièrement avant soit entièrement après tous les autres éléments de propriété sur cet élément objet. Cela est vrai si la valeur d’une propriété de contenu XAML est spécifiée sous forme de chaîne, ou en tant qu’un ou plusieurs objets. Par exemple, le balisage suivant n’analyse pas :  
  
```  
<Button>I am a   
  <Button.Background>Blue</Button.Background>  
  blue button</Button>  
```  
  
 C’est essentiellement non conforme, car si cette syntaxe ont été rendue explicite à l’aide de la syntaxe d’élément de propriété pour la propriété de contenu, puis la contenu propriété est définie à deux reprises :  
  
```xml  
<Button>  
  <Button.Content>I am a </Button.Content>  
  <Button.Background>Blue</Button.Background>  
  <Button.Content> blue button</Button.Content>  
</Button>  
```  
  
 Un exemple est si la propriété de contenu est une collection, et que les éléments enfants sont contenant des éléments de propriété :  
  
```xml  
<StackPanel>  
  <Button>This example</Button>  
  <StackPanel.Resources>  
    <SolidColorBrush x:Key="BlueBrush" Color="Blue"/>  
  </StackPanel.Resources>  
  <Button>... is illegal XAML</Button>  
</StackPanel>  
```  
  
<a name="content_properties_and_collection_syntax_combined"></a>   
## <a name="content-properties-and-collection-syntax-combined"></a>Combinaison des propriétés de contenu et de la syntaxe des collections  
 Pour accepter plusieurs éléments objet unique en tant que contenu, le type de la propriété de contenu doit être spécifiquement un type de collection. Comme pour la syntaxe d’élément de propriété pour les types de collection, un processeur XAML doit identifier les types qui sont des types de collection. Si un élément a une propriété de contenu XAML et le type de la propriété de contenu XAML est une collection, puis le type de collection implicite n’a pas besoin être spécifié dans le balisage en tant qu’objet élément et la propriété de contenu XAML n’a pas besoin d’être spécifiés comme un el de propriété organisation de l’affichage. Par conséquent, le modèle de contenu apparent dans le balisage peut désormais avoir plusieurs éléments enfants assignés en tant que le contenu. Voici la syntaxe de contenu pour un <xref:System.Windows.Controls.Panel> classe dérivée. Tous les <xref:System.Windows.Controls.Panel> classes dérivées établissent la propriété de contenu XAML pour être <xref:System.Windows.Controls.Panel.Children%2A>, ce qui nécessite une valeur de type <xref:System.Windows.Controls.UIElementCollection>.  
  
 [!code-xaml[XAMLOvwSupport#SyntaxContent](../../../../samples/snippets/csharp/VS_Snippets_Wpf/XAMLOvwSupport/CSharp/page5.xaml#syntaxcontent)]  
  
 Notez que ni l’élément de propriété pour <xref:System.Windows.Controls.Panel.Children%2A> ni l’élément de la <xref:System.Windows.Controls.UIElementCollection> est requis dans le balisage. Ceci est une fonctionnalité de conception de XAML afin que récursivement contenait des éléments qui définissent un [!INCLUDE[TLA2#tla_ui](../../../../includes/tla2sharptla-ui-md.md)] sont plus intuitivement représentée sous la forme d’une arborescence d’éléments imbriqués avec des relations parent-enfant immédiat, sans les balises d’élément de propriété qui interviennent ou collection d’objets. En fait, <xref:System.Windows.Controls.UIElementCollection> ne peut pas être spécifié explicitement dans le balisage en tant qu’élément objet, par conception. Étant donné que sa seule utilisation prévue est comme une collection implicite, <xref:System.Windows.Controls.UIElementCollection> n’expose pas de constructeur public par défaut et par conséquent ne peut pas être instancié comme un élément objet.  
  
### <a name="mixing-property-elements-and-object-elements-in-an-object-with-a-content-property"></a>Combinaison d’éléments de propriété et des éléments de l’objet dans un objet avec une propriété de contenu  
 La spécification XAML déclare qu’un processeur XAML peut appliquer que les éléments objet sont utilisées pour remplir la propriété de contenu XAML dans un élément objet doivent être contiguës et ne doivent pas être mélangées. Cette restriction par rapport à la combinaison d’éléments de propriété et de contenu est appliquée par le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] les processeurs XAML.  
  
 Vous pouvez avoir un élément objet enfant comme première balise immédiate dans un élément objet. Ensuite, vous pouvez introduire des éléments de propriété. Ou bien, vous pouvez spécifier un ou plusieurs éléments de propriété, puis contenu et autres éléments de propriété. Mais une fois qu’un élément de propriété suit le contenu, vous ne pouvez pas introduire d’autre contenu, vous pouvez uniquement ajouter des éléments de propriété.  
  
 Ce contenu / spécification ordre d’élément de propriété ne s’applique pas au texte interne utilisé en tant que contenu. Toutefois, il est toujours un style de balisage recommandé à garder le texte interne contigu, étant donné que les espaces blancs significatifs sera difficile de détecter visuellement dans le balisage si les éléments de propriété sont intercalés avec le texte interne.  
  
<a name="xaml_namespaces"></a>   
## <a name="xaml-namespaces"></a>Espaces de noms XAML  
 Aucun des exemples de syntaxe précédent spécifié un espace de noms XAML autre que l’espace de noms XAML par défaut. Dans type [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] applications, l’espace de noms XAML par défaut est spécifiée comme étant le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] espace de noms. Vous pouvez spécifier des espaces de noms XAML autre que l’espace de noms XAML par défaut et toujours utiliser une syntaxe similaire. Mais ensuite, n’importe où dans lequel une classe est nommée qui n’est pas accessible dans l’espace de noms XAML par défaut, ce nom de classe doit être précédé par le préfixe de l’espace de noms XAML comme mappé à l’espace de noms CLR correspondant. Par exemple, `<custom:Example/>` est la syntaxe d’élément objet pour instancier une instance de la `Example` (classe), où l’espace de noms CLR contenant cette classe (et éventuellement les informations d’assembly externe qui contient les types de stockage) a été précédemment mappée à la `custom` préfixe.  
  
 Pour plus d’informations sur les espaces de noms XAML, consultez [espaces de noms XAML et Namespace Mapping for WPF XAML](../../../../docs/framework/wpf/advanced/xaml-namespaces-and-namespace-mapping-for-wpf-xaml.md).  
  
<a name="markup_extensions"></a>   
## <a name="markup-extensions"></a>Extensions de balisage  
 XAML définit une extension de balisage programmation entité qui permet à un caractère d’échappement à partir de la gestion de processeur XAML normale de valeurs d’attribut de chaîne ou d’éléments de l’objet et diffère le traitement à une classe de stockage. Le caractère qui identifie une extension de balisage pour un processeur XAML à l’aide de la syntaxe d’attribut est l’accolade ouvrante ({}), suivie de n’importe quel caractère autre qu’une accolade fermante (}). La première chaîne suit l’accolade ouvrante doit faire référence à la classe qui fournit le comportement d’extension particulier, où la référence peut omettre la sous-chaîne « Extension » si celle-ci fait partie du nom de classe true. Par la suite, un espace unique peut sembler, et ensuite chaque caractère successif est utilisé en tant qu’entrée par l’implémentation d’extension, jusqu'à ce que l’accolade fermante est rencontrée.  
  
 L’implémentation XAML de .NET utilise le <xref:System.Windows.Markup.MarkupExtension> classe abstraite comme base pour toutes les extensions de balisage pris en charge par [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] , ainsi que d’autres infrastructures ou technologies. Les extensions de balisage qui [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] implémente spécifiquement est souvent destinées à fournir un moyen pour référencer d’autres objets existants, ou d’effectuer des références différées aux objets qui sont évaluées au moment de l’exécution. Par exemple, une liaison de données WPF simple s’effectue en spécifiant le `{Binding}` extension de balisage à la place de la valeur qu’une propriété particulière aurait normalement. La plupart des extensions de balisage WPF permettent une syntaxe d’attribut pour les propriétés où une syntaxe d’attribut serait autrement impossible. Par exemple, un <xref:System.Windows.Style> objet est un type relativement complexe qui contient une série imbriquée d’objets et propriétés. Les styles dans WPF sont généralement définies en tant que ressource dans un <xref:System.Windows.ResourceDictionary>, puis référencé via une des deux extensions de balisage qui demandent une ressource. L’extension de balisage qui diffère de la version d’évaluation de la valeur de propriété à une recherche de ressources et permet de fournir la valeur de la <xref:System.Windows.FrameworkElement.Style%2A> propriété, en prenant le type <xref:System.Windows.Style>, dans la syntaxe, comme dans l’exemple suivant d’attribut :  
  
 `<Button Style="{StaticResource MyStyle}">My button</Button>`  
  
 Ici, `StaticResource` identifie le <xref:System.Windows.StaticResourceExtension> classe qui fournit l’implémentation d’extension de balisage. La chaîne suivante `MyStyle` est utilisée comme entrée pour la non-valeur par défaut <xref:System.Windows.StaticResourceExtension> constructeur, où le paramètre récupéré à partir de la chaîne d’extension déclare demandé <xref:System.Windows.ResourceKey>. `MyStyle` est censé être le [x : Key](../../../../docs/framework/xaml-services/x-key-directive.md) valeur d’un <xref:System.Windows.Style> défini en tant que ressource. Le [Extension de balisage StaticResource](../../../../docs/framework/wpf/advanced/staticresource-markup-extension.md) utilisation demande que la ressource soit utilisée pour fournir la <xref:System.Windows.Style> valeur de propriété à travers la logique de recherche de ressources statiques au moment du chargement.  
  
 Pour plus d’informations sur les extensions de balisage, consultez [Extensions de balisage et XAML WPF](../../../../docs/framework/wpf/advanced/markup-extensions-and-wpf-xaml.md). Pour une référence d’extensions de balisage et d’autres fonctionnalités activées dans l’implémentation .NET XAML générale de la programmation de XAML, consultez [XAML Namespace (x :)) Fonctionnalités de langage](../../../../docs/framework/xaml-services/xaml-namespace-x-language-features.md). Pour les extensions de balisage spécifiques à WPF, consultez [les Extensions XAML WPF](../../../../docs/framework/wpf/advanced/wpf-xaml-extensions.md).  
  
<a name="attached_properties"></a>   
## <a name="attached-properties"></a>Propriétés jointes  
 Propriétés jointes sont un concept de programmation introduit dans XAML, par laquelle pouvez détenues et les propriétés définies par un type particulier, mais définies en tant qu’attributs ou éléments de propriété sur n’importe quel élément. Le scénario principal que les propriétés jointes sont utilisées pour consiste à permettre aux éléments enfants dans une structure de balisage pour signaler des informations à un élément parent sans avoir besoin d’un modèle d’objet largement partagée entre tous les éléments. À l’inverse, les propriétés jointes peuvent être utilisées par les éléments parents pour signaler des informations aux éléments enfants. Pour plus d’informations sur l’objectif de propriétés jointes et comment créer votre propre des propriétés jointes, consultez [vue d’ensemble des propriétés jointes](../../../../docs/framework/wpf/advanced/attached-properties-overview.md).  
  
 Les propriétés attachées utilisent une syntaxe qui ressemble en apparence à la syntaxe d’élément de propriété, dans la mesure où vous spécifiez également un *typeName*. *propertyName* combinaison. Il existe deux différences majeures :  
  
-   Vous pouvez utiliser la *typeName*. *propertyName* combinaison même lors de la définition d’une propriété jointe via la syntaxe d’attribut. Propriétés jointes sont que le seul cas où la qualification du nom de la propriété est une exigence dans une syntaxe d’attribut.  
  
-   Vous pouvez également utiliser la syntaxe d’élément de propriété pour les propriétés jointes. Toutefois, pour la syntaxe d’élément de propriété classique, le *typeName* que vous spécifiez est l’élément objet qui contient l’élément de propriété. Si vous faites référence à une propriété jointe, puis le *typeName* est la classe qui définit la propriété jointe, pas l’élément objet contenant.  
  
<a name="attached_events"></a>   
## <a name="attached-events"></a>Événements attachés  
 Événements attachés sont un autre concept de programmation XAML où les événements peuvent être définis par un type spécifique, mais les gestionnaires peuvent être joints à n’importe quel élément objet. Dans l’implémentation WOF, le type qui définit un événement attaché est souvent un type statique qui définit un service, et parfois, ces événements attachés sont exposés par un alias de l’événement routé dans les types qui exposent le service. Gestionnaires pour les événements attachés sont spécifiés via la syntaxe d’attribut. Comme avec les événements attachés, la syntaxe d’attribut est développée pour les événements attachés permettre une *typeName*. *eventName* utilisation, où *typeName* est la classe qui fournit `Add` et `Remove` accesseurs de gestionnaire d’événements pour l’infrastructure de l’événement attaché, et *eventName* est le nom de l’événement.  
  
<a name="anatomy_of_a_xaml_page_root_element"></a>   
## <a name="anatomy-of-a-xaml-root-element"></a>Anatomie d’un élément racine XAML  
 Le tableau suivant présente un type XAML élément racine ventilé, montrant les attributs spécifiques d’un élément racine :  
  
|||  
|-|-|  
|`<Page`|Élément objet d’ouverture de l’élément racine|  
|`xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"`|La valeur par défaut ([!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]) espace de noms XAML|  
|`xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"`|L’espace de noms XAML du langage XAML|  
|`x:Class="ExampleNamespace.ExampleCode"`|La déclaration de classe partielle qui connecte la balise à n’importe quel code-behind définie pour la classe partielle|  
|`>`|Fin de l’élément objet pour la racine. Objet n’est pas encore fermé, car l’élément contienne des éléments enfants|  
  
<a name="optional_and_nonrecommended_xaml_usages"></a>   
## <a name="optional-and-nonrecommended-xaml-usages"></a>Utilisations XAML facultatives et non recommandées  
 Les sections suivantes décrivent les utilisations XAML techniquement prises en charge par les processeurs XAML, mais qui produisent des commentaires ou autres problèmes esthétiques qui interfèrent avec les fichiers XAML restant contrôlable de visu lorsque votre développement d’applications qui contiennent des sources de XAML .  
  
### <a name="optional-property-element-usages"></a>Utilisations des éléments de propriété facultative  
 Utilisations des éléments de propriété facultative incluent écrire explicitement les propriétés de contenu d’élément que le processeur XAML considère comme implicite. Par exemple, lorsque vous déclarez le contenu d’un <xref:System.Windows.Controls.Menu>, vous pouvez choisir de déclarer explicitement le <xref:System.Windows.Controls.ItemsControl.Items%2A> collection de la <xref:System.Windows.Controls.Menu> en tant qu’un `<Menu.Items>` balise d’élément de propriété et place chaque <xref:System.Windows.Controls.MenuItem> dans `<Menu.Items>`, au lieu de cela à l’aide du comportement du processeur XAML implicit qui tous les éléments enfants d’un <xref:System.Windows.Controls.Menu> doit être un <xref:System.Windows.Controls.MenuItem> et sont placés dans le <xref:System.Windows.Controls.ItemsControl.Items%2A> collection. Les utilisations facultatives peuvent parfois aider à clarifier visuellement la structure d’objet, comme représenté dans le balisage. Ou, parfois, une utilisation d’élément de propriété explicite peut éviter de balisage est techniquement fonctionnel mais visuellement prêtent à confusion, telles que les extensions de balisage imbriquées au sein d’une valeur d’attribut.  
  
### <a name="full-typenamemembername-qualified-attributes"></a>Attributs Nom_type.nom_événement complet qualifié  
 Le *typeName*. *memberName* forment pour un attribut fonctionne en fait plus universellement que le cas d’événement routé. Mais dans d’autres situations ce formulaire est superflu et vous devez l’éviter, pour des raisons de style de balisage et la lisibilité. Dans l’exemple suivant, chacune des trois références à la <xref:System.Windows.Controls.Control.Background%2A> attribut sont totalement équivalents :  
  
 [!code-xaml[XAMLOvwSupport#TypeNameProp](../../../../samples/snippets/csharp/VS_Snippets_Wpf/XAMLOvwSupport/CSharp/page8.xaml#typenameprop)]  
  
 `Button.Background` fonctionne car la recherche qualifiée de cette propriété sur <xref:System.Windows.Controls.Button> réussit (<xref:System.Windows.Controls.Control.Background%2A> a été héritée de contrôle) et <xref:System.Windows.Controls.Button> est la classe de l’élément objet ou une classe de base. `Control.Background` fonctionne parce que le <xref:System.Windows.Controls.Control> classe définit réellement <xref:System.Windows.Controls.Control.Background%2A> et <xref:System.Windows.Controls.Control> est un <xref:System.Windows.Controls.Button> classe de base.  
  
 Toutefois, ce qui suit *typeName*. *memberName* suivant ne fonctionne pas et, est donc commenté :  
  
 [!code-xaml[XAMLOvwSupport#TypeNameBadProp](../../../../samples/snippets/csharp/VS_Snippets_Wpf/XAMLOvwSupport/CSharp/page8.xaml#typenamebadprop)]  
  
 <xref:System.Windows.Controls.Label> est une autre classe dérivée de <xref:System.Windows.Controls.Control>, et si vous aviez spécifié `Label.Background` au sein d’un <xref:System.Windows.Controls.Label> élément objet, cette utilisation aurait fonctionné. Toutefois, étant donné que <xref:System.Windows.Controls.Label> n’est pas la classe ou la classe de base de <xref:System.Windows.Controls.Button>, le comportement du processeur XAML spécifié consiste à traiter puis `Label.Background` comme propriété jointe. `Label.Background` n’est pas une propriété jointe disponible, et cette utilisation échoue.  
  
### <a name="basetypenamemembername-property-elements"></a>Éléments de propriété baseTypeName.memberName  
 De manière analogue à la manière dont le *typeName*. *memberName* formulaire fonctionne pour la syntaxe d’attribut, un *Nom_type_base*. *memberName* syntaxe fonctionne pour la syntaxe d’élément de propriété. Par exemple, la syntaxe suivante fonctionne :  
  
 [!code-xaml[XAMLOvwSupport#GoofyPE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/XAMLOvwSupport/CSharp/page8.xaml#goofype)]  
  
 Ici, l’élément de propriété a été attribuée comme `Control.Background` même si l’élément de propriété soit contenu dans `Button`.  
  
 Mais comme *typeName*. *memberName* formulaire pour les attributs, *Nom_type_base*. *memberName* est style médiocre dans le balisage, et vous devez l’éviter.  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble du langage XAML (WPF)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)  
 [Fonctionnalités de langage pour les espaces de noms XAML (x:)](../../../../docs/framework/xaml-services/xaml-namespace-x-language-features.md)  
 [Extensions XAML WPF](../../../../docs/framework/wpf/advanced/wpf-xaml-extensions.md)  
 [Vue d’ensemble des propriétés de dépendance](../../../../docs/framework/wpf/advanced/dependency-properties-overview.md)  
 [TypeConverters et XAML](../../../../docs/framework/wpf/advanced/typeconverters-and-xaml.md)  
 [XAML et classes personnalisées pour WPF](../../../../docs/framework/wpf/advanced/xaml-and-custom-classes-for-wpf.md)
