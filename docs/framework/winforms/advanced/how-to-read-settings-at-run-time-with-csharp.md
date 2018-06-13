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
ms.locfileid: "33521012"
---
# <a name="how-to-read-settings-at-run-time-with-c"></a><span data-ttu-id="28d96-102">Comment : lire des paramètres au moment de l'exécution avec C#</span><span class="sxs-lookup"><span data-stu-id="28d96-102">How To: Read Settings at Run Time With C#</span></span> #
<span data-ttu-id="28d96-103">Vous pouvez lire les paramètres de portée application et de portée utilisateur au moment de l'exécution via l'objet Propriétés.</span><span class="sxs-lookup"><span data-stu-id="28d96-103">You can read both Application-scoped and User-scoped settings at run time via the Properties object.</span></span> <span data-ttu-id="28d96-104">L'objet Propriétés expose tous les paramètres par défaut du projet via le membre Properties.Settings.Default.</span><span class="sxs-lookup"><span data-stu-id="28d96-104">The Properties object exposes all of the default settings for the project via the Properties.Settings.Default member.</span></span>  
  
### <a name="to-read-settings-at-run-time-with-c"></a><span data-ttu-id="28d96-105">Pour lire des paramètres au moment de l'exécution avec C#</span><span class="sxs-lookup"><span data-stu-id="28d96-105">To Read Settings at Run Time with C#</span></span>  
  
-   <span data-ttu-id="28d96-106">Accédez au paramètre approprié via le membre Properties.Settings.Default.</span><span class="sxs-lookup"><span data-stu-id="28d96-106">Access the appropriate setting via the Properties.Settings.Default member.</span></span> <span data-ttu-id="28d96-107">L'exemple suivant montre comment affecter un paramètre nommé `myColor` à une propriété BackColor.</span><span class="sxs-lookup"><span data-stu-id="28d96-107">The following example shows how to assign a setting named `myColor` to a BackColor property.</span></span> <span data-ttu-id="28d96-108">Au préalable, vous devez avoir créé un fichier de paramètres contenant un paramètre nommé `myColor` de type `System.Drawing.Color`.</span><span class="sxs-lookup"><span data-stu-id="28d96-108">It requires you to have previously created a Settings file containing a setting named `myColor` of type `System.Drawing.Color`.</span></span> <span data-ttu-id="28d96-109">Pour plus d’informations sur la création d’un fichier de paramètres, consultez [comment faire : créer un nouveau paramètre au moment du Design](../../../../docs/framework/winforms/advanced/how-to-create-a-new-setting-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="28d96-109">For information about creating a Settings file, see [How To: Create a New Setting at Design Time](../../../../docs/framework/winforms/advanced/how-to-create-a-new-setting-at-design-time.md).</span></span>  
  
    ```  
    // C#  
    this.BackColor = Properties.Settings.Default.myColor;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="28d96-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28d96-110">See Also</span></span>  
 [<span data-ttu-id="28d96-111">Utilisation de paramètres d'application et de paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="28d96-111">Using Application Settings and User Settings</span></span>](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)  
 [<span data-ttu-id="28d96-112">Guide pratique pour écrire des paramètres utilisateur au moment de l'exécution avec C#</span><span class="sxs-lookup"><span data-stu-id="28d96-112">How To: Write User Settings at Run Time with C#</span></span>](../../../../docs/framework/winforms/advanced/how-to-write-user-settings-at-run-time-with-csharp.md)  
 [<span data-ttu-id="28d96-113">Vue d'ensemble des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="28d96-113">Application Settings Overview</span></span>](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
