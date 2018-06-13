---
title: 1101 - WorkflowActivityStart
ms.date: 03/30/2017
ms.assetid: 831cd386-b9b5-47a9-9690-aff6292ff348
ms.openlocfilehash: 1e6db97284b7ca83d532166d96d7a42df0a51091
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510638"
---
# <a name="1101---workflowactivitystart"></a><span data-ttu-id="8b339-102">1101 - WorkflowActivityStart</span><span class="sxs-lookup"><span data-stu-id="8b339-102">1101 - WorkflowActivityStart</span></span>
## <a name="properties"></a><span data-ttu-id="8b339-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b339-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="8b339-104">ID</span><span class="sxs-lookup"><span data-stu-id="8b339-104">ID</span></span>|<span data-ttu-id="8b339-105">1101</span><span class="sxs-lookup"><span data-stu-id="8b339-105">1101</span></span>|  
|<span data-ttu-id="8b339-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8b339-106">Keywords</span></span>|<span data-ttu-id="8b339-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="8b339-107">WFRuntime</span></span>|  
|<span data-ttu-id="8b339-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="8b339-108">Level</span></span>|<span data-ttu-id="8b339-109">Information</span><span class="sxs-lookup"><span data-stu-id="8b339-109">Information</span></span>|  
|<span data-ttu-id="8b339-110">Canal</span><span class="sxs-lookup"><span data-stu-id="8b339-110">Channel</span></span>|<span data-ttu-id="8b339-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="8b339-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="8b339-112">Description</span><span class="sxs-lookup"><span data-stu-id="8b339-112">Description</span></span>  
 <span data-ttu-id="8b339-113">Indique qu'une activité du flux de travail a démarré.</span><span class="sxs-lookup"><span data-stu-id="8b339-113">Indicates a workflow activity has started.</span></span>  
  
## <a name="message"></a><span data-ttu-id="8b339-114">Message</span><span class="sxs-lookup"><span data-stu-id="8b339-114">Message</span></span>  
 <span data-ttu-id="8b339-115">ID WorkflowInstance : « %1 » Activité E2E</span><span class="sxs-lookup"><span data-stu-id="8b339-115">WorkflowInstance Id: '%1' E2E Activity</span></span>  
  
## <a name="details"></a><span data-ttu-id="8b339-116">Détails</span><span class="sxs-lookup"><span data-stu-id="8b339-116">Details</span></span>  
  
|<span data-ttu-id="8b339-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="8b339-117">Data Item Name</span></span>|<span data-ttu-id="8b339-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="8b339-118">Data Item Type</span></span>|<span data-ttu-id="8b339-119">Description</span><span class="sxs-lookup"><span data-stu-id="8b339-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="8b339-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="8b339-120">WorkflowInstanceId</span></span>|<span data-ttu-id="8b339-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="8b339-121">xs:string</span></span>|<span data-ttu-id="8b339-122">ID de l'instance de flux de travail.</span><span class="sxs-lookup"><span data-stu-id="8b339-122">The workflow instance id.</span></span>|  
|<span data-ttu-id="8b339-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="8b339-123">AppDomain</span></span>|<span data-ttu-id="8b339-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="8b339-124">xs:string</span></span>|<span data-ttu-id="8b339-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="8b339-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
