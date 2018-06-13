---
title: 202 - ClientMessageInspectorBeforeSendInvoked
ms.date: 03/30/2017
ms.assetid: 0b02ca82-8a55-45e3-b2e2-ddfe28a7269c
ms.openlocfilehash: 98de1d7e8e5e87ec7fbd783092f7fbc212fec65d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33459353"
---
# <a name="202---clientmessageinspectorbeforesendinvoked"></a><span data-ttu-id="a4a30-102">202 - ClientMessageInspectorBeforeSendInvoked</span><span class="sxs-lookup"><span data-stu-id="a4a30-102">202 - ClientMessageInspectorBeforeSendInvoked</span></span>
## <a name="properties"></a><span data-ttu-id="a4a30-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a4a30-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a4a30-104">Id</span><span class="sxs-lookup"><span data-stu-id="a4a30-104">ID</span></span>|<span data-ttu-id="a4a30-105">202</span><span class="sxs-lookup"><span data-stu-id="a4a30-105">202</span></span>|  
|<span data-ttu-id="a4a30-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a4a30-106">Keywords</span></span>|<span data-ttu-id="a4a30-107">Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="a4a30-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="a4a30-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="a4a30-108">Level</span></span>|<span data-ttu-id="a4a30-109">Information</span><span class="sxs-lookup"><span data-stu-id="a4a30-109">Information</span></span>|  
|<span data-ttu-id="a4a30-110">Canal</span><span class="sxs-lookup"><span data-stu-id="a4a30-110">Channel</span></span>|<span data-ttu-id="a4a30-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="a4a30-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="a4a30-112">Description</span><span class="sxs-lookup"><span data-stu-id="a4a30-112">Description</span></span>  
 <span data-ttu-id="a4a30-113">Cet événement est émis après que le modèle de service a appelé la méthode `BeforeSendRequest` sur un inspecteur de message client.</span><span class="sxs-lookup"><span data-stu-id="a4a30-113">This event is emitted after the Service Model has invoked the `BeforeSendRequest` method on a client message inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="a4a30-114">Message</span><span class="sxs-lookup"><span data-stu-id="a4a30-114">Message</span></span>  
 <span data-ttu-id="a4a30-115">Le répartiteur a appelé « BeforeSendRequest » sur un ClientMessageInspector de type « %1 ».</span><span class="sxs-lookup"><span data-stu-id="a4a30-115">The Dispatcher invoked 'BeforeSendRequest' on a ClientMessageInspector of type  '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="a4a30-116">Détails</span><span class="sxs-lookup"><span data-stu-id="a4a30-116">Details</span></span>  
  
|<span data-ttu-id="a4a30-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a4a30-117">Data Item Name</span></span>|<span data-ttu-id="a4a30-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a4a30-118">Data Item Type</span></span>|<span data-ttu-id="a4a30-119">Description</span><span class="sxs-lookup"><span data-stu-id="a4a30-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="a4a30-120">TypeName</span><span class="sxs-lookup"><span data-stu-id="a4a30-120">TypeName</span></span>|`xs:string`|<span data-ttu-id="a4a30-121">CLR FullName du type d'inspecteur appelé.</span><span class="sxs-lookup"><span data-stu-id="a4a30-121">The CLR FullName of the invoked inspector's type.</span></span>|  
|<span data-ttu-id="a4a30-122">HostReference</span><span class="sxs-lookup"><span data-stu-id="a4a30-122">HostReference</span></span>|`xs:string`|<span data-ttu-id="a4a30-123">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="a4a30-123">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="a4a30-124">Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="a4a30-124">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="a4a30-125">Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="a4a30-125">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="a4a30-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="a4a30-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="a4a30-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="a4a30-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
