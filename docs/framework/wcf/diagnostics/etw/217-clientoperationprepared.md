---
title: 217 - ClientOperationPrepared
ms.date: 03/30/2017
ms.assetid: ad207f04-b038-4f33-95e9-27a361df8ecd
ms.openlocfilehash: 5979cd8ffe0e05b61af01d2aa98c4a2c63fd432c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781761"
---
# <a name="217---clientoperationprepared"></a><span data-ttu-id="273bc-102">217 - ClientOperationPrepared</span><span class="sxs-lookup"><span data-stu-id="273bc-102">217 - ClientOperationPrepared</span></span>
## <a name="properties"></a><span data-ttu-id="273bc-103">Properties</span><span class="sxs-lookup"><span data-stu-id="273bc-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="273bc-104">Id</span><span class="sxs-lookup"><span data-stu-id="273bc-104">ID</span></span>|<span data-ttu-id="273bc-105">217</span><span class="sxs-lookup"><span data-stu-id="273bc-105">217</span></span>|  
|<span data-ttu-id="273bc-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="273bc-106">Keywords</span></span>|<span data-ttu-id="273bc-107">Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="273bc-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="273bc-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="273bc-108">Level</span></span>|<span data-ttu-id="273bc-109">Information</span><span class="sxs-lookup"><span data-stu-id="273bc-109">Information</span></span>|  
|<span data-ttu-id="273bc-110">Canal</span><span class="sxs-lookup"><span data-stu-id="273bc-110">Channel</span></span>|<span data-ttu-id="273bc-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="273bc-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="273bc-112">Description</span><span class="sxs-lookup"><span data-stu-id="273bc-112">Description</span></span>  
 <span data-ttu-id="273bc-113">Cet événement est émis par des clients juste avant qu'une opération soit envoyée au service.</span><span class="sxs-lookup"><span data-stu-id="273bc-113">This event is emitted by clients just before an operation is sent to the service.</span></span>  
  
## <a name="message"></a><span data-ttu-id="273bc-114">Message</span><span class="sxs-lookup"><span data-stu-id="273bc-114">Message</span></span>  
 <span data-ttu-id="273bc-115">Le client exécute l'action '%1' associée au contrat '%2'.</span><span class="sxs-lookup"><span data-stu-id="273bc-115">The Client is executing Action '%1' associated with the '%2' contract.</span></span> <span data-ttu-id="273bc-116">Le message sera envoyé à '%3'.</span><span class="sxs-lookup"><span data-stu-id="273bc-116">The message will be sent to '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="273bc-117">Détails</span><span class="sxs-lookup"><span data-stu-id="273bc-117">Details</span></span>  
  
|<span data-ttu-id="273bc-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="273bc-118">Data Item Name</span></span>|<span data-ttu-id="273bc-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="273bc-119">Data Item Type</span></span>|<span data-ttu-id="273bc-120">Description</span><span class="sxs-lookup"><span data-stu-id="273bc-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="273bc-121">Action</span><span class="sxs-lookup"><span data-stu-id="273bc-121">Action</span></span>|`xs:string`|<span data-ttu-id="273bc-122">En-tête d'action SOAP du message sortant.</span><span class="sxs-lookup"><span data-stu-id="273bc-122">The SOAP action header of the outgoing message.</span></span>|  
|<span data-ttu-id="273bc-123">Nom de contrat</span><span class="sxs-lookup"><span data-stu-id="273bc-123">Contract Name</span></span>|`xs:string`|<span data-ttu-id="273bc-124">Nom du contrat.</span><span class="sxs-lookup"><span data-stu-id="273bc-124">The name of the contract.</span></span> <span data-ttu-id="273bc-125">Exemple : ICalculator.</span><span class="sxs-lookup"><span data-stu-id="273bc-125">Example: ICalculator.</span></span>|  
|<span data-ttu-id="273bc-126">Destination</span><span class="sxs-lookup"><span data-stu-id="273bc-126">Destination</span></span>|`xs:string`|<span data-ttu-id="273bc-127">Adresse du point de terminaison de service auquel le message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="273bc-127">The address of the service endpoint that the message is sent to.</span></span>|  
|<span data-ttu-id="273bc-128">HostReference</span><span class="sxs-lookup"><span data-stu-id="273bc-128">HostReference</span></span>|`xs:string`|<span data-ttu-id="273bc-129">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="273bc-129">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="273bc-130">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="273bc-130">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="273bc-131">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="273bc-131">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="273bc-132">AppDomain</span><span class="sxs-lookup"><span data-stu-id="273bc-132">AppDomain</span></span>|`xs:string`|<span data-ttu-id="273bc-133">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="273bc-133">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
