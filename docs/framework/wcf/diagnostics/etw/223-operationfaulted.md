---
title: 223 - OperationFaulted
ms.date: 03/30/2017
ms.assetid: 2f7d89d7-3a6a-40fe-9610-5424eb6bbf61
ms.openlocfilehash: cf4a455d80a1a0ac09e99bad967c1feba3653842
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33459416"
---
# <a name="223---operationfaulted"></a><span data-ttu-id="c4e09-102">223 - OperationFaulted</span><span class="sxs-lookup"><span data-stu-id="c4e09-102">223 - OperationFaulted</span></span>
## <a name="properties"></a><span data-ttu-id="c4e09-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4e09-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c4e09-104">Id</span><span class="sxs-lookup"><span data-stu-id="c4e09-104">ID</span></span>|<span data-ttu-id="c4e09-105">223</span><span class="sxs-lookup"><span data-stu-id="c4e09-105">223</span></span>|  
|<span data-ttu-id="c4e09-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="c4e09-106">Keywords</span></span>|<span data-ttu-id="c4e09-107">EndToEndMonitoring, HealthMonitoring, Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c4e09-107">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="c4e09-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="c4e09-108">Level</span></span>|<span data-ttu-id="c4e09-109">Avertissement</span><span class="sxs-lookup"><span data-stu-id="c4e09-109">Warning</span></span>|  
|<span data-ttu-id="c4e09-110">Canal</span><span class="sxs-lookup"><span data-stu-id="c4e09-110">Channel</span></span>|<span data-ttu-id="c4e09-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="c4e09-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c4e09-112">Description</span><span class="sxs-lookup"><span data-stu-id="c4e09-112">Description</span></span>  
 <span data-ttu-id="c4e09-113">Cet événement est émis lorsque l'`OperationInvoker` par défaut du modèle de service a rencontré une exception dérivée de `FaultException` en appelant sa méthode.</span><span class="sxs-lookup"><span data-stu-id="c4e09-113">This event is emitted when the Service Model's default `OperationInvoker` has encountered an exception deriving from `FaultException` while invoking its method.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c4e09-114">Message</span><span class="sxs-lookup"><span data-stu-id="c4e09-114">Message</span></span>  
 <span data-ttu-id="c4e09-115">La méthode '%1' a levé un FaultException lors de l'appel effectué par l'OperationInvoker.</span><span class="sxs-lookup"><span data-stu-id="c4e09-115">The '%1' method threw a FaultException when invoked by the OperationInvoker.</span></span> <span data-ttu-id="c4e09-116">Durée de l'appel de méthode : '%2' ms.</span><span class="sxs-lookup"><span data-stu-id="c4e09-116">The method call duration was '%2' ms.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c4e09-117">Détails</span><span class="sxs-lookup"><span data-stu-id="c4e09-117">Details</span></span>  
  
|<span data-ttu-id="c4e09-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="c4e09-118">Data Item Name</span></span>|<span data-ttu-id="c4e09-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="c4e09-119">Data Item Type</span></span>|<span data-ttu-id="c4e09-120">Description</span><span class="sxs-lookup"><span data-stu-id="c4e09-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c4e09-121">MethodName</span><span class="sxs-lookup"><span data-stu-id="c4e09-121">MethodName</span></span>|`xs:string`|<span data-ttu-id="c4e09-122">Nom CLR de la méthode qui a été appelée par l'`OperationInvoker`.</span><span class="sxs-lookup"><span data-stu-id="c4e09-122">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="c4e09-123">Duration</span><span class="sxs-lookup"><span data-stu-id="c4e09-123">Duration</span></span>|`xs:long`|<span data-ttu-id="c4e09-124">Durée, en millisecondes, prise par l'`OperationInvoker` pour appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="c4e09-124">The time, in milliseconds, that it took the `OperationInvoker` to invoke the method.</span></span>|  
|<span data-ttu-id="c4e09-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="c4e09-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="c4e09-126">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="c4e09-126">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="c4e09-127">Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="c4e09-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="c4e09-128">Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="c4e09-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="c4e09-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="c4e09-129">AppDomain</span></span>|`xs:string`|<span data-ttu-id="c4e09-130">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="c4e09-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
