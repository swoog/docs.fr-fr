---
title: 3503 - DuplicateCorrelationQuery
ms.date: 03/30/2017
ms.assetid: b857f8e6-ce4d-4da4-bc9d-6cd63fa558a4
ms.openlocfilehash: 37a689b30b0bcab9124472deb98627afbe30dfee
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33511398"
---
# <a name="3503---duplicatecorrelationquery"></a><span data-ttu-id="cc809-102">3503 - DuplicateCorrelationQuery</span><span class="sxs-lookup"><span data-stu-id="cc809-102">3503 - DuplicateCorrelationQuery</span></span>
## <a name="properties"></a><span data-ttu-id="cc809-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cc809-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="cc809-104">ID</span><span class="sxs-lookup"><span data-stu-id="cc809-104">ID</span></span>|<span data-ttu-id="cc809-105">3503</span><span class="sxs-lookup"><span data-stu-id="cc809-105">3503</span></span>|  
|<span data-ttu-id="cc809-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="cc809-106">Keywords</span></span>|<span data-ttu-id="cc809-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="cc809-107">WFServices</span></span>|  
|<span data-ttu-id="cc809-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="cc809-108">Level</span></span>|<span data-ttu-id="cc809-109">Avertissement</span><span class="sxs-lookup"><span data-stu-id="cc809-109">Warning</span></span>|  
|<span data-ttu-id="cc809-110">Canal</span><span class="sxs-lookup"><span data-stu-id="cc809-110">Channel</span></span>|<span data-ttu-id="cc809-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="cc809-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="cc809-112">Description</span><span class="sxs-lookup"><span data-stu-id="cc809-112">Description</span></span>  
 <span data-ttu-id="cc809-113">Indique qu'un CorrelationQuery en double a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="cc809-113">Indicates a duplicate CorrelationQuery was found.</span></span> <span data-ttu-id="cc809-114">Cette requête en double ne sera pas utilisée lors du calcul de la corrélation.</span><span class="sxs-lookup"><span data-stu-id="cc809-114">The duplicate query will not be used when calculating correlation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="cc809-115">Message</span><span class="sxs-lookup"><span data-stu-id="cc809-115">Message</span></span>  
 <span data-ttu-id="cc809-116">CorrelationQuery en double trouvé avec Where='%1'.</span><span class="sxs-lookup"><span data-stu-id="cc809-116">A duplicate CorrelationQuery was found with Where='%1'.</span></span> <span data-ttu-id="cc809-117">Cette requête en double ne sera pas utilisée lors du calcul de la corrélation.</span><span class="sxs-lookup"><span data-stu-id="cc809-117">This duplicate query will not be used when calculating correlation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="cc809-118">Détails</span><span class="sxs-lookup"><span data-stu-id="cc809-118">Details</span></span>  
  
|<span data-ttu-id="cc809-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="cc809-119">Data Item Name</span></span>|<span data-ttu-id="cc809-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="cc809-120">Data Item Type</span></span>|<span data-ttu-id="cc809-121">Description</span><span class="sxs-lookup"><span data-stu-id="cc809-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="cc809-122">Où</span><span class="sxs-lookup"><span data-stu-id="cc809-122">Where</span></span>|<span data-ttu-id="cc809-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc809-123">xs:string</span></span>|<span data-ttu-id="cc809-124">Partie Where de la requête de corrélation.</span><span class="sxs-lookup"><span data-stu-id="cc809-124">The Where portion of the correlation query.</span></span>|  
|<span data-ttu-id="cc809-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="cc809-125">AppDomain</span></span>|<span data-ttu-id="cc809-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="cc809-126">xs:string</span></span>|<span data-ttu-id="cc809-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="cc809-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
