---
title: 4212 - LockRetryTimeout
ms.date: 03/30/2017
ms.assetid: d4ad415a-9871-49fc-85b8-8ee2ea149b1d
ms.openlocfilehash: 9b7a463851d380eba1ef7b28fbc6decd0cfc979c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774216"
---
# <a name="4212---lockretrytimeout"></a><span data-ttu-id="60f17-102">4212 - LockRetryTimeout</span><span class="sxs-lookup"><span data-stu-id="60f17-102">4212 - LockRetryTimeout</span></span>
## <a name="properties"></a><span data-ttu-id="60f17-103">Properties</span><span class="sxs-lookup"><span data-stu-id="60f17-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="60f17-104">Id</span><span class="sxs-lookup"><span data-stu-id="60f17-104">ID</span></span>|<span data-ttu-id="60f17-105">4212</span><span class="sxs-lookup"><span data-stu-id="60f17-105">4212</span></span>|  
|<span data-ttu-id="60f17-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="60f17-106">Keywords</span></span>|<span data-ttu-id="60f17-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="60f17-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="60f17-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="60f17-108">Level</span></span>|<span data-ttu-id="60f17-109">Warning</span><span class="sxs-lookup"><span data-stu-id="60f17-109">Warning</span></span>|  
|<span data-ttu-id="60f17-110">Canal</span><span class="sxs-lookup"><span data-stu-id="60f17-110">Channel</span></span>|<span data-ttu-id="60f17-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="60f17-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="60f17-112">Description</span><span class="sxs-lookup"><span data-stu-id="60f17-112">Description</span></span>  
 <span data-ttu-id="60f17-113">Le fournisseur SQL a rencontré une expiration du délai d'attente lors de la tentative d'acquisition du verrou d'instance.</span><span class="sxs-lookup"><span data-stu-id="60f17-113">SQL provider encountered a timeout trying to acquire the instance lock.</span></span>  
  
## <a name="message"></a><span data-ttu-id="60f17-114">Message</span><span class="sxs-lookup"><span data-stu-id="60f17-114">Message</span></span>  
 <span data-ttu-id="60f17-115">Délai d’expiration essaie d’acquérir le verrou d’instance.</span><span class="sxs-lookup"><span data-stu-id="60f17-115">Timeout trying to acquire the instance lock.</span></span>  <span data-ttu-id="60f17-116">L'opération ne s'est pas terminée dans le délai imparti de %1.</span><span class="sxs-lookup"><span data-stu-id="60f17-116">The operation did not complete within the allotted timeout of %1.</span></span> <span data-ttu-id="60f17-117">Le temps alloué à cette opération peut avoir été une partie d'un délai d'expiration plus long.</span><span class="sxs-lookup"><span data-stu-id="60f17-117">The time allotted to this operation may have been a portion of a longer timeout.</span></span>  
  
## <a name="details"></a><span data-ttu-id="60f17-118">Détails</span><span class="sxs-lookup"><span data-stu-id="60f17-118">Details</span></span>  
  
|<span data-ttu-id="60f17-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="60f17-119">Data Item Name</span></span>|<span data-ttu-id="60f17-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="60f17-120">Data Item Type</span></span>|<span data-ttu-id="60f17-121">Description</span><span class="sxs-lookup"><span data-stu-id="60f17-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="60f17-122">Délai</span><span class="sxs-lookup"><span data-stu-id="60f17-122">Delay</span></span>|<span data-ttu-id="60f17-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="60f17-123">xs:string</span></span>|<span data-ttu-id="60f17-124">Délai entre les tentatives.</span><span class="sxs-lookup"><span data-stu-id="60f17-124">The delay between retries.</span></span>|  
|<span data-ttu-id="60f17-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="60f17-125">AppDomain</span></span>|<span data-ttu-id="60f17-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="60f17-126">xs:string</span></span>|<span data-ttu-id="60f17-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="60f17-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
