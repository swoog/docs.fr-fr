---
title: 1004 - WorkflowInstanceAborted
ms.date: 03/30/2017
ms.assetid: edb9ab8c-0b9a-488d-aa96-9c8c7984b53c
ms.openlocfilehash: d34f6f1ab6af8e06a0f28fb043faf9fe16a8b211
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57485185"
---
# <a name="1004---workflowinstanceaborted"></a><span data-ttu-id="0a0de-102">1004 - WorkflowInstanceAborted</span><span class="sxs-lookup"><span data-stu-id="0a0de-102">1004 - WorkflowInstanceAborted</span></span>

## <a name="properties"></a><span data-ttu-id="0a0de-103">Properties</span><span class="sxs-lookup"><span data-stu-id="0a0de-103">Properties</span></span>

|||
|-|-|
|<span data-ttu-id="0a0de-104">ID</span><span class="sxs-lookup"><span data-stu-id="0a0de-104">ID</span></span>|<span data-ttu-id="0a0de-105">1004</span><span class="sxs-lookup"><span data-stu-id="0a0de-105">1004</span></span>|
|<span data-ttu-id="0a0de-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="0a0de-106">Keywords</span></span>|<span data-ttu-id="0a0de-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="0a0de-107">WFRuntime</span></span>|
|<span data-ttu-id="0a0de-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="0a0de-108">Level</span></span>|<span data-ttu-id="0a0de-109">Information</span><span class="sxs-lookup"><span data-stu-id="0a0de-109">Information</span></span>|
|<span data-ttu-id="0a0de-110">Canal</span><span class="sxs-lookup"><span data-stu-id="0a0de-110">Channel</span></span>|<span data-ttu-id="0a0de-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="0a0de-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|

## <a name="description"></a><span data-ttu-id="0a0de-112">Description</span><span class="sxs-lookup"><span data-stu-id="0a0de-112">Description</span></span>

<span data-ttu-id="0a0de-113">Indique une instance de workflow a été abandonnée avec une exception.</span><span class="sxs-lookup"><span data-stu-id="0a0de-113">Indicates a workflow instance has aborted with an exception.</span></span>

## <a name="message"></a><span data-ttu-id="0a0de-114">Message</span><span class="sxs-lookup"><span data-stu-id="0a0de-114">Message</span></span>

<span data-ttu-id="0a0de-115">ID WorkflowInstance : « %1 » a été abandonné avec une exception.</span><span class="sxs-lookup"><span data-stu-id="0a0de-115">WorkflowInstance Id: '%1' was aborted with an exception.</span></span>

## <a name="details"></a><span data-ttu-id="0a0de-116">Détails</span><span class="sxs-lookup"><span data-stu-id="0a0de-116">Details</span></span>

|<span data-ttu-id="0a0de-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="0a0de-117">Data Item Name</span></span>|<span data-ttu-id="0a0de-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="0a0de-118">Data Item Type</span></span>|<span data-ttu-id="0a0de-119">Description</span><span class="sxs-lookup"><span data-stu-id="0a0de-119">Description</span></span>|
|--------------------|--------------------|-----------------|
|<span data-ttu-id="0a0de-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="0a0de-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="0a0de-121">ID d'instance pour le workflow</span><span class="sxs-lookup"><span data-stu-id="0a0de-121">The instance id for the workflow</span></span>|
|<span data-ttu-id="0a0de-122">Exception</span><span class="sxs-lookup"><span data-stu-id="0a0de-122">Exception</span></span>|`xs:string`|<span data-ttu-id="0a0de-123">Détails de l'exception</span><span class="sxs-lookup"><span data-stu-id="0a0de-123">The exception details for the exception</span></span>|
|<span data-ttu-id="0a0de-124">AppDomain</span><span class="sxs-lookup"><span data-stu-id="0a0de-124">AppDomain</span></span>|`xs:string`|<span data-ttu-id="0a0de-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="0a0de-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
