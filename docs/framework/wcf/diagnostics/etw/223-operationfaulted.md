---
title: 223 - OperationFaulted
ms.date: 03/30/2017
ms.assetid: 2f7d89d7-3a6a-40fe-9610-5424eb6bbf61
ms.openlocfilehash: cf4a455d80a1a0ac09e99bad967c1feba3653842
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61596531"
---
# <a name="223---operationfaulted"></a><span data-ttu-id="cc3a2-102">223 - OperationFaulted</span><span class="sxs-lookup"><span data-stu-id="cc3a2-102">223 - OperationFaulted</span></span>
## <a name="properties"></a><span data-ttu-id="cc3a2-103">Properties</span><span class="sxs-lookup"><span data-stu-id="cc3a2-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="cc3a2-104">Id</span><span class="sxs-lookup"><span data-stu-id="cc3a2-104">ID</span></span>|<span data-ttu-id="cc3a2-105">223</span><span class="sxs-lookup"><span data-stu-id="cc3a2-105">223</span></span>|  
|<span data-ttu-id="cc3a2-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="cc3a2-106">Keywords</span></span>|<span data-ttu-id="cc3a2-107">EndToEndMonitoring, HealthMonitoring, Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="cc3a2-107">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="cc3a2-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="cc3a2-108">Level</span></span>|<span data-ttu-id="cc3a2-109">Warning</span><span class="sxs-lookup"><span data-stu-id="cc3a2-109">Warning</span></span>|  
|<span data-ttu-id="cc3a2-110">Canal</span><span class="sxs-lookup"><span data-stu-id="cc3a2-110">Channel</span></span>|<span data-ttu-id="cc3a2-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="cc3a2-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="cc3a2-112">Description</span><span class="sxs-lookup"><span data-stu-id="cc3a2-112">Description</span></span>  
 <span data-ttu-id="cc3a2-113">Cet événement est émis lorsque l'`OperationInvoker` par défaut du modèle de service a rencontré une exception dérivée de `FaultException` en appelant sa méthode.</span><span class="sxs-lookup"><span data-stu-id="cc3a2-113">This event is emitted when the Service Model's default `OperationInvoker` has encountered an exception deriving from `FaultException` while invoking its method.</span></span>  
  
## <a name="message"></a><span data-ttu-id="cc3a2-114">Message</span><span class="sxs-lookup"><span data-stu-id="cc3a2-114">Message</span></span>  
 <span data-ttu-id="cc3a2-115">La méthode '%1' a levé un FaultException lors de l'appel effectué par l'OperationInvoker.</span><span class="sxs-lookup"><span data-stu-id="cc3a2-115">The '%1' method threw a FaultException when invoked by the OperationInvoker.</span></span> <span data-ttu-id="cc3a2-116">Durée de l'appel de méthode : '%2' ms.</span><span class="sxs-lookup"><span data-stu-id="cc3a2-116">The method call duration was '%2' ms.</span></span>  
  
## <a name="details"></a><span data-ttu-id="cc3a2-117">Détails</span><span class="sxs-lookup"><span data-stu-id="cc3a2-117">Details</span></span>  
  
|<span data-ttu-id="cc3a2-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="cc3a2-118">Data Item Name</span></span>|<span data-ttu-id="cc3a2-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="cc3a2-119">Data Item Type</span></span>|<span data-ttu-id="cc3a2-120">Description</span><span class="sxs-lookup"><span data-stu-id="cc3a2-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="cc3a2-121">MethodName</span><span class="sxs-lookup"><span data-stu-id="cc3a2-121">MethodName</span></span>|`xs:string`|<span data-ttu-id="cc3a2-122">Nom CLR de la méthode qui a été appelée par l'`OperationInvoker`.</span><span class="sxs-lookup"><span data-stu-id="cc3a2-122">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="cc3a2-123">Duration</span><span class="sxs-lookup"><span data-stu-id="cc3a2-123">Duration</span></span>|`xs:long`|<span data-ttu-id="cc3a2-124">Durée, en millisecondes, prise par l'`OperationInvoker` pour appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="cc3a2-124">The time, in milliseconds, that it took the `OperationInvoker` to invoke the method.</span></span>|  
|<span data-ttu-id="cc3a2-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="cc3a2-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="cc3a2-126">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="cc3a2-126">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="cc3a2-127">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="cc3a2-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="cc3a2-128">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="cc3a2-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="cc3a2-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="cc3a2-129">AppDomain</span></span>|`xs:string`|<span data-ttu-id="cc3a2-130">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="cc3a2-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
