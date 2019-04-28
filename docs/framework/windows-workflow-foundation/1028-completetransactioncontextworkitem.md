---
title: 1028 - CompleteTransactionContextWorkItem
ms.date: 03/30/2017
ms.assetid: 95423f9d-d29a-460e-bcd8-096e80af5bd0
ms.openlocfilehash: 806a437822cef8802a2bef6a54f924f84c88ef60
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008809"
---
# <a name="1028---completetransactioncontextworkitem"></a><span data-ttu-id="dae58-102">1028 - CompleteTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="dae58-102">1028 - CompleteTransactionContextWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="dae58-103">Properties</span><span class="sxs-lookup"><span data-stu-id="dae58-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="dae58-104">Id</span><span class="sxs-lookup"><span data-stu-id="dae58-104">ID</span></span>|<span data-ttu-id="dae58-105">1028</span><span class="sxs-lookup"><span data-stu-id="dae58-105">1028</span></span>|  
|<span data-ttu-id="dae58-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="dae58-106">Keywords</span></span>|<span data-ttu-id="dae58-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="dae58-107">WFRuntime</span></span>|  
|<span data-ttu-id="dae58-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="dae58-108">Level</span></span>|<span data-ttu-id="dae58-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="dae58-109">Verbose</span></span>|  
|<span data-ttu-id="dae58-110">Canal</span><span class="sxs-lookup"><span data-stu-id="dae58-110">Channel</span></span>|<span data-ttu-id="dae58-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="dae58-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="dae58-112">Description</span><span class="sxs-lookup"><span data-stu-id="dae58-112">Description</span></span>  
 <span data-ttu-id="dae58-113">Indique qu'un TransactionContextWorkItem est terminé.</span><span class="sxs-lookup"><span data-stu-id="dae58-113">Indicates a TransactionContextWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="dae58-114">Message</span><span class="sxs-lookup"><span data-stu-id="dae58-114">Message</span></span>  
 <span data-ttu-id="dae58-115">TransactionContextWorkItem est terminé pour l’activité « %1 », DisplayName : « %2 », InstanceId : « %3 ».</span><span class="sxs-lookup"><span data-stu-id="dae58-115">A TransactionContextWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="dae58-116">Détails</span><span class="sxs-lookup"><span data-stu-id="dae58-116">Details</span></span>  
  
|<span data-ttu-id="dae58-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="dae58-117">Data Item Name</span></span>|<span data-ttu-id="dae58-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="dae58-118">Data Item Type</span></span>|<span data-ttu-id="dae58-119">Description</span><span class="sxs-lookup"><span data-stu-id="dae58-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="dae58-120">Activité</span><span class="sxs-lookup"><span data-stu-id="dae58-120">Activity</span></span>|<span data-ttu-id="dae58-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="dae58-121">xs:string</span></span>|<span data-ttu-id="dae58-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="dae58-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="dae58-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="dae58-123">DisplayName</span></span>|<span data-ttu-id="dae58-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="dae58-124">xs:string</span></span>|<span data-ttu-id="dae58-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="dae58-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="dae58-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="dae58-126">InstanceId</span></span>|<span data-ttu-id="dae58-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="dae58-127">xs:string</span></span>|<span data-ttu-id="dae58-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="dae58-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="dae58-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="dae58-129">AppDomain</span></span>|<span data-ttu-id="dae58-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="dae58-130">xs:string</span></span>|<span data-ttu-id="dae58-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="dae58-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
