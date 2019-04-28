---
title: 1002 - WorkflowApplicationTerminated
ms.date: 03/30/2017
ms.assetid: 4e8b111f-79dc-4898-bb4a-e9b36f69420f
ms.openlocfilehash: 01c9aba6e863e07a1a999a28fccefbab95a34d5b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008653"
---
# <a name="1002---workflowapplicationterminated"></a><span data-ttu-id="b3610-102">1002 - WorkflowApplicationTerminated</span><span class="sxs-lookup"><span data-stu-id="b3610-102">1002 - WorkflowApplicationTerminated</span></span>
## <a name="properties"></a><span data-ttu-id="b3610-103">Properties</span><span class="sxs-lookup"><span data-stu-id="b3610-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b3610-104">Id</span><span class="sxs-lookup"><span data-stu-id="b3610-104">ID</span></span>|<span data-ttu-id="b3610-105">1002</span><span class="sxs-lookup"><span data-stu-id="b3610-105">1002</span></span>|  
|<span data-ttu-id="b3610-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b3610-106">Keywords</span></span>|<span data-ttu-id="b3610-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="b3610-107">WFRuntime</span></span>|  
|<span data-ttu-id="b3610-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="b3610-108">Level</span></span>|<span data-ttu-id="b3610-109">Information</span><span class="sxs-lookup"><span data-stu-id="b3610-109">Information</span></span>|  
|<span data-ttu-id="b3610-110">Canal</span><span class="sxs-lookup"><span data-stu-id="b3610-110">Channel</span></span>|<span data-ttu-id="b3610-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="b3610-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b3610-112">Description</span><span class="sxs-lookup"><span data-stu-id="b3610-112">Description</span></span>  
 <span data-ttu-id="b3610-113">Indique qu'une application de workflow s'est arrêtée en l'état Faulted avec une exception.</span><span class="sxs-lookup"><span data-stu-id="b3610-113">Indicates a workflow application has terminated in the Faulted state with an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b3610-114">Message</span><span class="sxs-lookup"><span data-stu-id="b3610-114">Message</span></span>  
 <span data-ttu-id="b3610-115">Identificateur de WorkflowApplication : « %1 » a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="b3610-115">WorkflowApplication Id: '%1' was terminated.</span></span> <span data-ttu-id="b3610-116">Il s'est terminé dans l'état Faulted avec une exception.</span><span class="sxs-lookup"><span data-stu-id="b3610-116">It has completed in the Faulted state with an exception.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b3610-117">Détails</span><span class="sxs-lookup"><span data-stu-id="b3610-117">Details</span></span>  
  
|<span data-ttu-id="b3610-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="b3610-118">Data Item Name</span></span>|<span data-ttu-id="b3610-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="b3610-119">Data Item Type</span></span>|<span data-ttu-id="b3610-120">Description</span><span class="sxs-lookup"><span data-stu-id="b3610-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b3610-121">WorkflowApplicationId</span><span class="sxs-lookup"><span data-stu-id="b3610-121">WorkflowApplicationId</span></span>|`xs:string`|<span data-ttu-id="b3610-122">ID d'application de flux de travail</span><span class="sxs-lookup"><span data-stu-id="b3610-122">The workflow application id</span></span>|  
|<span data-ttu-id="b3610-123">Exception</span><span class="sxs-lookup"><span data-stu-id="b3610-123">Exception</span></span>|`xs:string`|<span data-ttu-id="b3610-124">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="b3610-124">The exception details for the exception</span></span>|  
|<span data-ttu-id="b3610-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="b3610-125">AppDomain</span></span>|`xs:string`|<span data-ttu-id="b3610-126">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="b3610-126">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
