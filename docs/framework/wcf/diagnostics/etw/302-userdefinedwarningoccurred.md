---
title: 302 - UserDefinedWarningOccurred
ms.date: 03/30/2017
ms.assetid: 8d1f0bf1-0151-45e6-be92-573d397b54de
ms.openlocfilehash: c70857951309ef54ba460e96e948c9320269d30f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61596750"
---
# <a name="302---userdefinedwarningoccurred"></a><span data-ttu-id="29ba2-102">302 - UserDefinedWarningOccurred</span><span class="sxs-lookup"><span data-stu-id="29ba2-102">302 - UserDefinedWarningOccurred</span></span>
## <a name="properties"></a><span data-ttu-id="29ba2-103">Properties</span><span class="sxs-lookup"><span data-stu-id="29ba2-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="29ba2-104">Id</span><span class="sxs-lookup"><span data-stu-id="29ba2-104">ID</span></span>|<span data-ttu-id="29ba2-105">302</span><span class="sxs-lookup"><span data-stu-id="29ba2-105">302</span></span>|  
|<span data-ttu-id="29ba2-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="29ba2-106">Keywords</span></span>|<span data-ttu-id="29ba2-107">Dépannage, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring</span><span class="sxs-lookup"><span data-stu-id="29ba2-107">Troubleshooting, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring</span></span>|  
|<span data-ttu-id="29ba2-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="29ba2-108">Level</span></span>|<span data-ttu-id="29ba2-109">Warning</span><span class="sxs-lookup"><span data-stu-id="29ba2-109">Warning</span></span>|  
|<span data-ttu-id="29ba2-110">Canal</span><span class="sxs-lookup"><span data-stu-id="29ba2-110">Channel</span></span>|<span data-ttu-id="29ba2-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="29ba2-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="29ba2-112">Description</span><span class="sxs-lookup"><span data-stu-id="29ba2-112">Description</span></span>  
 <span data-ttu-id="29ba2-113">Cet événement est émis à partir du code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29ba2-113">This event is emitted from user code.</span></span> <span data-ttu-id="29ba2-114">Les développeurs peuvent émettre cet événement lorsqu'un événement d'avertissement personnalisé se produit dans leur service.</span><span class="sxs-lookup"><span data-stu-id="29ba2-114">Developers can emit this event when a custom-defined warning event occurs in their service.</span></span> <span data-ttu-id="29ba2-115">Cela peut s'effectuer à l'aide des API <xref:System.Diagnostics.Eventing>.</span><span class="sxs-lookup"><span data-stu-id="29ba2-115">This can be done using the <xref:System.Diagnostics.Eventing> APIs.</span></span> <span data-ttu-id="29ba2-116">En outre, il existe un exemple WCF qui encapsule cette API et montre comment émettre correctement cet événement.</span><span class="sxs-lookup"><span data-stu-id="29ba2-116">Additionally, there is a WCF sample that wraps that API and demonstrates how to properly emit this event.</span></span>  
  
## <a name="message"></a><span data-ttu-id="29ba2-117">Message</span><span class="sxs-lookup"><span data-stu-id="29ba2-117">Message</span></span>  
 <span data-ttu-id="29ba2-118">Nom : '%1', Référence : '%2', Charge : %3</span><span class="sxs-lookup"><span data-stu-id="29ba2-118">Name:'%1', Reference:'%2', Payload:%3</span></span>  
  
## <a name="details"></a><span data-ttu-id="29ba2-119">Détails</span><span class="sxs-lookup"><span data-stu-id="29ba2-119">Details</span></span>  
  
|<span data-ttu-id="29ba2-120">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="29ba2-120">Data Item Name</span></span>|<span data-ttu-id="29ba2-121">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="29ba2-121">Data Item Type</span></span>|<span data-ttu-id="29ba2-122">Description</span><span class="sxs-lookup"><span data-stu-id="29ba2-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="29ba2-123">Nom</span><span class="sxs-lookup"><span data-stu-id="29ba2-123">Name</span></span>|`xs:string`|<span data-ttu-id="29ba2-124">Nom de l'événement défini par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29ba2-124">The user-defined name of the event.</span></span>|  
|<span data-ttu-id="29ba2-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="29ba2-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="29ba2-126">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="29ba2-126">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="29ba2-127">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="29ba2-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="29ba2-128">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="29ba2-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="29ba2-129">Charge utile</span><span class="sxs-lookup"><span data-stu-id="29ba2-129">Payload</span></span>|`xs:string`|<span data-ttu-id="29ba2-130">Charge utile de l'événement définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29ba2-130">The user-defined payload of the event.</span></span>|
