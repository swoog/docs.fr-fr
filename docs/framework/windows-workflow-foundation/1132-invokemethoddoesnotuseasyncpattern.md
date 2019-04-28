---
title: 1132 - InvokeMethodDoesNotUseAsyncPattern
ms.date: 03/30/2017
ms.assetid: 436b3767-4460-46b0-9ea3-fc2963260c11
ms.openlocfilehash: 64701d4c38c042e8273129be19f9caeb2c442abf
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61924213"
---
# <a name="1132---invokemethoddoesnotuseasyncpattern"></a><span data-ttu-id="ca490-102">1132 - InvokeMethodDoesNotUseAsyncPattern</span><span class="sxs-lookup"><span data-stu-id="ca490-102">1132 - InvokeMethodDoesNotUseAsyncPattern</span></span>
## <a name="properties"></a><span data-ttu-id="ca490-103">Properties</span><span class="sxs-lookup"><span data-stu-id="ca490-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ca490-104">Id</span><span class="sxs-lookup"><span data-stu-id="ca490-104">ID</span></span>|<span data-ttu-id="ca490-105">1132</span><span class="sxs-lookup"><span data-stu-id="ca490-105">1132</span></span>|  
|<span data-ttu-id="ca490-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="ca490-106">Keywords</span></span>|<span data-ttu-id="ca490-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ca490-107">WFRuntime</span></span>|  
|<span data-ttu-id="ca490-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="ca490-108">Level</span></span>|<span data-ttu-id="ca490-109">Information</span><span class="sxs-lookup"><span data-stu-id="ca490-109">Information</span></span>|  
|<span data-ttu-id="ca490-110">Canal</span><span class="sxs-lookup"><span data-stu-id="ca490-110">Channel</span></span>|<span data-ttu-id="ca490-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="ca490-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ca490-112">Description</span><span class="sxs-lookup"><span data-stu-id="ca490-112">Description</span></span>  
 <span data-ttu-id="ca490-113">Pendant l’étape CacheMetadata, l’activité InvokeMethod indique qu’elle n’utilise pas le modèle asynchrone lors de l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ca490-113">During CacheMetadata step, InvokeMethod activity indicates that it is not using the async pattern when invoking the method.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ca490-114">Message</span><span class="sxs-lookup"><span data-stu-id="ca490-114">Message</span></span>  
 <span data-ttu-id="ca490-115">InvokeMethod « %1 » - la méthode n’utilise pas un modèle asynchrone.</span><span class="sxs-lookup"><span data-stu-id="ca490-115">InvokeMethod '%1' - method does not use asynchronous pattern.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ca490-116">Détails</span><span class="sxs-lookup"><span data-stu-id="ca490-116">Details</span></span>  
  
|<span data-ttu-id="ca490-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="ca490-117">Data Item Name</span></span>|<span data-ttu-id="ca490-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="ca490-118">Data Item Type</span></span>|<span data-ttu-id="ca490-119">Description</span><span class="sxs-lookup"><span data-stu-id="ca490-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ca490-120">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="ca490-120">InvokeMethod</span></span>|<span data-ttu-id="ca490-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ca490-121">xs:string</span></span>|<span data-ttu-id="ca490-122">Nom complet de l'activité InvokeMethod.</span><span class="sxs-lookup"><span data-stu-id="ca490-122">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="ca490-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="ca490-123">AppDomain</span></span>|<span data-ttu-id="ca490-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="ca490-124">xs:string</span></span>|<span data-ttu-id="ca490-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="ca490-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
