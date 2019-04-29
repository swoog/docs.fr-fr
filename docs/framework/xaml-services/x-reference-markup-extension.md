---
title: x:Référence, extension de balisage
ms.date: 03/30/2017
helpviewer_keywords:
- x:Reference markup extension [XAML Services]
- XAML [XAML Services], x:Reference Markup Extension
- Reference markup extension [XAML Services]
ms.assetid: 2982e68b-d26b-4aa3-826a-34c57a9c5199
ms.openlocfilehash: 960f5c0e4192df72090c1a571dfc2fc5e3fd8ba3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61938877"
---
# <a name="xreference-markup-extension"></a>x:Référence, extension de balisage
Fait référence à une instance qui est déclarée ailleurs dans le balisage XAML. La référence fait référence à un élément `x:Name`.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xaml  
<object property="{x:Reference instancexName}" .../>  
```  
  
## <a name="xaml-object-element-usage"></a>Utilisation d'éléments objet XAML  
  
```xaml  
<object>  
  <object.property>  
    <x:Reference Name="instancexName"/>  
  </object.property>  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|`instancexName`|Le `x:Name` valeur (ou la valeur de la <xref:System.Windows.Markup.RuntimeNamePropertyAttribute>-propriété identifiée) de l’instance référencée.|  
  
## <a name="remarks"></a>Notes  
 `x:Reference` Fournit la prise en charge du niveau de langage XAML pour un concept de référence d’élément qui a été implémenté dans les infrastructures spécifiques telles que WPF.  
  
## <a name="xreference-and-wpf"></a>x : Reference et WPF  
 Dans WPF et XAML 2006, les références d’éléments sont adressées par la fonctionnalité au niveau du framework de <xref:System.Windows.Data.Binding.ElementName%2A> liaison. Pour la plupart des applications WPF et scénarios, <xref:System.Windows.Data.Binding.ElementName%2A> la liaison doit toujours être utilisée. Exceptions à cette recommandation générale peuvent inclure des cas où il existe le contexte de données ou d’autres considérations d’étendue qui rendent la liaison de données peu pratique et compilation du balisage n’est pas impliquée.  
  
 `x:Reference` est une construction définie dans XAML 2009. Dans WPF, vous pouvez utiliser les fonctionnalités XAML 2009, mais uniquement pour le code XAML qui n'est pas compilé par balisage WPF. Le code XAML compilé par balisage et la forme BAML du code XAML ne prennent actuellement pas en charge les mots clés de langage et fonctionnalités XAML 2009.
