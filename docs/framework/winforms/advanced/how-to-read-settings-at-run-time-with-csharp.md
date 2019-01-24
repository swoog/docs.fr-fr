---
title: 'Procédure : Lire des paramètres au moment de l’exécution avecC#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], reading
- application settings [Windows Forms], run time
- application settings [Windows Forms], C#
ms.assetid: dbe8bf09-5e1c-49da-9192-154033d7240b
ms.openlocfilehash: d798b40e5e337ea7652c8e82cb7fa860a87528b9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521749"
---
# <a name="how-to-read-settings-at-run-time-with-c"></a>Procédure : Lire des paramètres au moment de l’exécution avecC# #
Vous pouvez lire les paramètres de portée application et de portée utilisateur au moment de l'exécution via l'objet Propriétés. L'objet Propriétés expose tous les paramètres par défaut du projet via le membre Properties.Settings.Default.  
  
### <a name="to-read-settings-at-run-time-with-c"></a>Pour lire des paramètres au moment de l'exécution avec C#  
  
-   Accédez au paramètre approprié via le membre Properties.Settings.Default. L'exemple suivant montre comment affecter un paramètre nommé `myColor` à une propriété BackColor. Au préalable, vous devez avoir créé un fichier de paramètres contenant un paramètre nommé `myColor` de type `System.Drawing.Color`. Pour plus d’informations sur la création d’un fichier de paramètres, consultez [How To : Créer un nouveau paramètre au moment du Design](../../../../docs/framework/winforms/advanced/how-to-create-a-new-setting-at-design-time.md).  
  
    ```  
    // C#  
    this.BackColor = Properties.Settings.Default.myColor;  
    ```  
  
## <a name="see-also"></a>Voir aussi
- [Utilisation de paramètres d'application et de paramètres utilisateur](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)
- [Guide pratique pour Écrire des paramètres utilisateur en cours d’exécution avecC#](../../../../docs/framework/winforms/advanced/how-to-write-user-settings-at-run-time-with-csharp.md)
- [Vue d'ensemble des paramètres d'application](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
