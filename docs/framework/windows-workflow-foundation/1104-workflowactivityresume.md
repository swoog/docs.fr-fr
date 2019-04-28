---
title: 1104 - WorkflowActivityResume
ms.date: 03/30/2017
ms.assetid: 7fe95d1e-34bd-43ca-b92e-587d2d248fff
ms.openlocfilehash: 4c9ae5fd386fc93ea19578097aa4e0afdda527e2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924122"
---
# <a name="1104---workflowactivityresume"></a><span data-ttu-id="7d2d3-102">1104 - WorkflowActivityResume</span><span class="sxs-lookup"><span data-stu-id="7d2d3-102">1104 - WorkflowActivityResume</span></span>
## <a name="properties"></a><span data-ttu-id="7d2d3-103">Properties</span><span class="sxs-lookup"><span data-stu-id="7d2d3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7d2d3-104">Id</span><span class="sxs-lookup"><span data-stu-id="7d2d3-104">ID</span></span>|<span data-ttu-id="7d2d3-105">1104</span><span class="sxs-lookup"><span data-stu-id="7d2d3-105">1104</span></span>|  
|<span data-ttu-id="7d2d3-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="7d2d3-106">Keywords</span></span>|<span data-ttu-id="7d2d3-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="7d2d3-107">WFRuntime</span></span>|  
|<span data-ttu-id="7d2d3-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="7d2d3-108">Level</span></span>|<span data-ttu-id="7d2d3-109">Information</span><span class="sxs-lookup"><span data-stu-id="7d2d3-109">Information</span></span>|  
|<span data-ttu-id="7d2d3-110">Canal</span><span class="sxs-lookup"><span data-stu-id="7d2d3-110">Channel</span></span>|<span data-ttu-id="7d2d3-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="7d2d3-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7d2d3-112">Description</span><span class="sxs-lookup"><span data-stu-id="7d2d3-112">Description</span></span>  
 <span data-ttu-id="7d2d3-113">Indique qu'une activité du flux de travail a été reprise.</span><span class="sxs-lookup"><span data-stu-id="7d2d3-113">Indicates a workflow activity has been resumed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7d2d3-114">Message</span><span class="sxs-lookup"><span data-stu-id="7d2d3-114">Message</span></span>  
 <span data-ttu-id="7d2d3-115">ID WorkflowInstance : « %1 » Activité E2E</span><span class="sxs-lookup"><span data-stu-id="7d2d3-115">WorkflowInstance Id: '%1' E2E Activity</span></span>  
  
## <a name="details"></a><span data-ttu-id="7d2d3-116">Détails</span><span class="sxs-lookup"><span data-stu-id="7d2d3-116">Details</span></span>  
  
|<span data-ttu-id="7d2d3-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="7d2d3-117">Data Item Name</span></span>|<span data-ttu-id="7d2d3-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="7d2d3-118">Data Item Type</span></span>|<span data-ttu-id="7d2d3-119">Description</span><span class="sxs-lookup"><span data-stu-id="7d2d3-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7d2d3-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="7d2d3-120">WorkflowInstanceId</span></span>|<span data-ttu-id="7d2d3-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="7d2d3-121">xs:string</span></span>|<span data-ttu-id="7d2d3-122">ID de l'instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="7d2d3-122">The workflow instance id.</span></span>|  
|<span data-ttu-id="7d2d3-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="7d2d3-123">AppDomain</span></span>|<span data-ttu-id="7d2d3-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="7d2d3-124">xs:string</span></span>|<span data-ttu-id="7d2d3-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="7d2d3-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
