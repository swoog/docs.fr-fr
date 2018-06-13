---
title: Activité RangeEnumeration
ms.date: 03/30/2017
ms.assetid: ca5b78f4-94fa-4aa7-830d-26039ac422c8
ms.openlocfilehash: 9aa04c80f20e2d410fb49e2d07d836c8c5ab1b4d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33516576"
---
# <a name="rangeenumeration-activity"></a><span data-ttu-id="e59ab-102">Activité RangeEnumeration</span><span class="sxs-lookup"><span data-stu-id="e59ab-102">RangeEnumeration Activity</span></span>
<span data-ttu-id="e59ab-103">Cet exemple montre comment créer une activité personnalisée qui itère au sein d'une collection de nombres. Le tableau suivant détaille les fichiers principaux inclus dans l'exemple.</span><span class="sxs-lookup"><span data-stu-id="e59ab-103">This sample demonstrates how to create a custom activity that iterates over a collection of numbers.The following table details the main files included in the sample.</span></span>  
  
|<span data-ttu-id="e59ab-104">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="e59ab-104">File name</span></span>|<span data-ttu-id="e59ab-105">Description</span><span class="sxs-lookup"><span data-stu-id="e59ab-105">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e59ab-106">RangeEnumeration.cs</span><span class="sxs-lookup"><span data-stu-id="e59ab-106">RangeEnumeration.cs</span></span>|<span data-ttu-id="e59ab-107">Définit une activité personnalisée nommée `RangeEnumeration` qui substitue la classe <xref:System.Activities.NativeActivity> et effectue une boucle sur une série de nombres.</span><span class="sxs-lookup"><span data-stu-id="e59ab-107">Defines a custom activity named `RangeEnumeration` that overrides the <xref:System.Activities.NativeActivity> class and loops through a series of numbers.</span></span>|  
|<span data-ttu-id="e59ab-108">RangeEnumerationSample.cs</span><span class="sxs-lookup"><span data-stu-id="e59ab-108">RangeEnumerationSample.cs</span></span>|<span data-ttu-id="e59ab-109">Application cliente qui utilise l'activité `RangeEnumeration` pour itérer au sein d'une collection de nombres.</span><span class="sxs-lookup"><span data-stu-id="e59ab-109">A client application that uses the `RangeEnumeration` activity to iterate over a collection of numbers.</span></span>|  
  
 <span data-ttu-id="e59ab-110">Le tableau suivant détaille les propriétés de l'activité `RangeEnumeration`.</span><span class="sxs-lookup"><span data-stu-id="e59ab-110">The following table details the properties of the `RangeEnumeration` activity.</span></span>  
  
|<span data-ttu-id="e59ab-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="e59ab-111">Property</span></span>|<span data-ttu-id="e59ab-112">Description</span><span class="sxs-lookup"><span data-stu-id="e59ab-112">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="e59ab-113">Démarrer</span><span class="sxs-lookup"><span data-stu-id="e59ab-113">Start</span></span>|<span data-ttu-id="e59ab-114">Entier auquel démarrer la boucle.</span><span class="sxs-lookup"><span data-stu-id="e59ab-114">The integer to start the loop from.</span></span>|  
|<span data-ttu-id="e59ab-115">Arrêter</span><span class="sxs-lookup"><span data-stu-id="e59ab-115">Stop</span></span>|<span data-ttu-id="e59ab-116">Entier auquel arrêter la boucle.</span><span class="sxs-lookup"><span data-stu-id="e59ab-116">The integer to stop the loop at.</span></span>|  
|<span data-ttu-id="e59ab-117">Étape</span><span class="sxs-lookup"><span data-stu-id="e59ab-117">Step</span></span>|<span data-ttu-id="e59ab-118">Spécifie le volume d'itération à chaque fois.</span><span class="sxs-lookup"><span data-stu-id="e59ab-118">Specifies how much to iterate each time.</span></span>|  
|<span data-ttu-id="e59ab-119">Corps</span><span class="sxs-lookup"><span data-stu-id="e59ab-119">Body</span></span>|<span data-ttu-id="e59ab-120">Spécifie le code à exécuter pendant chaque itération.</span><span class="sxs-lookup"><span data-stu-id="e59ab-120">Specifies the code to execute during each iteration.</span></span>|  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="e59ab-121">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="e59ab-121">To use this sample</span></span>  
  
1.  <span data-ttu-id="e59ab-122">À l'aide de [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], ouvrez le fichier solution RangeEnumeration.sln.</span><span class="sxs-lookup"><span data-stu-id="e59ab-122">Using [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], open the RangeEnumeration.sln solution file.</span></span>  
  
2.  <span data-ttu-id="e59ab-123">Pour générer la solution, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="e59ab-123">To build the solution, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="e59ab-124">Pour exécuter la solution, appuyez sur Ctrl+F5.</span><span class="sxs-lookup"><span data-stu-id="e59ab-124">To run the solution, press CTRL+F5.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="e59ab-125">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e59ab-125">The samples may already be installed on your machine.</span></span> <span data-ttu-id="e59ab-126">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="e59ab-126">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="e59ab-127">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples Windows Workflow Foundation (WF) pour .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="e59ab-127">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="e59ab-128">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="e59ab-128">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\RangeEnumeration`