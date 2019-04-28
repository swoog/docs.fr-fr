---
title: 1027 - StartTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 116ae5ec-b9d5-4231-824e-270d00eea7b8
ms.openlocfilehash: 231a7607f2ce9a38e8dd6c1486a68bc9eb459e5e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008822"
---
# <a name="1027---starttransactioncontextworkitem"></a><span data-ttu-id="f42e5-102">1027 - StartTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="f42e5-102">1027 - StartTransactionContextWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="f42e5-103">Properties</span><span class="sxs-lookup"><span data-stu-id="f42e5-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f42e5-104">Id</span><span class="sxs-lookup"><span data-stu-id="f42e5-104">ID</span></span>|<span data-ttu-id="f42e5-105">1027</span><span class="sxs-lookup"><span data-stu-id="f42e5-105">1027</span></span>|  
|<span data-ttu-id="f42e5-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f42e5-106">Keywords</span></span>|<span data-ttu-id="f42e5-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="f42e5-107">WFRuntime</span></span>|  
|<span data-ttu-id="f42e5-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="f42e5-108">Level</span></span>|<span data-ttu-id="f42e5-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="f42e5-109">Verbose</span></span>|  
|<span data-ttu-id="f42e5-110">Canal</span><span class="sxs-lookup"><span data-stu-id="f42e5-110">Channel</span></span>|<span data-ttu-id="f42e5-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="f42e5-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f42e5-112">Description</span><span class="sxs-lookup"><span data-stu-id="f42e5-112">Description</span></span>  
 <span data-ttu-id="f42e5-113">Indique qu'un TransactionContextWorkItem démarre l'exécution.</span><span class="sxs-lookup"><span data-stu-id="f42e5-113">Indicates a TransactionContextWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f42e5-114">Message</span><span class="sxs-lookup"><span data-stu-id="f42e5-114">Message</span></span>  
 <span data-ttu-id="f42e5-115">Début de l’exécution d’un TransactionContextWorkItem pour l’activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="f42e5-115">Starting execution of a TransactionContextWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f42e5-116">Détails</span><span class="sxs-lookup"><span data-stu-id="f42e5-116">Details</span></span>  
  
|<span data-ttu-id="f42e5-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="f42e5-117">Data Item Name</span></span>|<span data-ttu-id="f42e5-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="f42e5-118">Data Item Type</span></span>|<span data-ttu-id="f42e5-119">Description</span><span class="sxs-lookup"><span data-stu-id="f42e5-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f42e5-120">Activité</span><span class="sxs-lookup"><span data-stu-id="f42e5-120">Activity</span></span>|<span data-ttu-id="f42e5-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="f42e5-121">xs:string</span></span>|<span data-ttu-id="f42e5-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="f42e5-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="f42e5-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="f42e5-123">DisplayName</span></span>|<span data-ttu-id="f42e5-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="f42e5-124">xs:string</span></span>|<span data-ttu-id="f42e5-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="f42e5-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="f42e5-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="f42e5-126">InstanceId</span></span>|<span data-ttu-id="f42e5-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="f42e5-127">xs:string</span></span>|<span data-ttu-id="f42e5-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="f42e5-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="f42e5-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="f42e5-129">AppDomain</span></span>|<span data-ttu-id="f42e5-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="f42e5-130">xs:string</span></span>|<span data-ttu-id="f42e5-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="f42e5-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
