---
title: 'Comment : accélérer l’accès à un objet comportant un chemin d’accès de qualification long (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], accessing
- variables [Visual Basic], object
- With statement [Visual Basic]
- With block
- object variables [Visual Basic], accessing
ms.assetid: 3eb7657f-c9fe-4e05-8bc3-4bb14d5ae585
ms.openlocfilehash: d52d13feb0f85065c0623b5937f558b841c036dd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33650197"
---
# <a name="how-to-speed-up-access-to-an-object-with-a-long-qualification-path-visual-basic"></a><span data-ttu-id="fc9df-102">Comment : accélérer l’accès à un objet comportant un chemin d’accès de qualification long (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fc9df-102">How to: Speed Up Access to an Object with a Long Qualification Path (Visual Basic)</span></span>
<span data-ttu-id="fc9df-103">Si vous accédez fréquemment à un objet qui requiert un chemin d’accès de qualification de plusieurs méthodes et propriétés, vous pouvez accélérer votre code en évitant de répéter le chemin d’accès de qualification.</span><span class="sxs-lookup"><span data-stu-id="fc9df-103">If you frequently access an object that requires a qualification path of several methods and properties, you can speed up your code by not repeating the qualification path.</span></span>  
  
 <span data-ttu-id="fc9df-104">Il existe deux façons, vous pouvez éviter de répéter le chemin d’accès de qualification.</span><span class="sxs-lookup"><span data-stu-id="fc9df-104">There are two ways you can avoid repeating the qualification path.</span></span> <span data-ttu-id="fc9df-105">Vous pouvez l’attribuer à une variable, ou vous pouvez l’utiliser dans un `With`... `End With` bloc.</span><span class="sxs-lookup"><span data-stu-id="fc9df-105">You can assign the object to a variable, or you can use it in a `With`...`End With` block.</span></span>  
  
### <a name="to-speed-up-access-to-a-heavily-qualified-object-by-assigning-it-to-a-variable"></a><span data-ttu-id="fc9df-106">Pour accélérer l’accès à un objet très qualifié en l’assignant à une variable</span><span class="sxs-lookup"><span data-stu-id="fc9df-106">To speed up access to a heavily qualified object by assigning it to a variable</span></span>  
  
1.  <span data-ttu-id="fc9df-107">Déclarez une variable du type de l’objet auquel vous accédez fréquemment.</span><span class="sxs-lookup"><span data-stu-id="fc9df-107">Declare a variable of the type of the object that you are accessing frequently.</span></span> <span data-ttu-id="fc9df-108">Spécifiez le chemin d’accès de qualification dans la partie de l’initialisation de la déclaration.</span><span class="sxs-lookup"><span data-stu-id="fc9df-108">Specify the qualification path in the initialization part of the declaration.</span></span>  
  
    ```  
    Dim ctrlActv As Control = someForm.ActiveForm.ActiveControl  
    ```  
  
2.  <span data-ttu-id="fc9df-109">Utilisez la variable pour accéder aux membres de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fc9df-109">Use the variable to access the object's members.</span></span>  
  
    ```  
    ctrlActv.Text = "Test"  
    ctrlActv.Location = New Point(100, 100)  
    ctrlActv.Show()  
    ```  
  
### <a name="to-speed-up-access-to-a-heavily-qualified-object-by-using-a-withend-with-block"></a><span data-ttu-id="fc9df-110">Pour accélérer l’accès à un objet très qualifié à l’aide de With... Bloc de fin avec</span><span class="sxs-lookup"><span data-stu-id="fc9df-110">To speed up access to a heavily qualified object by using a With...End With block</span></span>  
  
1.  <span data-ttu-id="fc9df-111">Placez le chemin d’accès de qualification dans un `With` instruction.</span><span class="sxs-lookup"><span data-stu-id="fc9df-111">Put the qualification path in a `With` statement.</span></span>  
  
    ```  
    With someForm.ActiveForm.ActiveControl  
    ```  
  
2.  <span data-ttu-id="fc9df-112">Accéder aux membres de l’objet à l’intérieur de la `With` bloquer, avant la `End With` instruction.</span><span class="sxs-lookup"><span data-stu-id="fc9df-112">Access the object's members inside the `With` block, before the `End With` statement.</span></span>  
  
    ```  
        .Text = "Test"  
        .Location = New Point(100, 100)  
        .Show()  
    End With  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="fc9df-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc9df-113">See Also</span></span>  
 [<span data-ttu-id="fc9df-114">Variables objets</span><span class="sxs-lookup"><span data-stu-id="fc9df-114">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)  
 [<span data-ttu-id="fc9df-115">With...End With (instruction)</span><span class="sxs-lookup"><span data-stu-id="fc9df-115">With...End With Statement</span></span>](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
