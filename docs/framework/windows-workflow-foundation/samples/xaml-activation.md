---
title: XAML Activation
ms.date: 03/30/2017
ms.assetid: 486760e2-bb10-4ed5-8c02-fe7472498d2d
ms.openlocfilehash: 8621b0ea7b390c81e76ac7eeedb0b547b44320d7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33517710"
---
# <a name="xaml-activation"></a><span data-ttu-id="43a54-102">XAML Activation</span><span class="sxs-lookup"><span data-stu-id="43a54-102">XAML Activation</span></span>
<span data-ttu-id="43a54-103">Cet exemple montre comment héberger un workflow déclaratif dans IIS.</span><span class="sxs-lookup"><span data-stu-id="43a54-103">This sample demonstrates how to host a declarative workflow in IIS.</span></span> <span data-ttu-id="43a54-104">C'est un workflow de base appelé `EchoService` qui comporte une opération.</span><span class="sxs-lookup"><span data-stu-id="43a54-104">The sample is a basic workflow called `EchoService` that has one operation.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="43a54-105">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="43a54-105">The samples may already be installed on your machine.</span></span> <span data-ttu-id="43a54-106">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="43a54-106">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="43a54-107">Si ce répertoire n’existe pas, accédez à (page de téléchargement) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="43a54-107">If this directory does not exist, go to (download page) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="43a54-108">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="43a54-108">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\XAMLActivation`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="43a54-109">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="43a54-109">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="43a54-110">Ouvrez la solution XAMLActivation.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="43a54-110">Open the XAMLActivation.sln solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="43a54-111">Générez la solution en appuyant sur **F5**.</span><span class="sxs-lookup"><span data-stu-id="43a54-111">Build the solution by pressing **F5**.</span></span>  
  
3.  <span data-ttu-id="43a54-112">Exécutez WcfTestClient.exe.</span><span class="sxs-lookup"><span data-stu-id="43a54-112">Run WcfTestClient.exe.</span></span> <span data-ttu-id="43a54-113">À partir d'une invite de commandes, tapez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="43a54-113">From a command prompt, type in the following:</span></span>  
  
    1.  <span data-ttu-id="43a54-114">cd %SystemDrive%\Program Files\Microsoft Visual Studio 10.0\Common7\IDE</span><span class="sxs-lookup"><span data-stu-id="43a54-114">cd %SystemDrive%\Program Files\Microsoft Visual Studio 10.0\Common7\IDE</span></span>  
  
    2.  <span data-ttu-id="43a54-115">Exécutez WcfTestClient.exe.</span><span class="sxs-lookup"><span data-stu-id="43a54-115">Run WcfTestClient.exe.</span></span>  
  
4.  <span data-ttu-id="43a54-116">Définir l’adresse du service sur WcfTestClient.exe en appuyant sur CTRL + MAJ + A et l’adresse du service http://localhost:56133/Service.xamlx.</span><span class="sxs-lookup"><span data-stu-id="43a54-116">Set the address of the service on WcfTestClient.exe by pressing CTRL+SHIFT+A and setting the service address to http://localhost:56133/Service.xamlx.</span></span>  
  
5.  <span data-ttu-id="43a54-117">Effectuez l'opération Echo pour tester le service.</span><span class="sxs-lookup"><span data-stu-id="43a54-117">Perform the echo operation to test the service.</span></span>  
  
6.  <span data-ttu-id="43a54-118">Déployez le service dans IIS en utilisant DeployToIIS.Bat dans une invite de commandes avec des privilèges d'administrateur.</span><span class="sxs-lookup"><span data-stu-id="43a54-118">Deploy the Service in IIS using DeployToIIS.Bat in a command prompt with administrator privileges.</span></span>  
  
7.  <span data-ttu-id="43a54-119">Mettre à jour l’adresse du service du client pour http://localhost/XAMLActivation/Service.xamlx et tester le service à l’aide de WcfTestClient.exe.</span><span class="sxs-lookup"><span data-stu-id="43a54-119">Update the service address in the client to http://localhost/XAMLActivation/Service.xamlx and test the service again using WcfTestClient.exe.</span></span>
