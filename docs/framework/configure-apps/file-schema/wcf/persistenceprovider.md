---
title: <persistenceProvider>
ms.date: 03/30/2017
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
ms.openlocfilehash: 054991687a54ecbf95cc18f58717a4ed3e36f050
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55260799"
---
# <a name="persistenceprovider"></a><span data-ttu-id="cad5f-101">\<persistenceProvider></span><span class="sxs-lookup"><span data-stu-id="cad5f-101">\<persistenceProvider></span></span>
<span data-ttu-id="cad5f-102">Indique le type d'implémentation de fournisseur de persistance à utiliser, ainsi que le délai d'expiration à utiliser pour les opérations de persistance.</span><span class="sxs-lookup"><span data-stu-id="cad5f-102">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
 <span data-ttu-id="cad5f-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="cad5f-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="cad5f-104">\<behaviors></span><span class="sxs-lookup"><span data-stu-id="cad5f-104">\<behaviors></span></span>  
<span data-ttu-id="cad5f-105">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="cad5f-105">\<serviceBehaviors></span></span>  
<span data-ttu-id="cad5f-106">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cad5f-106">\<behavior></span></span>  
<span data-ttu-id="cad5f-107">\<persistenceProvider></span><span class="sxs-lookup"><span data-stu-id="cad5f-107">\<persistenceProvider></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cad5f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cad5f-108">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"
                     type="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="cad5f-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="cad5f-109">Attributes and Elements</span></span>  
 <span data-ttu-id="cad5f-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="cad5f-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="cad5f-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="cad5f-111">Attributes</span></span>  
  
|<span data-ttu-id="cad5f-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="cad5f-112">Attribute</span></span>|<span data-ttu-id="cad5f-113">Description</span><span class="sxs-lookup"><span data-stu-id="cad5f-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="cad5f-114">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="cad5f-114">persistenceOperationTimeout</span></span>|<span data-ttu-id="cad5f-115">Valeur <xref:System.TimeSpan> indiquant le délai d'expiration utilisé pour les opérations de persistance.</span><span class="sxs-lookup"><span data-stu-id="cad5f-115">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="cad5f-116">La valeur par défaut est « 00 : 00:30 ».</span><span class="sxs-lookup"><span data-stu-id="cad5f-116">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="cad5f-117">type</span><span class="sxs-lookup"><span data-stu-id="cad5f-117">type</span></span>|<span data-ttu-id="cad5f-118">Chaîne indiquant le type à utiliser pour la fabrique de fournisseurs de persistance.</span><span class="sxs-lookup"><span data-stu-id="cad5f-118">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="cad5f-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cad5f-119">Child Elements</span></span>  
 <span data-ttu-id="cad5f-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cad5f-120">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="cad5f-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cad5f-121">Parent Elements</span></span>  
  
|<span data-ttu-id="cad5f-122">Élément</span><span class="sxs-lookup"><span data-stu-id="cad5f-122">Element</span></span>|<span data-ttu-id="cad5f-123">Description</span><span class="sxs-lookup"><span data-stu-id="cad5f-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="cad5f-124">\<behavior></span><span class="sxs-lookup"><span data-stu-id="cad5f-124">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="cad5f-125">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="cad5f-125">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cad5f-126">Notes</span><span class="sxs-lookup"><span data-stu-id="cad5f-126">Remarks</span></span>  
 <span data-ttu-id="cad5f-127">Cet élément spécifie le fournisseur de persistance à utiliser pour sérialiser l'état d'un service WCF.</span><span class="sxs-lookup"><span data-stu-id="cad5f-127">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="cad5f-128">Il doit être utilisé avec le `wsHttpContextBinding` qui transmet les informations d'état dans les en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="cad5f-128">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cad5f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cad5f-129">See also</span></span>
- <xref:System.ServiceModel.Configuration.PersistenceProviderElement>
- <xref:System.ServiceModel.Persistence.PersistenceProvider>
