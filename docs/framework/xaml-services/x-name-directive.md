---
title: x:Name, directive
ms.date: 03/30/2017
f1_keywords:
- x:Name
- xName
- Name
helpviewer_keywords:
- x:Name attribute [XAML Services]
- XAML [XAML Services], x:Name attribute
- Name attribute in XAML [XAML Services]
ms.assetid: b7e61222-e8cf-48d2-acd0-6df3b7685d48
ms.openlocfilehash: d25c8500250411083e9fb6b33b3f743e5cd103c0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61796524"
---
# <a name="xname-directive"></a>x:Name, directive
Identifie de façon unique les éléments définis dans XAML dans une portée de nom XAML. Portées de nom XAML et de leurs modèles d’unicité peuvent être appliquées aux objets instanciés, lorsque les infrastructures fournissent des API ou implémentent les comportements qui accèdent au graphique d’objets créé en XAML en cours d’exécution.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xaml  
<object x:Name="XAMLNameValue".../>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`XAMLNameValue`|Chaîne qui est conforme aux restrictions de la [XamlName, grammaire](xamlname-grammar.md).|  
  
## <a name="remarks"></a>Notes  
 Après avoir `x:Name` est appliqué à une infrastructure de stockage du modèle de programmation, le nom est équivalent à la variable qui contient une référence d’objet ou une instance, telle que retournée par un constructeur.  
  
 La valeur d’un `x:Name` utilisation de la directive doit être unique dans une portée de nom XAML. Par défaut lorsqu’il est utilisé par les API des Services XAML .NET Framework, la portée de nom XAML principale est définie à l’élément racine XAML d’une production XAML unique et comprend les éléments qui sont contenus dans cette production XAML. Portées de nom XAML supplémentaires discrètes qui peuvent se produire dans une production XAML unique peuvent être définies par les infrastructures pour résoudre des scénarios spécifiques. Par exemple, dans WPF, nouvelles portées de nom XAML sont définies et créées par n’importe quel modèle est également défini sur cette production XAML. Pour plus d’informations sur les portées de nom XAML (écrites pour WPF mais pertinents pour de nombreux concepts de portée de nom XAML), consultez [portées de nom XAML WPF](../wpf/advanced/wpf-xaml-namescopes.md).  
  
 En règle générale, `x:Name` ne doit pas être appliqué dans les situations qui utilisent également `x:Key`. Les implémentations XAML par les infrastructures spécifiques existantes ont introduit des concepts de substitution entre `x:Key` et `x:Name`, mais ce n’est pas une pratique recommandée. Les Services XAML .NET framework ne prend pas en charge ces concepts de substitution lors de la gestion des informations de nom/clé tels que <xref:System.Windows.Markup.INameScope> ou <xref:System.Windows.Markup.DictionaryKeyPropertyAttribute>.  
  
 Règles d’autorisation de `x:Name` , ainsi que la mise en œuvre de l’unicité de nom sont définies potentiellement par des infrastructures d’implémentation spécifiques. Toutefois, pour être utilisables avec les Services XAML .NET Framework, les définitions de framework d’unicité de portée de nom XAML doivent être cohérentes avec la définition de <xref:System.Windows.Markup.INameScope> informations contenues dans cette documentation et doivent utiliser les mêmes règles sur les endroits où le informations sont appliquées. Par exemple, le [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] implémentation divise les différents éléments de balisage en distinct <xref:System.Windows.NameScope> plages d’adresses, telles que des dictionnaires de ressources, l’arborescence logique par le niveau de la page XAML, modèles et d’autres différée contenu créé et applique ensuite XAML unicité des noms dans chacun de ces portées de nom XAML.  
  
 Pour les types personnalisés qui utilisent les writers d’objet XAML de Services XAML .NET Framework, une propriété qui est mappée à `x:Name` sur un type peut être établi ou modifié. Vous définissez ce comportement en référençant le nom de la propriété à mapper avec le <xref:System.Windows.Markup.RuntimeNamePropertyAttribute> dans le code de définition de type.  <xref:System.Windows.Markup.RuntimeNamePropertyAttribute> est un attribut au niveau du type.  
  
 Using.NET XAML Services Framework, et la logique de stockage pour la prise en charge de la portée de nom XAML peut être définies d’une façon indépendante du framework en implémentant le <xref:System.Windows.Markup.INameScope> interface.  
  
## <a name="wpf-usage-notes"></a>Remarques sur l’utilisation WPF  
 Sous la configuration de build standard pour un [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] application qui utilise XAML, les classes partielles et les code-behind, spécifié `x:Name` devient le nom d’un champ qui est créé dans sous-jacent le code lorsque [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] est traité par un balisage tâche de génération de compilation et que ce champ contient une référence à l’objet. Par défaut, le champ créé est interne. Vous pouvez modifier l’accès à un champ en spécifiant le [attribut x : FieldModifier](x-fieldmodifier-directive.md). Dans WPF et Silverlight, la séquence est que la compilation de balisage définit et noms de champ dans une classe partielle, mais la valeur est initialement vide. Ensuite, une méthode générée nommée `InitializeComponent` est appelée à partir du constructeur de classe. `InitializeComponent` se compose de `FindName` appelle à l’aide de chacun de la `x:Name` entrer des valeurs qui existent dans la partie définie en XAML de la classe partielle en tant que chaînes. Les valeurs de retour sont ensuite affectées à la référence de champ pour remplir les valeurs de champ avec des objets qui ont été créés à partir de XAML à l’analyse. L’exécution de `InitializeComponent` rendent possible le graphique d’objet moment de l’exécution à l’aide de référence le `x:Name` / nom du champ directement, plutôt que de devoir appeler `FindName` explicitement chaque fois que vous devez une référence à un objet défini par XAML.  
  
 Pour un WPF application qui utilise Microsoft Visual Basic cible et inclut des fichiers XAML avec `Page` action de génération, une propriété de référence distincte est créée pendant la compilation qui ajoute le `WithEvents` mot clé à tous les éléments qui ont un `x:Name`, pour prendre en charge `Handles` syntaxe pour les délégués de gestionnaire d’événements. Cette propriété est toujours publique. Pour plus d’informations, consultez [Gestion des événements Visual Basic et WPF](../wpf/advanced/visual-basic-and-wpf-event-handling.md).  
  
 `x:Name` est utilisé par le processeur WPF XAML pour inscrire un nom dans une portée de nom XAML au moment du chargement, même pour les cas où la page n’est pas compilé par balisage par les actions de génération (par exemple, un XAML libre d’un dictionnaire de ressources). L’une des raisons de ce comportement sont, car le `x:Name` est potentiellement nécessaire pour <xref:System.Windows.Data.Binding.ElementName%2A> liaison. Pour plus d’informations, consultez [vue d’ensemble de la liaison de données](../wpf/data/data-binding-overview.md).  
  
 Comme mentionné précédemment, `x:Name` (ou `Name`) ne doit pas être appliqué dans les situations qui utilisent également `x:Key`. Le [!INCLUDE[TLA2#tla_winclient](../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.ResourceDictionary> a un comportement spécial de se définir lui-même comme une portée de nom XAML, mais retourner non implémenté ou des valeurs null pour <xref:System.Windows.Markup.INameScope> API comme une méthode pour appliquer ce comportement. Si l’analyseur WPF XAML rencontre `Name` ou `x:Name` dans un XAML définis par le <xref:System.Windows.ResourceDictionary>, le nom n’est pas ajouté à une portée de nom XAML. Une tentative de recherche de ce nom à partir d’une portée de nom XAML et le `FindName` méthodes ne retournera pas de résultats valides.  
  
### <a name="xname-and-name"></a>x : Name et le nom  
 Nombreux scénarios d’application WPF peuvent éviter toute utilisation de la `x:Name` d’attribut, car le `Name` propriété de dépendance comme spécifié dans la valeur par défaut espace de noms XAML pour plusieurs des classes de base importantes telles que <xref:System.Windows.FrameworkElement> et <xref:System.Windows.FrameworkContentElement> est conforme à cette même fin. Il existe toujours des scénarios XAML et WPF courants où les accès à un élément sans nécessiter de code `Name` propriété au niveau de l’infrastructure est importante. Par exemple, certaines classes de prise en charge de l’animation et table de montage séquentiel ne prennent pas en charge un `Name` propriété, mais ils doivent souvent être référencées dans le code afin de contrôler l’animation. Vous devez spécifier `x:Name` en tant qu’attribut sur des chronologies et transformations créées dans XAML, si vous avez l’intention de faire référence ultérieurement à partir du code.  
  
 Si <xref:System.Windows.FrameworkElement.Name%2A> est disponible en tant que propriété sur la classe, <xref:System.Windows.FrameworkElement.Name%2A> et `x:Name` peuvent être utilisés indifféremment en tant qu’attributs, mais une exception d’analyse se produit si les deux sont sur le même élément. Si le XAML est compilé par balisage, l’exception se produira sur la compilation de balisage, sinon il se produit lors du chargement.  
  
 <xref:System.Windows.FrameworkElement.Name%2A> peut être définie à l’aide de la syntaxe d’attribut XAML et à l’aide de code <xref:System.Windows.DependencyObject.SetValue%2A>; Notez toutefois ce paramètre la <xref:System.Windows.FrameworkElement.Name%2A> propriété dans le code ne crée pas de référence de champ représentative dans la portée de nom XAML dans la plupart des cas où le XAML est déjà chargé. Au lieu de la tentative de définition <xref:System.Windows.FrameworkElement.Name%2A> dans le code, utilisez <xref:System.Windows.NameScope> méthodes à partir de code, par rapport à la portée de nom appropriée.  
  
 <xref:System.Windows.FrameworkElement.Name%2A> peut également être définie à l’aide de la syntaxe d’élément de propriété avec du texte interne, mais qui est rare. En revanche, `x:Name` ne peut pas être définie dans la syntaxe d’élément de propriété XAML, ou dans le code à l’aide <xref:System.Windows.DependencyObject.SetValue%2A>; elle peut uniquement être définie à l’aide de syntaxe d’attribut sur les objets car il s’agit d’une directive.  
  
## <a name="silverlight-usage-notes"></a>Remarques sur l’utilisation de Silverlight  
 `x:Name` pour Silverlight est documenté séparément. Pour plus d’informations, consultez [XAML Namespace (x :)) Fonctionnalités de langage (Silverlight)](https://go.microsoft.com/fwlink/?LinkId=199081).  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.FrameworkElement.Name%2A?displayProperty=nameWithType>
- <xref:System.Windows.FrameworkContentElement.Name%2A?displayProperty=nameWithType>
- [Arborescences dans WPF](../wpf/advanced/trees-in-wpf.md)
