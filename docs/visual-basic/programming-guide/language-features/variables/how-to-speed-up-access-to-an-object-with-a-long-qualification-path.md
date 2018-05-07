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
---
# <a name="how-to-speed-up-access-to-an-object-with-a-long-qualification-path-visual-basic"></a>Comment : accélérer l’accès à un objet comportant un chemin d’accès de qualification long (Visual Basic)
Si vous accédez fréquemment à un objet qui requiert un chemin d’accès de qualification de plusieurs méthodes et propriétés, vous pouvez accélérer votre code en évitant de répéter le chemin d’accès de qualification.  
  
 Il existe deux façons, vous pouvez éviter de répéter le chemin d’accès de qualification. Vous pouvez l’attribuer à une variable, ou vous pouvez l’utiliser dans un `With`... `End With` bloc.  
  
### <a name="to-speed-up-access-to-a-heavily-qualified-object-by-assigning-it-to-a-variable"></a>Pour accélérer l’accès à un objet très qualifié en l’assignant à une variable  
  
1.  Déclarez une variable du type de l’objet auquel vous accédez fréquemment. Spécifiez le chemin d’accès de qualification dans la partie de l’initialisation de la déclaration.  
  
    ```  
    Dim ctrlActv As Control = someForm.ActiveForm.ActiveControl  
    ```  
  
2.  Utilisez la variable pour accéder aux membres de l’objet.  
  
    ```  
    ctrlActv.Text = "Test"  
    ctrlActv.Location = New Point(100, 100)  
    ctrlActv.Show()  
    ```  
  
### <a name="to-speed-up-access-to-a-heavily-qualified-object-by-using-a-withend-with-block"></a>Pour accélérer l’accès à un objet très qualifié à l’aide de With... Bloc de fin avec  
  
1.  Placez le chemin d’accès de qualification dans un `With` instruction.  
  
    ```  
    With someForm.ActiveForm.ActiveControl  
    ```  
  
2.  Accéder aux membres de l’objet à l’intérieur de la `With` bloquer, avant la `End With` instruction.  
  
    ```  
        .Text = "Test"  
        .Location = New Point(100, 100)  
        .Show()  
    End With  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)  
 [With...End With (instruction)](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
