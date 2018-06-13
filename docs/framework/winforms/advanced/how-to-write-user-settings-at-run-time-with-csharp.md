---
title: "Comment : écrire des paramètres utilisateur au moment de l'exécution avec C#"
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], run time
- application settings [Windows Forms], writing user settings
- application settings [Windows Forms], C#
ms.assetid: 9d061c7d-b33b-470f-a36d-edccb1d6f9a3
ms.openlocfilehash: f289b6a6a4a726ffa6bb2c9df99c665e2872e8d5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33522293"
---
# <a name="how-to-write-user-settings-at-run-time-with-c"></a>Comment : écrire des paramètres utilisateur au moment de l'exécution avec C# #
Les paramètres de portée application sont en lecture seule et ne peuvent être modifiés qu'au moment du design ou en modifiant le fichier .config entre les sessions d'application. Les paramètres de portée utilisateur peuvent être écrits au moment de l'exécution tout comme vous modifieriez une valeur de propriété. La nouvelle valeur est conservée pendant toute la durée de la session d'application. Vous pouvez conserver les modifications apportées aux paramètres d'une session d'application à une autre en appelant la méthode Save.  
  
### <a name="how-to-write-and-persist-user-settings-at-run-time-with-c"></a>Comment : écrire et conserver des paramètres utilisateur au moment de l'exécution avec C#  
  
1.  Accédez au paramètre et attribuez-lui une nouvelle valeur comme indiqué dans cet exemple :  
  
    ```  
    // C#  
    Properties.Settings.Default.myColor = Color.AliceBlue;  
    ```  
  
2.  Si vous souhaitez conserver les modifications apportées aux paramètres d'une session d'application à l'autre, appelez la méthode Save comme indiqué dans cet exemple :  
  
    ```  
    // C#  
    Properties.Settings.Default.Save();  
    ```  
  
     Les paramètres utilisateur sont enregistrés dans un fichier dans un sous-dossier du dossier de données d’application masqué local de l’utilisateur.  
  
## <a name="see-also"></a>Voir aussi  
 [Utilisation de paramètres d'application et de paramètres utilisateur](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)  
 [Guide pratique pour lire des paramètres au moment de l'exécution avec C#](../../../../docs/framework/winforms/advanced/how-to-read-settings-at-run-time-with-csharp.md)  
 [Vue d'ensemble des paramètres d'application](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
