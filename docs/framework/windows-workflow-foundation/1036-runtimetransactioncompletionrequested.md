---
title: 1036 - RuntimeTransactionCompletionRequested
ms.date: 03/30/2017
ms.assetid: d36b9f44-7c0f-4083-9d3a-9034dd2b98de
ms.openlocfilehash: 649ba542a9ed2f330ac71e447602d637530dc601
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924837"
---
# <a name="1036---runtimetransactioncompletionrequested"></a><span data-ttu-id="3de54-102">1036 - RuntimeTransactionCompletionRequested</span><span class="sxs-lookup"><span data-stu-id="3de54-102">1036 - RuntimeTransactionCompletionRequested</span></span>
## <a name="properties"></a><span data-ttu-id="3de54-103">Properties</span><span class="sxs-lookup"><span data-stu-id="3de54-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3de54-104">Id</span><span class="sxs-lookup"><span data-stu-id="3de54-104">ID</span></span>|<span data-ttu-id="3de54-105">1036</span><span class="sxs-lookup"><span data-stu-id="3de54-105">1036</span></span>|  
|<span data-ttu-id="3de54-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="3de54-106">Keywords</span></span>|<span data-ttu-id="3de54-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="3de54-107">WFRuntime</span></span>|  
|<span data-ttu-id="3de54-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="3de54-108">Level</span></span>|<span data-ttu-id="3de54-109">Verbose</span><span class="sxs-lookup"><span data-stu-id="3de54-109">Verbose</span></span>|  
|<span data-ttu-id="3de54-110">Canal</span><span class="sxs-lookup"><span data-stu-id="3de54-110">Channel</span></span>|<span data-ttu-id="3de54-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="3de54-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3de54-112">Description</span><span class="sxs-lookup"><span data-stu-id="3de54-112">Description</span></span>  
 <span data-ttu-id="3de54-113">Indique qu’une activité a planifié la fin de la transaction runtime.</span><span class="sxs-lookup"><span data-stu-id="3de54-113">Indicates an activity has scheduled the completion of the runtime transaction.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3de54-114">Message</span><span class="sxs-lookup"><span data-stu-id="3de54-114">Message</span></span>  
 <span data-ttu-id="3de54-115">L’activité « %1 », DisplayName : « %2 », InstanceId : « %3 » a planifié la fin de la transaction runtime.</span><span class="sxs-lookup"><span data-stu-id="3de54-115">Activity '%1', DisplayName: '%2', InstanceId: '%3' has scheduled completion of the runtime transaction.</span></span>  
  
## <a name="details"></a><span data-ttu-id="3de54-116">Détails</span><span class="sxs-lookup"><span data-stu-id="3de54-116">Details</span></span>  
  
|<span data-ttu-id="3de54-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="3de54-117">Data Item Name</span></span>|<span data-ttu-id="3de54-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="3de54-118">Data Item Type</span></span>|<span data-ttu-id="3de54-119">Description</span><span class="sxs-lookup"><span data-stu-id="3de54-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3de54-120">Activité</span><span class="sxs-lookup"><span data-stu-id="3de54-120">Activity</span></span>|<span data-ttu-id="3de54-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="3de54-121">xs:string</span></span>|<span data-ttu-id="3de54-122">Nom de type de l'activité.</span><span class="sxs-lookup"><span data-stu-id="3de54-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="3de54-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="3de54-123">DisplayName</span></span>|<span data-ttu-id="3de54-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="3de54-124">xs:string</span></span>|<span data-ttu-id="3de54-125">Nom complet de l'activité.</span><span class="sxs-lookup"><span data-stu-id="3de54-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="3de54-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="3de54-126">InstanceId</span></span>|<span data-ttu-id="3de54-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="3de54-127">xs:string</span></span>|<span data-ttu-id="3de54-128">ID d'instance de l'activité.</span><span class="sxs-lookup"><span data-stu-id="3de54-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="3de54-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="3de54-129">AppDomain</span></span>|<span data-ttu-id="3de54-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="3de54-130">xs:string</span></span>|<span data-ttu-id="3de54-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="3de54-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
