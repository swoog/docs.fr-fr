---
title: 4203 - RenewLockSystemError
ms.date: 03/30/2017
ms.assetid: 6ec9ec6f-4ae2-45cf-b99b-02cdb9dc9ec9
ms.openlocfilehash: 984f7ddae8797cba17753a618d0820d21bde5eef
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33513927"
---
# <a name="4203---renewlocksystemerror"></a><span data-ttu-id="5211f-102">4203 - RenewLockSystemError</span><span class="sxs-lookup"><span data-stu-id="5211f-102">4203 - RenewLockSystemError</span></span>
## <a name="properties"></a><span data-ttu-id="5211f-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5211f-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="5211f-104">ID</span><span class="sxs-lookup"><span data-stu-id="5211f-104">ID</span></span>|<span data-ttu-id="5211f-105">4203</span><span class="sxs-lookup"><span data-stu-id="5211f-105">4203</span></span>|  
|<span data-ttu-id="5211f-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="5211f-106">Keywords</span></span>|<span data-ttu-id="5211f-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="5211f-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="5211f-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="5211f-108">Level</span></span>|<span data-ttu-id="5211f-109">Erreur</span><span class="sxs-lookup"><span data-stu-id="5211f-109">Error</span></span>|  
|<span data-ttu-id="5211f-110">Canal</span><span class="sxs-lookup"><span data-stu-id="5211f-110">Channel</span></span>|<span data-ttu-id="5211f-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="5211f-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="5211f-112">Description</span><span class="sxs-lookup"><span data-stu-id="5211f-112">Description</span></span>  
 <span data-ttu-id="5211f-113">Indique que le fournisseur SQL n'a pas pu étendre l'expiration du verrou, car l'expiration du verrou a déjà été passée ou le propriétaire de verrou a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="5211f-113">Indicates SQL provider has failed to extend lock expiration due to either lock expiration already passed or the lock owner was deleted.</span></span> <span data-ttu-id="5211f-114">Le SqlWorkflowInstanceStore sera annulé.</span><span class="sxs-lookup"><span data-stu-id="5211f-114">The SqlWorkflowInstanceStore will be aborted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="5211f-115">Message</span><span class="sxs-lookup"><span data-stu-id="5211f-115">Message</span></span>  
 <span data-ttu-id="5211f-116">Échec de l'extension de l'expiration du verrou ; l'expiration du verrou a déjà été passée ou le propriétaire de verrou a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="5211f-116">Failed to extend lock expiration, lock expiration already passed or the lock owner was deleted.</span></span> <span data-ttu-id="5211f-117">Abandon de SqlWorkflowInstanceStore.</span><span class="sxs-lookup"><span data-stu-id="5211f-117">Aborting SqlWorkflowInstanceStore.</span></span>  
  
## <a name="details"></a><span data-ttu-id="5211f-118">Détails</span><span class="sxs-lookup"><span data-stu-id="5211f-118">Details</span></span>  
  
|<span data-ttu-id="5211f-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="5211f-119">Data Item Name</span></span>|<span data-ttu-id="5211f-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="5211f-120">Data Item Type</span></span>|<span data-ttu-id="5211f-121">Description</span><span class="sxs-lookup"><span data-stu-id="5211f-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="5211f-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="5211f-122">AppDomain</span></span>|<span data-ttu-id="5211f-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="5211f-123">xs:string</span></span>|<span data-ttu-id="5211f-124">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="5211f-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
