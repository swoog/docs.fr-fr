---
title: 201 - ClientMessageInspectorAfterReceiveInvoked
ms.date: 03/30/2017
ms.assetid: 9ff637f1-cc26-4400-ab9b-546f70e5057d
ms.openlocfilehash: 96ca318c141d49e2ac5594d5ee101658a2aa8f21
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33459022"
---
# <a name="201---clientmessageinspectorafterreceiveinvoked"></a><span data-ttu-id="6f361-102">201 - ClientMessageInspectorAfterReceiveInvoked</span><span class="sxs-lookup"><span data-stu-id="6f361-102">201 - ClientMessageInspectorAfterReceiveInvoked</span></span>
## <a name="properties"></a><span data-ttu-id="6f361-103">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6f361-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="6f361-104">Id</span><span class="sxs-lookup"><span data-stu-id="6f361-104">ID</span></span>|<span data-ttu-id="6f361-105">201</span><span class="sxs-lookup"><span data-stu-id="6f361-105">201</span></span>|  
|<span data-ttu-id="6f361-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="6f361-106">Keywords</span></span>|<span data-ttu-id="6f361-107">Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="6f361-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="6f361-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="6f361-108">Level</span></span>|<span data-ttu-id="6f361-109">Information</span><span class="sxs-lookup"><span data-stu-id="6f361-109">Information</span></span>|  
|<span data-ttu-id="6f361-110">Canal</span><span class="sxs-lookup"><span data-stu-id="6f361-110">Channel</span></span>|<span data-ttu-id="6f361-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="6f361-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="6f361-112">Description</span><span class="sxs-lookup"><span data-stu-id="6f361-112">Description</span></span>  
 <span data-ttu-id="6f361-113">Cet événement est émis après que le modèle de service a appelé la méthode `AfterReceiveReply` sur un inspecteur de message client.</span><span class="sxs-lookup"><span data-stu-id="6f361-113">This event is emitted after the Service Model has invoked the `AfterReceiveReply` method on a client message inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="6f361-114">Message</span><span class="sxs-lookup"><span data-stu-id="6f361-114">Message</span></span>  
 <span data-ttu-id="6f361-115">Le répartiteur a appelé 'AfterReceiveReply' sur un ClientMessageInspector de type '%1.'</span><span class="sxs-lookup"><span data-stu-id="6f361-115">The Dispatcher invoked 'AfterReceiveReply' on a ClientMessageInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="6f361-116">Détails</span><span class="sxs-lookup"><span data-stu-id="6f361-116">Details</span></span>  
  
|<span data-ttu-id="6f361-117">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="6f361-117">Data Item Name</span></span>|<span data-ttu-id="6f361-118">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="6f361-118">Data Item Type</span></span>|<span data-ttu-id="6f361-119">Description</span><span class="sxs-lookup"><span data-stu-id="6f361-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="6f361-120">TypeName</span><span class="sxs-lookup"><span data-stu-id="6f361-120">TypeName</span></span>|`xs:string`|<span data-ttu-id="6f361-121">CLR FullName du type d'inspecteur appelé.</span><span class="sxs-lookup"><span data-stu-id="6f361-121">The CLR FullName of the invoked inspector's type.</span></span>|  
|<span data-ttu-id="6f361-122">HostReference</span><span class="sxs-lookup"><span data-stu-id="6f361-122">HostReference</span></span>|`xs:string`|<span data-ttu-id="6f361-123">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="6f361-123">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="6f361-124">Son format est défini en tant que ' chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="6f361-124">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="6f361-125">Exemple : ' Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="6f361-125">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="6f361-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="6f361-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="6f361-127">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="6f361-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
