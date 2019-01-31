---
title: L’attribut 'Extension' ne peut être appliqué qu’aux déclarations 'Module', 'Sub' ou 'Function'
ms.date: 07/20/2015
f1_keywords:
- bc36550
- vbc36550
helpviewer_keywords:
- BC36550
ms.assetid: 4387a51f-733c-45d7-abdb-eb64d4f51078
ms.openlocfilehash: e2e2c41d713b0b04b8bc7208a83d059f0d16bf06
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55278718"
---
# <a name="extension-attribute-can-be-applied-only-to-module-sub-or-function-declarations"></a>L’attribut 'Extension' ne peut être appliqué qu’aux déclarations 'Module', 'Sub' ou 'Function'
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
