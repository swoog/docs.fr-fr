---
title: 4209 - TimeoutOpeningSqlConnection
ms.date: 03/30/2017
ms.assetid: f0e56518-9758-41dc-a760-50d1a10fba6e
ms.openlocfilehash: d61d710959f99dbc8a91441766a690eb7e9a365c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774268"
---
# <a name="4209---timeoutopeningsqlconnection"></a><span data-ttu-id="518d2-102">4209 - TimeoutOpeningSqlConnection</span><span class="sxs-lookup"><span data-stu-id="518d2-102">4209 - TimeoutOpeningSqlConnection</span></span>
## <a name="properties"></a><span data-ttu-id="518d2-103">Properties</span><span class="sxs-lookup"><span data-stu-id="518d2-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="518d2-104">Id</span><span class="sxs-lookup"><span data-stu-id="518d2-104">ID</span></span>|<span data-ttu-id="518d2-105">4209</span><span class="sxs-lookup"><span data-stu-id="518d2-105">4209</span></span>|  
|<span data-ttu-id="518d2-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="518d2-106">Keywords</span></span>|<span data-ttu-id="518d2-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="518d2-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="518d2-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="518d2-108">Level</span></span>|<span data-ttu-id="518d2-109">Error</span><span class="sxs-lookup"><span data-stu-id="518d2-109">Error</span></span>|  
|<span data-ttu-id="518d2-110">Canal</span><span class="sxs-lookup"><span data-stu-id="518d2-110">Channel</span></span>|<span data-ttu-id="518d2-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="518d2-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="518d2-112">Description</span><span class="sxs-lookup"><span data-stu-id="518d2-112">Description</span></span>  
 <span data-ttu-id="518d2-113">Indique qu'une expiration de délai d'attente s'est produite lors de la tentative d'ouverture d'une connexion SQL.</span><span class="sxs-lookup"><span data-stu-id="518d2-113">Indicates a timeout was encountered when trying to open a SQL connection.</span></span>  
  
## <a name="message"></a><span data-ttu-id="518d2-114">Message</span><span class="sxs-lookup"><span data-stu-id="518d2-114">Message</span></span>  
 <span data-ttu-id="518d2-115">Expiration du délai d'attente lors de la tentative d'ouverture d'une connexion SQL.</span><span class="sxs-lookup"><span data-stu-id="518d2-115">Timeout trying to open a SQL connection.</span></span> <span data-ttu-id="518d2-116">L'opération ne s'est pas terminée dans le délai imparti de %1.</span><span class="sxs-lookup"><span data-stu-id="518d2-116">The operation did not complete within the allotted timeout of %1.</span></span> <span data-ttu-id="518d2-117">Le temps alloué à cette opération peut avoir été une partie d'un délai d'expiration plus long.</span><span class="sxs-lookup"><span data-stu-id="518d2-117">The time allotted to this operation may have been a portion of a longer timeout.</span></span>  
  
## <a name="details"></a><span data-ttu-id="518d2-118">Détails</span><span class="sxs-lookup"><span data-stu-id="518d2-118">Details</span></span>  
  
|<span data-ttu-id="518d2-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="518d2-119">Data Item Name</span></span>|<span data-ttu-id="518d2-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="518d2-120">Data Item Type</span></span>|<span data-ttu-id="518d2-121">Description</span><span class="sxs-lookup"><span data-stu-id="518d2-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="518d2-122">Délai</span><span class="sxs-lookup"><span data-stu-id="518d2-122">Timeout</span></span>|<span data-ttu-id="518d2-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="518d2-123">xs:string</span></span>|<span data-ttu-id="518d2-124">Valeur de délai d'attente pour ouvrir la connexion SQL.</span><span class="sxs-lookup"><span data-stu-id="518d2-124">The timeout value for opening the SQL connection.</span></span>|  
|<span data-ttu-id="518d2-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="518d2-125">AppDomain</span></span>|<span data-ttu-id="518d2-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="518d2-126">xs:string</span></span>|<span data-ttu-id="518d2-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="518d2-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
