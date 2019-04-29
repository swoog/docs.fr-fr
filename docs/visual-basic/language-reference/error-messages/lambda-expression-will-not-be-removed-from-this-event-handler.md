---
title: L’expression lambda ne sera pas supprimée de ce gestionnaire d’événements
ms.date: 07/20/2015
f1_keywords:
- bc42326
- vbc42326
helpviewer_keywords:
- BC42326
ms.assetid: 63214dc6-0112-4245-8ebf-7c9e8f5a5782
ms.openlocfilehash: 20e83306925e91e579aca52f2e7c209c8c686dee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946625"
---
# <a name="lambda-expression-will-not-be-removed-from-this-event-handler"></a><span data-ttu-id="b4def-102">L’expression lambda ne sera pas supprimée de ce gestionnaire d’événements</span><span class="sxs-lookup"><span data-stu-id="b4def-102">Lambda expression will not be removed from this event handler</span></span>
<span data-ttu-id="b4def-103">Expression lambda ne sera pas supprimée à partir de ce gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="b4def-103">Lambda expression will not be removed from this event handler.</span></span> <span data-ttu-id="b4def-104">Assignez l’expression lambda à une variable et utilisez la variable pour ajouter et supprimer l’événement.</span><span class="sxs-lookup"><span data-stu-id="b4def-104">Assign the lambda expression to a variable and use the variable to add and remove the event.</span></span>  
  
 <span data-ttu-id="b4def-105">Lorsque les expressions lambda sont utilisées avec les gestionnaires d’événements, vous ne verrez ne peut-être pas le comportement attendu.</span><span class="sxs-lookup"><span data-stu-id="b4def-105">When lambda expressions are used with event handlers, you may not see the behavior you expect.</span></span> <span data-ttu-id="b4def-106">Le compilateur génère une nouvelle méthode pour chaque définition d’expression lambda, même si elles sont identiques.</span><span class="sxs-lookup"><span data-stu-id="b4def-106">The compiler generates a new method for each lambda expression definition, even if they are identical.</span></span> <span data-ttu-id="b4def-107">Par conséquent, le code suivant affiche `False`.</span><span class="sxs-lookup"><span data-stu-id="b4def-107">Therefore, the following code displays `False`.</span></span>  
  
```vb  
Module Module1  
  
    Sub Main()  
        Dim fun1 As ChangeInteger = Function(p As Integer) p + 1  
        Dim fun2 As ChangeInteger = Function(p As Integer) p + 1  
        Console.WriteLine(fun1 = fun2)  
    End Sub  
  
    Delegate Function ChangeInteger(ByVal x As Integer) As Integer  
  
End Module  
```  
  
 <span data-ttu-id="b4def-108">Lorsque les expressions lambda sont utilisées avec les gestionnaires d’événements, cela peut entraîner des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="b4def-108">When lambda expressions are used with event handlers, this may cause unexpected results.</span></span> <span data-ttu-id="b4def-109">Dans l’exemple suivant, l’expression lambda ajoutée par `AddHandler` n’est pas supprimé par le `RemoveHandler` instruction.</span><span class="sxs-lookup"><span data-stu-id="b4def-109">In the following example, the lambda expression added by `AddHandler` is not removed by the `RemoveHandler` statement.</span></span>  
  
```vb  
Module Module1  
  
    Event ProcessInteger(ByVal x As Integer)  
  
    Sub Main()  
  
        ' The following line adds one listener to the event.  
        AddHandler ProcessInteger, Function(m As Integer) m  
  
        ' The following statement searches the current listeners   
        ' for a match to remove. However, this lambda is not the same  
        ' as the previous one, so nothing is removed.  
        RemoveHandler ProcessInteger, Function(m As Integer) m  
  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="b4def-110">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="b4def-110">By default, this message is a warning.</span></span> <span data-ttu-id="b4def-111">Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="b4def-111">For more information about how to hide warnings or treat warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="b4def-112">**ID d’erreur :** BC42326</span><span class="sxs-lookup"><span data-stu-id="b4def-112">**Error ID:** BC42326</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b4def-113">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="b4def-113">To correct this error</span></span>  
  
- <span data-ttu-id="b4def-114">Pour éviter l’avertissement et supprimer l’expression lambda, assignez l’expression lambda à une variable et utilisez la variable à la fois dans le `AddHandler` et `RemoveHandler` instructions, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="b4def-114">To avoid the warning and remove the lambda expression, assign the lambda expression to a variable and use the variable in both the `AddHandler` and `RemoveHandler` statements, as shown in the following example.</span></span>  
  
```vb  
Module Module1  
  
    Event ProcessInteger(ByVal x As Integer)  
  
    Dim PrintHandler As ProcessIntegerEventHandler  
  
    Sub Main()  
  
        ' Assign the lambda expression to a variable.  
        PrintHandler = Function(m As Integer) m  
  
        ' Use the variable to add the listener.  
        AddHandler ProcessInteger, PrintHandler  
  
        ' Use the variable again when you want to remove the listener.  
        RemoveHandler ProcessInteger, PrintHandler  
  
    End Sub  
End Module  
```  
  
## <a name="see-also"></a><span data-ttu-id="b4def-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4def-115">See also</span></span>

- [<span data-ttu-id="b4def-116">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="b4def-116">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
- [<span data-ttu-id="b4def-117">Conversion simplifiée des délégués</span><span class="sxs-lookup"><span data-stu-id="b4def-117">Relaxed Delegate Conversion</span></span>](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
- [<span data-ttu-id="b4def-118">Événements</span><span class="sxs-lookup"><span data-stu-id="b4def-118">Events</span></span>](../../../visual-basic/programming-guide/language-features/events/index.md)
