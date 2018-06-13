---
title: 216 - MessageSentByTransport
ms.date: 03/30/2017
ms.assetid: 150c3167-4154-4225-8d94-57cc94341233
ms.openlocfilehash: fa21568e4c8c38eefe359c417d47ec0a9d30a7c4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33458681"
---
# <a name="216---messagesentbytransport"></a><span data-ttu-id="f51c1-102">216 - MessageSentByTransport</span><span class="sxs-lookup"><span data-stu-id="f51c1-102">216 - MessageSentByTransport</span></span>
## <a name="properties"></a><span data-ttu-id="f51c1-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f51c1-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f51c1-104">Id</span><span class="sxs-lookup"><span data-stu-id="f51c1-104">ID</span></span>|<span data-ttu-id="f51c1-105">216</span><span class="sxs-lookup"><span data-stu-id="f51c1-105">216</span></span>|  
|<span data-ttu-id="f51c1-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f51c1-106">Keywords</span></span>|<span data-ttu-id="f51c1-107">Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f51c1-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="f51c1-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="f51c1-108">Level</span></span>|<span data-ttu-id="f51c1-109">Information</span><span class="sxs-lookup"><span data-stu-id="f51c1-109">Information</span></span>|  
|<span data-ttu-id="f51c1-110">Canal</span><span class="sxs-lookup"><span data-stu-id="f51c1-110">Channel</span></span>|<span data-ttu-id="f51c1-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="f51c1-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f51c1-112">Description</span><span class="sxs-lookup"><span data-stu-id="f51c1-112">Description</span></span>  
 <span data-ttu-id="f51c1-113">Cet événement se produit lorsqu'un transport basé sur TCP envoie un message.</span><span class="sxs-lookup"><span data-stu-id="f51c1-113">This event occurs when a TCP-based transport sends a message.</span></span> <span data-ttu-id="f51c1-114">Notez qu'au niveau du transport, plusieurs messages peuvent être échangés entre clients et services pour une seule opération.</span><span class="sxs-lookup"><span data-stu-id="f51c1-114">Note that at the transport level multiple messages can be exchanged between clients and services for a single operation.</span></span> <span data-ttu-id="f51c1-115">Cela peut être dû au comportement d'infrastructure, la sécurité étant un bon exemple.</span><span class="sxs-lookup"><span data-stu-id="f51c1-115">This may be due to infrastructure behavior, security being a good example.</span></span> <span data-ttu-id="f51c1-116">Par conséquent, le nombre de **MessageSentByTransport** les événements qui sont émis varient en fonction de la liaison de votre service et de sa configuration.</span><span class="sxs-lookup"><span data-stu-id="f51c1-116">Therefore, the number of **MessageSentByTransport** events that are emitted vary based on your service's binding and its configuration.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f51c1-117">Message</span><span class="sxs-lookup"><span data-stu-id="f51c1-117">Message</span></span>  
 <span data-ttu-id="f51c1-118">Le transport a envoyé un message à '%1.'</span><span class="sxs-lookup"><span data-stu-id="f51c1-118">The transport sent a message to '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f51c1-119">Détails</span><span class="sxs-lookup"><span data-stu-id="f51c1-119">Details</span></span>  
  
|<span data-ttu-id="f51c1-120">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="f51c1-120">Data Item Name</span></span>|<span data-ttu-id="f51c1-121">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="f51c1-121">Data Item Type</span></span>|<span data-ttu-id="f51c1-122">Description</span><span class="sxs-lookup"><span data-stu-id="f51c1-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f51c1-123">DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f51c1-123">DestinationAddress</span></span>|`xs:string`|<span data-ttu-id="f51c1-124">Adresse à laquelle le message de demande a été envoyé.</span><span class="sxs-lookup"><span data-stu-id="f51c1-124">The address that the request message was sent to.</span></span>|  
|<span data-ttu-id="f51c1-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="f51c1-125">HostReference</span></span>|<span data-ttu-id="f51c1-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="f51c1-126">xs:string</span></span>|<span data-ttu-id="f51c1-127">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="f51c1-127">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="f51c1-128">Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="f51c1-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="f51c1-129">Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="f51c1-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="f51c1-130">AppDomain</span><span class="sxs-lookup"><span data-stu-id="f51c1-130">AppDomain</span></span>|`xs:string`|<span data-ttu-id="f51c1-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="f51c1-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
