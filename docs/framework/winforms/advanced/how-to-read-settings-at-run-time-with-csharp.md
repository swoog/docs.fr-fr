---
title: 'Procédure : Lire des paramètres au moment de l’exécution avecC#'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], reading
- application settings [Windows Forms], run time
- application settings [Windows Forms], C#
ms.assetid: dbe8bf09-5e1c-49da-9192-154033d7240b
ms.openlocfilehash: 8cdc1a79f1ab327ae037cd6a04aa769196405127
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56974846"
---
# <a name="how-to-read-settings-at-run-time-with-c"></a><span data-ttu-id="e41d8-102">Procédure : Lire des paramètres au moment de l’exécution avec C\#</span><span class="sxs-lookup"><span data-stu-id="e41d8-102">How To: Read Settings at Run Time With C\#</span></span>

<span data-ttu-id="e41d8-103">Vous pouvez lire les paramètres de portée application et de portée utilisateur au moment de l'exécution via l'objet Propriétés.</span><span class="sxs-lookup"><span data-stu-id="e41d8-103">You can read both Application-scoped and User-scoped settings at run time via the Properties object.</span></span> <span data-ttu-id="e41d8-104">L'objet Propriétés expose tous les paramètres par défaut du projet via le membre Properties.Settings.Default.</span><span class="sxs-lookup"><span data-stu-id="e41d8-104">The Properties object exposes all of the default settings for the project via the Properties.Settings.Default member.</span></span>  
  
## <a name="to-read-settings-at-run-time-with-c"></a><span data-ttu-id="e41d8-105">Pour lire des paramètres au moment de l’exécution avec C\#</span><span class="sxs-lookup"><span data-stu-id="e41d8-105">To Read Settings at Run Time with C\#</span></span>
  
<span data-ttu-id="e41d8-106">Accédez au paramètre approprié via le membre Properties.Settings.Default.</span><span class="sxs-lookup"><span data-stu-id="e41d8-106">Access the appropriate setting via the Properties.Settings.Default member.</span></span> <span data-ttu-id="e41d8-107">L'exemple suivant montre comment affecter un paramètre nommé `myColor` à une propriété BackColor.</span><span class="sxs-lookup"><span data-stu-id="e41d8-107">The following example shows how to assign a setting named `myColor` to a BackColor property.</span></span> <span data-ttu-id="e41d8-108">Au préalable, vous devez avoir créé un fichier de paramètres contenant un paramètre nommé `myColor` de type `System.Drawing.Color`.</span><span class="sxs-lookup"><span data-stu-id="e41d8-108">It requires you to have previously created a Settings file containing a setting named `myColor` of type `System.Drawing.Color`.</span></span> <span data-ttu-id="e41d8-109">Pour plus d’informations sur la création d’un fichier de paramètres, consultez [How To : Créer un nouveau paramètre au moment du Design](how-to-create-a-new-setting-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="e41d8-109">For information about creating a Settings file, see [How To: Create a New Setting at Design Time](how-to-create-a-new-setting-at-design-time.md).</span></span>  
  
```csharp
this.BackColor = Properties.Settings.Default.myColor;  
```  
  
## <a name="see-also"></a><span data-ttu-id="e41d8-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e41d8-110">See also</span></span>

- [<span data-ttu-id="e41d8-111">Utilisation de paramètres d'application et de paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="e41d8-111">Using Application Settings and User Settings</span></span>](using-application-settings-and-user-settings.md)
- [<span data-ttu-id="e41d8-112">Guide pratique pour Écrire des paramètres utilisateur en cours d’exécution avecC#</span><span class="sxs-lookup"><span data-stu-id="e41d8-112">How To: Write User Settings at Run Time with C#</span></span>](how-to-write-user-settings-at-run-time-with-csharp.md)
- [<span data-ttu-id="e41d8-113">Vue d'ensemble des paramètres d'application</span><span class="sxs-lookup"><span data-stu-id="e41d8-113">Application Settings Overview</span></span>](application-settings-overview.md)
