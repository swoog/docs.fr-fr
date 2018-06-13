---
title: 499 - TransferEmitted
ms.date: 03/30/2017
ms.assetid: 07a26434-a7a0-40fc-b5d0-3520a04328ae
ms.openlocfilehash: b1ade828ee6519288165e272e7d9f36fd6aca9ff
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33469506"
---
# <a name="499---transferemitted"></a><span data-ttu-id="72829-102">499 - TransferEmitted</span><span class="sxs-lookup"><span data-stu-id="72829-102">499 - TransferEmitted</span></span>
## <a name="properties"></a><span data-ttu-id="72829-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="72829-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="72829-104">Id</span><span class="sxs-lookup"><span data-stu-id="72829-104">ID</span></span>|<span data-ttu-id="72829-105">499</span><span class="sxs-lookup"><span data-stu-id="72829-105">499</span></span>|  
|<span data-ttu-id="72829-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="72829-106">Keywords</span></span>|<span data-ttu-id="72829-107">Dépannage, UserEvents, EndToEndMonitoring, ServiceModel, WFTracking, ServiceHost, WCFMessageLogging</span><span class="sxs-lookup"><span data-stu-id="72829-107">Troubleshooting, UserEvents, EndToEndMonitoring, ServiceModel, WFTracking, ServiceHost, WCFMessageLogging</span></span>|  
|<span data-ttu-id="72829-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="72829-108">Level</span></span>|<span data-ttu-id="72829-109">LogAlways</span><span class="sxs-lookup"><span data-stu-id="72829-109">LogAlways</span></span>|  
|<span data-ttu-id="72829-110">Canal</span><span class="sxs-lookup"><span data-stu-id="72829-110">Channel</span></span>|<span data-ttu-id="72829-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="72829-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="72829-112">Description</span><span class="sxs-lookup"><span data-stu-id="72829-112">Description</span></span>  
 <span data-ttu-id="72829-113">Cet événement est émis lorsque l'événement de transfert se produit.</span><span class="sxs-lookup"><span data-stu-id="72829-113">This event is emitted when the transfer event takes place.</span></span>  
  
## <a name="message"></a><span data-ttu-id="72829-114">Message</span><span class="sxs-lookup"><span data-stu-id="72829-114">Message</span></span>  
 <span data-ttu-id="72829-115">Événement Transfer émis.</span><span class="sxs-lookup"><span data-stu-id="72829-115">Transfer event emitted.</span></span>  
  
## <a name="details"></a><span data-ttu-id="72829-116">Détails</span><span class="sxs-lookup"><span data-stu-id="72829-116">Details</span></span>  
  
|<span data-ttu-id="72829-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="72829-117">Data Item Name</span></span>|<span data-ttu-id="72829-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="72829-118">Data Item Type</span></span>|<span data-ttu-id="72829-119">Description</span><span class="sxs-lookup"><span data-stu-id="72829-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="72829-120">HostReference</span><span class="sxs-lookup"><span data-stu-id="72829-120">HostReference</span></span>|`xs:string`|<span data-ttu-id="72829-121">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="72829-121">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="72829-122">Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="72829-122">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="72829-123">Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="72829-123">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="72829-124">AppDomain</span><span class="sxs-lookup"><span data-stu-id="72829-124">AppDomain</span></span>|`xs:string`|<span data-ttu-id="72829-125">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="72829-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
