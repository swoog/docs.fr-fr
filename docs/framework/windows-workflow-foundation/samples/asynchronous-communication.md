---
title: Communication asynchrone
ms.date: 03/30/2017
ms.assetid: 128dc092-9eb2-4e33-9470-9a7f62b60df6
ms.openlocfilehash: e85f7efb0de1326ceb5091c305b20f34809eab57
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43670715"
---
# <a name="asynchronous-communication"></a><span data-ttu-id="edd0e-102">Communication asynchrone</span><span class="sxs-lookup"><span data-stu-id="edd0e-102">Asynchronous Communication</span></span>
<span data-ttu-id="edd0e-103">Cet exemple montre comment la communication entre deux services Windows Workflow Foundation (WF) s’effectue de façon asynchrone par défaut.</span><span class="sxs-lookup"><span data-stu-id="edd0e-103">This sample demonstrates how the communication between two different Windows Workflow Foundation (WF) services is done asynchronously by default.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="edd0e-104">Démonstrations</span><span class="sxs-lookup"><span data-stu-id="edd0e-104">Demonstrates</span></span>  
 <span data-ttu-id="edd0e-105">Communication asynchrone entre des services [!INCLUDE[wf1](../../../../includes/wf1-md.md)].</span><span class="sxs-lookup"><span data-stu-id="edd0e-105">Asynchronous communication between [!INCLUDE[wf1](../../../../includes/wf1-md.md)] services.</span></span>  
  
## <a name="discussion"></a><span data-ttu-id="edd0e-106">Discussion</span><span class="sxs-lookup"><span data-stu-id="edd0e-106">Discussion</span></span>  
 <span data-ttu-id="edd0e-107">Cet exemple montre comment la communication entre des applications [!INCLUDE[wf1](../../../../includes/wf1-md.md)] s'effectue de façon asynchrone à l'aide des activités de messagerie fournies par le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="edd0e-107">This sample shows how the communication between [!INCLUDE[wf1](../../../../includes/wf1-md.md)] applications is done asynchronously by using the messaging activities provided by .NET Framework.</span></span>  
  
 <span data-ttu-id="edd0e-108">Cet exemple est composé des trois projets suivants :</span><span class="sxs-lookup"><span data-stu-id="edd0e-108">This sample consists of the following three projects.</span></span>  
  
 <span data-ttu-id="edd0e-109">CreditCheckService</span><span class="sxs-lookup"><span data-stu-id="edd0e-109">CreditCheckService</span></span>  
 <span data-ttu-id="edd0e-110">Ce service reçoit le niveau de crédit d'une personne particulière ou la valeur de l'élément à acquérir, puis décide si le crédit est accordé à la personne.</span><span class="sxs-lookup"><span data-stu-id="edd0e-110">This service receives the credit score of a particular person or the value of the item to acquire, and then decides whether the credit is given to the person.</span></span>  
  
 <span data-ttu-id="edd0e-111">RentalApprovalService</span><span class="sxs-lookup"><span data-stu-id="edd0e-111">RentalApprovalService</span></span>  
 <span data-ttu-id="edd0e-112">Ce service reçoit une application d'une personne qui a besoin d'un crédit.</span><span class="sxs-lookup"><span data-stu-id="edd0e-112">This service receives an application from a person who is in need of some credit.</span></span> <span data-ttu-id="edd0e-113">Il communique de façon asynchrone avec `CreditCheckService` pour décider si l'application de crédit est valide.</span><span class="sxs-lookup"><span data-stu-id="edd0e-113">This service communicates asynchronously with the `CreditCheckService` to decide whether the credit application is valid.</span></span>  
  
 <span data-ttu-id="edd0e-114">Client</span><span class="sxs-lookup"><span data-stu-id="edd0e-114">Client</span></span>  
 <span data-ttu-id="edd0e-115">Le client communique de façon synchrone avec `RentalApprovalService` pour savoir si le crédit est approuvé.</span><span class="sxs-lookup"><span data-stu-id="edd0e-115">The client communicates synchronously with the `RentalApprovalService` to know whether the credit is approved.</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="edd0e-116">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="edd0e-116">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="edd0e-117">Cliquez sur le **AsynchronousCommunication** solution, puis sélectionnez **propriétés**.</span><span class="sxs-lookup"><span data-stu-id="edd0e-117">Right-click the **AsynchronousCommunication** solution and select **Properties**.</span></span>  
  
2.  <span data-ttu-id="edd0e-118">Dans **propriétés communes**, sélectionnez **projet de démarrage**, puis sélectionnez **plusieurs projets de démarrage**.</span><span class="sxs-lookup"><span data-stu-id="edd0e-118">In **Common Properties**, select **Startup Project**, and select **Multiple Startup Projects**.</span></span>  
  
3.  <span data-ttu-id="edd0e-119">Déplacer **RentalApprovalService** pour la première position dans la liste, suivi de **CreditCheckService**, suivie **Client**.</span><span class="sxs-lookup"><span data-stu-id="edd0e-119">Move **RentalApprovalService** to the first position in the list, followed by **CreditCheckService**, followed by **Client**.</span></span> <span data-ttu-id="edd0e-120">Définir le **Démarrer** action sur toutes les trois projets.</span><span class="sxs-lookup"><span data-stu-id="edd0e-120">Set the **Start** action on all three projects.</span></span>  
  
4.  <span data-ttu-id="edd0e-121">Cliquez sur **OK**, et appuyez sur F5 pour exécuter l’exemple.</span><span class="sxs-lookup"><span data-stu-id="edd0e-121">Click **OK**, and press F5 to run the sample.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="edd0e-122">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="edd0e-122">The samples may already be installed on your machine.</span></span> <span data-ttu-id="edd0e-123">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="edd0e-123">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="edd0e-124">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="edd0e-124">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="edd0e-125">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="edd0e-125">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\Services\AsynchronousCommunication`
