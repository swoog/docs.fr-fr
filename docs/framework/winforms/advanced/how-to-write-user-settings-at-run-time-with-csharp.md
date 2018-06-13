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
# <a name="how-to-write-user-settings-at-run-time-with-c"></a><span data-ttu-id="57dc4-102">Comment : écrire des paramètres utilisateur au moment de l'exécution avec C#</span><span class="sxs-lookup"><span data-stu-id="57dc4-102">How To: Write User Settings at Run Time with C#</span></span> #
<span data-ttu-id="57dc4-103">Les paramètres de portée application sont en lecture seule et ne peuvent être modifiés qu'au moment du design ou en modifiant le fichier .config entre les sessions d'application.</span><span class="sxs-lookup"><span data-stu-id="57dc4-103">Settings that are application-scoped are read-only, and can only be changed at design time or by altering the .config file in between application sessions.</span></span> <span data-ttu-id="57dc4-104">Les paramètres de portée utilisateur peuvent être écrits au moment de l'exécution tout comme vous modifieriez une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="57dc4-104">Settings that are user-scoped, however, can be written at run time just as you would change any property value.</span></span> <span data-ttu-id="57dc4-105">La nouvelle valeur est conservée pendant toute la durée de la session d'application.</span><span class="sxs-lookup"><span data-stu-id="57dc4-105">The new value persists for the duration of the application session.</span></span> <span data-ttu-id="57dc4-106">Vous pouvez conserver les modifications apportées aux paramètres d'une session d'application à une autre en appelant la méthode Save.</span><span class="sxs-lookup"><span data-stu-id="57dc4-106">You can persist the changes to the settings between application sessions by calling the Save method.</span></span>  
  
### <a name="how-to-write-and-persist-user-settings-at-run-time-with-c"></a><span data-ttu-id="57dc4-107">Comment : écrire et conserver des paramètres utilisateur au moment de l'exécution avec C#</span><span class="sxs-lookup"><span data-stu-id="57dc4-107">How To: Write and Persist User Settings at Run Time with C#</span></span>  
  
1.  <span data-ttu-id="57dc4-108">Accédez au paramètre et attribuez-lui une nouvelle valeur comme indiqué dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="57dc4-108">Access the setting and assign it a new value as shown in this example:</span></span>  
  
    ```  
    // C#  
    Properties.Settings.Default.myColor = Color.AliceBlue;  
    ```  
  
2.  <span data-ttu-id="57dc4-109">Si vous souhaitez conserver les modifications apportées aux paramètres d'une session d'application à l'autre, appelez la méthode Save comme indiqué dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="57dc4-109">If you want to persist the changes to the settings between application sessions, call the Save method as shown in this example:</span></span>  
  
    ```  
    // C#  
    Properties.Settings.Default.Save();  
    ```  
  
     <span data-ttu-id="57dc4-110">Les paramètres utilisateur sont enregistrés dans un fichier dans un sous-dossier du dossier de données d’application masqué local de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="57dc4-110">User settings are saved in a file within a subfolder of the user’s local hidden application data folder.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57dc4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57dc4-111">See Also</span></span>  
 [<span data-ttu-id="57dc4-112">Utilisation de paramètres d'application et de paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="57dc4-112">Using Application Settings and User Settings</span></span>](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)  
 [<span data-ttu-id="57dc4-113">Guide pratique pour lire des paramètres au moment de l'exécution avec C#</span><span class="sxs-lookup"><span data-stu-id="57dc4-113">How To: Read Settings at Run Time With C#</span></span>](../../../../docs/framework/winforms/advanced/how-to-read-settings-at-run-time-with-csharp.md)  
 [<span data-ttu-id="57dc4-114">Vue d'ensemble des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="57dc4-114">Application Settings Overview</span></span>](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
