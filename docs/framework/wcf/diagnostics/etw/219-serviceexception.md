---
title: 219 - ServiceException
ms.date: 03/30/2017
ms.assetid: 81e2efac-39aa-4ed2-85a9-97eb8793b844
ms.openlocfilehash: eb4289c0346c9e1d9481347d69db8c5f007e4325
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61781730"
---
# <a name="219---serviceexception"></a><span data-ttu-id="a9dc8-102">219 - ServiceException</span><span class="sxs-lookup"><span data-stu-id="a9dc8-102">219 - ServiceException</span></span>
## <a name="properties"></a><span data-ttu-id="a9dc8-103">Properties</span><span class="sxs-lookup"><span data-stu-id="a9dc8-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="a9dc8-104">Id</span><span class="sxs-lookup"><span data-stu-id="a9dc8-104">ID</span></span>|<span data-ttu-id="a9dc8-105">219</span><span class="sxs-lookup"><span data-stu-id="a9dc8-105">219</span></span>|  
|<span data-ttu-id="a9dc8-106">Mots clés</span><span class="sxs-lookup"><span data-stu-id="a9dc8-106">Keywords</span></span>|<span data-ttu-id="a9dc8-107">EndToEndMonitoring, HealthMonitoring, Dépannage, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="a9dc8-107">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="a9dc8-108">Niveau</span><span class="sxs-lookup"><span data-stu-id="a9dc8-108">Level</span></span>|<span data-ttu-id="a9dc8-109">Error</span><span class="sxs-lookup"><span data-stu-id="a9dc8-109">Error</span></span>|  
|<span data-ttu-id="a9dc8-110">Canal</span><span class="sxs-lookup"><span data-stu-id="a9dc8-110">Channel</span></span>|<span data-ttu-id="a9dc8-111">Microsoft-Windows-Application Server-Applications/Analyse</span><span class="sxs-lookup"><span data-stu-id="a9dc8-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="a9dc8-112">Description</span><span class="sxs-lookup"><span data-stu-id="a9dc8-112">Description</span></span>  
 <span data-ttu-id="a9dc8-113">Cet événement est émis lorsqu'un service WCF rencontre une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-113">This event is emitted when a WCF service encounters an unhandled exception.</span></span> <span data-ttu-id="a9dc8-114">Cela inclut les exceptions non gérées pendant l'activation, pendant le traitement du message et dans le code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-114">This includes unhandled exceptions during activation, during message processing, and in user code.</span></span>  
  
## <a name="message"></a><span data-ttu-id="a9dc8-115">Message</span><span class="sxs-lookup"><span data-stu-id="a9dc8-115">Message</span></span>  
 <span data-ttu-id="a9dc8-116">Une exception non gérée de type '%2' s'est produite lors du traitement du message.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-116">There was an unhandled exception of type '%2' during message processing.</span></span> <span data-ttu-id="a9dc8-117">Exception totale ToString : %1.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-117">Full Exception ToString: %1.</span></span>  
  
## <a name="details"></a><span data-ttu-id="a9dc8-118">Détails</span><span class="sxs-lookup"><span data-stu-id="a9dc8-118">Details</span></span>  
  
|<span data-ttu-id="a9dc8-119">Nom d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a9dc8-119">Data Item Name</span></span>|<span data-ttu-id="a9dc8-120">Type d'élément de données</span><span class="sxs-lookup"><span data-stu-id="a9dc8-120">Data Item Type</span></span>|<span data-ttu-id="a9dc8-121">Description</span><span class="sxs-lookup"><span data-stu-id="a9dc8-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="a9dc8-122">ExceptionToString</span><span class="sxs-lookup"><span data-stu-id="a9dc8-122">ExceptionToString</span></span>|`xs:string`|<span data-ttu-id="a9dc8-123">Résultat de l'appel à `ToString`() sur l'exception CLR.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-123">The result of calling `ToString`() on the CLR exception.</span></span>|  
|<span data-ttu-id="a9dc8-124">ExceptionTypeName</span><span class="sxs-lookup"><span data-stu-id="a9dc8-124">ExceptionTypeName</span></span>|`xs:string`|<span data-ttu-id="a9dc8-125">CLR FullName du type de l'exception.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-125">The CLR FullName of the exception's type.</span></span>|  
|<span data-ttu-id="a9dc8-126">HostReference</span><span class="sxs-lookup"><span data-stu-id="a9dc8-126">HostReference</span></span>|`xs:string`|<span data-ttu-id="a9dc8-127">Pour les services hébergés par le Web, ce champ identifie de manière unique le service dans la hiérarchie Web.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-127">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="a9dc8-128">Son format est défini en tant que « chemin d’accès virtuel de Site Web nom Application&#124;chemin d’accès virtuel du Service&#124;ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="a9dc8-129">Exemple : « Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService ».</span><span class="sxs-lookup"><span data-stu-id="a9dc8-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="a9dc8-130">AppDomain</span><span class="sxs-lookup"><span data-stu-id="a9dc8-130">AppDomain</span></span>|`xs:string`|<span data-ttu-id="a9dc8-131">Chaîne retournée par AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="a9dc8-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
