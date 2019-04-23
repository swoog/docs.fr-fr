---
title: <persistenceProvider>
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: dc8dea0ddd1ea074c08952e3e2ebfef2d12f7183
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59099285"
---
# <a name="persistenceprovider"></a><span data-ttu-id="28c51-101">\<persistenceProvider></span><span class="sxs-lookup"><span data-stu-id="28c51-101">\<persistenceProvider></span></span>
<span data-ttu-id="28c51-102">Indique le type d'implémentation de fournisseur de persistance à utiliser, ainsi que le délai d'expiration à utiliser pour les opérations de persistance.</span><span class="sxs-lookup"><span data-stu-id="28c51-102">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
 <span data-ttu-id="28c51-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="28c51-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="28c51-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="28c51-104">\<behaviors></span></span>  
<span data-ttu-id="28c51-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="28c51-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="28c51-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="28c51-106">\<behavior></span></span>  
<span data-ttu-id="28c51-107">\<persistenceProvider></span><span class="sxs-lookup"><span data-stu-id="28c51-107">\<persistenceProvider></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28c51-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28c51-108">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="28c51-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="28c51-109">Attributes and Elements</span></span>  
 <span data-ttu-id="28c51-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="28c51-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="28c51-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="28c51-111">Attributes</span></span>  
  
|<span data-ttu-id="28c51-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="28c51-112">Attribute</span></span>|<span data-ttu-id="28c51-113">Description</span><span class="sxs-lookup"><span data-stu-id="28c51-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="28c51-114">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="28c51-114">persistenceOperationTimeout</span></span>|<span data-ttu-id="28c51-115">Valeur <xref:System.TimeSpan> indiquant le délai d'expiration utilisé pour les opérations de persistance.</span><span class="sxs-lookup"><span data-stu-id="28c51-115">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="28c51-116">La valeur par défaut est « 00 : 00:30 ».</span><span class="sxs-lookup"><span data-stu-id="28c51-116">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="28c51-117">type</span><span class="sxs-lookup"><span data-stu-id="28c51-117">type</span></span>|<span data-ttu-id="28c51-118">Chaîne indiquant le type à utiliser pour la fabrique de fournisseurs de persistance.</span><span class="sxs-lookup"><span data-stu-id="28c51-118">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="28c51-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="28c51-119">Child Elements</span></span>  
 <span data-ttu-id="28c51-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="28c51-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="28c51-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="28c51-121">Parent Elements</span></span>  
  
|<span data-ttu-id="28c51-122">Élément</span><span class="sxs-lookup"><span data-stu-id="28c51-122">Element</span></span>|<span data-ttu-id="28c51-123">Description</span><span class="sxs-lookup"><span data-stu-id="28c51-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="28c51-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="28c51-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="28c51-125">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="28c51-125">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="28c51-126">Notes</span><span class="sxs-lookup"><span data-stu-id="28c51-126">Remarks</span></span>  
 <span data-ttu-id="28c51-127">Cet élément spécifie le fournisseur de persistance à utiliser pour sérialiser l'état d'un service WCF.</span><span class="sxs-lookup"><span data-stu-id="28c51-127">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="28c51-128">Il doit être utilisé avec le `wsHttpContextBinding` qui transmet les informations d'état dans les en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="28c51-128">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28c51-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28c51-129">See also</span></span>

- <xref:System.ServiceModel.Configuration.PersistenceProviderElement>
- <xref:System.ServiceModel.Persistence.PersistenceProvider>
