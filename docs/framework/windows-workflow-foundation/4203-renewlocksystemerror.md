---
title: 4203 - RenewLockSystemError
ms.date: 03/30/2017
ms.assetid: 6ec9ec6f-4ae2-45cf-b99b-02cdb9dc9ec9
ms.openlocfilehash: 984f7ddae8797cba17753a618d0820d21bde5eef
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774346"
---
# <a name="4203---renewlocksystemerror"></a><span data-ttu-id="462f7-102">4203 - RenewLockSystemError</span><span class="sxs-lookup"><span data-stu-id="462f7-102">4203 - RenewLockSystemError</span></span>
## <a name="properties"></a><span data-ttu-id="462f7-103">Properties</span><span class="sxs-lookup"><span data-stu-id="462f7-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="462f7-104">Id</span><span class="sxs-lookup"><span data-stu-id="462f7-104">ID</span></span>|<span data-ttu-id="462f7-105">4203</span><span class="sxs-lookup"><span data-stu-id="462f7-105">4203</span></span>|  
|<span data-ttu-id="462f7-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="462f7-106">Keywords</span></span>|<span data-ttu-id="462f7-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="462f7-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="462f7-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="462f7-108">Level</span></span>|<span data-ttu-id="462f7-109">Error</span><span class="sxs-lookup"><span data-stu-id="462f7-109">Error</span></span>|  
|<span data-ttu-id="462f7-110">Canal</span><span class="sxs-lookup"><span data-stu-id="462f7-110">Channel</span></span>|<span data-ttu-id="462f7-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="462f7-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="462f7-112">Description</span><span class="sxs-lookup"><span data-stu-id="462f7-112">Description</span></span>  
 <span data-ttu-id="462f7-113">Indique que le fournisseur SQL n'a pas pu étendre l'expiration du verrou, car l'expiration du verrou a déjà été passée ou le propriétaire de verrou a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="462f7-113">Indicates SQL provider has failed to extend lock expiration due to either lock expiration already passed or the lock owner was deleted.</span></span> <span data-ttu-id="462f7-114">Le SqlWorkflowInstanceStore sera annulé.</span><span class="sxs-lookup"><span data-stu-id="462f7-114">The SqlWorkflowInstanceStore will be aborted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="462f7-115">Message</span><span class="sxs-lookup"><span data-stu-id="462f7-115">Message</span></span>  
 <span data-ttu-id="462f7-116">Échec de l'extension de l'expiration du verrou ; l'expiration du verrou a déjà été passée ou le propriétaire de verrou a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="462f7-116">Failed to extend lock expiration, lock expiration already passed or the lock owner was deleted.</span></span> <span data-ttu-id="462f7-117">Abandon de SqlWorkflowInstanceStore.</span><span class="sxs-lookup"><span data-stu-id="462f7-117">Aborting SqlWorkflowInstanceStore.</span></span>  
  
## <a name="details"></a><span data-ttu-id="462f7-118">Détails</span><span class="sxs-lookup"><span data-stu-id="462f7-118">Details</span></span>  
  
|<span data-ttu-id="462f7-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="462f7-119">Data Item Name</span></span>|<span data-ttu-id="462f7-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="462f7-120">Data Item Type</span></span>|<span data-ttu-id="462f7-121">Description</span><span class="sxs-lookup"><span data-stu-id="462f7-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="462f7-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="462f7-122">AppDomain</span></span>|<span data-ttu-id="462f7-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="462f7-123">xs:string</span></span>|<span data-ttu-id="462f7-124">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="462f7-124">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
