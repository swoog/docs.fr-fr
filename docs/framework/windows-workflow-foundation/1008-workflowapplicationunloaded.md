---
title: 1008 - WorkflowApplicationUnloaded
ms.date: 03/30/2017
ms.assetid: a605b780-4a7e-43ab-92e7-0a3b01d053b0
ms.openlocfilehash: c7c22e6e4270a3fc3e91e1711db5da9bd5a378b9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61925227"
---
# <a name="1008---workflowapplicationunloaded"></a><span data-ttu-id="7f586-102">1008 - WorkflowApplicationUnloaded</span><span class="sxs-lookup"><span data-stu-id="7f586-102">1008 - WorkflowApplicationUnloaded</span></span>
## <a name="properties"></a><span data-ttu-id="7f586-103">Properties</span><span class="sxs-lookup"><span data-stu-id="7f586-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7f586-104">Id</span><span class="sxs-lookup"><span data-stu-id="7f586-104">ID</span></span>|<span data-ttu-id="7f586-105">1008</span><span class="sxs-lookup"><span data-stu-id="7f586-105">1008</span></span>|  
|<span data-ttu-id="7f586-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="7f586-106">Keywords</span></span>|<span data-ttu-id="7f586-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="7f586-107">WFRuntime</span></span>|  
|<span data-ttu-id="7f586-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="7f586-108">Level</span></span>|<span data-ttu-id="7f586-109">Information</span><span class="sxs-lookup"><span data-stu-id="7f586-109">Information</span></span>|  
|<span data-ttu-id="7f586-110">Canal</span><span class="sxs-lookup"><span data-stu-id="7f586-110">Channel</span></span>|<span data-ttu-id="7f586-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="7f586-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7f586-112">Description</span><span class="sxs-lookup"><span data-stu-id="7f586-112">Description</span></span>  
 <span data-ttu-id="7f586-113">Indique qu'une application de workflow a été déchargée.</span><span class="sxs-lookup"><span data-stu-id="7f586-113">Indicates a workflow application has unloaded.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7f586-114">Message</span><span class="sxs-lookup"><span data-stu-id="7f586-114">Message</span></span>  
 <span data-ttu-id="7f586-115">ID WorkflowInstance : « %1 » était Unloaded.</span><span class="sxs-lookup"><span data-stu-id="7f586-115">WorkflowInstance Id: '%1' was Unloaded.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7f586-116">Détails</span><span class="sxs-lookup"><span data-stu-id="7f586-116">Details</span></span>  
  
|<span data-ttu-id="7f586-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="7f586-117">Data Item Name</span></span>|<span data-ttu-id="7f586-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="7f586-118">Data Item Type</span></span>|<span data-ttu-id="7f586-119">Description</span><span class="sxs-lookup"><span data-stu-id="7f586-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7f586-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="7f586-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="7f586-121">ID d'instance pour le workflow</span><span class="sxs-lookup"><span data-stu-id="7f586-121">The instance id for the workflow</span></span>|  
|<span data-ttu-id="7f586-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="7f586-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="7f586-123">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="7f586-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
