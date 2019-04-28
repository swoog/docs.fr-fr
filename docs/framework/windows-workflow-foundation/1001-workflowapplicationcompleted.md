---
title: 1001 - WorkflowApplicationCompleted
ms.date: 03/30/2017
ms.assetid: 7a2ab59a-cf66-437a-b01e-f8f7268a3f7a
ms.openlocfilehash: 430174b96a499fff7e0156327bb15e066ce2ca36
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008640"
---
# <a name="1001---workflowapplicationcompleted"></a><span data-ttu-id="2582d-102">1001 - WorkflowApplicationCompleted</span><span class="sxs-lookup"><span data-stu-id="2582d-102">1001 - WorkflowApplicationCompleted</span></span>
## <a name="properties"></a><span data-ttu-id="2582d-103">Properties</span><span class="sxs-lookup"><span data-stu-id="2582d-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="2582d-104">Id</span><span class="sxs-lookup"><span data-stu-id="2582d-104">ID</span></span>|<span data-ttu-id="2582d-105">1001</span><span class="sxs-lookup"><span data-stu-id="2582d-105">1001</span></span>|  
|<span data-ttu-id="2582d-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="2582d-106">Keywords</span></span>|<span data-ttu-id="2582d-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="2582d-107">WFRuntime</span></span>|  
|<span data-ttu-id="2582d-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="2582d-108">Level</span></span>|<span data-ttu-id="2582d-109">Information</span><span class="sxs-lookup"><span data-stu-id="2582d-109">Information</span></span>|  
|<span data-ttu-id="2582d-110">Canal</span><span class="sxs-lookup"><span data-stu-id="2582d-110">Channel</span></span>|<span data-ttu-id="2582d-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="2582d-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="2582d-112">Description</span><span class="sxs-lookup"><span data-stu-id="2582d-112">Description</span></span>  
 <span data-ttu-id="2582d-113">Indique qu'une application de workflow s'est terminée à l'état Closed.</span><span class="sxs-lookup"><span data-stu-id="2582d-113">Indicates a workflow application has completed in the Closed state.</span></span>  
  
## <a name="message"></a><span data-ttu-id="2582d-114">Message</span><span class="sxs-lookup"><span data-stu-id="2582d-114">Message</span></span>  
 <span data-ttu-id="2582d-115">ID WorkflowInstance : « %1 » s'est terminé à l'état Closed.</span><span class="sxs-lookup"><span data-stu-id="2582d-115">WorkflowInstance Id: '%1' has completed in the Closed state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="2582d-116">Détails</span><span class="sxs-lookup"><span data-stu-id="2582d-116">Details</span></span>  
  
|<span data-ttu-id="2582d-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="2582d-117">Data Item Name</span></span>|<span data-ttu-id="2582d-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="2582d-118">Data Item Type</span></span>|<span data-ttu-id="2582d-119">Description</span><span class="sxs-lookup"><span data-stu-id="2582d-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="2582d-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="2582d-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="2582d-121">ID d'instance pour le workflow</span><span class="sxs-lookup"><span data-stu-id="2582d-121">The instance id for the workflow</span></span>|  
|<span data-ttu-id="2582d-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="2582d-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="2582d-123">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="2582d-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
