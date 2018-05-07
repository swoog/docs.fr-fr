---
title: "Comment : lire des paramètres au moment de l'exécution avec C#"
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], reading
- application settings [Windows Forms], run time
- application settings [Windows Forms], C#
ms.assetid: dbe8bf09-5e1c-49da-9192-154033d7240b
ms.openlocfilehash: 8259e2f429718793c01868855651d1000620fae5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-read-settings-at-run-time-with-c"></a>Comment : lire des paramètres au moment de l'exécution avec C# #
Vous pouvez lire les paramètres de portée application et de portée utilisateur au moment de l'exécution via l'objet Propriétés. L'objet Propriétés expose tous les paramètres par défaut du projet via le membre Properties.Settings.Default.  
  
### <a name="to-read-settings-at-run-time-with-c"></a>Pour lire des paramètres au moment de l'exécution avec C#  
  
-   Accédez au paramètre approprié via le membre Properties.Settings.Default. L'exemple suivant montre comment affecter un paramètre nommé `myColor` à une propriété BackColor. Au préalable, vous devez avoir créé un fichier de paramètres contenant un paramètre nommé `myColor` de type `System.Drawing.Color`. Pour plus d’informations sur la création d’un fichier de paramètres, consultez [comment faire : créer un nouveau paramètre au moment du Design](../../../../docs/framework/winforms/advanced/how-to-create-a-new-setting-at-design-time.md).  
  
    ```  
    // C#  
    this.BackColor = Properties.Settings.Default.myColor;  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [Utilisation de paramètres d'application et de paramètres utilisateur](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)  
 [Guide pratique pour écrire des paramètres utilisateur au moment de l'exécution avec C#](../../../../docs/framework/winforms/advanced/how-to-write-user-settings-at-run-time-with-csharp.md)  
 [Vue d'ensemble des paramètres d'application](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
