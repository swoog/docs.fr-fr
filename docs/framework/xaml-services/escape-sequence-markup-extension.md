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
ms.openlocfilehash: 9f6743dd8a82891ac2233978550e5679130de0be
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61855605"
---
# <a name="-escape-sequence--markup-extension"></a>{} Séquence d’échappement/Extension de balisage
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
|*literalValue*|La chaîne littérale qui suit la séquence d’échappement. En général, cette chaîne contient une accolade ouvrante ou fermante ({ou}).|  
  
## <a name="remarks"></a>Notes  
 La séquence d’échappement ({}) est utilisé afin qu’une accolade ouvrante ({}) peut être utilisée comme un caractère littéral dans XAML.  
  
 Les lecteurs XAML utilisent généralement l’accolade ouvrante ({}) pour indiquer le point d’entrée d’une extension de balisage ; toutefois, ils vérifient d’abord le caractère suivant pour déterminer s’il s’agit d’une accolade fermante (}). Uniquement lorsque les deux accolades ({}) sont adjacente, sont elles considérées comme une séquence d’échappement.  
  
 Si la séquence d’échappement est rencontrée, le lecteur XAML doit traiter le reste de la chaîne sous forme de chaîne. Toutefois, si la séquence d’échappement est appliquée à un membre qui a un convertisseur de type, la chaîne peut subir une conversion de type lorsqu’il est interprété par un writer XAML.  
  
 La séquence d’échappement n’est pas une extension de balisage et n’est pas stockée par une classe. Toutefois, il est une convention qui respectent les lecteurs XAML (y compris les lecteurs XAML personnalisés).  
  
 Un guillemet (") ne peut pas être utilisé comme une séquence d’échappement de cette manière. Si vous avez besoin définir un guillemet comme une valeur de propriété pour une propriété de non-contenu, utilisez la syntaxe d’élément de propriété et placez le guillemet sous forme de chaîne à l’intérieur de l’élément de propriété ou utiliser une entité de caractère XML. Pour une propriété de contenu, le guillemet peut être l’intégralité du contenu.  
  
 La séquence d’échappement ({}) est souvent nécessaire lors de la spécification d’un type XML qui doit inclure un qualificateur d’espace de noms dans un emplacement où une extension de balisage XAML peut apparaître. Cela inclut le début d’une valeur d’attribut XAML et dans une extension de balisage, immédiatement après un signe égal (=). L’exemple suivant montre des séquences d’échappement pour un espace de noms XML qui apparaît au début d’une valeur d’attribut XAML.  
  
 [!code-xaml[XLINQExample#StackPanelResources](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#stackpanelresources)]  
  
## <a name="see-also"></a>Voir aussi

- [Convertisseurs de types et extensions de balisage pour XAML](type-converters-and-markup-extensions-for-xaml.md)
- [Entités de caractères XML et XAML](xml-character-entities-and-xaml.md)
