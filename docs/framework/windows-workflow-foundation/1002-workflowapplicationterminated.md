---
title: 1002 - WorkflowApplicationTerminated
ms.date: 03/30/2017
ms.assetid: 4e8b111f-79dc-4898-bb4a-e9b36f69420f
ms.openlocfilehash: 01c9aba6e863e07a1a999a28fccefbab95a34d5b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510077"
---
# <a name="1002---workflowapplicationterminated"></a><span data-ttu-id="6e32c-102">1002 - WorkflowApplicationTerminated</span><span class="sxs-lookup"><span data-stu-id="6e32c-102">1002 - WorkflowApplicationTerminated</span></span>
## <a name="properties"></a><span data-ttu-id="6e32c-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e32c-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="6e32c-104">ID</span><span class="sxs-lookup"><span data-stu-id="6e32c-104">ID</span></span>|<span data-ttu-id="6e32c-105">1002</span><span class="sxs-lookup"><span data-stu-id="6e32c-105">1002</span></span>|  
|<span data-ttu-id="6e32c-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="6e32c-106">Keywords</span></span>|<span data-ttu-id="6e32c-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="6e32c-107">WFRuntime</span></span>|  
|<span data-ttu-id="6e32c-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="6e32c-108">Level</span></span>|<span data-ttu-id="6e32c-109">Information</span><span class="sxs-lookup"><span data-stu-id="6e32c-109">Information</span></span>|  
|<span data-ttu-id="6e32c-110">Canal</span><span class="sxs-lookup"><span data-stu-id="6e32c-110">Channel</span></span>|<span data-ttu-id="6e32c-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="6e32c-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="6e32c-112">Description</span><span class="sxs-lookup"><span data-stu-id="6e32c-112">Description</span></span>  
 <span data-ttu-id="6e32c-113">Indique qu'une application de workflow s'est arrêtée en l'état Faulted avec une exception.</span><span class="sxs-lookup"><span data-stu-id="6e32c-113">Indicates a workflow application has terminated in the Faulted state with an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="6e32c-114">Message</span><span class="sxs-lookup"><span data-stu-id="6e32c-114">Message</span></span>  
 <span data-ttu-id="6e32c-115">Identificateur de WorkflowApplication : « %1 » a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="6e32c-115">WorkflowApplication Id: '%1' was terminated.</span></span> <span data-ttu-id="6e32c-116">Il s'est terminé dans l'état Faulted avec une exception.</span><span class="sxs-lookup"><span data-stu-id="6e32c-116">It has completed in the Faulted state with an exception.</span></span>  
  
## <a name="details"></a><span data-ttu-id="6e32c-117">Détails</span><span class="sxs-lookup"><span data-stu-id="6e32c-117">Details</span></span>  
  
|<span data-ttu-id="6e32c-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="6e32c-118">Data Item Name</span></span>|<span data-ttu-id="6e32c-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="6e32c-119">Data Item Type</span></span>|<span data-ttu-id="6e32c-120">Description</span><span class="sxs-lookup"><span data-stu-id="6e32c-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="6e32c-121">WorkflowApplicationId</span><span class="sxs-lookup"><span data-stu-id="6e32c-121">WorkflowApplicationId</span></span>|`xs:string`|<span data-ttu-id="6e32c-122">ID d'application de flux de travail</span><span class="sxs-lookup"><span data-stu-id="6e32c-122">The workflow application id</span></span>|  
|<span data-ttu-id="6e32c-123">Exception</span><span class="sxs-lookup"><span data-stu-id="6e32c-123">Exception</span></span>|`xs:string`|<span data-ttu-id="6e32c-124">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="6e32c-124">The exception details for the exception</span></span>|  
|<span data-ttu-id="6e32c-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="6e32c-125">AppDomain</span></span>|`xs:string`|<span data-ttu-id="6e32c-126">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="6e32c-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
