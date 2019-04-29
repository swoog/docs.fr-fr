---
title: 215 - MessageReceivedByTransport
ms.date: 03/30/2017
ms.assetid: bb32aa60-5207-4711-9f08-110e8ac327e5
ms.openlocfilehash: a8ba90b88ef8dbe3c8651bc565da61aae16a0a4a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781834"
---
# <a name="215---messagereceivedbytransport"></a><span data-ttu-id="a337d-102">215 - MessageReceivedByTransport</span><span class="sxs-lookup"><span data-stu-id="a337d-102">215 - MessageReceivedByTransport</span></span>
## <a name="properties"></a><span data-ttu-id="a337d-103">Properties</span><span class="sxs-lookup"><span data-stu-id="a337d-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a337d-104">Id</span><span class="sxs-lookup"><span data-stu-id="a337d-104">ID</span></span>|<span data-ttu-id="a337d-105">215</span><span class="sxs-lookup"><span data-stu-id="a337d-105">215</span></span>|  
|<span data-ttu-id="a337d-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a337d-106">Keywords</span></span>|<span data-ttu-id="a337d-107">Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="a337d-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="a337d-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="a337d-108">Level</span></span>|<span data-ttu-id="a337d-109">Information</span><span class="sxs-lookup"><span data-stu-id="a337d-109">Information</span></span>|  
|<span data-ttu-id="a337d-110">Canal</span><span class="sxs-lookup"><span data-stu-id="a337d-110">Channel</span></span>|<span data-ttu-id="a337d-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="a337d-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="a337d-112">Description</span><span class="sxs-lookup"><span data-stu-id="a337d-112">Description</span></span>  
 <span data-ttu-id="a337d-113">Cet événement se produit lorsqu'un transport basé sur TCP reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="a337d-113">This event occurs when a TCP-based transport receives a message.</span></span> <span data-ttu-id="a337d-114">Notez qu'au niveau du transport, plusieurs messages peuvent être échangés entre clients et services pour une seule opération.</span><span class="sxs-lookup"><span data-stu-id="a337d-114">Note that at the transport level, multiple messages can be exchanged between clients and services for a single operation.</span></span> <span data-ttu-id="a337d-115">Cela peut être dû au comportement d'infrastructure, la sécurité étant un bon exemple.</span><span class="sxs-lookup"><span data-stu-id="a337d-115">This can be due to infrastructure behavior, security is a good example.</span></span> <span data-ttu-id="a337d-116">Par conséquent, le nombre d'événements `MessageReceivedByTransport` émis varie en fonction de la liaison de votre service et de sa configuration.</span><span class="sxs-lookup"><span data-stu-id="a337d-116">Therefore, the number of `MessageReceivedByTransport` events that are emitted vary based on your service's binding and its configuration.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a337d-117">Cet événement n'est pas émis pour les transports unidirectionnels.</span><span class="sxs-lookup"><span data-stu-id="a337d-117">This event is not emitted for one-way transports.</span></span>  
  
## <a name="message"></a><span data-ttu-id="a337d-118">Message</span><span class="sxs-lookup"><span data-stu-id="a337d-118">Message</span></span>  
 <span data-ttu-id="a337d-119">Le transport a reçu un message de '%1'.</span><span class="sxs-lookup"><span data-stu-id="a337d-119">The transport received a message from '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="a337d-120">Détails</span><span class="sxs-lookup"><span data-stu-id="a337d-120">Details</span></span>  
  
|<span data-ttu-id="a337d-121">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a337d-121">Data Item Name</span></span>|<span data-ttu-id="a337d-122">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a337d-122">Data Item Type</span></span>|<span data-ttu-id="a337d-123">Description</span><span class="sxs-lookup"><span data-stu-id="a337d-123">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="a337d-124">Adresse d'écoute</span><span class="sxs-lookup"><span data-stu-id="a337d-124">Listen Address</span></span>|`xs:string`|<span data-ttu-id="a337d-125">Adresse qui a reçu le message.</span><span class="sxs-lookup"><span data-stu-id="a337d-125">The address that received the message.</span></span>|  
|<span data-ttu-id="a337d-126">HostReference</span><span class="sxs-lookup"><span data-stu-id="a337d-126">HostReference</span></span>|`xs:string`|<span data-ttu-id="a337d-127">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="a337d-127">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="a337d-128">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="a337d-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="a337d-129">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="a337d-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="a337d-130">AppDomain</span><span class="sxs-lookup"><span data-stu-id="a337d-130">AppDomain</span></span>|`xs:string`|<span data-ttu-id="a337d-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="a337d-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
