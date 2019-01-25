---
title: '&#39;Extension&#39; attribut peut être appliqué uniquement à &#39;Module&#39;, &#39;Sub&#39;, ou &#39;fonction&#39; déclarations'
ms.date: 07/20/2015
f1_keywords:
- bc36550
- vbc36550
helpviewer_keywords:
- BC36550
ms.assetid: 4387a51f-733c-45d7-abdb-eb64d4f51078
ms.openlocfilehash: fabd602f31a362fe33954253d565e86a065e0a83
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54718232"
---
# <a name="39extension39-attribute-can-be-applied-only-to-39module39-39sub39-or-39function39-declarations"></a>&#39;Extension&#39; attribut peut être appliqué uniquement à &#39;Module&#39;, &#39;Sub&#39;, ou &#39;fonction&#39; déclarations
La seule façon d’étendre un type de données en Visual Basic consiste à définir une méthode d’extension à l’intérieur d’un module standard. La méthode d’extension peut être un `Sub` procédure ou un `Function` procédure. Toutes les méthodes d’extension doivent être marqués avec l’attribut d’extension, `<Extension()>`, à partir de la <xref:System.Runtime.CompilerServices?displayProperty=nameWithType> espace de noms. Si vous le souhaitez, un module qui contient une méthode d’extension peut être marqué de la même façon. Aucune autre utilisation de l’attribut d’extension n’est valide.  
  
 **ID d’erreur :** BC36550  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Supprimez l’attribut d’extension.  
  
-   Reconcevez votre extension en tant que méthode, définie dans un module englobant.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit un `Print` méthode pour le `String` type de données.  
  
```  
Imports StringUtility  
Imports System.Runtime.CompilerServices  
Namespace StringUtility  
    <Extension()>   
    Module StringExtensions  
        <Extension()>   
        Public Sub Print (ByVal str As String)  
            Console.WriteLine(str)  
        End Sub  
    End Module  
End Namespace  
```  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble des attributs](../../../visual-basic/programming-guide/concepts/attributes/index.md)
- [Méthodes d’extension](../../../visual-basic/programming-guide/language-features/procedures/extension-methods.md)
- [Module (instruction)](../../../visual-basic/language-reference/statements/module-statement.md)
