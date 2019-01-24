---
title: 'Procédure : Écrire des paramètres utilisateur en cours d’exécution avecC#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], run time
- application settings [Windows Forms], writing user settings
- application settings [Windows Forms], C#
ms.assetid: 9d061c7d-b33b-470f-a36d-edccb1d6f9a3
ms.openlocfilehash: a62bf540ebdc383f26bd4aed760b2562437047aa
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54560937"
---
# <a name="how-to-write-user-settings-at-run-time-with-c"></a><span data-ttu-id="ad2f8-102">Procédure : Écrire des paramètres utilisateur en cours d’exécution avecC#</span><span class="sxs-lookup"><span data-stu-id="ad2f8-102">How To: Write User Settings at Run Time with C#</span></span> #
<span data-ttu-id="ad2f8-103">Les paramètres de portée application sont en lecture seule et ne peuvent être modifiés qu'au moment du design ou en modifiant le fichier .config entre les sessions d'application.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-103">Settings that are application-scoped are read-only, and can only be changed at design time or by altering the .config file in between application sessions.</span></span> <span data-ttu-id="ad2f8-104">Les paramètres de portée utilisateur peuvent être écrits au moment de l'exécution tout comme vous modifieriez une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-104">Settings that are user-scoped, however, can be written at run time just as you would change any property value.</span></span> <span data-ttu-id="ad2f8-105">La nouvelle valeur est conservée pendant toute la durée de la session d'application.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-105">The new value persists for the duration of the application session.</span></span> <span data-ttu-id="ad2f8-106">Vous pouvez conserver les modifications apportées aux paramètres d'une session d'application à une autre en appelant la méthode Save.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-106">You can persist the changes to the settings between application sessions by calling the Save method.</span></span>  
  
### <a name="how-to-write-and-persist-user-settings-at-run-time-with-c"></a><span data-ttu-id="ad2f8-107">Procédure : Écrire et conserver des paramètres utilisateur en cours d’exécution avecC#</span><span class="sxs-lookup"><span data-stu-id="ad2f8-107">How To: Write and Persist User Settings at Run Time with C#</span></span>  
  
1.  <span data-ttu-id="ad2f8-108">Accédez au paramètre et attribuez-lui une nouvelle valeur comme indiqué dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="ad2f8-108">Access the setting and assign it a new value as shown in this example:</span></span>  
  
    ```  
    // C#  
    Properties.Settings.Default.myColor = Color.AliceBlue;  
    ```  
  
2.  <span data-ttu-id="ad2f8-109">Si vous souhaitez conserver les modifications apportées aux paramètres d'une session d'application à l'autre, appelez la méthode Save comme indiqué dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="ad2f8-109">If you want to persist the changes to the settings between application sessions, call the Save method as shown in this example:</span></span>  
  
    ```  
    // C#  
    Properties.Settings.Default.Save();  
    ```  
  
     <span data-ttu-id="ad2f8-110">Les paramètres utilisateur sont enregistrés dans un fichier dans un sous-dossier du dossier de données d’application masqué local de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad2f8-110">User settings are saved in a file within a subfolder of the user’s local hidden application data folder.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad2f8-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad2f8-111">See also</span></span>
- [<span data-ttu-id="ad2f8-112">Utilisation de paramètres d'application et de paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="ad2f8-112">Using Application Settings and User Settings</span></span>](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)
- [<span data-ttu-id="ad2f8-113">Guide pratique pour Lire des paramètres au moment de l’exécution avecC#</span><span class="sxs-lookup"><span data-stu-id="ad2f8-113">How To: Read Settings at Run Time With C#</span></span>](../../../../docs/framework/winforms/advanced/how-to-read-settings-at-run-time-with-csharp.md)
- [<span data-ttu-id="ad2f8-114">Vue d'ensemble des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="ad2f8-114">Application Settings Overview</span></span>](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
