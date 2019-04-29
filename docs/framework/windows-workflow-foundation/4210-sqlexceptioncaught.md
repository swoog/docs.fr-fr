---
title: 4210 - SqlExceptionCaught
ms.date: 03/30/2017
ms.assetid: f0ce8af3-eb4c-48c8-b3d9-dd2f94b5574b
ms.openlocfilehash: 2493014e80e79ac2935c1bcc685147a74e48fb47
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61774255"
---
# <a name="4210---sqlexceptioncaught"></a><span data-ttu-id="27c32-102">4210 - SqlExceptionCaught</span><span class="sxs-lookup"><span data-stu-id="27c32-102">4210 - SqlExceptionCaught</span></span>
## <a name="properties"></a><span data-ttu-id="27c32-103">Properties</span><span class="sxs-lookup"><span data-stu-id="27c32-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="27c32-104">Id</span><span class="sxs-lookup"><span data-stu-id="27c32-104">ID</span></span>|<span data-ttu-id="27c32-105">4210</span><span class="sxs-lookup"><span data-stu-id="27c32-105">4210</span></span>|  
|<span data-ttu-id="27c32-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="27c32-106">Keywords</span></span>|<span data-ttu-id="27c32-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="27c32-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="27c32-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="27c32-108">Level</span></span>|<span data-ttu-id="27c32-109">Warning</span><span class="sxs-lookup"><span data-stu-id="27c32-109">Warning</span></span>|  
|<span data-ttu-id="27c32-110">Canal</span><span class="sxs-lookup"><span data-stu-id="27c32-110">Channel</span></span>|<span data-ttu-id="27c32-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="27c32-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="27c32-112">Description</span><span class="sxs-lookup"><span data-stu-id="27c32-112">Description</span></span>  
 <span data-ttu-id="27c32-113">Indique qu'une exception SQL a été interceptée.</span><span class="sxs-lookup"><span data-stu-id="27c32-113">Indicates a SQL exception was caught.</span></span>  
  
## <a name="message"></a><span data-ttu-id="27c32-114">Message</span><span class="sxs-lookup"><span data-stu-id="27c32-114">Message</span></span>  
 <span data-ttu-id="27c32-115">Message %2 avec numéro d'exception SQL %1 intercepté.</span><span class="sxs-lookup"><span data-stu-id="27c32-115">Caught SQL Exception number %1 message %2.</span></span>  
  
## <a name="details"></a><span data-ttu-id="27c32-116">Détails</span><span class="sxs-lookup"><span data-stu-id="27c32-116">Details</span></span>  
  
|<span data-ttu-id="27c32-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="27c32-117">Data Item Name</span></span>|<span data-ttu-id="27c32-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="27c32-118">Data Item Type</span></span>|<span data-ttu-id="27c32-119">Description</span><span class="sxs-lookup"><span data-stu-id="27c32-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="27c32-120">ErrorNumber</span><span class="sxs-lookup"><span data-stu-id="27c32-120">ErrorNumber</span></span>|<span data-ttu-id="27c32-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="27c32-121">xs:string</span></span>|<span data-ttu-id="27c32-122">Numéro d'erreur SQL.</span><span class="sxs-lookup"><span data-stu-id="27c32-122">The SQL error number.</span></span>|  
|<span data-ttu-id="27c32-123">ExceptionMessage</span><span class="sxs-lookup"><span data-stu-id="27c32-123">ExceptionMessage</span></span>|<span data-ttu-id="27c32-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="27c32-124">xs:string</span></span>|<span data-ttu-id="27c32-125">Message de l'exception SQL.</span><span class="sxs-lookup"><span data-stu-id="27c32-125">The message from the SQL exception.</span></span>|  
|<span data-ttu-id="27c32-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="27c32-126">AppDomain</span></span>|<span data-ttu-id="27c32-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="27c32-127">xs:string</span></span>|<span data-ttu-id="27c32-128">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="27c32-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
