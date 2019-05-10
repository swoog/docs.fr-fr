---
title: Le premier opérande d'une expression binaire 'If' doit être de type nullable ou référence
ms.date: 07/20/2015
f1_keywords:
- bc33107
- vbc33107
helpviewer_keywords:
- BC33107
ms.assetid: 493c8899-3f6b-4471-8eb6-9284e8492768
ms.openlocfilehash: a73a66313e7ca540711838c4d147d6bd163ec8d6
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64625564"
---
# <a name="first-operand-in-a-binary-if-expression-must-be-nullable-or-a-reference-type"></a>Le premier opérande d'une expression binaire 'If' doit être de type nullable ou référence
Un `If` expression peut prendre deux ou trois arguments. Lorsque vous envoyez uniquement deux arguments, le premier argument doit être un type référence ou un type nullable. Si le premier argument prend la valeur sur n’importe quelle autre que `Nothing`, sa valeur est retournée. Si le premier argument prend la valeur `Nothing`, le deuxième argument est évalué et retourné.  
  
 Par exemple, le code suivant contient deux `If` expressions, une avec trois arguments et l’autre avec deux arguments. Les expressions calculer et retournent la même valeur.  
  
```vb  
' firstChoice is a nullable value type.  
Dim firstChoice? As Integer = Nothing  
Dim secondChoice As Integer = 1128  
' If expression with three arguments.  
Console.WriteLine(If(firstChoice IsNot Nothing, firstChoice, secondChoice))  
' If expression with two arguments.  
Console.WriteLine(If(firstChoice, secondChoice))  
```  
  
 Les expressions suivantes provoquent cette erreur :  
  
```vb  
Dim choice1 = 4  
Dim choice2 = 5  
Dim booleanVar = True  
  
' Not valid.  
'Console.WriteLine(If(choice1 < choice2, 1))  
' Not valid.  
'Console.WriteLine(If(booleanVar, "Test returns True."))  
```  
  
 **ID d’erreur :** BC33107  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Si vous ne pouvez pas modifier le code afin que le premier argument est un type nullable ou un type référence, envisagez de convertir à un argument de trois `If` expression, ou à un `If...Then...Else` instruction.  
  
```vb  
Console.WriteLine(If(choice1 < choice2, 1, 2))  
Console.WriteLine(If(booleanVar, "Test returns True.", "Test returns False."))  
```  
  
## <a name="see-also"></a>Voir aussi

- [If (opérateur)](../../../visual-basic/language-reference/operators/if-operator.md)
- [If...Then...Else (instruction)](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
- [Types valeur Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
