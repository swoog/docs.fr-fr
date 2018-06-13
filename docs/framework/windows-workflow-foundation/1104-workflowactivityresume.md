---
title: 1104 - WorkflowActivityResume
ms.date: 03/30/2017
ms.assetid: 7fe95d1e-34bd-43ca-b92e-587d2d248fff
ms.openlocfilehash: 4c9ae5fd386fc93ea19578097aa4e0afdda527e2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33511054"
---
# <a name="1104---workflowactivityresume"></a><span data-ttu-id="a9ef1-102">1104 - WorkflowActivityResume</span><span class="sxs-lookup"><span data-stu-id="a9ef1-102">1104 - WorkflowActivityResume</span></span>
## <a name="properties"></a><span data-ttu-id="a9ef1-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9ef1-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a9ef1-104">ID</span><span class="sxs-lookup"><span data-stu-id="a9ef1-104">ID</span></span>|<span data-ttu-id="a9ef1-105">1104</span><span class="sxs-lookup"><span data-stu-id="a9ef1-105">1104</span></span>|  
|<span data-ttu-id="a9ef1-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a9ef1-106">Keywords</span></span>|<span data-ttu-id="a9ef1-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="a9ef1-107">WFRuntime</span></span>|  
|<span data-ttu-id="a9ef1-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="a9ef1-108">Level</span></span>|<span data-ttu-id="a9ef1-109">Information</span><span class="sxs-lookup"><span data-stu-id="a9ef1-109">Information</span></span>|  
|<span data-ttu-id="a9ef1-110">Canal</span><span class="sxs-lookup"><span data-stu-id="a9ef1-110">Channel</span></span>|<span data-ttu-id="a9ef1-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="a9ef1-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="a9ef1-112">Description</span><span class="sxs-lookup"><span data-stu-id="a9ef1-112">Description</span></span>  
 <span data-ttu-id="a9ef1-113">Indique qu'une activité du flux de travail a été reprise.</span><span class="sxs-lookup"><span data-stu-id="a9ef1-113">Indicates a workflow activity has been resumed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="a9ef1-114">Message</span><span class="sxs-lookup"><span data-stu-id="a9ef1-114">Message</span></span>  
 <span data-ttu-id="a9ef1-115">ID WorkflowInstance : « %1 » Activité E2E</span><span class="sxs-lookup"><span data-stu-id="a9ef1-115">WorkflowInstance Id: '%1' E2E Activity</span></span>  
  
## <a name="details"></a><span data-ttu-id="a9ef1-116">Détails</span><span class="sxs-lookup"><span data-stu-id="a9ef1-116">Details</span></span>  
  
|<span data-ttu-id="a9ef1-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a9ef1-117">Data Item Name</span></span>|<span data-ttu-id="a9ef1-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a9ef1-118">Data Item Type</span></span>|<span data-ttu-id="a9ef1-119">Description</span><span class="sxs-lookup"><span data-stu-id="a9ef1-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="a9ef1-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="a9ef1-120">WorkflowInstanceId</span></span>|<span data-ttu-id="a9ef1-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="a9ef1-121">xs:string</span></span>|<span data-ttu-id="a9ef1-122">ID de l'instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="a9ef1-122">The workflow instance id.</span></span>|  
|<span data-ttu-id="a9ef1-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="a9ef1-123">AppDomain</span></span>|<span data-ttu-id="a9ef1-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="a9ef1-124">xs:string</span></span>|<span data-ttu-id="a9ef1-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="a9ef1-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
