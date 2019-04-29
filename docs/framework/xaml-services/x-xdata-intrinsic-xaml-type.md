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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61938825"
---
# <a name="xxdata-intrinsic-xaml-type"></a>x:XData, type XAML intrinsèque
Permet de positionner des îlots de données XML dans une production XAML. Éléments XML dans `x:XData` ne doit pas être traités par les processeurs XAML comme s’ils sont une partie de l’espace de noms XAML par défaut d’agissant ou tout autre espace de noms XAML. `x:XData` peut contenir arbitraire XML bien formé.  
  
## <a name="xaml-object-element-usage"></a>Utilisation d'éléments objet XAML  
  
```  
<x:XData>  
  <elementDataRoot>  
    [elementData]  
  </elementDataRoot>  
</x:XData>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`elementDataRoot`|L’élément racine unique de l’îlot de données incorporé. Pour la plupart des consommateurs éventuelle, XML qui n’a pas d’une racine unique est considérée comme non valide. En particulier, une racine unique est requise si la `x:XData` est destiné à une source de données XML WPF ou bien d’autres technologies qui utilisent des sources XML pour la liaison de données.|  
|`[elementData]`|Optionnel. Code XML qui représente les données XML. N’importe quel nombre d’éléments peut être inclu en tant que données de l’élément et les éléments imbriqués peuvent être contenus dans d’autres éléments ; Toutefois, les règles générales de XML s’appliquent.|  
  
## <a name="remarks"></a>Notes  
 Les éléments XML dans un `x:XData` objet peut déclarer de nouveau tous les espaces de noms possibles et les préfixes contenant XMLDOM leurs au sein des données.  
  
 Accès par programme aux données XML et le `x:XData` type XAML intrinsèque est possible dans les Services XAML .NET Framework via la <xref:System.Windows.Markup.XData> classe.  
  
## <a name="wpf-usage-notes"></a>Remarques sur l’utilisation WPF  
 Le `x:XData` objet est principalement utilisé comme un objet enfant d’un <xref:System.Windows.Data.XmlDataProvider>, vous pouvez aussi en tant que l’objet enfant de le <xref:System.Windows.Data.XmlDataProvider.XmlSerializer%2A?displayProperty=nameWithType> propriété (en XAML, cela est exprimé en général dans la syntaxe d’élément de propriété).  
  
 Généralement, les données doivent redéfinir l’espace de noms XML base dans l’îlot de données en tant que nouvel espace de noms XML par défaut (la valeur est une chaîne vide). Il s’agit le plus simple pour les îlots de données simples, car le <xref:System.Windows.Data.Binding.XPath%2A> expressions qui sont utilisées pour référencer et lier les données peuvent éviter l’inclusion de préfixes. Les îlots de données plus complexes peuvent définir plusieurs préfixes pour les données et utiliser un préfixe spécifique pour l’espace de noms XML à la racine. Dans ce cas, tous les <xref:System.Windows.Data.Binding.XPath%2A> références d’expression doivent inclure le préfixe d’espace de noms mappé approprié. Pour plus d’informations, consultez [Vue d’ensemble de la liaison de données](../wpf/data/data-binding-overview.md).  
  
 Techniquement, `x:XData` peut être utilisé en tant que le contenu de n’importe quelle propriété de type <xref:System.Xml.Serialization.IXmlSerializable>. Toutefois, <xref:System.Windows.Data.XmlDataProvider.XmlSerializer%2A?displayProperty=nameWithType> est la seule implémentation apparente.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Data.XmlDataProvider>
- [Vue d’ensemble de la liaison de données](../wpf/data/data-binding-overview.md)
- [Binding, extension de balisage](../wpf/advanced/binding-markup-extension.md)
