---
title: 1027 - StartTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 116ae5ec-b9d5-4231-824e-270d00eea7b8
ms.openlocfilehash: 231a7607f2ce9a38e8dd6c1486a68bc9eb459e5e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510807"
---
# <a name="1027---starttransactioncontextworkitem"></a><span data-ttu-id="959d3-102">1027 - StartTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="959d3-102">1027 - StartTransactionContextWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="959d3-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="959d3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="959d3-104">ID</span><span class="sxs-lookup"><span data-stu-id="959d3-104">ID</span></span>|<span data-ttu-id="959d3-105">1027</span><span class="sxs-lookup"><span data-stu-id="959d3-105">1027</span></span>|  
|<span data-ttu-id="959d3-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="959d3-106">Keywords</span></span>|<span data-ttu-id="959d3-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="959d3-107">WFRuntime</span></span>|  
|<span data-ttu-id="959d3-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="959d3-108">Level</span></span>|<span data-ttu-id="959d3-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="959d3-109">Verbose</span></span>|  
|<span data-ttu-id="959d3-110">Canal</span><span class="sxs-lookup"><span data-stu-id="959d3-110">Channel</span></span>|<span data-ttu-id="959d3-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="959d3-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="959d3-112">Description</span><span class="sxs-lookup"><span data-stu-id="959d3-112">Description</span></span>  
 <span data-ttu-id="959d3-113">Indique qu'un TransactionContextWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="959d3-113">Indicates a TransactionContextWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="959d3-114">Message</span><span class="sxs-lookup"><span data-stu-id="959d3-114">Message</span></span>  
 <span data-ttu-id="959d3-115">Début de l'exécution d'un TransactionContextWorkItem pour l'activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="959d3-115">Starting execution of a TransactionContextWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="959d3-116">Détails</span><span class="sxs-lookup"><span data-stu-id="959d3-116">Details</span></span>  
  
|<span data-ttu-id="959d3-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="959d3-117">Data Item Name</span></span>|<span data-ttu-id="959d3-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="959d3-118">Data Item Type</span></span>|<span data-ttu-id="959d3-119">Description</span><span class="sxs-lookup"><span data-stu-id="959d3-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="959d3-120">Activité</span><span class="sxs-lookup"><span data-stu-id="959d3-120">Activity</span></span>|<span data-ttu-id="959d3-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="959d3-121">xs:string</span></span>|<span data-ttu-id="959d3-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="959d3-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="959d3-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="959d3-123">DisplayName</span></span>|<span data-ttu-id="959d3-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="959d3-124">xs:string</span></span>|<span data-ttu-id="959d3-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="959d3-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="959d3-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="959d3-126">InstanceId</span></span>|<span data-ttu-id="959d3-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="959d3-127">xs:string</span></span>|<span data-ttu-id="959d3-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="959d3-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="959d3-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="959d3-129">AppDomain</span></span>|<span data-ttu-id="959d3-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="959d3-130">xs:string</span></span>|<span data-ttu-id="959d3-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="959d3-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
