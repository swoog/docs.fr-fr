---
title: 'Procédure : lire des paramètres au moment de l’exécution avec C#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], reading
- application settings [Windows Forms], run time
- application settings [Windows Forms], C#
ms.assetid: dbe8bf09-5e1c-49da-9192-154033d7240b
ms.openlocfilehash: 8cdc1a79f1ab327ae037cd6a04aa769196405127
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61966908"
---
# <a name="how-to-read-settings-at-run-time-with-c"></a>Procédure : Lire des paramètres au moment de l’exécution avec C\#

Vous pouvez lire les paramètres de portée application et de portée utilisateur au moment de l'exécution via l'objet Propriétés. L'objet Propriétés expose tous les paramètres par défaut du projet via le membre Properties.Settings.Default.  
  
## <a name="to-read-settings-at-run-time-with-c"></a>Pour lire des paramètres au moment de l’exécution avec C\#
  
Accédez au paramètre approprié via le membre Properties.Settings.Default. L'exemple suivant montre comment affecter un paramètre nommé `myColor` à une propriété BackColor. Au préalable, vous devez avoir créé un fichier de paramètres contenant un paramètre nommé `myColor` de type `System.Drawing.Color`. Pour plus d’informations sur la création d’un fichier de paramètres, consultez [How To : Créer un nouveau paramètre au moment du Design](how-to-create-a-new-setting-at-design-time.md).  
  
```csharp
this.BackColor = Properties.Settings.Default.myColor;  
```  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation de paramètres d'application et de paramètres utilisateur](using-application-settings-and-user-settings.md)
- [Guide pratique pour Écrire des paramètres utilisateur en cours d’exécution avecC#](how-to-write-user-settings-at-run-time-with-csharp.md)
- [Vue d'ensemble des paramètres d'application](application-settings-overview.md)
