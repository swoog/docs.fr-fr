---
title: Exemple d'activité compensable
ms.date: 03/30/2017
ms.assetid: 58f4898c-b2b8-44a4-9a73-3bef4da6d5ba
ms.openlocfilehash: 3bf1d120cd700830a98f53495f7e9989ffec73db
ms.sourcegitcommit: f513a91160b3fec289dd06646d0d6f81f8fcf910
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46287541"
---
# <a name="compensable-activity-sample"></a><span data-ttu-id="eed8c-102">Exemple d'activité compensable</span><span class="sxs-lookup"><span data-stu-id="eed8c-102">Compensable Activity Sample</span></span>
<span data-ttu-id="eed8c-103">Cet exemple montre comment utiliser l'activité `CompensableActivity` pour définir le travail à faire pour une action donnée pendant une exécution normale et le travail qui doit être fait pour compenser cette action, si nécessaire ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="eed8c-103">This sample demonstrates how to use the `CompensableActivity` activity to define the work to be done for a given action during normal execution and the work that is necessary to be done to compensate that action, if necessary at a later time.</span></span>  <span data-ttu-id="eed8c-104">La première partie de l’exemple montre comment les unités de travail compensable peuvent être définies dans Windows Workflow Foundation (WF) à l’aide un `CompensableActivity` activité et comment elles sont exécutées dans une exécution réussie.</span><span class="sxs-lookup"><span data-stu-id="eed8c-104">The first part of the sample shows how units of compensable work can be defined in Windows Workflow Foundation (WF) using a `CompensableActivity` activity and how they are executed in a successful run.</span></span>  <span data-ttu-id="eed8c-105">La deuxième partie de l'exemple montre comment ces mêmes unités de travail compensable se chargent automatiquement de la compensation lorsqu'un événement inattendu est atteint et que l'instance de workflow est annulée.</span><span class="sxs-lookup"><span data-stu-id="eed8c-105">The second part of the sample shows how the same units of compensable work automatically take care of compensation when an unexpected event is hit and the workflow instance is canceled.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="eed8c-106">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="eed8c-106">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="eed8c-107">À l'aide de Visual Studio 2010, ouvrez CompensableActivity.sln.</span><span class="sxs-lookup"><span data-stu-id="eed8c-107">Using Visual Studio 2010, open the CompensableActivity.sln.</span></span>  
  
2.  <span data-ttu-id="eed8c-108">Générez la solution en appuyant sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="eed8c-108">Build the solution by pressing CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="eed8c-109">Exécutez l'application en appuyant sur F5.</span><span class="sxs-lookup"><span data-stu-id="eed8c-109">Run the application by pressing F5.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="eed8c-110">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="eed8c-110">The samples may already be installed on your machine.</span></span> <span data-ttu-id="eed8c-111">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="eed8c-111">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="eed8c-112">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="eed8c-112">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="eed8c-113">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="eed8c-113">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Compensation\BasicCompensableActivity`