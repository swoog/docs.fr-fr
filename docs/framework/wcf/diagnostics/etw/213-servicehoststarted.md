---
title: 213 - ServiceHostStarted
ms.date: 03/30/2017
ms.assetid: a6f7facc-342f-46bb-9d52-a470178ba6bb
ms.openlocfilehash: 819efa2e13c94e2c7a16c24f6ba9c7ef2b87ef8c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781821"
---
# <a name="213---servicehoststarted"></a><span data-ttu-id="422b3-102">213 - ServiceHostStarted</span><span class="sxs-lookup"><span data-stu-id="422b3-102">213 - ServiceHostStarted</span></span>
## <a name="properties"></a><span data-ttu-id="422b3-103">Properties</span><span class="sxs-lookup"><span data-stu-id="422b3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="422b3-104">Id</span><span class="sxs-lookup"><span data-stu-id="422b3-104">ID</span></span>|<span data-ttu-id="422b3-105">213</span><span class="sxs-lookup"><span data-stu-id="422b3-105">213</span></span>|  
|<span data-ttu-id="422b3-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="422b3-106">Keywords</span></span>|<span data-ttu-id="422b3-107">EndToEndMonitoring, HealthMonitoring, Dépannage, ServiceHost</span><span class="sxs-lookup"><span data-stu-id="422b3-107">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceHost</span></span>|  
|<span data-ttu-id="422b3-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="422b3-108">Level</span></span>|<span data-ttu-id="422b3-109">LogAlways</span><span class="sxs-lookup"><span data-stu-id="422b3-109">LogAlways</span></span>|  
|<span data-ttu-id="422b3-110">Canal</span><span class="sxs-lookup"><span data-stu-id="422b3-110">Channel</span></span>|<span data-ttu-id="422b3-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="422b3-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="422b3-112">Description</span><span class="sxs-lookup"><span data-stu-id="422b3-112">Description</span></span>  
 <span data-ttu-id="422b3-113">Cet événement est émis lors du démarrage d'un hôte de service hébergé par le Web.</span><span class="sxs-lookup"><span data-stu-id="422b3-113">This event is emitted when a Web-hosted service host is started.</span></span> <span data-ttu-id="422b3-114">Cela se produit en général lorsque le service est activé par un message.</span><span class="sxs-lookup"><span data-stu-id="422b3-114">This typically happens when the service is activated by a message.</span></span> <span data-ttu-id="422b3-115">Cela peut également arriver si le service est configuré pour démarrer automatiquement.</span><span class="sxs-lookup"><span data-stu-id="422b3-115">It may also happen if the service is configured to be automatically started.</span></span>  
  
## <a name="message"></a><span data-ttu-id="422b3-116">Message</span><span class="sxs-lookup"><span data-stu-id="422b3-116">Message</span></span>  
 <span data-ttu-id="422b3-117">ServiceHost a démarré : '%1'.</span><span class="sxs-lookup"><span data-stu-id="422b3-117">ServiceHost started: '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="422b3-118">Détails</span><span class="sxs-lookup"><span data-stu-id="422b3-118">Details</span></span>  
  
|<span data-ttu-id="422b3-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="422b3-119">Data Item Name</span></span>|<span data-ttu-id="422b3-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="422b3-120">Data Item Type</span></span>|<span data-ttu-id="422b3-121">Description</span><span class="sxs-lookup"><span data-stu-id="422b3-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="422b3-122">Nom de type de service</span><span class="sxs-lookup"><span data-stu-id="422b3-122">Service Type Name</span></span>|`xs:string`|<span data-ttu-id="422b3-123">CLR FullName du type de l'implémentation de service.</span><span class="sxs-lookup"><span data-stu-id="422b3-123">The CLR FullName of the type of the service implementation.</span></span>|  
|<span data-ttu-id="422b3-124">HostReference</span><span class="sxs-lookup"><span data-stu-id="422b3-124">HostReference</span></span>|`xs:string`|<span data-ttu-id="422b3-125">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="422b3-125">For Web hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="422b3-126">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="422b3-126">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="422b3-127">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="422b3-127">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="422b3-128">AppDomain</span><span class="sxs-lookup"><span data-stu-id="422b3-128">AppDomain</span></span>|`xs:string`|<span data-ttu-id="422b3-129">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="422b3-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
