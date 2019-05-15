---
title: 'Procédure : Créer et utiliser des assemblys à l’aide de la ligne de commande (Visual Basic)'
ms.date: 03/14/2018
ms.assetid: 229ff9fb-1bd1-403b-946b-526104864c60
ms.openlocfilehash: a30d4b3ea203a8b4d3ba621fc7b0310477ddf10d
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65592688"
---
# <a name="how-to-create-and-use-assemblies-using-the-command-line-visual-basic"></a><span data-ttu-id="4b09b-102">Procédure : Créer et utiliser des assemblys à l’aide de la ligne de commande (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="4b09b-102">How to: Create and Use Assemblies Using the Command Line (Visual Basic)</span></span>
<span data-ttu-id="4b09b-103">Un assembly, ou une bibliothèque de lien dynamique (DLL), est lié à votre programme au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4b09b-103">An assembly, or a dynamic linking library (DLL), is linked to your program at run time.</span></span> <span data-ttu-id="4b09b-104">Pour illustrer la génération et l’utilisation d’une DLL, considérez le scénario suivant :</span><span class="sxs-lookup"><span data-stu-id="4b09b-104">To demonstrate building and using a DLL, consider the following scenario:</span></span>  
  
- <span data-ttu-id="4b09b-105">`MathLibrary.DLL`: fichier bibliothèque qui contient les méthodes à appeler au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4b09b-105">`MathLibrary.DLL`: The library file that contains the methods to be called at run time.</span></span> <span data-ttu-id="4b09b-106">Dans cet exemple, la DLL contient deux méthodes, `Add` et `Multiply`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-106">In this example, the DLL contains two methods, `Add` and `Multiply`.</span></span>  
  
- <span data-ttu-id="4b09b-107">`Add`: fichier source qui contient la méthode `Add`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-107">`Add`: The source file that contains the method `Add`.</span></span> <span data-ttu-id="4b09b-108">Il retourne la somme de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="4b09b-108">It returns the sum of its parameters.</span></span> <span data-ttu-id="4b09b-109">La classe `AddClass` qui contient la méthode `Add` est un membre de l’espace de noms `UtilityMethods`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-109">The class `AddClass` that contains the method `Add` is a member of the namespace `UtilityMethods`.</span></span>  
  
- <span data-ttu-id="4b09b-110">`Mult`: code source qui contient la méthode `Multiply`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-110">`Mult`: The source code that contains the method `Multiply`.</span></span> <span data-ttu-id="4b09b-111">Il retourne le produit de ses paramètres.</span><span class="sxs-lookup"><span data-stu-id="4b09b-111">It returns the product of its parameters.</span></span> <span data-ttu-id="4b09b-112">La classe `MultiplyClass` qui contient la méthode `Multiply` est également un membre de l’espace de noms `UtilityMethods`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-112">The class `MultiplyClass` that contains the method `Multiply` is also a member of the namespace `UtilityMethods`.</span></span>  
  
- <span data-ttu-id="4b09b-113">`TestCode`: fichier qui contient la méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-113">`TestCode`: The file that contains the `Main` method.</span></span> <span data-ttu-id="4b09b-114">Il utilise les méthodes dans le fichier DLL pour calculer la somme et le produit des arguments d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4b09b-114">It uses the methods in the DLL file to calculate the sum and the product of the run-time arguments.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4b09b-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="4b09b-115">Example</span></span>  
  
```vb  
' File: Add.vb   
Namespace UtilityMethods  
    Public Class AddClass  
        Public Shared Function Add(ByVal i As Long, ByVal j As Long) As Long  
            Return i + j  
        End Function  
    End Class  
End Namespace  
```  
  
```vb  
' File: Mult.vb  
Namespace UtilityMethods  
    Public Class MultiplyClass  
        Public Shared Function Multiply(ByVal x As Long, ByVal y As Long) As Long  
            Return x * y  
        End Function  
    End Class  
End Namespace  
```  
  
```vb  
' File: TestCode.vb  
  
Imports UtilityMethods  
  
Module Test  
  
    Sub Main(ByVal args As String())  
  
        System.Console.WriteLine("Calling methods from MathLibrary.DLL:")  
  
        If args.Length <> 2 Then  
            System.Console.WriteLine("Usage: TestCode <num1> <num2>")  
            Return  
        End If  
  
        Dim num1 As Long = Long.Parse(args(0))  
        Dim num2 As Long = Long.Parse(args(1))  
  
        Dim sum As Long = AddClass.Add(num1, num2)  
        Dim product As Long = MultiplyClass.Multiply(num1, num2)  
  
        System.Console.WriteLine("{0} + {1} = {2}", num1, num2, sum)  
        System.Console.WriteLine("{0} * {1} = {2}", num1, num2, product)  
  
    End Sub  
  
End Module  
  
' Output (assuming 1234 and 5678 are entered as command-line arguments):  
' Calling methods from MathLibrary.DLL:  
' 1234 + 5678 = 6912  
' 1234 * 5678 = 7006652  
```  
  
 <span data-ttu-id="4b09b-116">Ce fichier contient l’algorithme qui utilise les méthodes de la DLL, `Add` et `Multiply`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-116">This file contains the algorithm that uses the DLL methods, `Add` and `Multiply`.</span></span> <span data-ttu-id="4b09b-117">Il commence par analyser les arguments entrés à partir de la ligne de commande, `num1` et `num2`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-117">It starts with parsing the arguments entered from the command line, `num1` and `num2`.</span></span> <span data-ttu-id="4b09b-118">Il calcule ensuite la somme en utilisant la méthode `Add` sur la classe `AddClass`, et le produit en utilisant la méthode `Multiply` sur la classe `MultiplyClass`.</span><span class="sxs-lookup"><span data-stu-id="4b09b-118">Then it calculates the sum by using the `Add` method on the `AddClass` class, and the product by using the `Multiply` method on the `MultiplyClass` class.</span></span>  
  
 <span data-ttu-id="4b09b-119">Notez que la `Imports` instruction au début du fichier vous permet d’utiliser les noms de classes non qualifiés pour référencer les méthodes de la DLL au moment de la compilation, comme suit :</span><span class="sxs-lookup"><span data-stu-id="4b09b-119">Notice that the  `Imports` statement at the beginning of the file enables you to use the unqualified class names to reference the DLL methods at compile time, as follows:</span></span>  
  
```vb  
MultiplyClass.Multiply(num1, num2)  
```  
  
 <span data-ttu-id="4b09b-120">Sinon, vous devez utiliser les noms qualifiés complets, comme suit :</span><span class="sxs-lookup"><span data-stu-id="4b09b-120">Otherwise, you have to use the fully qualified names, as follows:</span></span>  
  
```vb  
UtilityMethods.MultiplyClass.Multiply(num1, num2)  
```  
  
## <a name="execution"></a><span data-ttu-id="4b09b-121">Exécution</span><span class="sxs-lookup"><span data-stu-id="4b09b-121">Execution</span></span>  
 <span data-ttu-id="4b09b-122">Pour exécuter le programme, entrez le nom du fichier EXE, suivi de deux nombres, comme suit :</span><span class="sxs-lookup"><span data-stu-id="4b09b-122">To run the program, enter the name of the EXE file, followed by two numbers, as follows:</span></span>  
  
 `TestCode 1234 5678`  
  
## <a name="see-also"></a><span data-ttu-id="4b09b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b09b-123">See also</span></span>

- [<span data-ttu-id="4b09b-124">Concepts de programmation</span><span class="sxs-lookup"><span data-stu-id="4b09b-124">Programming Concepts</span></span>](../../../../visual-basic/programming-guide/concepts/index.md)
- [<span data-ttu-id="4b09b-125">Assemblys dans .NET</span><span class="sxs-lookup"><span data-stu-id="4b09b-125">Assemblies in .NET</span></span>](../../../../standard/assembly/index.md)
- [<span data-ttu-id="4b09b-126">Création d’une classe pour contenir des fonctions DLL</span><span class="sxs-lookup"><span data-stu-id="4b09b-126">Creating a Class to Hold DLL Functions</span></span>](../../../../framework/interop/creating-a-class-to-hold-dll-functions.md)
