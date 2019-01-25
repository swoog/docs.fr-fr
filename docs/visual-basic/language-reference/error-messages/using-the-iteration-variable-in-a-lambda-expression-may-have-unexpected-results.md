---
title: L’utilisation de la variable d’itération dans une expression lambda peut provoquer des résultats inattendus
ms.date: 07/20/2015
f1_keywords:
- vbc42324
- bc42324
helpviewer_keywords:
- BC42324
ms.assetid: b5c2c4bd-3b2a-4a73-aaeb-55728eb03b68
ms.openlocfilehash: 358c7a988ae95c2326a26bc048f5436e11acb340
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54641588"
---
# <a name="using-the-iteration-variable-in-a-lambda-expression-may-have-unexpected-results"></a><span data-ttu-id="05841-102">L’utilisation de la variable d’itération dans une expression lambda peut provoquer des résultats inattendus</span><span class="sxs-lookup"><span data-stu-id="05841-102">Using the iteration variable in a lambda expression may have unexpected results</span></span>
<span data-ttu-id="05841-103">L’utilisation de la variable d’itération dans une expression lambda peut avoir des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="05841-103">Using the iteration variable in a lambda expression may have unexpected results.</span></span> <span data-ttu-id="05841-104">Au lieu de cela, créez une variable locale dans la boucle et affectez-lui la valeur de la variable d’itération.</span><span class="sxs-lookup"><span data-stu-id="05841-104">Instead, create a local variable within the loop and assign it the value of the iteration variable.</span></span>  
  
 <span data-ttu-id="05841-105">Cet avertissement s’affiche lorsque vous utilisez une variable d’itération de boucle dans une expression lambda qui est déclarée à l’intérieur de la boucle.</span><span class="sxs-lookup"><span data-stu-id="05841-105">This warning appears when you use a loop iteration variable in a lambda expression that is declared inside the loop.</span></span> <span data-ttu-id="05841-106">Par exemple, l’exemple suivant provoque l’avertissement apparaît.</span><span class="sxs-lookup"><span data-stu-id="05841-106">For example, the following example causes the warning to appear.</span></span>  
  
```vb  
For i As Integer = 1 To 10  
    ' The warning is given for the use of i.  
    Dim exampleFunc As Func(Of Integer) = Function() i  
Next  
```  
  
 <span data-ttu-id="05841-107">L’exemple suivant montre les résultats inattendus peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="05841-107">The following example shows the unexpected results that might occur.</span></span>  
  
```vb  
Module Module1  
    Sub Main()  
        Dim array1 As Func(Of Integer)() = New Func(Of Integer)(4) {}  
  
        For i As Integer = 0 To 4  
            array1(i) = Function() i  
        Next  
  
        For Each funcElement In array1  
            System.Console.WriteLine(funcElement())  
        Next  
  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="05841-108">Le `For` boucle crée un tableau d’expressions lambda, chacune d'entre elles retourne la valeur de la variable d’itération de boucle `i`.</span><span class="sxs-lookup"><span data-stu-id="05841-108">The `For` loop creates an array of lambda expressions, each of which returns the value of the loop iteration variable `i`.</span></span> <span data-ttu-id="05841-109">Lorsque les expressions lambda sont évaluées dans le `For Each` boucle, vous attendez peut-être à voir 0, 1, 2, 3 et 4 affichés, les valeurs consécutives de `i` dans le `For` boucle.</span><span class="sxs-lookup"><span data-stu-id="05841-109">When the lambda expressions are evaluated in the `For Each` loop, you might expect to see 0, 1, 2, 3, and 4 displayed, the successive values of `i` in the `For` loop.</span></span> <span data-ttu-id="05841-110">Au lieu de cela, vous voyez la valeur finale de `i` affichée cinq fois :</span><span class="sxs-lookup"><span data-stu-id="05841-110">Instead, you see the final value of `i` displayed five times:</span></span>  
  
 `5`  
  
 `5`  
  
 `5`  
  
 `5`  
  
 `5`  
  
 <span data-ttu-id="05841-111">Par défaut, ce message est un avertissement.</span><span class="sxs-lookup"><span data-stu-id="05841-111">By default, this message is a warning.</span></span> <span data-ttu-id="05841-112">Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="05841-112">For more information about hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="05841-113">**ID d’erreur :** BC42324</span><span class="sxs-lookup"><span data-stu-id="05841-113">**Error ID:** BC42324</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="05841-114">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="05841-114">To correct this error</span></span>  
  
-   <span data-ttu-id="05841-115">Affectez la valeur de la variable d’itération à une variable locale et utilisez la variable locale dans l’expression lambda.</span><span class="sxs-lookup"><span data-stu-id="05841-115">Assign the value of the iteration variable to a local variable, and use the local variable in the lambda expression.</span></span>  
  
```vb  
Module Module1  
    Sub Main()  
        Dim array1 As Func(Of Integer)() = New Func(Of Integer)(4) {}  
  
        For i As Integer = 0 To 4  
            Dim j = i  
            array1(i) = Function() j  
        Next  
  
        For Each funcElement In array1  
            System.Console.WriteLine(funcElement())  
        Next  
  
    End Sub  
End Module  
```  
  
## <a name="see-also"></a><span data-ttu-id="05841-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05841-116">See also</span></span>
- [<span data-ttu-id="05841-117">Expressions lambda</span><span class="sxs-lookup"><span data-stu-id="05841-117">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)
