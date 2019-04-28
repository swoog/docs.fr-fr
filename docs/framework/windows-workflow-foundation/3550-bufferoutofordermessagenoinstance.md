---
title: 3550 - BufferOutOfOrderMessageNoInstance
ms.date: 03/30/2017
ms.assetid: 1299d294-99b8-430e-98b1-55f5f17002f3
ms.openlocfilehash: 1af943e23aa643c6614b946175c0b1854a7ceb62
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61755582"
---
# <a name="3550---bufferoutofordermessagenoinstance"></a><span data-ttu-id="8d8b4-102">3550 - BufferOutOfOrderMessageNoInstance</span><span class="sxs-lookup"><span data-stu-id="8d8b4-102">3550 - BufferOutOfOrderMessageNoInstance</span></span>
## <a name="properties"></a><span data-ttu-id="8d8b4-103">Properties</span><span class="sxs-lookup"><span data-stu-id="8d8b4-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="8d8b4-104">Id</span><span class="sxs-lookup"><span data-stu-id="8d8b4-104">ID</span></span>|<span data-ttu-id="8d8b4-105">3550</span><span class="sxs-lookup"><span data-stu-id="8d8b4-105">3550</span></span>|  
|<span data-ttu-id="8d8b4-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="8d8b4-106">Keywords</span></span>|<span data-ttu-id="8d8b4-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="8d8b4-107">WFServices</span></span>|  
|<span data-ttu-id="8d8b4-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="8d8b4-108">Level</span></span>|<span data-ttu-id="8d8b4-109">Information</span><span class="sxs-lookup"><span data-stu-id="8d8b4-109">Information</span></span>|  
|<span data-ttu-id="8d8b4-110">Canal</span><span class="sxs-lookup"><span data-stu-id="8d8b4-110">Channel</span></span>|<span data-ttu-id="8d8b4-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="8d8b4-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="8d8b4-112">Description</span><span class="sxs-lookup"><span data-stu-id="8d8b4-112">Description</span></span>  
 <span data-ttu-id="8d8b4-113">Indique qu'une réception mise en mémoire tampon a échoué.</span><span class="sxs-lookup"><span data-stu-id="8d8b4-113">Indicates a buffered receive has failed.</span></span> <span data-ttu-id="8d8b4-114">Une autre tentative d'opération sera faite lorsque l'instance de service sera prête à traiter cette opération.</span><span class="sxs-lookup"><span data-stu-id="8d8b4-114">The operation will be attempted again when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="8d8b4-115">Message</span><span class="sxs-lookup"><span data-stu-id="8d8b4-115">Message</span></span>  
 <span data-ttu-id="8d8b4-116">Impossible d'effectuer l'opération « %1 » actuellement.</span><span class="sxs-lookup"><span data-stu-id="8d8b4-116">Operation '%1' cannot be performed at this time.</span></span> <span data-ttu-id="8d8b4-117">Une autre tentative sera faite lorsque l'instance de service sera prête à traiter cette opération.</span><span class="sxs-lookup"><span data-stu-id="8d8b4-117">Another attempt will be made when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="8d8b4-118">Détails</span><span class="sxs-lookup"><span data-stu-id="8d8b4-118">Details</span></span>  
  
|<span data-ttu-id="8d8b4-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="8d8b4-119">Data Item Name</span></span>|<span data-ttu-id="8d8b4-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="8d8b4-120">Data Item Type</span></span>|<span data-ttu-id="8d8b4-121">Description</span><span class="sxs-lookup"><span data-stu-id="8d8b4-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="8d8b4-122">OperationName</span><span class="sxs-lookup"><span data-stu-id="8d8b4-122">OperationName</span></span>|<span data-ttu-id="8d8b4-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="8d8b4-123">xs:string</span></span>|<span data-ttu-id="8d8b4-124">Nom de l'opération.</span><span class="sxs-lookup"><span data-stu-id="8d8b4-124">The name of the operation.</span></span>|  
|<span data-ttu-id="8d8b4-125">AppDomain</span><span class="sxs-lookup"><span data-stu-id="8d8b4-125">AppDomain</span></span>|<span data-ttu-id="8d8b4-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="8d8b4-126">xs:string</span></span>|<span data-ttu-id="8d8b4-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="8d8b4-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
