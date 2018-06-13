---
title: 1125 - InvokeMethodIsNotStatic
ms.date: 03/30/2017
ms.assetid: ea2b3827-63da-497b-b2c3-d5cebefe57a1
ms.openlocfilehash: 692c5e56dac0a69ab5705acd284f048391145641
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33511941"
---
# <a name="1125---invokemethodisnotstatic"></a><span data-ttu-id="0ebd5-102">1125 - InvokeMethodIsNotStatic</span><span class="sxs-lookup"><span data-stu-id="0ebd5-102">1125 - InvokeMethodIsNotStatic</span></span>
## <a name="properties"></a><span data-ttu-id="0ebd5-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ebd5-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0ebd5-104">ID</span><span class="sxs-lookup"><span data-stu-id="0ebd5-104">ID</span></span>|<span data-ttu-id="0ebd5-105">1125</span><span class="sxs-lookup"><span data-stu-id="0ebd5-105">1125</span></span>|  
|<span data-ttu-id="0ebd5-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="0ebd5-106">Keywords</span></span>|<span data-ttu-id="0ebd5-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="0ebd5-107">WFRuntime</span></span>|  
|<span data-ttu-id="0ebd5-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="0ebd5-108">Level</span></span>|<span data-ttu-id="0ebd5-109">Information</span><span class="sxs-lookup"><span data-stu-id="0ebd5-109">Information</span></span>|  
|<span data-ttu-id="0ebd5-110">Canal</span><span class="sxs-lookup"><span data-stu-id="0ebd5-110">Channel</span></span>|<span data-ttu-id="0ebd5-111">Microsoft-Windows-Application Server-Applications/Débogage</span><span class="sxs-lookup"><span data-stu-id="0ebd5-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0ebd5-112">Description</span><span class="sxs-lookup"><span data-stu-id="0ebd5-112">Description</span></span>  
 <span data-ttu-id="0ebd5-113">Pendant l'étape CacheMetadata, l'activité InvokeMethod indique que la méthode à appeler n'est pas statique.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-113">During CacheMetadata step, InvokeMethod activity indicates the method to be invoked is not static.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0ebd5-114">Message</span><span class="sxs-lookup"><span data-stu-id="0ebd5-114">Message</span></span>  
 <span data-ttu-id="0ebd5-115">InvokeMethod « %1 » - la méthode n'est pas statique.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-115">InvokeMethod '%1' - method is not Static.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0ebd5-116">Détails</span><span class="sxs-lookup"><span data-stu-id="0ebd5-116">Details</span></span>  
  
|<span data-ttu-id="0ebd5-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="0ebd5-117">Data Item Name</span></span>|<span data-ttu-id="0ebd5-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="0ebd5-118">Data Item Type</span></span>|<span data-ttu-id="0ebd5-119">Description</span><span class="sxs-lookup"><span data-stu-id="0ebd5-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0ebd5-120">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="0ebd5-120">InvokeMethod</span></span>|<span data-ttu-id="0ebd5-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="0ebd5-121">xs:string</span></span>|<span data-ttu-id="0ebd5-122">Nom complet de l'activité InvokeMethod.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-122">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="0ebd5-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="0ebd5-123">AppDomain</span></span>|<span data-ttu-id="0ebd5-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="0ebd5-124">xs:string</span></span>|<span data-ttu-id="0ebd5-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="0ebd5-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
