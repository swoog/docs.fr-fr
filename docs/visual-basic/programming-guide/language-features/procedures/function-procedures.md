---
title: Procédures Function (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Function procedures
- return values [Visual Basic], function procedures
- Visual Basic code, procedures
- procedures [Visual Basic], calling
- procedures [Visual Basic], Function procedures
- syntax [Visual Basic], function procedures
ms.assetid: 1b9f632c-553b-4cb6-920a-ded117ead8c0
ms.openlocfilehash: 568489d6034316e895cd999801241fa995aadefa
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58834242"
---
# <a name="function-procedures-visual-basic"></a>Procédures Function (Visual Basic)
Un `Function` procédure est une série d’instructions Visual Basic délimitée par le `Function` et `End Function` instructions. Le `Function` procédure effectue une tâche, puis retourne le contrôle au code appelant. Lorsqu’elle retourne le contrôle, elle retourne également une valeur au code appelant.  
  
 Chaque fois que la procédure est appelée, ses instructions sont exécutées, en commençant par la première instruction exécutable après le `Function` instruction et se terminant par la première `End Function`, `Exit Function`, ou `Return` instruction rencontrée.  
  
 Vous pouvez définir un `Function` procédure dans un module, une classe ou une structure. Il est `Public` par défaut, ce qui signifie que vous pouvez l’appeler depuis n’importe où dans votre application qui a accès au module, classe ou structure dans laquelle vous l’avez définie.  
  
 Un `Function` procédure peut prendre des arguments, tels que les constantes, variables ou expressions qui sont passées par le code appelant.  
  
## <a name="declaration-syntax"></a>Syntaxe de déclaration  
 La syntaxe pour déclarer un `Function` procédure est la suivante :  
  
```vb  
[Modifiers] Function FunctionName [(ParameterList)] As ReturnType  
    [Statements]  
End Function  
```  
  
 Le *modificateurs* peut spécifier des informations concernant la surcharge, substitution, le partage et l’occultation et niveau d’accès. Pour plus d’informations, consultez [Function, instruction](../../../../visual-basic/language-reference/statements/function-statement.md).  
  
 Vous déclarez chaque paramètre de la même façon que vous le feriez pour [procédures Sub](./sub-procedures.md).  
  
### <a name="data-type"></a>Type de données  
 Chaque `Function` procédure possède un type de données, de fait de simplement chaque variable. Ce type de données est spécifié par le `As` clause dans la `Function` instruction, qui détermine le type de données de la valeur de la fonction retourne au code appelant. Les exemples de déclarations suivantes illustrent ce principe.  
  
```vb  
Function yesterday() As Date  
End Function  
  
Function findSqrt(ByVal radicand As Single) As Single  
End Function  
```  
  
 Pour plus d’informations, consultez « Parties » dans [Function, instruction](../../../../visual-basic/language-reference/statements/function-statement.md).  
  
## <a name="returning-values"></a>Retourner des valeurs  
 La valeur un `Function` procédure envoie arrière au code appelant est appelé sa valeur de retour. La procédure retourne cette valeur de deux manières :  
  
-   Il utilise le `Return` contrôler l’instruction pour spécifier la valeur de retour et retourne immédiatement au programme appelant. L'exemple suivant illustre ce comportement.  
  
```vb  
Function FunctionName [(ParameterList)] As ReturnType  
    ' The following statement immediately transfers control back  
    ' to the calling code and returns the value of Expression.  
    Return Expression  
End Function  
```  
  
-   Il attribue une valeur à son propre nom de fonction dans une ou plusieurs instructions de la procédure. Contrôle ne retourne pas au programme appelant jusqu'à un `Exit Function` ou `End Function` instruction est exécutée. L'exemple suivant illustre ce comportement.  
  
```vb  
Function FunctionName [(ParameterList)] As ReturnType  
    ' The following statement does not transfer control back to the calling code.  
    FunctionName = Expression  
    ' When control returns to the calling code, Expression is the return value.  
End Function  
```  
  
 L’avantage de l’affectation de la valeur de retour pour le nom de fonction est que le contrôle ne retourne pas de la procédure, jusqu'à ce qu’il rencontre un `Exit Function` ou `End Function` instruction. Cela vous permet de vous assigner une valeur préliminaire et l’ajuster ultérieurement si nécessaire.  
  
 Pour plus d’informations sur le retour de valeurs, consultez [Function, instruction](../../../../visual-basic/language-reference/statements/function-statement.md). Pour plus d’informations sur le retour des tableaux, consultez [tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md).  
  
## <a name="calling-syntax"></a>Syntaxe d’appel  
 Vous appelez un `Function` procédure en incluant son nom et ses arguments soit situé à droite d’une instruction d’assignation ou dans une expression. Vous devez fournir des valeurs pour tous les arguments qui ne sont pas facultatives, et vous devez placer la liste d’arguments entre parenthèses. Si aucun argument n’est fourni, vous pouvez éventuellement omettre les parenthèses.  
  
 La syntaxe pour un appel à une `Function` procédure est la suivante :  
  
 *lvalue*  `=`  *functionname* `[(` *argumentlist* `)]`  
  
 `If ((` *functionname* `[(` *argumentlist* `)] / 3) <=`  *expression* `) Then`  
  
 Lorsque vous appelez un `Function` procédure, il est inutile d’utiliser sa valeur de retour. Si vous ne le faites pas, toutes les actions de la fonction sont exécutées, mais la valeur de retour est ignorée. <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> est souvent appelé de cette manière.  
  
### <a name="illustration-of-declaration-and-call"></a>Illustration de déclaration et d’appel  
 Ce qui suit `Function` procédure calcule le côté le plus long, ou hypoténuse, d’un triangle rectangle, d’après les valeurs pour les deux côtés.  
  
 [!code-vb[VbVbcnProcedures#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#1)]  
  
 L’exemple suivant montre un appel typique à `hypotenuse`.  
  
 [!code-vb[VbVbcnProcedures#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#6)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Function (instruction)](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Guide pratique pour Créer une procédure qui retourne une valeur](./how-to-create-a-procedure-that-returns-a-value.md)
- [Guide pratique pour Retourner une valeur à partir d’une procédure](./how-to-return-a-value-from-a-procedure.md)
- [Guide pratique pour Appeler une procédure qui retourne une valeur](./how-to-call-a-procedure-that-returns-a-value.md)
