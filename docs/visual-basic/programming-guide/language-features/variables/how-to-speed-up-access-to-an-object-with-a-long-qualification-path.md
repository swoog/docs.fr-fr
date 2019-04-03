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
ms.openlocfilehash: b10876c22d2f6dd5832baa0d498db7c4205a3fcb
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58816281"
---
# <a name="how-to-speed-up-access-to-an-object-with-a-long-qualification-path-visual-basic"></a>Procédure : Accélérer l’accès à un objet avec un chemin d’accès de Qualification Long (Visual Basic)
Si vous accédez fréquemment à un objet qui requiert un chemin d’accès de qualification de plusieurs méthodes et propriétés, vous pouvez accélérer votre code en répétant ne pas le chemin d’accès de qualification.  
  
 Il existe deux façons vous pouvez éviter de répéter le chemin d’accès de qualification. Vous pouvez affecter l’objet à une variable, ou vous pouvez l’utiliser dans un `With`... `End With` bloc.  
  
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
  
### <a name="to-speed-up-access-to-a-heavily-qualified-object-by-using-a-withend-with-block"></a>Pour accélérer l’accès à un objet très qualifié à l’aide de r avec... Bloc End With  
  
1.  Placez le chemin d’accès de qualification dans un `With` instruction.  
  
    ```  
    With someForm.ActiveForm.ActiveControl  
    ```  
  
2.  Accéder aux membres de l’objet à l’intérieur de la `With` bloquer avant la `End With` instruction.  
  
    ```  
        .Text = "Test"  
        .Location = New Point(100, 100)  
        .Show()  
    End With  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Variables objets](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)
- [With...End With (instruction)](../../../../visual-basic/language-reference/statements/with-end-with-statement.md)
