---
title: Utilisation d'Interop avec l'échange interne de données
ms.date: 03/30/2017
ms.assetid: 96f6fe26-5305-494f-9119-7748e0c4b3fa
ms.openlocfilehash: 534321e5b5568e0dd0988333dc98ccc18ff33df8
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43804826"
---
# <a name="using-interop-with-external-data-exchange"></a><span data-ttu-id="a3575-102">Utilisation d'Interop avec l'échange interne de données</span><span class="sxs-lookup"><span data-stu-id="a3575-102">Using Interop with External Data Exchange</span></span>
<span data-ttu-id="a3575-103">Le <xref:System.Activities.Statements.Interop> activité peut être utilisée pour exécuter des activités à partir de Windows Workflow Foundation (WF) dans [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)] et [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)] (WF3) et des flux de travail dans Windows Workflow Foundation dans [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] (WF4).</span><span class="sxs-lookup"><span data-stu-id="a3575-103">The <xref:System.Activities.Statements.Interop> activity can be used to execute activities from Windows Workflow Foundation (WF) in [!INCLUDE[vstecwinfx](../../../../includes/vstecwinfx-md.md)] and [!INCLUDE[netfx35_long](../../../../includes/netfx35-long-md.md)] (WF3), and workflows within Windows Workflow Foundation in [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] (WF4).</span></span> <span data-ttu-id="a3575-104">Cet exemple montre comment configurer et exécuter un workflow WF3 qui utilise <xref:System.Workflow.Activities.ExternalDataExchangeService> (et les activités personnalisées correspondantes pour appeler les méthodes et gérer les événements) à l'aide de l'activité <xref:System.Activities.Statements.Interop> dans un service de workflow WF4.</span><span class="sxs-lookup"><span data-stu-id="a3575-104">This sample shows how to configure and run a WF3 workflow that uses <xref:System.Workflow.Activities.ExternalDataExchangeService> (and corresponding custom activities for calling methods and handling events) by using the <xref:System.Activities.Statements.Interop> activity in a WF4 workflow service.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="a3575-105">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a3575-105">The samples may already be installed on your machine.</span></span> <span data-ttu-id="a3575-106">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="a3575-106">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="a3575-107">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="a3575-107">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="a3575-108">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="a3575-108">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Migration\ExternalDataExchange`  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="a3575-109">Pour utiliser cet exemple</span><span class="sxs-lookup"><span data-stu-id="a3575-109">To use this sample</span></span>  
  
1.  <span data-ttu-id="a3575-110">Ouvrez le fichier ExternalDataExchange.sln dans [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="a3575-110">Open the ExternalDataExchange.sln file in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="a3575-111">Pour créer l'exemple, appuyez sur Ctrl+Maj+B.</span><span class="sxs-lookup"><span data-stu-id="a3575-111">To build the sample, press CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="a3575-112">Pour exécuter l'exemple, appuyez sur F5.</span><span class="sxs-lookup"><span data-stu-id="a3575-112">To run the sample, press F5.</span></span>
