---
title: '{} Échappement - Extension de balisage'
ms.date: 03/30/2017
f1_keywords:
- '{}'
helpviewer_keywords:
- XAML [XAML Services], quotation mark (")
- '{} escape sequence [XAML Services]'
- XAML [XAML Services], {} escape sequence
- XAML [XAML Services], escape sequence
- quotation mark (") [XAML Services]
- escape sequence [XAML Services]
ms.assetid: 3ce3e2ad-a868-43f9-9c98-b29561cb146e
ms.openlocfilehash: a90f6928d68eddd29762e6206769dd7f07704e4c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="-escape-sequence--markup-extension"></a>{} Séquence d’échappement / Extension de balisage
Fournit la séquence d’échappement XAML pour les valeurs d’attribut. La séquence d’échappement autorise les valeurs suivantes dans l’attribut doit être interprété comme un littéral.  
  
## <a name="xaml-attribute-usage"></a>Utilisation d'attributs XAML  
  
```xml  
<object property="{} literalValue" .../>  
```  
  
## <a name="xaml-property-element-usage"></a>Utilisation des éléments de propriété XAML  
  
```  
<object>  
  <object.property>  
    {} literalValue  
  </object.property>  
</object>  
```  
  
## <a name="xaml-values"></a>Valeurs XAML  
  
|||  
|-|-|  
|*LiteralValue*|La chaîne littérale qui suit la séquence d’échappement. En général, cette chaîne contient une accolade ouvrante ou fermante ({ou}).|  
  
## <a name="remarks"></a>Notes  
 La séquence d’échappement ({}) est utilisé afin qu’une accolade ouvrante ({}) peut être utilisée comme un caractère littéral dans XAML.  
  
 Lecteurs XAML utilisent en général l’accolade ouvrante ({}) pour indiquer le point d’entrée d’une extension de balisage ; toutefois, ils vérifient d’abord le caractère suivant pour déterminer s’il s’agit d’une accolade fermante (}). Uniquement lorsque les deux accolades ({}) sont adjacent, sont elles considérées comme une séquence d’échappement.  
  
 Si la séquence d’échappement est rencontrée, le lecteur XAML doit traiter le reste de la chaîne en tant que chaîne. Toutefois, si la séquence d’échappement est appliquée à un membre qui a un convertisseur de type, la chaîne peut subir une conversion de type lorsqu’il est interprété par un writer XAML.  
  
 La séquence d’échappement n’est pas une extension de balisage et n’est pas sauvegardée par une classe. Toutefois, il est une convention qui doivent respecter les lecteurs XAML (y compris les lecteurs XAML personnalisés).  
  
 Un guillemet (") ne peut pas être utilisé comme une séquence d’échappement de cette manière. Si vous devez définir un guillemet comme une valeur de propriété pour une propriété de non-contenu, utilisez la syntaxe d’élément de propriété et placez le guillemet comme une chaîne à l’intérieur de l’élément de propriété ou utilisez une entité de caractère XML. Pour une propriété de contenu, le guillemet peut être l’ensemble du contenu.  
  
 La séquence d’échappement ({}) est souvent nécessaire lors de la spécification d’un type XML qui doit inclure un qualificateur d’espace de noms dans un emplacement où une extension de balisage XAML peut apparaître. Cela inclut le début d’une valeur d’attribut XAML et dans une extension de balisage, immédiatement après un signe égal (=). L’exemple suivant montre des séquences d’échappement pour un espace de noms XML qui apparaît au début d’une valeur d’attribut XAML.  
  
 [!code-xaml[XLINQExample#StackPanelResources](../../../samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#stackpanelresources)]  
  
## <a name="see-also"></a>Voir aussi  
 [Convertisseurs de types et extensions de balisage pour XAML](../../../docs/framework/xaml-services/type-converters-and-markup-extensions-for-xaml.md)  
 [Entités de caractères XML et XAML](../../../docs/framework/xaml-services/xml-character-entities-and-xaml.md)
