---
title: x:XData, type XAML intrinsèque
ms.date: 03/30/2017
f1_keywords:
- x:XData
- XData
- xXData
helpviewer_keywords:
- XAML [XAML Services], x:XData directive element
- XData in XAML [XAML Services]
- x:XData XAML directive element [XAML Services]
ms.assetid: 7ce209c2-621b-4977-b643-565f7e663534
ms.openlocfilehash: c8044bc341ded6ef7b03bbdf701e724654460d54
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59125157"
---
# <a name="xxdata-intrinsic-xaml-type"></a><span data-ttu-id="63b9a-102">x:XData, type XAML intrinsèque</span><span class="sxs-lookup"><span data-stu-id="63b9a-102">x:XData Intrinsic XAML Type</span></span>
<span data-ttu-id="63b9a-103">Permet de positionner des îlots de données XML dans une production XAML.</span><span class="sxs-lookup"><span data-stu-id="63b9a-103">Enables placement of XML data islands within a XAML production.</span></span> <span data-ttu-id="63b9a-104">Éléments XML dans `x:XData` ne doit pas être traités par les processeurs XAML comme s’ils sont une partie de l’espace de noms XAML par défaut d’agissant ou tout autre espace de noms XAML.</span><span class="sxs-lookup"><span data-stu-id="63b9a-104">XML elements within `x:XData` should not be treated by XAML processors as if they are a part of the acting default XAML namespace or any other XAML namespace.</span></span> `x:XData` <span data-ttu-id="63b9a-105">peut contenir arbitraire XML bien formé.</span><span class="sxs-lookup"><span data-stu-id="63b9a-105">can contain arbitrary well-formed XML.</span></span>  
  
## <a name="xaml-object-element-usage"></a><span data-ttu-id="63b9a-106">Utilisation d'éléments objet XAML</span><span class="sxs-lookup"><span data-stu-id="63b9a-106">XAML Object Element Usage</span></span>  
  
```  
<x:XData>  
  <elementDataRoot>  
    [elementData]  
  </elementDataRoot>  
</x:XData>  
```  
  
## <a name="xaml-values"></a><span data-ttu-id="63b9a-107">Valeurs XAML</span><span class="sxs-lookup"><span data-stu-id="63b9a-107">XAML Values</span></span>  
  
|||  
|-|-|  
|`elementDataRoot`|<span data-ttu-id="63b9a-108">L’élément racine unique de l’îlot de données incorporé.</span><span class="sxs-lookup"><span data-stu-id="63b9a-108">The single root element of the enclosed data island.</span></span> <span data-ttu-id="63b9a-109">Pour la plupart des consommateurs éventuelle, XML qui n’a pas d’une racine unique est considérée comme non valide.</span><span class="sxs-lookup"><span data-stu-id="63b9a-109">For most eventual consumers, XML that does not have a single root is considered invalid.</span></span> <span data-ttu-id="63b9a-110">En particulier, une racine unique est requise si la `x:XData` est destiné à une source de données XML WPF ou bien d’autres technologies qui utilisent des sources XML pour la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="63b9a-110">In particular, a single root is required if the `x:XData` is intended as an XML data source for WPF or many other technologies that use XML sources for data binding.</span></span>|  
|`[elementData]`|<span data-ttu-id="63b9a-111">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="63b9a-111">Optional.</span></span> <span data-ttu-id="63b9a-112">Code XML qui représente les données XML.</span><span class="sxs-lookup"><span data-stu-id="63b9a-112">XML that represents the XML data.</span></span> <span data-ttu-id="63b9a-113">N’importe quel nombre d’éléments peut être inclu en tant que données de l’élément et les éléments imbriqués peuvent être contenus dans d’autres éléments ; Toutefois, les règles générales de XML s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="63b9a-113">Any number of elements can be contained as element data and nested elements can be contained in other elements; however, the general rules of XML apply.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="63b9a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="63b9a-114">Remarks</span></span>  
 <span data-ttu-id="63b9a-115">Les éléments XML dans un `x:XData` objet peut déclarer de nouveau tous les espaces de noms possibles et les préfixes contenant XMLDOM leurs au sein des données.</span><span class="sxs-lookup"><span data-stu-id="63b9a-115">The XML elements within an `x:XData` object can re-declare all possible namespaces and prefixes of the containing XMLDOM within the data.</span></span>  
  
 <span data-ttu-id="63b9a-116">Accès par programme aux données XML et le `x:XData` type XAML intrinsèque est possible dans les Services XAML .NET Framework via la <xref:System.Windows.Markup.XData> classe.</span><span class="sxs-lookup"><span data-stu-id="63b9a-116">Programmatic access to XML data and the `x:XData` intrinsic XAML type is possible in .NET Framework XAML Services through the <xref:System.Windows.Markup.XData> class.</span></span>  
  
## <a name="wpf-usage-notes"></a><span data-ttu-id="63b9a-117">Remarques sur l’utilisation WPF</span><span class="sxs-lookup"><span data-stu-id="63b9a-117">WPF Usage Notes</span></span>  
 <span data-ttu-id="63b9a-118">Le `x:XData` objet est principalement utilisé comme un objet enfant d’un <xref:System.Windows.Data.XmlDataProvider>, vous pouvez aussi en tant que l’objet enfant de le <xref:System.Windows.Data.XmlDataProvider.XmlSerializer%2A?displayProperty=nameWithType> propriété (en XAML, cela est exprimé en général dans la syntaxe d’élément de propriété).</span><span class="sxs-lookup"><span data-stu-id="63b9a-118">The `x:XData` object is primarily used as a child object of an <xref:System.Windows.Data.XmlDataProvider>, or alternatively, as the child object of the <xref:System.Windows.Data.XmlDataProvider.XmlSerializer%2A?displayProperty=nameWithType> property (in XAML, this is typically expressed in property element syntax).</span></span>  
  
 <span data-ttu-id="63b9a-119">Généralement, les données doivent redéfinir l’espace de noms XML base dans l’îlot de données en tant que nouvel espace de noms XML par défaut (la valeur est une chaîne vide).</span><span class="sxs-lookup"><span data-stu-id="63b9a-119">The data should typically redefine the base XML namespace within the data island to be a new default XML namespace (set to an empty string).</span></span> <span data-ttu-id="63b9a-120">Il s’agit le plus simple pour les îlots de données simples, car le <xref:System.Windows.Data.Binding.XPath%2A> expressions qui sont utilisées pour référencer et lier les données peuvent éviter l’inclusion de préfixes.</span><span class="sxs-lookup"><span data-stu-id="63b9a-120">This is easiest for simple data islands because the <xref:System.Windows.Data.Binding.XPath%2A> expressions that are used to reference and bind to the data can avoid inclusion of prefixes.</span></span> <span data-ttu-id="63b9a-121">Les îlots de données plus complexes peuvent définir plusieurs préfixes pour les données et utiliser un préfixe spécifique pour l’espace de noms XML à la racine.</span><span class="sxs-lookup"><span data-stu-id="63b9a-121">More complex data islands might define multiple prefixes for the data and use a specific prefix for the XML namespace at the root.</span></span> <span data-ttu-id="63b9a-122">Dans ce cas, tous les <xref:System.Windows.Data.Binding.XPath%2A> références d’expression doivent inclure le préfixe d’espace de noms mappé approprié.</span><span class="sxs-lookup"><span data-stu-id="63b9a-122">In this case, all <xref:System.Windows.Data.Binding.XPath%2A> expression references should include the appropriate namespace-mapped prefix.</span></span> <span data-ttu-id="63b9a-123">Pour plus d’informations, consultez [Vue d’ensemble de la liaison de données](../wpf/data/data-binding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="63b9a-123">For more information, see [Data Binding Overview](../wpf/data/data-binding-overview.md).</span></span>  
  
 <span data-ttu-id="63b9a-124">Techniquement, `x:XData` peut être utilisé en tant que le contenu de n’importe quelle propriété de type <xref:System.Xml.Serialization.IXmlSerializable>.</span><span class="sxs-lookup"><span data-stu-id="63b9a-124">Technically, `x:XData` can be used as the content of any property of type <xref:System.Xml.Serialization.IXmlSerializable>.</span></span> <span data-ttu-id="63b9a-125">Toutefois, <xref:System.Windows.Data.XmlDataProvider.XmlSerializer%2A?displayProperty=nameWithType> est la seule implémentation apparente.</span><span class="sxs-lookup"><span data-stu-id="63b9a-125">However, <xref:System.Windows.Data.XmlDataProvider.XmlSerializer%2A?displayProperty=nameWithType> is the only prominent implementation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63b9a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63b9a-126">See also</span></span>

- <xref:System.Windows.Data.XmlDataProvider>
- [<span data-ttu-id="63b9a-127">Vue d’ensemble de la liaison de données</span><span class="sxs-lookup"><span data-stu-id="63b9a-127">Data Binding Overview</span></span>](../wpf/data/data-binding-overview.md)
- [<span data-ttu-id="63b9a-128">Binding, extension de balisage</span><span class="sxs-lookup"><span data-stu-id="63b9a-128">Binding Markup Extension</span></span>](../wpf/advanced/binding-markup-extension.md)
