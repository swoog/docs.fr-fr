---
title: Mise en forme des messages dans les services de workflow
ms.date: 03/30/2017
ms.assetid: 6d15d44b-20f8-4cb7-bd4f-598c32781ebc
ms.openlocfilehash: eb9a6b3a83a28154dc968bd4c1c41d34028bdd41
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44134790"
---
# <a name="formatting-messages-in-workflow-services"></a><span data-ttu-id="17a21-102">Mise en forme des messages dans les services de workflow</span><span class="sxs-lookup"><span data-stu-id="17a21-102">Formatting messages in Workflow Services</span></span>
<span data-ttu-id="17a21-103">Cet exemple montre comment différents types utilisateur peuvent être utilisés dans des activités de messagerie (services WF).</span><span class="sxs-lookup"><span data-stu-id="17a21-103">This sample shows how different user types can be used in messaging activities (WF services).</span></span> <span data-ttu-id="17a21-104">L'exemple de service est un service d'approbation des dépenses simple qui expose trois opérations.</span><span class="sxs-lookup"><span data-stu-id="17a21-104">The sample service is a simple expense approval service and exposes three operations.</span></span> <span data-ttu-id="17a21-105">`ApproveExpense` prend un type de contrat de données et montre comment utiliser des types connus.</span><span class="sxs-lookup"><span data-stu-id="17a21-105">`ApproveExpense` takes a data contract type and shows how to use known types.</span></span> <span data-ttu-id="17a21-106">L'opération retourne `true` ou `false` selon le montant de la dépense.</span><span class="sxs-lookup"><span data-stu-id="17a21-106">The operation returns `true` or `false` based on the expense amount.</span></span> <span data-ttu-id="17a21-107">`ApprovePO` prend un type XmlSerializer et retourne `true` ou `false` selon le montant des dépenses.`ApprovedVendor`</span><span class="sxs-lookup"><span data-stu-id="17a21-107">`ApprovePO` takes an XmlSerializer type and returns `true` or `false` based on the expense amount.`ApprovedVendor`</span></span> <span data-ttu-id="17a21-108">prend un type de contrat de message et retourne `true` ou `false` si le fournisseur est dans la liste des fournisseurs approuvés ou si la demande provient du service financier (le service financier peut utiliser n’importe quel fournisseur).</span><span class="sxs-lookup"><span data-stu-id="17a21-108">takes a message contract type and returns `true` or `false` if the vendor is in the list of approved vendors or if the request came from the finance department (the finance department can use any vendor).</span></span>  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="17a21-109">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="17a21-109">To use this sample</span></span>  
  
1.  <span data-ttu-id="17a21-110">Chargez la solution du projet dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] et générez le projet.</span><span class="sxs-lookup"><span data-stu-id="17a21-110">Load the project solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] and build the project.</span></span>  
  
2.  <span data-ttu-id="17a21-111">En premier lieu, exécutez le service, généré dans [répertoire de base de la solution]\FormatterService\bin\debug\.</span><span class="sxs-lookup"><span data-stu-id="17a21-111">First run the service, generated in [solution base directory]\FormatterService\bin\debug\\</span></span>  
  
3.  <span data-ttu-id="17a21-112">En second lieu, exécutez l'application cliente, générée dans [répertoire de base de la solution]\FormatterClient\bin\debug.</span><span class="sxs-lookup"><span data-stu-id="17a21-112">Second, run the Client application generated in [solution base directory]\FormatterClient\bin\debug.</span></span>  
  
4.  <span data-ttu-id="17a21-113">Le client appelle trois opérations sur le service et imprime les résultats.</span><span class="sxs-lookup"><span data-stu-id="17a21-113">The client calls three operations on the service and prints the results.</span></span> <span data-ttu-id="17a21-114">Une fois cette opération terminée, appuyez sur ENTRÉE pour quitter le client, puis le service.</span><span class="sxs-lookup"><span data-stu-id="17a21-114">When complete, press ENTER to exit the client and then the service.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="17a21-115">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="17a21-115">The samples may already be installed on your machine.</span></span> <span data-ttu-id="17a21-116">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="17a21-116">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="17a21-117">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="17a21-117">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="17a21-118">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="17a21-118">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\Formatter`