---
title: 1008 - WorkflowApplicationUnloaded
ms.date: 03/30/2017
ms.assetid: a605b780-4a7e-43ab-92e7-0a3b01d053b0
ms.openlocfilehash: c7c22e6e4270a3fc3e91e1711db5da9bd5a378b9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33509559"
---
# <a name="1008---workflowapplicationunloaded"></a><span data-ttu-id="e9123-102">1008 - WorkflowApplicationUnloaded</span><span class="sxs-lookup"><span data-stu-id="e9123-102">1008 - WorkflowApplicationUnloaded</span></span>
## <a name="properties"></a><span data-ttu-id="e9123-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e9123-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e9123-104">ID</span><span class="sxs-lookup"><span data-stu-id="e9123-104">ID</span></span>|<span data-ttu-id="e9123-105">1008</span><span class="sxs-lookup"><span data-stu-id="e9123-105">1008</span></span>|  
|<span data-ttu-id="e9123-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="e9123-106">Keywords</span></span>|<span data-ttu-id="e9123-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="e9123-107">WFRuntime</span></span>|  
|<span data-ttu-id="e9123-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="e9123-108">Level</span></span>|<span data-ttu-id="e9123-109">Information</span><span class="sxs-lookup"><span data-stu-id="e9123-109">Information</span></span>|  
|<span data-ttu-id="e9123-110">Canal</span><span class="sxs-lookup"><span data-stu-id="e9123-110">Channel</span></span>|<span data-ttu-id="e9123-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="e9123-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e9123-112">Description</span><span class="sxs-lookup"><span data-stu-id="e9123-112">Description</span></span>  
 <span data-ttu-id="e9123-113">Indique qu'une application de workflow a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="e9123-113">Indicates a workflow application has unloaded.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e9123-114">Message</span><span class="sxs-lookup"><span data-stu-id="e9123-114">Message</span></span>  
 <span data-ttu-id="e9123-115">ID WorkflowInstance : « %1 » était Unloaded.</span><span class="sxs-lookup"><span data-stu-id="e9123-115">WorkflowInstance Id: '%1' was Unloaded.</span></span>  
  
## <a name="details"></a><span data-ttu-id="e9123-116">Détails</span><span class="sxs-lookup"><span data-stu-id="e9123-116">Details</span></span>  
  
|<span data-ttu-id="e9123-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="e9123-117">Data Item Name</span></span>|<span data-ttu-id="e9123-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="e9123-118">Data Item Type</span></span>|<span data-ttu-id="e9123-119">Description</span><span class="sxs-lookup"><span data-stu-id="e9123-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e9123-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="e9123-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="e9123-121">ID d'instance pour le workflow</span><span class="sxs-lookup"><span data-stu-id="e9123-121">The instance id for the workflow</span></span>|  
|<span data-ttu-id="e9123-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="e9123-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="e9123-123">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="e9123-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
