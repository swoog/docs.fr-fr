---
title: 1003 - WorkflowInstanceCanceled
ms.date: 03/30/2017
ms.assetid: 64754dc2-c160-4bf3-869a-13d56694e2dc
ms.openlocfilehash: c76a2dab6a95bda7f3969af07f814aba30071c7f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008627"
---
# <a name="1003---workflowinstancecanceled"></a><span data-ttu-id="c2db3-102">1003 - WorkflowInstanceCanceled</span><span class="sxs-lookup"><span data-stu-id="c2db3-102">1003 - WorkflowInstanceCanceled</span></span>
## <a name="properties"></a><span data-ttu-id="c2db3-103">Properties</span><span class="sxs-lookup"><span data-stu-id="c2db3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c2db3-104">Id</span><span class="sxs-lookup"><span data-stu-id="c2db3-104">ID</span></span>|<span data-ttu-id="c2db3-105">1003</span><span class="sxs-lookup"><span data-stu-id="c2db3-105">1003</span></span>|  
|<span data-ttu-id="c2db3-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c2db3-106">Keywords</span></span>|<span data-ttu-id="c2db3-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="c2db3-107">WFRuntime</span></span>|  
|<span data-ttu-id="c2db3-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="c2db3-108">Level</span></span>|<span data-ttu-id="c2db3-109">Information</span><span class="sxs-lookup"><span data-stu-id="c2db3-109">Information</span></span>|  
|<span data-ttu-id="c2db3-110">Canal</span><span class="sxs-lookup"><span data-stu-id="c2db3-110">Channel</span></span>|<span data-ttu-id="c2db3-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="c2db3-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c2db3-112">Description</span><span class="sxs-lookup"><span data-stu-id="c2db3-112">Description</span></span>  
 <span data-ttu-id="c2db3-113">Indique qu'une instance de workflow s'est terminée à l'état Canceled.</span><span class="sxs-lookup"><span data-stu-id="c2db3-113">Indicates a workflow instance has completed in the Canceled state.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c2db3-114">Message</span><span class="sxs-lookup"><span data-stu-id="c2db3-114">Message</span></span>  
 <span data-ttu-id="c2db3-115">ID WorkflowInstance : « %1 » s'est terminé à l'état Canceled.</span><span class="sxs-lookup"><span data-stu-id="c2db3-115">WorkflowInstance Id: '%1' has completed in the Canceled state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c2db3-116">Détails</span><span class="sxs-lookup"><span data-stu-id="c2db3-116">Details</span></span>  
  
|<span data-ttu-id="c2db3-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="c2db3-117">Data Item Name</span></span>|<span data-ttu-id="c2db3-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="c2db3-118">Data Item Type</span></span>|<span data-ttu-id="c2db3-119">Description</span><span class="sxs-lookup"><span data-stu-id="c2db3-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c2db3-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="c2db3-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="c2db3-121">ID d'instance pour le workflow</span><span class="sxs-lookup"><span data-stu-id="c2db3-121">The instance id for the workflow</span></span>|  
|<span data-ttu-id="c2db3-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="c2db3-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="c2db3-123">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="c2db3-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
