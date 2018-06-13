---
title: Utilisation d'activités procédurales
ms.date: 03/30/2017
ms.assetid: 1c67f739-3878-48ad-806c-b2ce0d6733a0
ms.openlocfilehash: 787e61a989cb5769461f5155738520dea4609d1f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33516007"
---
# <a name="using-procedural-activities"></a><span data-ttu-id="e0962-102">Utilisation d'activités procédurales</span><span class="sxs-lookup"><span data-stu-id="e0962-102">Using Procedural Activities</span></span>
<span data-ttu-id="e0962-103">L'exemple utilise les activités <xref:System.Activities.Statements.Sequence>, <xref:System.Activities.Statements.Assign>, <xref:System.Activities.Statements.If>, <xref:System.Activities.Statements.While>, <xref:System.Activities.Statements.Switch%601>, <xref:System.Activities.Statements.TryCatch> et <xref:System.Activities.Statements.WriteLine> pour implémenter un jeu d'estimation.</span><span class="sxs-lookup"><span data-stu-id="e0962-103">The sample uses the <xref:System.Activities.Statements.Sequence>, <xref:System.Activities.Statements.Assign>, <xref:System.Activities.Statements.If>, <xref:System.Activities.Statements.While>, <xref:System.Activities.Statements.Switch%601>, <xref:System.Activities.Statements.TryCatch>, and <xref:System.Activities.Statements.WriteLine> activities to implement a guessing game.</span></span> <span data-ttu-id="e0962-104">Le jeu d'estimation sélectionne un nombre aléatoire et le joueur doit deviner ce nombre.</span><span class="sxs-lookup"><span data-stu-id="e0962-104">The guessing game selects a random number and the player has to guess that number.</span></span> <span data-ttu-id="e0962-105">Lorsque le joueur soumet une estimation incorrecte, le workflow fournit une indication signalant si la valeur à deviner est supérieure ou inférieure.</span><span class="sxs-lookup"><span data-stu-id="e0962-105">When the player submits an incorrect guess, the workflow provides a hint whether to guess higher or lower.</span></span> <span data-ttu-id="e0962-106">Si le joueur devine le nombre en moins de 7 tentatives, un message de félicitation spécial s'affiche à l'attention de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e0962-106">If the player guesses the number in less than 7 attempts, a special congratulations is displayed to the user.</span></span>  
  
## <a name="custom-activities-in-this-sample"></a><span data-ttu-id="e0962-107">Activités personnalisées dans cet exemple</span><span class="sxs-lookup"><span data-stu-id="e0962-107">Custom Activities in this Sample</span></span>  
  
### <a name="readline"></a><span data-ttu-id="e0962-108">ReadLine</span><span class="sxs-lookup"><span data-stu-id="e0962-108">ReadLine</span></span>  
 <span data-ttu-id="e0962-109">Lit une ligne de texte à partir de la console.</span><span class="sxs-lookup"><span data-stu-id="e0962-109">Reads a line of text from the console.</span></span> <span data-ttu-id="e0962-110">Cette activité dérive de la classe <xref:System.Activities.NativeActivity> et crée un signet qui est repris par l'application console lorsqu'une ligne est lue.</span><span class="sxs-lookup"><span data-stu-id="e0962-110">This activity derives from the <xref:System.Activities.NativeActivity> class and creates a bookmark that is resumed by the console application when a line is read.</span></span>  
  
### <a name="promptint"></a><span data-ttu-id="e0962-111">PromptInt</span><span class="sxs-lookup"><span data-stu-id="e0962-111">PromptInt</span></span>  
 <span data-ttu-id="e0962-112">Invite l'utilisateur à taper un nombre, puis le lit à partir d'une fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="e0962-112">Prompts the user to type in a number and then reads it from a console window.</span></span> <span data-ttu-id="e0962-113">L'activité dérive de <xref:System.Activities.Activity%601> et utilise les activités <xref:System.Activities.Statements.WriteLine> et `ReadLine`.</span><span class="sxs-lookup"><span data-stu-id="e0962-113">The activity derives from <xref:System.Activities.Activity%601> and uses the <xref:System.Activities.Statements.WriteLine> and `ReadLine` activities.</span></span>  
  
##### <a name="to-use-this-sample"></a><span data-ttu-id="e0962-114">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="e0962-114">To use this sample</span></span>  
  
1.  <span data-ttu-id="e0962-115">À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution GuessingGame.sln.</span><span class="sxs-lookup"><span data-stu-id="e0962-115">Using [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], open the GuessingGame.sln solution file.</span></span>  
  
2.  <span data-ttu-id="e0962-116">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="e0962-116">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="e0962-117">Pour exécuter la solution, appuyez sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="e0962-117">To run the solution, press CTRL+F5.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e0962-118">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e0962-118">The samples may already be installed on your machine.</span></span> <span data-ttu-id="e0962-119">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="e0962-119">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="e0962-120">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="e0962-120">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="e0962-121">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="e0962-121">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Built-InActivities\Procedurals`