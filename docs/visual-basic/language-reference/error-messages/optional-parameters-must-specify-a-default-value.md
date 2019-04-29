---
title: Les paramètres optionnels doivent spécifier une valeur par défaut
ms.date: 07/20/2015
f1_keywords:
- vbc30812
- bc30812
helpviewer_keywords:
- BC30812
ms.assetid: 5091a250-be66-413b-98a3-2a9974c4d600
ms.openlocfilehash: 01c0abb366e8605a9b153333e645fc3276b6bd16
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772591"
---
# <a name="optional-parameters-must-specify-a-default-value"></a>Les paramètres optionnels doivent spécifier une valeur par défaut
Paramètres optionnels doivent fournir des valeurs par défaut qui peuvent être utilisées si aucun paramètre n’est fourni par une procédure appelante.  
  
 **ID d’erreur :** BC30812  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Spécifiez les valeurs par défaut pour les paramètres facultatifs ; par exemple :  
  
    ```  
    Sub Proc1(ByVal X As Integer,   
          Optional ByVal Y As String = "Default Value")  
       MsgBox("Default argument is: " & Y)  
    End Sub  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Optional](../../../visual-basic/language-reference/modifiers/optional.md)
