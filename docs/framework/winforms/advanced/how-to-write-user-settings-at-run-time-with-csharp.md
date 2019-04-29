---
title: 'Procédure : écrire des paramètres utilisateur au moment de l’exécution avec C#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], run time
- application settings [Windows Forms], writing user settings
- application settings [Windows Forms], C#
ms.assetid: 9d061c7d-b33b-470f-a36d-edccb1d6f9a3
ms.openlocfilehash: 264fa9706f9255d7324cad6d02c36cc424e28995
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778831"
---
# <a name="how-to-write-user-settings-at-run-time-with-c"></a>Procédure : Écrire des paramètres utilisateur en cours d’exécution avec C\#

Les paramètres de portée application sont en lecture seule et ne peuvent être modifiés qu'au moment du design ou en modifiant le fichier .config entre les sessions d'application. Les paramètres de portée utilisateur peuvent être écrits au moment de l'exécution tout comme vous modifieriez une valeur de propriété. La nouvelle valeur est conservée pendant toute la durée de la session d'application. Vous pouvez conserver les modifications apportées aux paramètres d'une session d'application à une autre en appelant la méthode Save.  
  
## <a name="how-to-write-and-persist-user-settings-at-run-time-with-c"></a>Procédure : Écrire et conserver des paramètres utilisateur en cours d’exécution avec C\#
  
1. Accédez au paramètre et attribuez-lui une nouvelle valeur comme indiqué dans cet exemple :  
  
   ```csharp
   Properties.Settings.Default.myColor = Color.AliceBlue;  
   ```  
  
2. Si vous souhaitez conserver les modifications apportées aux paramètres d'une session d'application à l'autre, appelez la méthode Save comme indiqué dans cet exemple :  
  
    ```csharp
    Properties.Settings.Default.Save();  
    ```  
  
Les paramètres utilisateur sont enregistrés dans un fichier dans un sous-dossier du dossier de données d’application masqué local de l’utilisateur.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de paramètres d'application et de paramètres utilisateur](using-application-settings-and-user-settings.md)
- [Guide pratique pour Lire des paramètres au moment de l’exécution avecC#](how-to-read-settings-at-run-time-with-csharp.md)
- [Vue d'ensemble des paramètres d'application](application-settings-overview.md)
