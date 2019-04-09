---
title: Utilisation de paramètres d'application et de paramètres utilisateur
ms.date: 03/30/2017
helpviewer_keywords:
- user settings [Windows Forms]
- application settings [Windows Forms], how-to topics
ms.assetid: 54682d3b-1cbf-4683-9351-012b8b4286b5
ms.openlocfilehash: ea6994e653b3a06239634f5a0fddea84a07086e2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59107261"
---
# <a name="using-application-settings-and-user-settings"></a><span data-ttu-id="972ca-102">Utilisation de paramètres d'application et de paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="972ca-102">Using Application Settings and User Settings</span></span>
<span data-ttu-id="972ca-103">À compter de .NET Framework 2.0, vous pouvez créer et accéder aux valeurs qui sont conservées entre les sessions de l’exécution d’application.</span><span class="sxs-lookup"><span data-stu-id="972ca-103">Starting with the .NET Framework 2.0, you can create and access values that are persisted between application execution sessions.</span></span> <span data-ttu-id="972ca-104">Ces valeurs sont appelées *paramètres*.</span><span class="sxs-lookup"><span data-stu-id="972ca-104">These values are called *settings*.</span></span> <span data-ttu-id="972ca-105">Les paramètres peuvent représenter des préférences de l’utilisateur ou des informations précieuses l’application doivent utiliser.</span><span class="sxs-lookup"><span data-stu-id="972ca-105">Settings can represent user preferences, or valuable information the application needs to use.</span></span> <span data-ttu-id="972ca-106">Par exemple, vous pouvez créer une série de paramètres correspondant aux préférences de l’utilisateur pour le jeu de couleurs d’une application.</span><span class="sxs-lookup"><span data-stu-id="972ca-106">For example, you might create a series of settings that store user preferences for the color scheme of an application.</span></span> <span data-ttu-id="972ca-107">Ou vous pouvez stocker la chaîne de connexion qui spécifie une base de données que votre application utilise.</span><span class="sxs-lookup"><span data-stu-id="972ca-107">Or you might store the connection string that specifies a database that your application uses.</span></span> <span data-ttu-id="972ca-108">Les paramètres permettent de que vous permettent de conserver des informations critiques à l’application en dehors du code et pour créer des profils qui stockent les préférences des utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="972ca-108">Settings allow you to both persist information that is critical to the application outside the code, and to create profiles that store the preferences of individual users.</span></span>  
  
 <span data-ttu-id="972ca-109">Les rubriques de cette section décrivent comment utiliser des paramètres au moment du design et la durée d’exécution.</span><span class="sxs-lookup"><span data-stu-id="972ca-109">The topics in this section describe how to use settings at design time and run time.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="972ca-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="972ca-110">In This Section</span></span>  
 [<span data-ttu-id="972ca-111">Procédure : créer un paramètre au moment du design</span><span class="sxs-lookup"><span data-stu-id="972ca-111">How To: Create a New Setting at Design Time</span></span>](how-to-create-a-new-setting-at-design-time.md)  
  
 <span data-ttu-id="972ca-112">Explique comment utiliser Visual Studio pour créer un nouveau paramètre pour une application.</span><span class="sxs-lookup"><span data-stu-id="972ca-112">Explains how to use Visual Studio to create a new setting for an application.</span></span>  
  
 [<span data-ttu-id="972ca-113">Procédure : modifier la valeur d’un paramètre existant au moment du design</span><span class="sxs-lookup"><span data-stu-id="972ca-113">How To: Change the Value of an Existing Setting at Design Time</span></span>](how-to-change-the-value-of-an-existing-setting-at-design-time.md)  
  
 <span data-ttu-id="972ca-114">Décrit comment utiliser Visual Studio pour modifier la valeur d’un paramètre existant.</span><span class="sxs-lookup"><span data-stu-id="972ca-114">Describes how to use Visual Studio to change the value of an existing setting.</span></span>  
  
 [<span data-ttu-id="972ca-115">Procédure : modifier la valeur d’un paramètre entre des sessions d’application</span><span class="sxs-lookup"><span data-stu-id="972ca-115">How To: Change the Value of a Setting Between Application Sessions</span></span>](how-to-change-the-value-of-a-setting-between-application-sessions.md)  
  
 <span data-ttu-id="972ca-116">Explique comment modifier la valeur d’un paramètre dans une application compilée entre les sessions de l’application.</span><span class="sxs-lookup"><span data-stu-id="972ca-116">Details how to change the value of a setting in a compiled application between application sessions.</span></span>  
  
 [<span data-ttu-id="972ca-117">Procédure : lire des paramètres au moment de l’exécution avec C#</span><span class="sxs-lookup"><span data-stu-id="972ca-117">How To: Read Settings at Run Time With C#</span></span>](how-to-read-settings-at-run-time-with-csharp.md)  
  
 <span data-ttu-id="972ca-118">Décrit comment utiliser le code pour lire des paramètres avec C#.</span><span class="sxs-lookup"><span data-stu-id="972ca-118">Describes how to use code to read settings with C#.</span></span>  
  
 [<span data-ttu-id="972ca-119">Procédure : écrire des paramètres utilisateur au moment de l’exécution avec C#</span><span class="sxs-lookup"><span data-stu-id="972ca-119">How To: Write User Settings at Run Time with C#</span></span>](how-to-write-user-settings-at-run-time-with-csharp.md)  
  
 <span data-ttu-id="972ca-120">Explique comment utiliser le code pour écrire et enregistrer les valeurs des paramètres utilisateur avec C#.</span><span class="sxs-lookup"><span data-stu-id="972ca-120">Explains how to use code to write and save the values of user settings with C#.</span></span>  
  
 [<span data-ttu-id="972ca-121">Procédure : ajouter plusieurs jeux de paramètres à votre application en C#</span><span class="sxs-lookup"><span data-stu-id="972ca-121">How To: Add Multiple Sets of Settings To Your Application in C#</span></span>](how-to-add-multiple-sets-of-settings-to-your-application-in-csharp.md)  
  
 <span data-ttu-id="972ca-122">Explique comment ajouter plusieurs jeux de paramètres à une application avec C#.</span><span class="sxs-lookup"><span data-stu-id="972ca-122">Details how to add multiple sets of settings to an application with C#.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="972ca-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="972ca-123">See also</span></span>

- [<span data-ttu-id="972ca-124">Paramètres d'application pour les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="972ca-124">Application Settings for Windows Forms</span></span>](application-settings-for-windows-forms.md)
