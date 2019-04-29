---
title: 222 - OperationFailed
ms.date: 03/30/2017
ms.assetid: 6b530ded-8f20-4d78-8bfe-1875276df6ba
ms.openlocfilehash: c49aad0f93ce47b66306d75741267530dc6d3fe5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781639"
---
# <a name="222---operationfailed"></a><span data-ttu-id="f179e-102">222 - OperationFailed</span><span class="sxs-lookup"><span data-stu-id="f179e-102">222 - OperationFailed</span></span>
## <a name="properties"></a><span data-ttu-id="f179e-103">Properties</span><span class="sxs-lookup"><span data-stu-id="f179e-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f179e-104">Id</span><span class="sxs-lookup"><span data-stu-id="f179e-104">ID</span></span>|<span data-ttu-id="f179e-105">222</span><span class="sxs-lookup"><span data-stu-id="f179e-105">222</span></span>|  
|<span data-ttu-id="f179e-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="f179e-106">Keywords</span></span>|<span data-ttu-id="f179e-107">EndToEndMonitoring, HealthMonitoring, Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f179e-107">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="f179e-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="f179e-108">Level</span></span>|<span data-ttu-id="f179e-109">Warning</span><span class="sxs-lookup"><span data-stu-id="f179e-109">Warning</span></span>|  
|<span data-ttu-id="f179e-110">Canal</span><span class="sxs-lookup"><span data-stu-id="f179e-110">Channel</span></span>|<span data-ttu-id="f179e-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="f179e-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f179e-112">Description</span><span class="sxs-lookup"><span data-stu-id="f179e-112">Description</span></span>  
 <span data-ttu-id="f179e-113">Cet événement est émis lorsque l'`OperationInvoker` par défaut du modèle de service a rencontré une exception lors de l'appel de sa méthode.</span><span class="sxs-lookup"><span data-stu-id="f179e-113">This event is emitted when the Service Model's default `OperationInvoker` has encountered an exception while invoking its method.</span></span> <span data-ttu-id="f179e-114">Notez que les exceptions dérivant de `FaultException` empêchent cet événement d'être émis.</span><span class="sxs-lookup"><span data-stu-id="f179e-114">Note that exceptions that derive from `FaultException` cause this event to not be emitted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f179e-115">Message</span><span class="sxs-lookup"><span data-stu-id="f179e-115">Message</span></span>  
 <span data-ttu-id="f179e-116">La méthode '%1' a levé une exception non gérée lors de l'appel effectué par l'OperationInvoker.</span><span class="sxs-lookup"><span data-stu-id="f179e-116">The '%1' method threw an unhandled exception when invoked by the OperationInvoker.</span></span> <span data-ttu-id="f179e-117">Durée de l'appel de méthode : '%2' ms.</span><span class="sxs-lookup"><span data-stu-id="f179e-117">The method call duration was '%2' ms.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f179e-118">Détails</span><span class="sxs-lookup"><span data-stu-id="f179e-118">Details</span></span>  
  
|<span data-ttu-id="f179e-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="f179e-119">Data Item Name</span></span>|<span data-ttu-id="f179e-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="f179e-120">Data Item Type</span></span>|<span data-ttu-id="f179e-121">Description</span><span class="sxs-lookup"><span data-stu-id="f179e-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f179e-122">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="f179e-122">Method Name</span></span>|`xs:string`|<span data-ttu-id="f179e-123">Nom CLR de la méthode qui a été appelée par l'`OperationInvoker`.</span><span class="sxs-lookup"><span data-stu-id="f179e-123">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="f179e-124">Duration</span><span class="sxs-lookup"><span data-stu-id="f179e-124">Duration</span></span>|`xs:long`|<span data-ttu-id="f179e-125">Durée, en millisecondes, prise par l'`OperationInvoker` pour appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="f179e-125">The time, in milliseconds, that it took the `OperationInvoker` to invoke the method.</span></span>|  
|<span data-ttu-id="f179e-126">HostReference</span><span class="sxs-lookup"><span data-stu-id="f179e-126">HostReference</span></span>|`xs:string`|<span data-ttu-id="f179e-127">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="f179e-127">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="f179e-128">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="f179e-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="f179e-129">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="f179e-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="f179e-130">AppDomain</span><span class="sxs-lookup"><span data-stu-id="f179e-130">AppDomain</span></span>|`xs:string`|<span data-ttu-id="f179e-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="f179e-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
