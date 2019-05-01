---
title: 1102 - WorkflowActivityStop
ms.date: 03/30/2017
ms.assetid: 285e5cb8-e90d-4914-ac06-e9b176ffefa2
ms.openlocfilehash: 44617e9f53be0e601424746f83b171d33956197e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62052792"
---
# <a name="1102---workflowactivitystop"></a><span data-ttu-id="95625-102">1102 - WorkflowActivityStop</span><span class="sxs-lookup"><span data-stu-id="95625-102">1102 - WorkflowActivityStop</span></span>
## <a name="properties"></a><span data-ttu-id="95625-103">Properties</span><span class="sxs-lookup"><span data-stu-id="95625-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="95625-104">Id</span><span class="sxs-lookup"><span data-stu-id="95625-104">ID</span></span>|<span data-ttu-id="95625-105">1102</span><span class="sxs-lookup"><span data-stu-id="95625-105">1102</span></span>|  
|<span data-ttu-id="95625-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="95625-106">Keywords</span></span>|<span data-ttu-id="95625-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="95625-107">WFRuntime</span></span>|  
|<span data-ttu-id="95625-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="95625-108">Level</span></span>|<span data-ttu-id="95625-109">Information</span><span class="sxs-lookup"><span data-stu-id="95625-109">Information</span></span>|  
|<span data-ttu-id="95625-110">Canal</span><span class="sxs-lookup"><span data-stu-id="95625-110">Channel</span></span>|<span data-ttu-id="95625-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="95625-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="95625-112">Description</span><span class="sxs-lookup"><span data-stu-id="95625-112">Description</span></span>  
 <span data-ttu-id="95625-113">Indique qu'une activité du flux de travail s'est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="95625-113">Indicates a workflow activity has stopped.</span></span>  
  
## <a name="message"></a><span data-ttu-id="95625-114">Message</span><span class="sxs-lookup"><span data-stu-id="95625-114">Message</span></span>  
 <span data-ttu-id="95625-115">ID WorkflowInstance : « %1 » Activité E2E</span><span class="sxs-lookup"><span data-stu-id="95625-115">WorkflowInstance Id: '%1' E2E Activity</span></span>  
  
## <a name="details"></a><span data-ttu-id="95625-116">Détails</span><span class="sxs-lookup"><span data-stu-id="95625-116">Details</span></span>  
  
|<span data-ttu-id="95625-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="95625-117">Data Item Name</span></span>|<span data-ttu-id="95625-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="95625-118">Data Item Type</span></span>|<span data-ttu-id="95625-119">Description</span><span class="sxs-lookup"><span data-stu-id="95625-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="95625-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="95625-120">WorkflowInstanceId</span></span>|<span data-ttu-id="95625-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="95625-121">xs:string</span></span>|<span data-ttu-id="95625-122">ID de l'instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="95625-122">The workflow instance id.</span></span>|  
|<span data-ttu-id="95625-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="95625-123">AppDomain</span></span>|<span data-ttu-id="95625-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="95625-124">xs:string</span></span>|<span data-ttu-id="95625-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="95625-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
