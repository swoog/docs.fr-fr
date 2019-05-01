---
title: 214 - OperationCompleted
ms.date: 03/30/2017
ms.assetid: a6287eef-023f-4816-813c-1802c82366df
ms.openlocfilehash: da1021b674b555b683f8f745f5a2a0073c9567e8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61967997"
---
# <a name="214---operationcompleted"></a><span data-ttu-id="3f482-102">214 - OperationCompleted</span><span class="sxs-lookup"><span data-stu-id="3f482-102">214 - OperationCompleted</span></span>
## <a name="properties"></a><span data-ttu-id="3f482-103">Properties</span><span class="sxs-lookup"><span data-stu-id="3f482-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="3f482-104">Id</span><span class="sxs-lookup"><span data-stu-id="3f482-104">ID</span></span>|<span data-ttu-id="3f482-105">214</span><span class="sxs-lookup"><span data-stu-id="3f482-105">214</span></span>|  
|<span data-ttu-id="3f482-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="3f482-106">Keywords</span></span>|<span data-ttu-id="3f482-107">HealthMonitoring, EndToEndMonitoring, Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="3f482-107">HealthMonitoring, EndToEndMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="3f482-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="3f482-108">Level</span></span>|<span data-ttu-id="3f482-109">Information</span><span class="sxs-lookup"><span data-stu-id="3f482-109">Information</span></span>|  
|<span data-ttu-id="3f482-110">Canal</span><span class="sxs-lookup"><span data-stu-id="3f482-110">Channel</span></span>|<span data-ttu-id="3f482-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="3f482-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="3f482-112">Description</span><span class="sxs-lookup"><span data-stu-id="3f482-112">Description</span></span>  
 <span data-ttu-id="3f482-113">Cet événement est émis lorsque l'`OperationInvoker` par défaut du modèle de service a terminé un appel à une méthode, sans que cette méthode lève une exception.</span><span class="sxs-lookup"><span data-stu-id="3f482-113">This event is emitted when the Service Model's default `OperationInvoker` has completed a call to a method without that method throwing an exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="3f482-114">Message</span><span class="sxs-lookup"><span data-stu-id="3f482-114">Message</span></span>  
 <span data-ttu-id="3f482-115">OperationInvoker a terminé l'appel de la méthode '%1'.</span><span class="sxs-lookup"><span data-stu-id="3f482-115">An OperationInvoker completed the call to the '%1' method.</span></span> <span data-ttu-id="3f482-116">Durée de l'appel de méthode : '%2' ms.</span><span class="sxs-lookup"><span data-stu-id="3f482-116">The method call duration was '%2' ms.</span></span>  
  
## <a name="details"></a><span data-ttu-id="3f482-117">Détails</span><span class="sxs-lookup"><span data-stu-id="3f482-117">Details</span></span>  
  
|<span data-ttu-id="3f482-118">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="3f482-118">Data Item Name</span></span>|<span data-ttu-id="3f482-119">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="3f482-119">Data Item Type</span></span>|<span data-ttu-id="3f482-120">Description</span><span class="sxs-lookup"><span data-stu-id="3f482-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="3f482-121">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="3f482-121">Method Name</span></span>|`xs:string`|<span data-ttu-id="3f482-122">Nom CLR de la méthode qui a été appelée par l'`OperationInvoker`.</span><span class="sxs-lookup"><span data-stu-id="3f482-122">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="3f482-123">Duration</span><span class="sxs-lookup"><span data-stu-id="3f482-123">Duration</span></span>|`xs:long`|<span data-ttu-id="3f482-124">Durée, en millisecondes, prise par l'`OperationInvoker` pour appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="3f482-124">The time, in milliseconds, that it took the `OperationInvoker` to invoke the method.</span></span>|  
|<span data-ttu-id="3f482-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="3f482-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="3f482-126">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="3f482-126">For web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="3f482-127">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="3f482-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="3f482-128">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="3f482-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="3f482-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="3f482-129">AppDomain</span></span>|`xs:string`|<span data-ttu-id="3f482-130">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="3f482-130">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
