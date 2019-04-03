---
title: La variable '<variablename>'masque une variable dans un bloc englobant
ms.date: 07/20/2015
f1_keywords:
- vbc30616
- bc30616
helpviewer_keywords:
- BC30616
ms.assetid: e7658ebc-da45-451b-a409-a0f8915f0beb
ms.openlocfilehash: 15c35cbb829bec782771b584ea25b111b81b5e1f
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58827131"
---
# <a name="variable-variablename-hides-a-variable-in-an-enclosing-block"></a>Variable '\<nom_variable >' masque une variable dans un bloc englobant
Une variable dans un bloc a le même nom qu’une autre variable locale.  
  
 **ID d’erreur :** BC30616  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Renommez la variable du bloc englobé afin qu’il ne soit pas identique à toutes les variables locales. Exemple :  
  
    ```  
    Dim a, b, x As Integer  
    If a = b Then  
       Dim y As Integer = 20 ' Uniquely named block variable.  
    End If  
    ```  
  
-   Une cause courante de cette erreur est l’utilisation de `Catch e As Exception` à l’intérieur d’un gestionnaire d’événements. Si c’est le cas, nommez le `Catch` variable bloc `ex` plutôt que `e`.  
  
-   Une autre source courante de cette erreur est une tentative d’accès d’une variable locale déclarée dans un `Try` bloquer dans une fonction `Catch` bloc. Pour corriger ce problème, déclarez la variable en dehors de la `Try...Catch...Finally` structure.  
  
## <a name="see-also"></a>Voir aussi

- [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
- [Déclaration de variable](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
