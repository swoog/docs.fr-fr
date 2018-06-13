---
title: 220 - MessageSentToTransport
ms.date: 03/30/2017
ms.assetid: aef4e781-240b-45bc-bff8-400053037e71
ms.openlocfilehash: 92ec664aead15470fbed576bf157d64d984ddebf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33460432"
---
# <a name="220---messagesenttotransport"></a><span data-ttu-id="4abd2-102">220 - MessageSentToTransport</span><span class="sxs-lookup"><span data-stu-id="4abd2-102">220 - MessageSentToTransport</span></span>
## <a name="properties"></a><span data-ttu-id="4abd2-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4abd2-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="4abd2-104">Id</span><span class="sxs-lookup"><span data-stu-id="4abd2-104">Id</span></span>|<span data-ttu-id="4abd2-105">220</span><span class="sxs-lookup"><span data-stu-id="4abd2-105">220</span></span>|  
|<span data-ttu-id="4abd2-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="4abd2-106">Keywords</span></span>|<span data-ttu-id="4abd2-107">EndToEndMonitoring, Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="4abd2-107">EndToEndMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="4abd2-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="4abd2-108">Level</span></span>|<span data-ttu-id="4abd2-109">Information</span><span class="sxs-lookup"><span data-stu-id="4abd2-109">Information</span></span>|  
|<span data-ttu-id="4abd2-110">Canal</span><span class="sxs-lookup"><span data-stu-id="4abd2-110">Channel</span></span>|<span data-ttu-id="4abd2-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="4abd2-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="4abd2-112">Description</span><span class="sxs-lookup"><span data-stu-id="4abd2-112">Description</span></span>  
 <span data-ttu-id="4abd2-113">Cet événement est émis lorsque le modèle de service envoie un message au transport.</span><span class="sxs-lookup"><span data-stu-id="4abd2-113">This event is emitted when the Service Model sends a message to the transport.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4abd2-114">Il n'est pas émis pour les transports unidirectionnels.</span><span class="sxs-lookup"><span data-stu-id="4abd2-114">This event will not be emitted for one-way transports.</span></span>  
  
## <a name="message"></a><span data-ttu-id="4abd2-115">Message</span><span class="sxs-lookup"><span data-stu-id="4abd2-115">Message</span></span>  
 <span data-ttu-id="4abd2-116">Le répartiteur a envoyé un message au transport.</span><span class="sxs-lookup"><span data-stu-id="4abd2-116">The Dispatcher sent a message to the transport.</span></span> <span data-ttu-id="4abd2-117">ID de corrélation == '%1.'</span><span class="sxs-lookup"><span data-stu-id="4abd2-117">Correlation ID == '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="4abd2-118">Détails</span><span class="sxs-lookup"><span data-stu-id="4abd2-118">Details</span></span>  
  
|<span data-ttu-id="4abd2-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="4abd2-119">Data Item Name</span></span>|<span data-ttu-id="4abd2-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="4abd2-120">Data Item Type</span></span>|<span data-ttu-id="4abd2-121">Description</span><span class="sxs-lookup"><span data-stu-id="4abd2-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="4abd2-122">ID de corrélation</span><span class="sxs-lookup"><span data-stu-id="4abd2-122">Correlation ID</span></span>|`xs:GUID`|<span data-ttu-id="4abd2-123">ID d'activité utilisé pour mettre en corrélation un événement `MessageSentToTransport` provenant d'un service ou d'un client avec son événement `MessageReceivedFromTransport` correspondant à l'autre bout.</span><span class="sxs-lookup"><span data-stu-id="4abd2-123">The activity ID used to correlate a `MessageSentToTransport` event from a service or client to its corresponding `MessageReceivedFromTransport` on the other end.</span></span>|  
|<span data-ttu-id="4abd2-124">HostReference</span><span class="sxs-lookup"><span data-stu-id="4abd2-124">HostReference</span></span>|`xs:string`|<span data-ttu-id="4abd2-125">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="4abd2-125">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="4abd2-126">Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="4abd2-126">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="4abd2-127">Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="4abd2-127">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="4abd2-128">AppDomain</span><span class="sxs-lookup"><span data-stu-id="4abd2-128">AppDomain</span></span>|`xs:string`|<span data-ttu-id="4abd2-129">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="4abd2-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
