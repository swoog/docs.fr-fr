---
title: 3502 - InferredOperationDescription
ms.date: 03/30/2017
ms.assetid: 6aebb614-3c72-4537-ba11-3cc7200ef1f1
ms.openlocfilehash: 752cd73066c3c15ecbb36c40c417ee84b3fcf184
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61756089"
---
# <a name="3502---inferredoperationdescription"></a><span data-ttu-id="d2779-102">3502 - InferredOperationDescription</span><span class="sxs-lookup"><span data-stu-id="d2779-102">3502 - InferredOperationDescription</span></span>
## <a name="properties"></a><span data-ttu-id="d2779-103">Properties</span><span class="sxs-lookup"><span data-stu-id="d2779-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d2779-104">Id</span><span class="sxs-lookup"><span data-stu-id="d2779-104">ID</span></span>|<span data-ttu-id="d2779-105">3502</span><span class="sxs-lookup"><span data-stu-id="d2779-105">3502</span></span>|  
|<span data-ttu-id="d2779-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d2779-106">Keywords</span></span>|<span data-ttu-id="d2779-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="d2779-107">WFServices</span></span>|  
|<span data-ttu-id="d2779-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="d2779-108">Level</span></span>|<span data-ttu-id="d2779-109">Information</span><span class="sxs-lookup"><span data-stu-id="d2779-109">Information</span></span>|  
|<span data-ttu-id="d2779-110">Canal</span><span class="sxs-lookup"><span data-stu-id="d2779-110">Channel</span></span>|<span data-ttu-id="d2779-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="d2779-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d2779-112">Description</span><span class="sxs-lookup"><span data-stu-id="d2779-112">Description</span></span>  
 <span data-ttu-id="d2779-113">Indique qu'un OperationDescription a été déduit de WorkflowService.</span><span class="sxs-lookup"><span data-stu-id="d2779-113">Indicates an OperationDescription has been inferred from WorkflowService.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d2779-114">Message</span><span class="sxs-lookup"><span data-stu-id="d2779-114">Message</span></span>  
 <span data-ttu-id="d2779-115">OperationDescription avec Name='%1' dans le contrat « %2 » a été déduit de WorkflowService.</span><span class="sxs-lookup"><span data-stu-id="d2779-115">OperationDescription with Name='%1' in contract '%2' has been inferred from WorkflowService.</span></span> <span data-ttu-id="d2779-116">IsOneWay=%3.</span><span class="sxs-lookup"><span data-stu-id="d2779-116">IsOneWay=%3.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d2779-117">Détails</span><span class="sxs-lookup"><span data-stu-id="d2779-117">Details</span></span>  
  
|<span data-ttu-id="d2779-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="d2779-118">Data Item Name</span></span>|<span data-ttu-id="d2779-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="d2779-119">Data Item Type</span></span>|<span data-ttu-id="d2779-120">Description</span><span class="sxs-lookup"><span data-stu-id="d2779-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d2779-121">OperationName</span><span class="sxs-lookup"><span data-stu-id="d2779-121">OperationName</span></span>|<span data-ttu-id="d2779-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="d2779-122">xs:string</span></span>|<span data-ttu-id="d2779-123">Nom de l'opération.</span><span class="sxs-lookup"><span data-stu-id="d2779-123">The name of the operation.</span></span>|  
|<span data-ttu-id="d2779-124">ContractName</span><span class="sxs-lookup"><span data-stu-id="d2779-124">ContractName</span></span>|<span data-ttu-id="d2779-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="d2779-125">xs:string</span></span>|<span data-ttu-id="d2779-126">Nom du contrat.</span><span class="sxs-lookup"><span data-stu-id="d2779-126">The name of the contract.</span></span>|  
|<span data-ttu-id="d2779-127">IsOneWay</span><span class="sxs-lookup"><span data-stu-id="d2779-127">IsOneWay</span></span>|<span data-ttu-id="d2779-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="d2779-128">xs:string</span></span>|<span data-ttu-id="d2779-129">True ou False indiquant si le contrat est unidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="d2779-129">True or False indicating if the contract is one-way.</span></span>|  
|<span data-ttu-id="d2779-130">AppDomain</span><span class="sxs-lookup"><span data-stu-id="d2779-130">AppDomain</span></span>|<span data-ttu-id="d2779-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="d2779-131">xs:string</span></span>|<span data-ttu-id="d2779-132">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="d2779-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
