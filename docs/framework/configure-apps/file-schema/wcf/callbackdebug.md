---
title: '&lt;callbackDebug&gt;'
ms.date: 03/30/2017
ms.assetid: 4073feda-1857-4be4-9947-227afb847ced
ms.openlocfilehash: 1aa292a3fe06af9cf1dbc53ebf5bbdf9841be8d9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54687373"
---
# <a name="ltcallbackdebuggt"></a><span data-ttu-id="1d513-102">&lt;callbackDebug&gt;</span><span class="sxs-lookup"><span data-stu-id="1d513-102">&lt;callbackDebug&gt;</span></span>
<span data-ttu-id="1d513-103">Spécifie le débogage de service pour un objet de rappel Windows Communication Foundation (WCF).</span><span class="sxs-lookup"><span data-stu-id="1d513-103">Specifies service debugging for a Windows Communication Foundation (WCF) callback object.</span></span>  
  
 <span data-ttu-id="1d513-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="1d513-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="1d513-105">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="1d513-105">\<behaviors></span></span>  
<span data-ttu-id="1d513-106">\<endpointBehaviors></span><span class="sxs-lookup"><span data-stu-id="1d513-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="1d513-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1d513-107">\<behavior></span></span>  
<span data-ttu-id="1d513-108">\<callbackDebug></span><span class="sxs-lookup"><span data-stu-id="1d513-108">\<callbackDebug></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1d513-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d513-109">Syntax</span></span>  
  
```xml  
<callbackDebug includeExceptionDetailInFaults="Boolean" />
```  
  
## <a name="type"></a><span data-ttu-id="1d513-110">Type</span><span class="sxs-lookup"><span data-stu-id="1d513-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1d513-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1d513-111">Attributes and Elements</span></span>  
 <span data-ttu-id="1d513-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1d513-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1d513-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="1d513-113">Attributes</span></span>  
  
|<span data-ttu-id="1d513-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="1d513-114">Attribute</span></span>|<span data-ttu-id="1d513-115">Description</span><span class="sxs-lookup"><span data-stu-id="1d513-115">Description</span></span>|  
|---------------|-----------------|  
|`includeExceptionDetailInFaults`|<span data-ttu-id="1d513-116">Valeur qui spécifie si les objets de rappel client retournent au service des informations sur les exceptions managées dans les erreurs SOAP.</span><span class="sxs-lookup"><span data-stu-id="1d513-116">A value that specifies whether client callback objects return managed exception information in SOAP faults back to the service.</span></span><br /><br /> <span data-ttu-id="1d513-117">Si vous définissez cet attribut par programme à `true`, vous pouvez activer le retour du flux d'informations sur les exceptions managées dans un objet de rappel client, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="1d513-117">If you set this attribute to `true` programmatically, you can enable the flow of managed exception information in a client callback object back to the service for debugging purposes.</span></span> <span data-ttu-id="1d513-118">**Attention :**  Le retour des informations sur les exceptions managées aux clients peut entraîner un problème de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1d513-118">**Caution:**  Returning managed exception information to clients can be a security risk.</span></span> <span data-ttu-id="1d513-119">En effet, les détails de l'exception exposent des informations relatives à l'implémentation d'un service interne qui peuvent être utilisées par des clients non autorisés.</span><span class="sxs-lookup"><span data-stu-id="1d513-119">This is because exception details expose information about the internal service implementation that could be used by unauthorized clients.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1d513-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1d513-120">Child Elements</span></span>  
 <span data-ttu-id="1d513-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1d513-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1d513-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1d513-122">Parent Elements</span></span>  
  
|<span data-ttu-id="1d513-123">Élément</span><span class="sxs-lookup"><span data-stu-id="1d513-123">Element</span></span>|<span data-ttu-id="1d513-124">Description</span><span class="sxs-lookup"><span data-stu-id="1d513-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1d513-125">\<behavior></span><span class="sxs-lookup"><span data-stu-id="1d513-125">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="1d513-126">Spécifie un comportement de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1d513-126">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1d513-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d513-127">See also</span></span>
- <xref:System.ServiceModel.Configuration.CallbackDebugElement>
- <xref:System.ServiceModel.Description.CallbackDebugBehavior>
