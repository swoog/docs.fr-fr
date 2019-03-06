---
title: Expressions lambda (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.LambdaFunction
helpviewer_keywords:
- functions [Visual Basic], lambda expressions
- lambda expressions [Visual Basic]
- expressions [Visual Basic], lambda
- inline functions [Visual Basic]
ms.assetid: 137064b0-3928-4bfa-ba71-c3f9cbd951e2
ms.openlocfilehash: 02377b0765144064df8d51fa63768412ca4b606a
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57363475"
---
# <a name="lambda-expressions-visual-basic"></a>Expressions lambda (Visual Basic)
Un *expression lambda* est une fonction ou une sous-routine sans nom qui peut être utilisé partout où un délégué est valid. Expressions lambda peuvent être des fonctions ou sous-routines et peuvent être une ou plusieurs lignes. Vous pouvez transmettre des valeurs à partir de la portée actuelle à une expression lambda.  
  
> [!NOTE]
>  La `RemoveHandler` instruction est une exception. Vous ne pouvez pas passer une expression lambda pour le paramètre de délégué de `RemoveHandler`.  
  
 Vous créez des expressions lambda à l’aide de la `Function` ou `Sub` mot clé, tout comme vous créez une fonction standard ou une sous-routine. Toutefois, les expressions lambda sont incluses dans une instruction.  
  
 L’exemple suivant est une expression lambda qui incrémente son argument et retourne la valeur. L’exemple montre les deux la syntaxe d’expression lambda multiligne ou de plusieurs lignes pour une fonction.  
  
 [!code-vb[VbVbalrLambdas#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#14)]  
  
 L’exemple suivant est une expression lambda qui écrit une valeur dans la console. L’exemple montre les deux la syntaxe d’expression lambda multiligne ou de plusieurs lignes d’une sous-routine.  
  
 [!code-vb[VbVbalrLambdas#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#15)]  
  
 Notez que, dans les exemples précédents, les expressions lambda sont affectées à un nom de variable. Chaque fois que vous faites référence à la variable, vous appelez l’expression lambda. Vous pouvez également déclarer et appeler une expression lambda en même temps, comme illustré dans l’exemple suivant.  
  
 [!code-vb[VbVbalrLambdas#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#3)]  
  
 Une expression lambda peut être retournée en tant que la valeur d’un appel de fonction (comme illustré dans l’exemple de la [contexte](#context) section plus loin dans cette rubrique), ou transmise en tant qu’argument à un paramètre qui accepte un type délégué, comme indiqué dans le code suivant exemple.  
  
 [!code-vb[VbVbalrLambdas#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class2.vb#8)]  
  
## <a name="lambda-expression-syntax"></a>Syntaxe d’expression lambda  
 La syntaxe d’une expression lambda ressemble à celle d’une fonction standard ou une sous-routine. Les différences sont les suivantes :  
  
-   Une expression lambda n’a pas un nom.  
  
-   Expressions lambda ne peut pas avoir de modificateurs, tels que `Overloads` ou `Overrides`.  
  
-   Les fonctions lambda sur une ligne n’utilisent pas un `As` clause pour désigner le type de retour. Au lieu de cela, le type est déduit à partir de la valeur que prend le corps de l’expression lambda. Par exemple, si le corps de l’expression lambda est `cust.City = "London"`, son type de retour est `Boolean`.  
  
-   Dans les fonctions lambda sur plusieurs lignes, vous pouvez spécifier un type de retour à l’aide un `As` clause, ou omettre le `As` clause afin que le type de retour est déduit. Lorsque le `As` clause est omise pour une fonction lambda sur plusieurs lignes, le type de retour est déduit pour être le type dominant à partir de tous les `Return` instructions dans la fonction lambda sur plusieurs lignes. Le *type dominant* est un type unique auquel tous les autres types peuvent s’étendre. Si ce type unique ne peut pas être déterminé, le type dominant est le type unique auquel tous les autres types dans le tableau peuvent se limiter. Si aucun de ces types uniques ne peut être déterminé, le type dominant est `Object`. Dans ce cas, si `Option Strict` a la valeur `On`, une erreur du compilateur se produit.  
  
     Par exemple, si les expressions fournies dans le `Return` instruction contiennent des valeurs de type `Integer`, `Long`, et `Double`, le tableau obtenu est de type `Double`. Les deux `Integer` et `Long` s’étendre au `Double` et uniquement `Double`. Par conséquent, `Double` est le type dominant. Pour plus d’informations, consultez [Widening and Narrowing Conversions](../../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md).  
  
-   Le corps d’une fonction d’une ligne doit être une expression qui retourne une valeur, pas une instruction. Il existe aucune `Return` instruction pour les fonctions d’une ligne. La valeur retournée par la fonction d’une ligne est la valeur de l’expression dans le corps de la fonction.  
  
-   Le corps d’une sous-routine sur une ligne doit être l’instruction de ligne.  
  
-   Fonctions sur une ligne et des sous-routines n’incluent pas une `End Function` ou `End Sub` instruction.  
  
-   Vous pouvez spécifier le type de données d’un paramètre d’expression lambda à l’aide de la `As` mot clé ou le type de données du paramètre peut être déduit. Tous les paramètres doivent avoir spécifié les types de données ou l’ensemble doit être déduit.  
  
-   `Optional` et `Paramarray` les paramètres ne sont pas autorisés.  
  
-   Paramètres génériques ne sont pas autorisées.  
  
## <a name="async-lambdas"></a>Lambdas asynchrones  
 Vous pouvez facilement créer des expressions lambda et des instructions qui incorporent le traitement asynchrone à l’aide de la [Async](../../../../visual-basic/language-reference/modifiers/async.md) et [opérateur Await](../../../../visual-basic/language-reference/operators/await-operator.md) mots clés. Par exemple, l'exemple Windows Forms suivant contient un gestionnaire d'événements qui appelle et attend une méthode async `ExampleMethodAsync`.  
  
```vb  
Public Class Form1  
  
    Async Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click  
        ' ExampleMethodAsync returns a Task.  
        Await ExampleMethodAsync()  
        TextBox1.Text = vbCrLf & "Control returned to button1_Click."  
    End Sub  
  
    Async Function ExampleMethodAsync() As Task  
        ' The following line simulates a task-returning asynchronous process.  
        Await Task.Delay(1000)  
    End Function  
  
End Class  
```  
  
 Vous pouvez ajouter le même gestionnaire d’événements à l’aide d’une expression lambda asynchrone dans un [AddHandler, instruction](../../../../visual-basic/language-reference/statements/addhandler-statement.md). Pour ajouter ce gestionnaire, ajoutez un modificateur `Async` avant la liste des paramètres lambda, comme le montre l'exemple suivant.  
  
```vb  
Public Class Form1  
  
    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load  
        AddHandler Button1.Click,   
            Async Sub(sender1, e1)  
                ' ExampleMethodAsync returns a Task.  
                Await ExampleMethodAsync()  
                TextBox1.Text = vbCrLf & "Control returned to Button1_ Click."  
            End Sub  
    End Sub  
  
    Async Function ExampleMethodAsync() As Task  
        ' The following line simulates a task-returning asynchronous process.  
        Await Task.Delay(1000)  
    End Function  
  
End Class  
```  
  
 Pour plus d’informations sur comment créer et utiliser des méthodes asynchrones, consultez [programmation asynchrone avec Async et Await](../../../../visual-basic/programming-guide/concepts/async/index.md).  
  
## <a name="context"></a> Contexte  
 Une expression lambda partage son contexte avec l’étendue dans laquelle il est défini. Il a les mêmes droits d’accès que tout code écrit dans l’étendue contenante. Cela inclut l’accès à des variables membres, des fonctions et des sous-routines, `Me`et des paramètres et des variables locales dans l’étendue contenante.  
  
 Accès aux variables locales et les paramètres dans l’étendue contenante peut s’étendre au-delà de la durée de vie de cette étendue. Tant qu’un délégué se référant à une expression lambda n’est pas disponible pour le garbage collection, l’accès aux variables dans l’environnement d’origine est conservé. Dans l’exemple suivant, la variable `target` est local à `makeTheGame`, la méthode dans laquelle l’expression lambda `playTheGame` est défini. Notez que l’expression lambda retournée, assignée à `takeAGuess` dans `Main`, a toujours accès à la variable locale `target`.  
  
 [!code-vb[VbVbalrLambdas#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class6.vb#12)]  
  
 L’exemple suivant montre le large éventail de droits d’accès de l’expression lambda imbriquée. Lorsque l’expression lambda retournée est exécutée à partir de `Main` comme `aDel`, il accède aux éléments suivants :  
  
-   Un champ de la classe dans laquelle elle est définie : `aField`  
  
-   Une propriété de la classe dans laquelle elle est définie : `aProp`  
  
-   Un paramètre de méthode `functionWithNestedLambda`, dans lequel il est défini : `level1`  
  
-   Une variable locale du `functionWithNestedLambda`: `localVar`  
  
-   Un paramètre de l’expression lambda dans laquelle elle est imbriquée : `level2`  
  
 [!code-vb[VbVbalrLambdas#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class3.vb#9)]  
  
## <a name="converting-to-a-delegate-type"></a>Conversion en un Type délégué  
 Une expression lambda peut être implicitement convertie en un type délégué compatible. Pour plus d’informations sur la configuration générale requise pour la compatibilité, consultez [Conversion souple des délégués](../../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md). Par exemple, l’exemple de code suivant montre une expression lambda qui convertit implicitement en `Func(Of Integer, Boolean)` ou une signature de délégué correspondant.  
  
 [!code-vb[VbVbalrLambdas#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#16)]  
  
 L’exemple de code suivant montre une expression lambda qui convertit implicitement en `Sub(Of Double, String, Double)` ou une signature de délégué correspondant.  
  
 [!code-vb[VbVbalrLambdas#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/class7.vb#23)]  
  
 Lorsque vous assignez des expressions lambda aux délégués ou les passer comme arguments à des procédures, vous pouvez spécifier les noms de paramètres, mais omettre leurs types de données, les types vous permettant de prendre à partir du délégué.  
  
## <a name="examples"></a>Exemples  
  
-   L’exemple suivant définit une expression lambda qui retourne `True` si l’argument nullable a une valeur assignée, et `False` si sa valeur est `Nothing`.  
  
     [!code-vb[VbVbalrLambdas#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#4)]  
  
-   L’exemple suivant définit une expression lambda qui retourne l’index du dernier élément dans un tableau.  
  
     [!code-vb[VbVbalrLambdas#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrLambdas/VB/Class1.vb#5)]  
  
## <a name="see-also"></a>Voir aussi
- [Procédures](./index.md)
- [Introduction à LINQ en Visual Basic](../../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)
- [Délégués](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [Function (instruction)](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Sub (instruction)](../../../../visual-basic/language-reference/statements/sub-statement.md)
- [Types valeur Nullable](../../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [Guide pratique pour Passer des procédures à une autre procédure en Visual Basic](../../../../visual-basic/programming-guide/language-features/delegates/how-to-pass-procedures-to-another-procedure.md)
- [Guide pratique pour Créer une Expression Lambda](./how-to-create-a-lambda-expression.md)
- [Conversion simplifiée des délégués](../../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
