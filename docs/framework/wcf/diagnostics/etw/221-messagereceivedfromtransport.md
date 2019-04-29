---
title: 221 - MessageReceivedFromTransport
ms.date: 03/30/2017
ms.assetid: 4995f0d5-c182-4d97-981f-6951da6df1fb
ms.openlocfilehash: 98dbf2728242fa73b3e54b7cf32f9e227e5251b2
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781717"
---
# <a name="221---messagereceivedfromtransport"></a><span data-ttu-id="abdf9-102">221 - MessageReceivedFromTransport</span><span class="sxs-lookup"><span data-stu-id="abdf9-102">221 - MessageReceivedFromTransport</span></span>
## <a name="properties"></a><span data-ttu-id="abdf9-103">Properties</span><span class="sxs-lookup"><span data-stu-id="abdf9-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="abdf9-104">Id</span><span class="sxs-lookup"><span data-stu-id="abdf9-104">ID</span></span>|<span data-ttu-id="abdf9-105">221</span><span class="sxs-lookup"><span data-stu-id="abdf9-105">221</span></span>|  
|<span data-ttu-id="abdf9-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="abdf9-106">Keywords</span></span>|<span data-ttu-id="abdf9-107">EndToEndMonitoring, Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="abdf9-107">EndToEndMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="abdf9-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="abdf9-108">Level</span></span>|<span data-ttu-id="abdf9-109">Information</span><span class="sxs-lookup"><span data-stu-id="abdf9-109">Information</span></span>|  
|<span data-ttu-id="abdf9-110">Canal</span><span class="sxs-lookup"><span data-stu-id="abdf9-110">Channel</span></span>|<span data-ttu-id="abdf9-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="abdf9-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="abdf9-112">Description</span><span class="sxs-lookup"><span data-stu-id="abdf9-112">Description</span></span>  
 <span data-ttu-id="abdf9-113">Cet événement est émis lorsque le modèle de service reçoit un message du transport.</span><span class="sxs-lookup"><span data-stu-id="abdf9-113">This event is emitted when the Service Model receives a message from the transport.</span></span>  
  
## <a name="message"></a><span data-ttu-id="abdf9-114">Message</span><span class="sxs-lookup"><span data-stu-id="abdf9-114">Message</span></span>  
 <span data-ttu-id="abdf9-115">Le répartiteur a reçu un message du transport.</span><span class="sxs-lookup"><span data-stu-id="abdf9-115">The Dispatcher received a message from the transport.</span></span> <span data-ttu-id="abdf9-116">ID de corrélation == '%1.'</span><span class="sxs-lookup"><span data-stu-id="abdf9-116">Correlation ID == '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="abdf9-117">Détails</span><span class="sxs-lookup"><span data-stu-id="abdf9-117">Details</span></span>  
  
|<span data-ttu-id="abdf9-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="abdf9-118">Data Item Name</span></span>|<span data-ttu-id="abdf9-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="abdf9-119">Data Item Type</span></span>|<span data-ttu-id="abdf9-120">Description</span><span class="sxs-lookup"><span data-stu-id="abdf9-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="abdf9-121">ID de corrélation</span><span class="sxs-lookup"><span data-stu-id="abdf9-121">Correlation ID</span></span>|`xs:GUID`|<span data-ttu-id="abdf9-122">ID d'activité utilisé pour mettre en corrélation un événement `MessageSentToTransport` provenant d'un service ou d'un client avec son événement `MessageReceivedFromTransport` correspondant à l'autre bout.</span><span class="sxs-lookup"><span data-stu-id="abdf9-122">The activity ID used to correlate a `MessageSentToTransport` event from a service or client to its corresponding `MessageReceivedFromTransport` on the other end.</span></span>|  
|<span data-ttu-id="abdf9-123">HostReference</span><span class="sxs-lookup"><span data-stu-id="abdf9-123">HostReference</span></span>|`xs:string`|<span data-ttu-id="abdf9-124">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="abdf9-124">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="abdf9-125">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="abdf9-125">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="abdf9-126">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="abdf9-126">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="abdf9-127">AppDomain</span><span class="sxs-lookup"><span data-stu-id="abdf9-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="abdf9-128">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="abdf9-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
