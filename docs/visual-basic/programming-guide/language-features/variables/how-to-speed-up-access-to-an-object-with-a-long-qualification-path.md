---
title: 'Procédure : Accélérer l’accès à un objet avec un chemin d’accès de Qualification Long (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], accessing
- variables [Visual Basic], object
- With statement [Visual Basic]
- With block
- object variables [Visual Basic], accessing
ms.assetid: 3eb7657f-c9fe-4e05-8bc3-4bb14d5ae585
ms.openlocfilehash: 94c838a69aab9fcae9dc0c79b6038ee90e2369e7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59299135"
---
# <a name="how-to-speed-up-access-to-an-object-with-a-long-qualification-path-visual-basic"></a>Procédure : Accélérer l’accès à un objet avec un chemin d’accès de Qualification Long (Visual Basic)
Si vous accédez fréquemment à un objet qui requiert un chemin d’accès de qualification de plusieurs méthodes et propriétés, vous pouvez accélérer votre code en répétant ne pas le chemin d’accès de qualification.  
  
 Il existe deux façons vous pouvez éviter de répéter le chemin d’accès de qualification. Vous pouvez affecter l’objet à une variable, ou vous pouvez l’utiliser dans un `With`... `End With` bloc.  
  
### <a name="to-speed-up-access-to-a-heavily-qualified-object-by-assigning-it-to-a-variable"></a>Pour accélérer l’accès à un objet très qualifié en l’assignant à une variable  
  
1. Déclarez une variable du type de l’objet auquel vous accédez fréquemment. Spécifiez le chemin d’accès de qualification dans la partie de l’initialisation de la déclaration.  
  
    ```  
    Dim ctrlActv As Control = someForm.ActiveForm.ActiveControl  
    ```  
  
2. Utilisez la variable pour accéder aux membres de l’objet.  
  
    ```  
    ctrlActv.Text = "Test"  
    ctrlActv.Location = New Point(100, 100)  
    ctrlActv.Show()  
    ```  
  
### <a name="to-speed-up-access-to-a-heavily-qualified-object-by-using-a-withend-with-block"></a>Pour accélérer l’accès à un objet très qualifié à l’aide de r avec... Bloc End With  
  
1. Placez le chemin d’accès de qualification dans un `With` instruction.  
  
    ```  
    With someForm.ActiveForm.ActiveControl  
    ```  
  
2. Accéder aux membres de l’objet à l’intérieur de la `With` bloquer avant la `End With` instruction.  
  
    ```  
        .Text = "Test"  
        .Location = New Point(100, 100)  
        .Show()  
    End With  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [With...End With (instruction)](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
