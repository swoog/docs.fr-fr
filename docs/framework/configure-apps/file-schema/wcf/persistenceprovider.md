---
title: '&lt;persistenceProvider&gt;'
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: 3c7fd74a84184ddbf8cc8db90141174ed84e5774
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltpersistenceprovidergt"></a><span data-ttu-id="9f2d6-102">&lt;persistenceProvider&gt;</span><span class="sxs-lookup"><span data-stu-id="9f2d6-102">&lt;persistenceProvider&gt;</span></span>
<span data-ttu-id="9f2d6-103">Indique le type d'implémentation de fournisseur de persistance à utiliser, ainsi que le délai d'expiration à utiliser pour les opérations de persistance.</span><span class="sxs-lookup"><span data-stu-id="9f2d6-103">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
 <span data-ttu-id="9f2d6-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="9f2d6-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="9f2d6-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="9f2d6-105">\<behaviors></span></span>  
<span data-ttu-id="9f2d6-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="9f2d6-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="9f2d6-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="9f2d6-107">\<behavior></span></span>  
<span data-ttu-id="9f2d6-108">\<persistenceProvider ></span><span class="sxs-lookup"><span data-stu-id="9f2d6-108">\<persistenceProvider></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f2d6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f2d6-109">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"  
   type="String" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9f2d6-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9f2d6-110">Attributes and Elements</span></span>  
 <span data-ttu-id="9f2d6-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9f2d6-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9f2d6-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="9f2d6-112">Attributes</span></span>  
  
|<span data-ttu-id="9f2d6-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="9f2d6-113">Attribute</span></span>|<span data-ttu-id="9f2d6-114">Description</span><span class="sxs-lookup"><span data-stu-id="9f2d6-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9f2d6-115">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="9f2d6-115">persistenceOperationTimeout</span></span>|<span data-ttu-id="9f2d6-116">Valeur <xref:System.TimeSpan> indiquant le délai d'expiration utilisé pour les opérations de persistance.</span><span class="sxs-lookup"><span data-stu-id="9f2d6-116">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="9f2d6-117">La valeur par défaut est « 00 : 00:30 ».</span><span class="sxs-lookup"><span data-stu-id="9f2d6-117">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="9f2d6-118">type</span><span class="sxs-lookup"><span data-stu-id="9f2d6-118">type</span></span>|<span data-ttu-id="9f2d6-119">Chaîne indiquant le type à utiliser pour la fabrique de fournisseurs de persistance.</span><span class="sxs-lookup"><span data-stu-id="9f2d6-119">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9f2d6-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9f2d6-120">Child Elements</span></span>  
 <span data-ttu-id="9f2d6-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9f2d6-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9f2d6-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9f2d6-122">Parent Elements</span></span>  
  
|<span data-ttu-id="9f2d6-123">Élément</span><span class="sxs-lookup"><span data-stu-id="9f2d6-123">Element</span></span>|<span data-ttu-id="9f2d6-124">Description</span><span class="sxs-lookup"><span data-stu-id="9f2d6-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9f2d6-125">\<behavior></span><span class="sxs-lookup"><span data-stu-id="9f2d6-125">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="9f2d6-126">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="9f2d6-126">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9f2d6-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9f2d6-127">Remarks</span></span>  
 <span data-ttu-id="9f2d6-128">Cet élément spécifie le fournisseur de persistance à utiliser pour sérialiser l'état d'un service WCF.</span><span class="sxs-lookup"><span data-stu-id="9f2d6-128">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="9f2d6-129">Il doit être utilisé avec le `wsHttpContextBinding` qui transmet les informations d'état dans les en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="9f2d6-129">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f2d6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f2d6-130">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PersistenceProviderElement>  
 <xref:System.ServiceModel.Persistence.PersistenceProvider>
