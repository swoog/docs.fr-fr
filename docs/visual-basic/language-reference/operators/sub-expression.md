---
title: Sous-expression (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [Visual Basic], sub expression
- Sub Expression [Visual Basic]
- subroutines [Visual Basic], sub expressions
ms.assetid: 36b6bfd1-6539-4d8f-a5eb-6541a745ffde
ms.openlocfilehash: 6cdb75f150831ae3857a510d87b58773bdcf13c9
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64609595"
---
# <a name="sub-expression-visual-basic"></a>Sous-expression (Visual Basic)
Déclare les paramètres et le code qui définissent une expression lambda de sous-routine.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Sub ( [ parameterlist ] ) statement  
- or -  
Sub ( [ parameterlist ] )  
  [ statements ]  
End Sub  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`parameterlist`|Facultatif. Liste des noms de variables locales qui représentent les paramètres de la procédure. Les parenthèses doivent être présents même lorsque la liste est vide. Pour plus d'informations, consultez [Parameter List](../../../visual-basic/language-reference/statements/parameter-list.md).|  
|`statement`|Obligatoire. Une instruction unique.|  
|`statements`|Obligatoire. Une liste d’instructions.|  
  
## <a name="remarks"></a>Notes  
 Un *expression lambda* est une sous-routine qui n’a pas un nom et qui s’exécute une ou plusieurs instructions. Vous pouvez utiliser une expression lambda n’importe où que vous pouvez utiliser un type délégué, sauf en tant qu’argument à `RemoveHandler`. Pour plus d’informations sur les délégués et l’utilisation d’expressions lambda avec les délégués, consultez [instruction Delegate](../../../visual-basic/language-reference/statements/delegate-statement.md) et [Conversion souple des délégués](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).  
  
## <a name="lambda-expression-syntax"></a>Syntaxe d’expression lambda  
 La syntaxe d’une expression lambda ressemble à celle d’une sous-routine standard. Les différences sont les suivantes :  
  
- Une expression lambda n’a pas un nom.  
  
- Une expression lambda ne peut pas avoir un modificateur, tel que `Overloads` ou `Overrides`.  
  
- Le corps d’une expression lambda sur une ligne doit être une instruction, pas une expression. Le corps peut se composer d’un appel à une procédure sub, mais pas un appel à une procédure de fonction.  
  
- Dans une expression lambda, soit tous les paramètres doivent avoir spécifié tous les paramètres ou types de données doivent être déduits.  
  
- Facultatif et `ParamArray` paramètres ne sont pas autorisés dans les expressions lambda.  
  
- Paramètres génériques ne sont pas autorisées dans les expressions lambda.  
  
## <a name="example"></a>Exemple  
 Voici un exemple d’une expression lambda qui écrit une valeur dans la console. L’exemple montre les deux la syntaxe d’expression lambda multiligne ou plusieurs lignes d’une sous-routine. Pour plus d’exemples, consultez [Expressions Lambda](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).  
  
 [!code-vb[VbVbalrLambdas#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#15)]  
  
## <a name="see-also"></a>Voir aussi

- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Expressions lambda](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [Opérateurs et expressions](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
- [Instructions](../../../visual-basic/programming-guide/language-features/statements.md)
- [Conversion simplifiée des délégués](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
