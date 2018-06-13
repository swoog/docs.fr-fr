---
title: 'Comment : appeler une méthode déléguée (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: b56866ae-abf9-4a5a-a855-486359455e9c
ms.openlocfilehash: aca87dd9fa1990d44c99aab7753f2fd7d508adc1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33646950"
---
# <a name="how-to-invoke-a-delegate-method-visual-basic"></a>Comment : appeler une méthode déléguée (Visual Basic)
Cet exemple montre comment associer une méthode à un délégué, puis appelez cette méthode via le délégué.  
  
### <a name="create-the-delegate-and-matching-procedures"></a>Création du délégué et les procédures correspondantes  
  
1.  Créez un délégué nommé `MySubDelegate`.  
  
    ```  
    Delegate Sub MySubDelegate(ByVal x As Integer)  
    ```  
  
2.  Déclarez une classe qui contient une méthode avec la même signature que le délégué.  
  
    ```  
    Class class1  
        Sub Sub1(ByVal x As Integer)  
            MsgBox("The value of x is: " & CStr(x))  
        End Sub  
    End Class  
    ```  
  
3.  Définir une méthode qui crée une instance du délégué et appelle la méthode associée au délégué en appelant la fonction intégrée `Invoke` (méthode).  
  
    ```  
    Protected Sub DelegateTest()  
        Dim c1 As New class1  
        ' Create an instance of the delegate.  
        Dim msd As MySubDelegate = AddressOf c1.Sub1  
        ' Call the method.  
        msd.Invoke(10)  
    End Sub  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [Delegate (instruction)](../../../../visual-basic/language-reference/statements/delegate-statement.md)  
 [Délégués](../../../../visual-basic/programming-guide/language-features/delegates/index.md)  
 [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md)  
 [Applications multithread](http://msdn.microsoft.com/library/a06a1a56-dd16-44e8-bc01-2c2255511bc6)
