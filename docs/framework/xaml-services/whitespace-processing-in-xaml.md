---
title: Espace blanc dans XAML de traitement
ms.date: 03/30/2017
helpviewer_keywords:
- East Asian characters [XAML Services]
- XAML [XAML Services], white-space processing
- white-space processing in XAML [XAML Services]
- characters [XAML Services], East Asian
ms.assetid: cc9cc377-7544-4fd0-b65b-117b90bb0b23
ms.openlocfilehash: 89f8a4675b3edc23913549bc24f0d9ae16917519
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46007046"
---
# <a name="white-space-processing-in-xaml"></a>Espace blanc dans XAML de traitement
Les règles de langage pour XAML d’état que l’espace blanc significatif doit être traité par un [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] implémentation du processeur. Cette rubrique documente ces règles de langage XAML. Il traite également de la gestion des espaces blancs supplémentaires définie par le [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] implémentation du processeur XAML et le writer XAML pour la sérialisation.  
  
<a name="whitespace_definition"></a>   
## <a name="white-space-definition"></a>Définition d’un espace blanc  
 Cohérente avec [!INCLUDE[TLA2#tla_xml](../../../includes/tla2sharptla-xml-md.md)], les caractères espace blanc de [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] sont des espaces, de saut de ligne et de tabulations. Ils correspondent respectivement aux valeurs [!INCLUDE[TLA#tla_unicode](../../../includes/tlasharptla-unicode-md.md)] 0020, 000A et 0009, respectivement.  
  
<a name="whitespace_normalization"></a>   
## <a name="white-space-normalization"></a>Normalisation des espaces blancs  
 Par défaut la normalisation des espaces blancs suivante se produit lorsqu’un [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] processus du processeur une [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] fichier :  
  
1.  Les caractères de saut de ligne entre les caractères d'Extrême-Orient sont supprimés. Consultez la section « Caractères d'Extrême-Orient », plus loin dans cette rubrique, pour obtenir une définition de ce terme.  
  
2.  Tous les caractères d’espace blanc (espace, saut de ligne, onglet) sont convertis en espaces.  
  
3.  Tous les espaces consécutifs sont supprimés et remplacés par un espace.  
  
4.  Un espace qui suit immédiatement la balise de début est supprimé.  
  
5.  Un espace qui précède immédiatement la balise de fin est supprimé.  
  
 La « valeur par défaut » correspond à l'état désigné par la valeur par défaut de l'attribut [xml:space](../../../docs/framework/xaml-services/xml-space-handling-in-xaml.md) .  
  
<a name="whitespace_in_inner_text_and_string_primitives"></a>   
## <a name="white-space-in-inner-text-and-string-primitives"></a>Espace blanc dans le texte interne et primitives de chaîne  
 Les règles de normalisation précédentes s'appliquent au texte interne que l'on trouve dans les éléments XAML. Après la normalisation, un processeur XAML convertit tout texte interne en un type approprié, comme suit :  
  
-   Si le type de la propriété n'est pas une collection, mais n'est pas directement un type <xref:System.Object> , le processeur XAML tente de convertir en ce type à l'aide de son convertisseur de type. En cas d'échec de la conversion, une erreur de compilation survient.  
  
-   Si le type de la propriété est une collection et que le texte interne est contigu (aucune balise d'élément intermédiaire), le texte interne est analysé comme un élément <xref:System.String>String. Si le type de collection ne peut pas accepter <xref:System.String>, une erreur de compilation est également générée.  
  
-   Si le type de la propriété est <xref:System.Object>, le texte interne est analysé comme un objet <xref:System.String>unique. En cas de balises d'élément intermédiaires, une erreur de compilation est générée car le type <xref:System.Object> implique un objet unique (<xref:System.String> ou autre).  
  
-   Si le type de la propriété est une collection et que le texte interne n'est pas contigu, la première sous-chaîne est convertie en <xref:System.String> et ajoutée en tant qu'élément de collection, l'élément intermédiaire est ajouté en tant qu'élément de collection et la sous-chaîne de fin (le cas échéant) est ajoutée à la collection comme troisième élément <xref:System.String> .  
  
<a name="preserving_whitespace"></a>   
## <a name="preserving-white-space"></a>Conserver les espaces  
 Il existe plusieurs techniques pour conserver les espaces blancs dans la source [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] pour une présentation finale ne sont pas affectés par [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] normalisation des espaces blancs du processeur.  
  
 **XML : space = « preserve »**: spécifiez cet attribut au niveau de l’élément où la conservation de l’espace blanc est souhaitée. Cela permet de conserver l'ensemble de l'espace blanc, ce qui inclut les espaces pouvant être ajoutés par des applications d'édition de code pour imprimer correctement des éléments comme une imbrication visuellement intuitive. Toutefois, le rendu de ces espaces est déterminé par le modèle de contenu pour l'élément conteneur. Évitez de spécifier `xml:space="preserve"` au niveau racine, car la plupart des modèles objet ne considèrent pas blancs espace comme significatif, quelle que soit la façon dont vous définissez l’attribut. Le fait de définir `xml:space` de façon globale peut avoir des conséquences sur les performances de traitement XAML (en particulier, la sérialisation) dans certaines implémentations. Il est préférable de définir uniquement l’attribut spécifiquement au niveau des éléments qui rendre les espaces blancs dans les chaînes, ou sont des collections significatives d’espaces blancs.  
  
 **Entités et espaces insécables**: le langage [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] prend en charge l'insertion d'une entité [!INCLUDE[TLA#tla_unicode](../../../includes/tlasharptla-unicode-md.md)] dans un modèle objet de texte. Vous pouvez utiliser des entités dédiées telles que des espaces insécables (&\#160 ; dans l’encodage UTF-8). Vous pouvez également utiliser des contrôles de texte enrichi qui prennent en charge les caractères d'espace insécable. Soyez prudent lorsque vous utilisez des entités pour simuler des caractéristiques de mise en page telles que la mise en retrait, car la sortie à l'exécution des entités variera suivant que le nombre de facteurs est plus élevé que les fonctionnalités de mise en page générales, telles que l'utilisation appropriée de panneaux et de marges. Par exemple, les entités sont mappées aux polices et peuvent changer de taille en fonction de la police sélectionnée par l'utilisateur.  
  
<a name="east_asian_characters"></a>   
## <a name="east-asian-characters"></a>Caractères d’Extrême-Orient  
 Les caractères d'Extrême-Orient sont définis comme un jeu de caractères [!INCLUDE[TLA2#tla_unicode](../../../includes/tla2sharptla-unicode-md.md)] allant de U+20000 à U+2FFFD et de U+30000 à U+3FFFD. Ce sous-ensemble est parfois également appelé « idéogrammes CJK ». Pour plus d’informations, consultez [http://www.unicode.org](http://www.unicode.org/).  
  
<a name="whitespace_and_text_content_models"></a>   
## <a name="white-space-and-text-content-models"></a>Espace blanc et le texte des modèles de contenu  
 Dans la pratique, en conservant un espace blanc ne concerne que pour un sous-ensemble de tous les modèles de contenu possibles. Ce sous-ensemble se compose des modèles de contenu qui peuvent prendre un type <xref:System.String> singleton d'une certaine manière, une collection <xref:System.String> dédiée ou un mélange de <xref:System.String> et d'autres types dans une collection <xref:System.Collections.IList> ou <xref:System.Collections.Generic.ICollection%601> .  
  
### <a name="white-space-and-text-content-models-in-wpf"></a>Espace blanc et le texte des modèles de contenu dans WPF  
 À des fins d'illustration, le reste de cette section référence des types particuliers définis par WPF. Les fonctionnalités de gestion des espaces blancs sont décrits dans cette rubrique sont appliquent généralement à la fois les Services XAML .NET Framework et WPF. Pour voir ce comportement en action, il peut se révéler utile d'expérimenter des balises XAML WPF et de consulter les résultats dans un graphique d'objets, puis de procéder une nouvelle fois à une désérialisation en balises.  
  
 Même pour les modèles de contenu qui peuvent prendre des chaînes, le comportement par défaut au sein de ces modèles de contenu est que n’importe quel espace blanc restant n’est pas traité comme significatif. Par exemple, <xref:System.Windows.Controls.ListBox> prend un <xref:System.Collections.IList>, mais l’espace blanc (sauts de ligne entre chaque <xref:System.Windows.Controls.ListBoxItem>) est pas conservé et pas restitué. Si vous tentez d'utiliser des sauts de ligne comme séparateurs entre des chaînes pour les éléments <xref:System.Windows.Controls.ListBoxItem> , cela ne fonctionne pas du tout ; les chaînes séparées par des sauts de ligne sont traitées comme une chaîne et un élément.  
  
 Ces collections qui traitent l’espace blanc comme significatif font généralement partie du modèle de document de flux. La principale collection qui prend en charge le comportement de conservation de l’espace blanc est <xref:System.Windows.Documents.InlineCollection>. Cette classe de collection est déclarée avec le <xref:System.Windows.Markup.WhitespaceSignificantCollectionAttribute>; lorsque cet attribut est trouvé, le [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] processeur traite l’espace blanc dans la collection comme significatif. La combinaison de `xml:space="preserve"` et l’espace blanc dans un <xref:System.Windows.Markup.WhitespaceSignificantCollectionAttribute> dénotée engendre la collection que tous les espaces blancs est conservés et rendus. La combinaison de `xml:space="default"` et l’espace blanc dans un <xref:System.Windows.Markup.WhitespaceSignificantCollectionAttribute> entraîne la normalisation d’espace blanc initiale décrite ci-dessus, ce qui laisse un espace dans certaines positions et ces espaces est conservés et rendus. À vous de déterminer le comportement souhaité et d'utiliser `xml:space` de manière sélective pour activer le comportement de votre choix.  
  
 En outre, certains éléments inclus qui correspondent à un saut de ligne dans un modèle de document de flux ne doivent pas introduire délibérément un espace supplémentaire même dans une collection d’espaces blancs significative. Par exemple, le <xref:System.Windows.Documents.LineBreak> élément a le même objectif que le \<BR / > baliser dans [!INCLUDE[TLA2#tla_html](../../../includes/tla2sharptla-html-md.md)]et pour une meilleure lisibilité dans le balisage, généralement un <xref:System.Windows.Documents.LineBreak> n’importe quel texte qui suit est séparé par un saut de ligne créé. Ce saut de ligne ne doit pas être normalisé pour devenir un espace de début dans la ligne suivante. Pour activer ce comportement, la définition de classe pour le <xref:System.Windows.Documents.LineBreak> élément s’applique le <xref:System.Windows.Markup.TrimSurroundingWhitespaceAttribute>, qui est ensuite interprété par le [!INCLUDE[TLA2#tla_xaml](../../../includes/tla2sharptla-xaml-md.md)] processeur comme signifiant que l’espace blanc qui entoure <xref:System.Windows.Documents.LineBreak> est toujours supprimé.  
  
## <a name="see-also"></a>Voir aussi  
 [Vue d’ensemble du langage XAML (WPF)](../../../docs/framework/wpf/advanced/xaml-overview-wpf.md)  
 [Entités de caractères XML et XAML](../../../docs/framework/xaml-services/xml-character-entities-and-xaml.md)  
 [XML : space en XAML de gestion des](../../../docs/framework/xaml-services/xml-space-handling-in-xaml.md)
