---
title: 'Procédure : Appeler une méthode déléguée (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: b56866ae-abf9-4a5a-a855-486359455e9c
ms.openlocfilehash: 42d56fca7e1d33c071db2e7e38935aa00caa5b7d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676209"
---
# <a name="how-to-invoke-a-delegate-method-visual-basic"></a><span data-ttu-id="e6b22-102">Procédure : Appeler une méthode déléguée (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e6b22-102">How to: Invoke a Delegate Method (Visual Basic)</span></span>
<span data-ttu-id="e6b22-103">Cet exemple montre comment associer une méthode à un délégué, puis appelez cette méthode via le délégué.</span><span class="sxs-lookup"><span data-stu-id="e6b22-103">This example shows how to associate a method with a delegate and then invoke that method through the delegate.</span></span>  
  
### <a name="create-the-delegate-and-matching-procedures"></a><span data-ttu-id="e6b22-104">Créer le délégué et les procédures correspondantes</span><span class="sxs-lookup"><span data-stu-id="e6b22-104">Create the delegate and matching procedures</span></span>  
  
1.  <span data-ttu-id="e6b22-105">Créez un délégué nommé `MySubDelegate`.</span><span class="sxs-lookup"><span data-stu-id="e6b22-105">Create a delegate named `MySubDelegate`.</span></span>  
  
    ```  
    Delegate Sub MySubDelegate(ByVal x As Integer)  
    ```  
  
2.  <span data-ttu-id="e6b22-106">Déclarez une classe qui contient une méthode avec la même signature que le délégué.</span><span class="sxs-lookup"><span data-stu-id="e6b22-106">Declare a class that contains a method with the same signature as the delegate.</span></span>  
  
    ```  
    Class class1  
        Sub Sub1(ByVal x As Integer)  
            MsgBox("The value of x is: " & CStr(x))  
        End Sub  
    End Class  
    ```  
  
3.  <span data-ttu-id="e6b22-107">Définir une méthode qui crée une instance du délégué et appelle la méthode associée au délégué en appelant intégrés `Invoke` (méthode).</span><span class="sxs-lookup"><span data-stu-id="e6b22-107">Define a method that creates an instance of the delegate and invokes the method associated with the delegate by calling the built-in `Invoke` method.</span></span>  
  
    ```  
    Protected Sub DelegateTest()  
        Dim c1 As New class1  
        ' Create an instance of the delegate.  
        Dim msd As MySubDelegate = AddressOf c1.Sub1  
        ' Call the method.  
        msd.Invoke(10)  
    End Sub  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="e6b22-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6b22-108">See also</span></span>

- [<span data-ttu-id="e6b22-109">Delegate (instruction)</span><span class="sxs-lookup"><span data-stu-id="e6b22-109">Delegate Statement</span></span>](../../../../visual-basic/language-reference/statements/delegate-statement.md)
- [<span data-ttu-id="e6b22-110">Délégués</span><span class="sxs-lookup"><span data-stu-id="e6b22-110">Delegates</span></span>](../../../../visual-basic/programming-guide/language-features/delegates/index.md)
- [<span data-ttu-id="e6b22-111">Événements</span><span class="sxs-lookup"><span data-stu-id="e6b22-111">Events</span></span>](../../../../visual-basic/programming-guide/language-features/events/index.md)
- [<span data-ttu-id="e6b22-112">Applications multithread</span><span class="sxs-lookup"><span data-stu-id="e6b22-112">Multithreaded Applications</span></span>](../../../../standard/threading/using-threads-and-threading.md)
