---
title: 1006 - WorkflowApplicationUnhandledException
ms.date: 03/30/2017
ms.assetid: dfe0f316-e03b-47fb-b6a3-622c56bfd753
ms.openlocfilehash: 471f3ecea66ebbd07a09686ab536a84b25d46e6b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924707"
---
# <a name="1006---workflowapplicationunhandledexception"></a><span data-ttu-id="04b5e-102">1006 - WorkflowApplicationUnhandledException</span><span class="sxs-lookup"><span data-stu-id="04b5e-102">1006 - WorkflowApplicationUnhandledException</span></span>
## <a name="properties"></a><span data-ttu-id="04b5e-103">Properties</span><span class="sxs-lookup"><span data-stu-id="04b5e-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="04b5e-104">Id</span><span class="sxs-lookup"><span data-stu-id="04b5e-104">ID</span></span>|<span data-ttu-id="04b5e-105">1006</span><span class="sxs-lookup"><span data-stu-id="04b5e-105">1006</span></span>|  
|<span data-ttu-id="04b5e-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="04b5e-106">Keywords</span></span>|<span data-ttu-id="04b5e-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="04b5e-107">WFRuntime</span></span>|  
|<span data-ttu-id="04b5e-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="04b5e-108">Level</span></span>|<span data-ttu-id="04b5e-109">Error</span><span class="sxs-lookup"><span data-stu-id="04b5e-109">Error</span></span>|  
|<span data-ttu-id="04b5e-110">Canal</span><span class="sxs-lookup"><span data-stu-id="04b5e-110">Channel</span></span>|<span data-ttu-id="04b5e-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="04b5e-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="04b5e-112">Description</span><span class="sxs-lookup"><span data-stu-id="04b5e-112">Description</span></span>  
 <span data-ttu-id="04b5e-113">Indique qu'une application de workflow a rencontré une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="04b5e-113">Indicates a workflow application has encountered an unhandled exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="04b5e-114">Message</span><span class="sxs-lookup"><span data-stu-id="04b5e-114">Message</span></span>  
 <span data-ttu-id="04b5e-115">WorkflowInstance Id : '%1' a rencontré une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="04b5e-115">WorkflowInstance Id: '%1' has encountered an unhandled exception.</span></span>  <span data-ttu-id="04b5e-116">L’exception provient de l’activité « %2 », DisplayName : '%3'.</span><span class="sxs-lookup"><span data-stu-id="04b5e-116">The exception originated from Activity '%2', DisplayName: '%3'.</span></span>  <span data-ttu-id="04b5e-117">L’action suivante sera effectuée : %4.</span><span class="sxs-lookup"><span data-stu-id="04b5e-117">The following action will be taken: %4.</span></span>  
  
## <a name="details"></a><span data-ttu-id="04b5e-118">Détails</span><span class="sxs-lookup"><span data-stu-id="04b5e-118">Details</span></span>  
  
|<span data-ttu-id="04b5e-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="04b5e-119">Data Item Name</span></span>|<span data-ttu-id="04b5e-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="04b5e-120">Data Item Type</span></span>|<span data-ttu-id="04b5e-121">Description</span><span class="sxs-lookup"><span data-stu-id="04b5e-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="04b5e-122">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="04b5e-122">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="04b5e-123">ID d'instance pour le workflow</span><span class="sxs-lookup"><span data-stu-id="04b5e-123">The instance id for the workflow</span></span>|  
|<span data-ttu-id="04b5e-124">Exception</span><span class="sxs-lookup"><span data-stu-id="04b5e-124">Exception</span></span>|`xs:string`|<span data-ttu-id="04b5e-125">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="04b5e-125">The exception details for the exception</span></span>|  
|<span data-ttu-id="04b5e-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="04b5e-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="04b5e-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="04b5e-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
