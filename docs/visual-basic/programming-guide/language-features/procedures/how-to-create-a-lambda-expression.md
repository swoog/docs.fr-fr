---
title: 'Procédure : Créer une Expression Lambda (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [Visual Basic]
- expressions [Visual Basic], lambda
ms.assetid: 3279bd5c-80f7-410a-a7ba-f7085ed36aa5
ms.openlocfilehash: 35df64848c0506a1c0a97bd8cd34f158f9febcd7
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56970166"
---
# <a name="how-to-create-a-lambda-expression-visual-basic"></a>Procédure : Créer une Expression Lambda (Visual Basic)
Un *expression lambda* est une fonction ou une sous-routine qui n’a pas de nom. Une expression lambda peut être utilisée partout où un type délégué est valide.  
  
### <a name="to-create-a-single-line-lambda-expression-function"></a>Pour créer une fonction d’expression lambda sur une ligne  
  
1.  Dans les cas où un type délégué peut être utilisé, tapez le mot clé `Function`, comme dans l’exemple suivant :  
  
     `Dim add1 =`   `Function`  
  
2.  Entre parenthèses, directement après `Function`, tapez les paramètres de la fonction. Notez que vous ne spécifiez pas de nom après `Function`.  
  
     `Dim add1 = Function`   `(num As Integer)`  
  
3.  Après la liste de paramètres, tapez une expression unique comme corps de la fonction. La valeur que prend l’expression est la valeur retournée par la fonction. Vous n’utilisez pas un `As` clause pour spécifier le type de retour.  
  
     [!code-vb[VbVbalrLambdas#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#1)]  
  
     Vous appelez l’expression lambda en passant un argument entier.  
  
     [!code-vb[VbVbalrLambdas#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#2)]  
  
4.  Vous pouvez également le même résultat s’effectue par l’exemple suivant :  
  
     [!code-vb[VbVbalrLambdas#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#3)]  
  
### <a name="to-create-a-single-line-lambda-expression-subroutine"></a>Pour créer une sous-routine d’expression lambda sur une ligne  
  
1.  Dans les cas où un type délégué peut être utilisé, tapez le mot clé `Sub`, comme illustré dans l’exemple suivant.  
  
     `Dim add1 =`   `Sub`  
  
2.  Entre parenthèses, directement après `Sub`, tapez les paramètres de la sous-routine. Notez que vous ne spécifiez pas de nom après `Sub`.  
  
     `Dim add1 = Sub`   `(msg As String)`  
  
3.  À la suite de la liste de paramètres, tapez une instruction unique comme corps de la sous-routine.  
  
     [!code-vb[VbVbalrLambdas#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#17)]  
  
     Vous appelez l’expression lambda en passant un argument de chaîne.  
  
     [!code-vb[VbVbalrLambdas#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#18)]  
  
### <a name="to-create-a-multiline-lambda-expression-function"></a>Pour créer une fonction d’expression lambda multiligne  
  
1.  Dans les cas où un type délégué peut être utilisé, tapez le mot clé `Function`, comme illustré dans l’exemple suivant.  
  
     `Dim add1 =`   `Function`  
  
2.  Entre parenthèses, directement après `Function`, tapez les paramètres de la fonction. Notez que vous ne spécifiez pas de nom après `Function`.  
  
     `Dim add1 = Function`   `(index As Integer)`  
  
3.  Appuyez sur Entrée. La `End Function` instruction est automatiquement ajoutée.  
  
4.  Dans le corps de la fonction, ajoutez le code suivant pour créer une expression et la valeur de retour. Vous n’utilisez pas un `As` clause pour spécifier le type de retour.  
  
     [!code-vb[VbVbalrLambdas#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#19)]  
  
     Vous appelez l’expression lambda en passant un argument entier.  
  
     [!code-vb[VbVbalrLambdas#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#20)]  
  
### <a name="to-create-a-multiline-lambda-expression-subroutine"></a>Pour créer une sous-routine d’expression lambda multiligne  
  
1.  Dans les cas où un type délégué peut être utilisé, tapez le mot clé `Sub`, comme illustré dans l’exemple suivant :  
  
     `Dim add1 =`   `Sub`  
  
2.  Entre parenthèses, directement après `Sub`, tapez les paramètres de la sous-routine. Notez que vous ne spécifiez pas de nom après `Sub`.  
  
     `Dim add1 = Sub`  `(msg As String)`  
  
3.  Appuyez sur Entrée. La `End Sub` instruction est automatiquement ajoutée.  
  
4.  Dans le corps de la fonction, ajoutez le code suivant à exécuter lorsque la sous-routine est appelée.  
  
     [!code-vb[VbVbalrLambdas#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#21)]  
  
     Vous appelez l’expression lambda en passant un argument de chaîne.  
  
     [!code-vb[VbVbalrLambdas#22](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#22)]  
  
## <a name="example"></a>Exemple  
 Une utilisation courante des expressions lambda consiste à définir une fonction qui peut être passée comme argument pour un paramètre dont le type est `Delegate`. Dans l’exemple suivant, la <xref:System.Diagnostics.Process.GetProcesses%2A> méthode retourne un tableau des processus en cours d’exécution sur l’ordinateur local. Le <xref:System.Linq.Enumerable.Where%2A> méthode à partir de la <xref:System.Linq.Enumerable> classe nécessite une `Boolean` délégué comme argument. L’expression lambda dans l’exemple est utilisée à cet effet. Elle retourne `True` pour chaque processus qui a un seul thread, et ces dernières sont sélectionnées dans `filteredList`.  
  
 [!code-vb[VbVbalrLambdas#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class4.vb#10)]  
  
 L’exemple précédent équivaut au code suivant, qui est écrit en [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] syntaxe :  
  
 [!code-vb[VbVbalrLambdas#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class5.vb#11)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Linq.Enumerable>
- [Expressions lambda](./lambda-expressions.md)
- [Function (instruction)](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Sub (instruction)](../../../../visual-basic/language-reference/statements/sub-statement.md)
- [Délégués](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [Guide pratique pour Passer des procédures à une autre procédure en Visual Basic](../../../../visual-basic/programming-guide/language-features/delegates/how-to-pass-procedures-to-another-procedure.md)
- [Delegate (instruction)](../../../../visual-basic/language-reference/statements/delegate-statement.md)
- [Introduction à LINQ en Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
