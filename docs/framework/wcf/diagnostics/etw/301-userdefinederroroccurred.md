---
title: 301 - UserDefinedErrorOccurred
ms.date: 03/30/2017
ms.assetid: a0285d1c-550f-4c14-9c36-a96e97f1c4e4
ms.openlocfilehash: 6eb80d6f0b20af9aae6e7de5248323088e352b26
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33459477"
---
# <a name="301---userdefinederroroccurred"></a><span data-ttu-id="12ba3-102">301 - UserDefinedErrorOccurred</span><span class="sxs-lookup"><span data-stu-id="12ba3-102">301 - UserDefinedErrorOccurred</span></span>
## <a name="properties"></a><span data-ttu-id="12ba3-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="12ba3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="12ba3-104">Id</span><span class="sxs-lookup"><span data-stu-id="12ba3-104">ID</span></span>|<span data-ttu-id="12ba3-105">301</span><span class="sxs-lookup"><span data-stu-id="12ba3-105">301</span></span>|  
|<span data-ttu-id="12ba3-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="12ba3-106">Keywords</span></span>|<span data-ttu-id="12ba3-107">Dépannage, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring</span><span class="sxs-lookup"><span data-stu-id="12ba3-107">Troubleshooting, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring</span></span>|  
|<span data-ttu-id="12ba3-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="12ba3-108">Level</span></span>|<span data-ttu-id="12ba3-109">Erreur</span><span class="sxs-lookup"><span data-stu-id="12ba3-109">Error</span></span>|  
|<span data-ttu-id="12ba3-110">Canal</span><span class="sxs-lookup"><span data-stu-id="12ba3-110">Channel</span></span>|<span data-ttu-id="12ba3-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="12ba3-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="12ba3-112">Description</span><span class="sxs-lookup"><span data-stu-id="12ba3-112">Description</span></span>  
 <span data-ttu-id="12ba3-113">Cet événement est émis à partir du code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12ba3-113">This event is emitted from user code.</span></span> <span data-ttu-id="12ba3-114">Les développeurs peuvent émettre cet événement lorsqu'une erreur personnalisée se produit dans leur service.</span><span class="sxs-lookup"><span data-stu-id="12ba3-114">Developers can emit this event when a custom-defined error occurs in their service.</span></span> <span data-ttu-id="12ba3-115">Cela peut s'effectuer à l'aide des API <xref:System.Diagnostics.Eventing>.</span><span class="sxs-lookup"><span data-stu-id="12ba3-115">This can be done using the <xref:System.Diagnostics.Eventing> APIs.</span></span> <span data-ttu-id="12ba3-116">En outre, il existe un exemple WCF qui encapsule cette API et montre comment émettre correctement cet événement.</span><span class="sxs-lookup"><span data-stu-id="12ba3-116">Additionally, there is a WCF sample that wraps that API and demonstrates how to properly emit this event.</span></span>  
  
## <a name="message"></a><span data-ttu-id="12ba3-117">Message</span><span class="sxs-lookup"><span data-stu-id="12ba3-117">Message</span></span>  
 <span data-ttu-id="12ba3-118">Nom : '%1', Référence : '%2', Charge : %3</span><span class="sxs-lookup"><span data-stu-id="12ba3-118">Name:'%1', Reference:'%2', Payload:%3</span></span>  
  
## <a name="details"></a><span data-ttu-id="12ba3-119">Détails</span><span class="sxs-lookup"><span data-stu-id="12ba3-119">Details</span></span>  
  
|<span data-ttu-id="12ba3-120">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="12ba3-120">Data Item Name</span></span>|<span data-ttu-id="12ba3-121">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="12ba3-121">Data Item Type</span></span>|<span data-ttu-id="12ba3-122">Description</span><span class="sxs-lookup"><span data-stu-id="12ba3-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="12ba3-123">Name</span><span class="sxs-lookup"><span data-stu-id="12ba3-123">Name</span></span>|`xs:string`|<span data-ttu-id="12ba3-124">Nom de l'événement défini par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12ba3-124">The user-defined name of the event.</span></span>|  
|<span data-ttu-id="12ba3-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="12ba3-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="12ba3-126">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="12ba3-126">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="12ba3-127">Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="12ba3-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="12ba3-128">Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="12ba3-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="12ba3-129">Charge utile</span><span class="sxs-lookup"><span data-stu-id="12ba3-129">Payload</span></span>|`xs:string`|<span data-ttu-id="12ba3-130">Charge utile de l'événement définie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12ba3-130">The user-defined payload of the event.</span></span>|
