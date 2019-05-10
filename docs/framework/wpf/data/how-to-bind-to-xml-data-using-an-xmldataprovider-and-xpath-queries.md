---
title: 'Procédure : Effectuer une liaison à des données XML à l’aide d’un XMLDataProvider et de requêtes XPath'
ms.date: 03/30/2017
helpviewer_keywords:
- XmlDataProvider [WPF], binding to XML data
- data binding [WPF], binding to XML data using XmlDataProvider queries
- binding [WPF], to XML data using XmlDataProvider queries
ms.assetid: 7dcd018f-16aa-4870-8e47-c1b4ea31e574
ms.openlocfilehash: 49f32ae4f358885268044cbfd785239f537940ae
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64609418"
---
# <a name="how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries"></a>Procédure : Effectuer une liaison à des données XML à l’aide d’un XMLDataProvider et de requêtes XPath
Cet exemple montre comment lier à [!INCLUDE[TLA#tla_xml](../../../../includes/tlasharptla-xml-md.md)] données à l’aide un <xref:System.Windows.Data.XmlDataProvider>.  
  
 Avec un <xref:System.Windows.Data.XmlDataProvider>, le sous-jacente des données qui sont accessibles via la liaison de données dans votre application peut être n’importe quel arbre de [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] nœuds. En d’autres termes, une <xref:System.Windows.Data.XmlDataProvider> fournit un moyen pratique d’utiliser n’importe quel arbre de [!INCLUDE[TLA#tla_xml](../../../../includes/tlasharptla-xml-md.md)] nœuds comme source de liaison.  
  
## <a name="example"></a>Exemple  
 Dans l’exemple suivant, les données sont incorporées directement comme un [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] *îlot de données* au sein de la <xref:System.Windows.FrameworkElement.Resources%2A> section. Un îlot de données [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] doit être encapsulé dans des balises `<x:XData>` et toujours avoir un nœud racine unique (*Inventory* dans cet exemple).  
  
> [!NOTE]
>  Le nœud racine des données [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] est un attribut **xmlns** qui définit l’espace de noms [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] sur une chaîne vide. Il s’agit d’une condition requise pour appliquer des requêtes XPath à un îlot de données inline dans la page [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)]. Dans ce cas inline, le [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], et donc de l’îlot de données, le <xref:System.Windows> espace de noms. Pour cette raison, vous devez définir l’espace de noms vide pour conserver les requêtes XPath ne soient pas qualifiées par le <xref:System.Windows> espace de noms, ce qui risque de mal orienter les requêtes.  
  
 [!code-xaml[XMLDataSource#1](~/samples/snippets/csharp/VS_Snippets_Wpf/XmlDataSource/CS/Window1.xaml#1)]  
  
 Comme indiqué dans cet exemple, pour créer la même déclaration de liaison dans la syntaxe d’attribut, vous devez échapper les caractères spéciaux correctement. Pour plus d’informations, consultez [Entités de caractères XML et XAML](../../xaml-services/xml-character-entities-and-xaml.md).  
  
 Le <xref:System.Windows.Controls.ListBox> affichera les éléments suivants lors de l’exécution de cet exemple. Il s’agit de tous les objets *Title*s de tous les éléments sous *Books* ayant une valeur *Stock* de *« out »* ou une valeur *Number* de 3 ou supérieure ou égale à 8. Notez qu’aucun *CD* les éléments sont retournés, car le <xref:System.Windows.Data.XmlDataProvider.XPath%2A> a de valeur sur le <xref:System.Windows.Data.XmlDataProvider> indique que seul le *la documentation* éléments doivent être exposés (ce qui définit essentiellement un filtre).  
  
 ![Capture d’écran de l’exemple XPath montrant le titre de quatre livres.](./media/how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries/xpath-example-listbox-details.png)  
  
 Dans cet exemple, les titres des ouvrages sont affichés car le <xref:System.Windows.Data.Binding.XPath%2A> de la <xref:System.Windows.Controls.TextBlock> liaison dans le <xref:System.Windows.DataTemplate> a la valeur «*titre*». Si vous souhaitez afficher la valeur d’un attribut, tel que le *ISBN*, vous définiriez qui <xref:System.Windows.Data.Binding.XPath%2A> valeur «`@ISBN`».  
  
 Les propriétés **XPath** dans [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] sont gérées par la méthode XmlNode.SelectNodes. Vous pouvez modifier les requêtes **XPath** pour obtenir des résultats différents. Voici quelques exemples pour le <xref:System.Windows.Data.Binding.XPath%2A> sur la limite de requête <xref:System.Windows.Controls.ListBox> à partir de l’exemple précédent :  
  
- `XPath="Book[1]"` retourne le premier élément d’ouvrage (« XML in Action »). Notez que les index **XPath** sont basés sur 1, et non sur 0.  
  
- `XPath="Book[@*]"` retourne tous les éléments d’ouvrage avec des attributs.  
  
- `XPath="Book[last()-1]"` retourne l’avant dernier élément d’ouvrage (« Introducing Microsoft .NET »).  
  
- `XPath="*[position()>3]"` retournera tous les éléments d’ouvrage, à l’exception des 3 premiers.  
  
 Lorsque vous exécutez un **XPath** de requête, elle retourne un <xref:System.Xml.XmlNode> ou une liste de XmlNodes. <xref:System.Xml.XmlNode> est un [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] objet, ce qui signifie que vous pouvez utiliser la <xref:System.Windows.Data.Binding.Path%2A> propriété à lier le [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] propriétés. Regardez de nouveau l’exemple précédent. Si le reste de l’exemple reste le même et que vous modifiez le <xref:System.Windows.Controls.TextBlock> de liaison à ce qui suit, vous verrez les noms des XmlNodes retournés dans le <xref:System.Windows.Controls.ListBox>. Dans ce cas, le nom de tous les nœuds retournés est « *Book* ».  
  
 [!code-xaml[XmlDataSourceVariation#XmlNodePath](~/samples/snippets/csharp/VS_Snippets_Wpf/XmlDataSourceVariation/CS/Page1.xaml#xmlnodepath)]  
  
 Dans certaines applications, l’incorporation du [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] comme îlot de données dans la source de la page [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] peut être gênante, car le contenu exact des données doit être connu au moment de la compilation. Par conséquent, l’obtention de données à partir d’un fichier [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] externe est également prise en charge, comme dans l’exemple suivant :  
  
 [!code-xaml[XMLDataSource2#XmlFileExample](~/samples/snippets/csharp/VS_Snippets_Wpf/XmlDataSource2/CS/Window1.xaml#xmlfileexample)]  
  
 Si le [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] données résident dans un référentiel distant [!INCLUDE[TLA2#tla_xml](../../../../includes/tla2sharptla-xml-md.md)] fichier, définissez l’accès aux données en assignant une approprié [!INCLUDE[TLA2#tla_url](../../../../includes/tla2sharptla-url-md.md)] à la <xref:System.Windows.Data.XmlDataProvider.Source%2A> attribut comme suit :  
  
```xml  
<XmlDataProvider x:Key="BookData" Source="http://MyUrl" XPath="Books"/>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Data.ObjectDataProvider>
- [Effectuer une liaison avec XDocument, XElement ou LINQ pour des résultats de requête XML](how-to-bind-to-xdocument-xelement-or-linq-for-xml-query-results.md)
- [Utiliser le modèle maître/détail avec des données XML hiérarchiques](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md)
- [Vue d'ensemble des sources de liaison](binding-sources-overview.md)
- [Vue d’ensemble de la liaison de données](data-binding-overview.md)
- [Rubriques de guide pratique](data-binding-how-to-topics.md)
