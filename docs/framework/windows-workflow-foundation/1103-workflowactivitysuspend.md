---
title: 1103 - WorkflowActivitySuspend
ms.date: 03/30/2017
ms.assetid: b64e15c2-cb2c-4314-9074-ce2c6717232e
ms.openlocfilehash: 4311bd8dc1c5e2c43bf21b411a4c52a7bfc7b230
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33511109"
---
# <a name="1103---workflowactivitysuspend"></a><span data-ttu-id="e2572-102">1103 - WorkflowActivitySuspend</span><span class="sxs-lookup"><span data-stu-id="e2572-102">1103 - WorkflowActivitySuspend</span></span>
## <a name="properties"></a><span data-ttu-id="e2572-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e2572-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e2572-104">ID</span><span class="sxs-lookup"><span data-stu-id="e2572-104">ID</span></span>|<span data-ttu-id="e2572-105">1103</span><span class="sxs-lookup"><span data-stu-id="e2572-105">1103</span></span>|  
|<span data-ttu-id="e2572-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e2572-106">Keywords</span></span>|<span data-ttu-id="e2572-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="e2572-107">WFRuntime</span></span>|  
|<span data-ttu-id="e2572-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="e2572-108">Level</span></span>|<span data-ttu-id="e2572-109">Information</span><span class="sxs-lookup"><span data-stu-id="e2572-109">Information</span></span>|  
|<span data-ttu-id="e2572-110">Canal</span><span class="sxs-lookup"><span data-stu-id="e2572-110">Channel</span></span>|<span data-ttu-id="e2572-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="e2572-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e2572-112">Description</span><span class="sxs-lookup"><span data-stu-id="e2572-112">Description</span></span>  
 <span data-ttu-id="e2572-113">Indique qu'une activité du flux de travail a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="e2572-113">Indicates a workflow activity has been suspended.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e2572-114">Message</span><span class="sxs-lookup"><span data-stu-id="e2572-114">Message</span></span>  
 <span data-ttu-id="e2572-115">ID WorkflowInstance : « %1 » Activité E2E</span><span class="sxs-lookup"><span data-stu-id="e2572-115">WorkflowInstance Id: '%1' E2E Activity</span></span>  
  
## <a name="details"></a><span data-ttu-id="e2572-116">Détails</span><span class="sxs-lookup"><span data-stu-id="e2572-116">Details</span></span>  
  
|<span data-ttu-id="e2572-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="e2572-117">Data Item Name</span></span>|<span data-ttu-id="e2572-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="e2572-118">Data Item Type</span></span>|<span data-ttu-id="e2572-119">Description</span><span class="sxs-lookup"><span data-stu-id="e2572-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e2572-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="e2572-120">WorkflowInstanceId</span></span>|<span data-ttu-id="e2572-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="e2572-121">xs:string</span></span>|<span data-ttu-id="e2572-122">ID de l'instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="e2572-122">The workflow instance id.</span></span>|  
|<span data-ttu-id="e2572-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="e2572-123">AppDomain</span></span>|<span data-ttu-id="e2572-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="e2572-124">xs:string</span></span>|<span data-ttu-id="e2572-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="e2572-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
