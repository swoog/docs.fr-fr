---
title: 1103 - WorkflowActivitySuspend
ms.date: 03/30/2017
ms.assetid: b64e15c2-cb2c-4314-9074-ce2c6717232e
ms.openlocfilehash: 4311bd8dc1c5e2c43bf21b411a4c52a7bfc7b230
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052779"
---
# <a name="1103---workflowactivitysuspend"></a><span data-ttu-id="8d67d-102">1103 - WorkflowActivitySuspend</span><span class="sxs-lookup"><span data-stu-id="8d67d-102">1103 - WorkflowActivitySuspend</span></span>
## <a name="properties"></a><span data-ttu-id="8d67d-103">Properties</span><span class="sxs-lookup"><span data-stu-id="8d67d-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="8d67d-104">Id</span><span class="sxs-lookup"><span data-stu-id="8d67d-104">ID</span></span>|<span data-ttu-id="8d67d-105">1103</span><span class="sxs-lookup"><span data-stu-id="8d67d-105">1103</span></span>|  
|<span data-ttu-id="8d67d-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8d67d-106">Keywords</span></span>|<span data-ttu-id="8d67d-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="8d67d-107">WFRuntime</span></span>|  
|<span data-ttu-id="8d67d-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="8d67d-108">Level</span></span>|<span data-ttu-id="8d67d-109">Information</span><span class="sxs-lookup"><span data-stu-id="8d67d-109">Information</span></span>|  
|<span data-ttu-id="8d67d-110">Canal</span><span class="sxs-lookup"><span data-stu-id="8d67d-110">Channel</span></span>|<span data-ttu-id="8d67d-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="8d67d-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="8d67d-112">Description</span><span class="sxs-lookup"><span data-stu-id="8d67d-112">Description</span></span>  
 <span data-ttu-id="8d67d-113">Indique qu'une activité du flux de travail a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="8d67d-113">Indicates a workflow activity has been suspended.</span></span>  
  
## <a name="message"></a><span data-ttu-id="8d67d-114">Message</span><span class="sxs-lookup"><span data-stu-id="8d67d-114">Message</span></span>  
 <span data-ttu-id="8d67d-115">ID WorkflowInstance : « %1 » Activité E2E</span><span class="sxs-lookup"><span data-stu-id="8d67d-115">WorkflowInstance Id: '%1' E2E Activity</span></span>  
  
## <a name="details"></a><span data-ttu-id="8d67d-116">Détails</span><span class="sxs-lookup"><span data-stu-id="8d67d-116">Details</span></span>  
  
|<span data-ttu-id="8d67d-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="8d67d-117">Data Item Name</span></span>|<span data-ttu-id="8d67d-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="8d67d-118">Data Item Type</span></span>|<span data-ttu-id="8d67d-119">Description</span><span class="sxs-lookup"><span data-stu-id="8d67d-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="8d67d-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="8d67d-120">WorkflowInstanceId</span></span>|<span data-ttu-id="8d67d-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="8d67d-121">xs:string</span></span>|<span data-ttu-id="8d67d-122">ID de l'instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="8d67d-122">The workflow instance id.</span></span>|  
|<span data-ttu-id="8d67d-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="8d67d-123">AppDomain</span></span>|<span data-ttu-id="8d67d-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="8d67d-124">xs:string</span></span>|<span data-ttu-id="8d67d-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="8d67d-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
