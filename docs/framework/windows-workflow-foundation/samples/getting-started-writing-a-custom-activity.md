---
title: Mise en route avec l'écriture d'une activité personnalisée
ms.date: 03/30/2017
ms.assetid: 3902f5fa-8a43-4048-8a6a-6b15472f90f0
ms.openlocfilehash: 1c455009a0c658429c13da5e93d07c744402dd61
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33513310"
---
# <a name="getting-started-writing-a-custom-activity"></a><span data-ttu-id="b0456-102">Mise en route avec l'écriture d'une activité personnalisée</span><span class="sxs-lookup"><span data-stu-id="b0456-102">Getting Started Writing a Custom Activity</span></span>
<span data-ttu-id="b0456-103">Cet exemple montre comment définir une activité personnalisée simple en XAML.</span><span class="sxs-lookup"><span data-stu-id="b0456-103">This sample demonstrates how to define a simple custom activity in XAML.</span></span> <span data-ttu-id="b0456-104">Le nom `Rhyme` est attribué à l'activité, et sa logique est une séquence de trois activités <xref:System.Activities.Statements.WriteLine>.</span><span class="sxs-lookup"><span data-stu-id="b0456-104">The activity is given the name `Rhyme`, and its logic is a sequence of three <xref:System.Activities.Statements.WriteLine> activities.</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="b0456-105">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="b0456-105">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="b0456-106">Ouvrez le **Simple.sln** exemple de solution dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="b0456-106">Open the **Simple.sln** sample solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="b0456-107">Générez et exécutez la solution.</span><span class="sxs-lookup"><span data-stu-id="b0456-107">Build and run the solution.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b0456-108">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b0456-108">The samples may already be installed on your machine.</span></span> <span data-ttu-id="b0456-109">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="b0456-109">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="b0456-110">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="b0456-110">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="b0456-111">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="b0456-111">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\CustomActivities\Composite\GettingStarted`