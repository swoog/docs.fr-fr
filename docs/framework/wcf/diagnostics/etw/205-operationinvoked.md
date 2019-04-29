---
title: 205 - OperationInvoked
ms.date: 03/30/2017
ms.assetid: 9c8d6c90-dfa5-4ae0-a589-96679a8fb3ba
ms.openlocfilehash: e95b6923d21307b2ef68d4a5369b3cee86540239
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781977"
---
# <a name="205---operationinvoked"></a><span data-ttu-id="b9ce3-102">205 - OperationInvoked</span><span class="sxs-lookup"><span data-stu-id="b9ce3-102">205 - OperationInvoked</span></span>
## <a name="properties"></a><span data-ttu-id="b9ce3-103">Properties</span><span class="sxs-lookup"><span data-stu-id="b9ce3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b9ce3-104">Id</span><span class="sxs-lookup"><span data-stu-id="b9ce3-104">ID</span></span>|<span data-ttu-id="b9ce3-105">205</span><span class="sxs-lookup"><span data-stu-id="b9ce3-105">205</span></span>|  
|<span data-ttu-id="b9ce3-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="b9ce3-106">Keywords</span></span>|<span data-ttu-id="b9ce3-107">Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="b9ce3-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="b9ce3-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="b9ce3-108">Level</span></span>|<span data-ttu-id="b9ce3-109">Information</span><span class="sxs-lookup"><span data-stu-id="b9ce3-109">Information</span></span>|  
|<span data-ttu-id="b9ce3-110">Canal</span><span class="sxs-lookup"><span data-stu-id="b9ce3-110">Channel</span></span>|<span data-ttu-id="b9ce3-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="b9ce3-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b9ce3-112">Description</span><span class="sxs-lookup"><span data-stu-id="b9ce3-112">Description</span></span>  
 <span data-ttu-id="b9ce3-113">Cet événement est émis juste avant que l'`OperationInvoker` par défaut du modèle de service commence à appeler une méthode.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-113">This event is emitted just before the Service Model's default `OperationInvoker` begins a call to a method.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b9ce3-114">Message</span><span class="sxs-lookup"><span data-stu-id="b9ce3-114">Message</span></span>  
 <span data-ttu-id="b9ce3-115">Un OperationInvoker a appelé la méthode '%1'.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-115">An OperationInvoker invoked the '%1' method.</span></span> <span data-ttu-id="b9ce3-116">Informations sur l'appelant : '%2'.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-116">Caller information: '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b9ce3-117">Détails</span><span class="sxs-lookup"><span data-stu-id="b9ce3-117">Details</span></span>  
  
|<span data-ttu-id="b9ce3-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="b9ce3-118">Data Item Name</span></span>|<span data-ttu-id="b9ce3-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="b9ce3-119">Data Item Type</span></span>|<span data-ttu-id="b9ce3-120">Description</span><span class="sxs-lookup"><span data-stu-id="b9ce3-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b9ce3-121">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="b9ce3-121">Method Name</span></span>|`xs:string`|<span data-ttu-id="b9ce3-122">Nom CLR de la méthode qui a été appelée par l'`OperationInvoker`.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-122">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="b9ce3-123">Informations relatives à l'appelant</span><span class="sxs-lookup"><span data-stu-id="b9ce3-123">Caller Information</span></span>|`xs:string`|<span data-ttu-id="b9ce3-124">Adresse IP et numéro de port du client au format « Adresse IP:Numéro de port ».</span><span class="sxs-lookup"><span data-stu-id="b9ce3-124">The IP address and port number of the client in the format 'IPAddress:PortNumber'.</span></span> <span data-ttu-id="b9ce3-125">Les deux valeurs sont extraites de la propriété de message « System.ServiceModel.Channels.RemoteEndpointMessageProperty » dans le contexte de l'opération.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-125">The two values are retrieved from the 'System.ServiceModel.Channels.RemoteEndpointMessageProperty' message property within the operation context.</span></span> <span data-ttu-id="b9ce3-126">Notez que pour les liaisons autres que TCP, cette valeur est `null`.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-126">Note that for non-TCP bindings this value `null`.</span></span>|  
|<span data-ttu-id="b9ce3-127">HostReference</span><span class="sxs-lookup"><span data-stu-id="b9ce3-127">HostReference</span></span>|`xs:string`|<span data-ttu-id="b9ce3-128">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-128">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="b9ce3-129">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-129">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="b9ce3-130">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="b9ce3-130">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="b9ce3-131">AppDomain</span><span class="sxs-lookup"><span data-stu-id="b9ce3-131">AppDomain</span></span>|`xs:string`|<span data-ttu-id="b9ce3-132">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="b9ce3-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
