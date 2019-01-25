---
title: '&lt;pnrpPeerResolver&gt;'
ms.date: 03/30/2017
ms.assetid: c1b34f3b-68e5-4911-a367-de49fb61dbc6
ms.openlocfilehash: cefd46d7810149264f9c431a212da0f3f51f8186
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577644"
---
# <a name="ltpnrppeerresolvergt"></a><span data-ttu-id="4f0c2-102">&lt;pnrpPeerResolver&gt;</span><span class="sxs-lookup"><span data-stu-id="4f0c2-102">&lt;pnrpPeerResolver&gt;</span></span>
<span data-ttu-id="4f0c2-103">Spécifie que le programme de résolution PNRP (Peer Name Resolution Protocol) doit être utilisé comme un programme de résolution.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-103">Specifies that the PNRP (Peer Name Resolution Protocol) resolver is to be used as a resolver.</span></span> <span data-ttu-id="4f0c2-104">Cet élément est facultatif parce que PNRP est le programme de résolution par défaut.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-104">This element is optional because PNRP is the default resolver.</span></span>  
  
 <span data-ttu-id="4f0c2-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4f0c2-105">\<system.serviceModel></span></span>  
<span data-ttu-id="4f0c2-106">\<bindings></span><span class="sxs-lookup"><span data-stu-id="4f0c2-106">\<bindings></span></span>  
<span data-ttu-id="4f0c2-107">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4f0c2-107">\<customBinding></span></span>  
<span data-ttu-id="4f0c2-108">\<binding></span><span class="sxs-lookup"><span data-stu-id="4f0c2-108">\<binding></span></span>  
<span data-ttu-id="4f0c2-109">\<pnrpResolver></span><span class="sxs-lookup"><span data-stu-id="4f0c2-109">\<pnrpResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f0c2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f0c2-110">Syntax</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4f0c2-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4f0c2-111">Attributes and Elements</span></span>  
 <span data-ttu-id="4f0c2-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4f0c2-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="4f0c2-113">Attributes</span></span>  
  
|<span data-ttu-id="4f0c2-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="4f0c2-114">Attribute</span></span>|<span data-ttu-id="4f0c2-115">Description</span><span class="sxs-lookup"><span data-stu-id="4f0c2-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4f0c2-116">resolverType</span><span class="sxs-lookup"><span data-stu-id="4f0c2-116">resolverType</span></span>|<span data-ttu-id="4f0c2-117">Chaîne qui spécifie le programme de résolution à utiliser.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-117">A string that specifies the resolver to be used.</span></span> <span data-ttu-id="4f0c2-118">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-118">This attribute is optional.</span></span> <span data-ttu-id="4f0c2-119">S'il n'est pas défini ou s'il a pour valeur une chaîne vide, PNRP est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-119">If it is not set, or if it is set to an empty string, PNRP is used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4f0c2-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4f0c2-120">Child Elements</span></span>  
 <span data-ttu-id="4f0c2-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-121">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4f0c2-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4f0c2-122">Parent Elements</span></span>  
  
|<span data-ttu-id="4f0c2-123">Élément</span><span class="sxs-lookup"><span data-stu-id="4f0c2-123">Element</span></span>|<span data-ttu-id="4f0c2-124">Description</span><span class="sxs-lookup"><span data-stu-id="4f0c2-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4f0c2-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="4f0c2-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="4f0c2-126">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4f0c2-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="4f0c2-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="4f0c2-127">Example</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="see-also"></a><span data-ttu-id="4f0c2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f0c2-128">See also</span></span>
- <xref:System.ServiceModel.Configuration.PnrpPeerResolverElement>
- <xref:System.ServiceModel.Channels.PnrpPeerResolverBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="4f0c2-129">Liaisons</span><span class="sxs-lookup"><span data-stu-id="4f0c2-129">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="4f0c2-130">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="4f0c2-130">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="4f0c2-131">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="4f0c2-131">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="4f0c2-132">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4f0c2-132">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [<span data-ttu-id="4f0c2-133">Programmes de résolution d’homologue</span><span class="sxs-lookup"><span data-stu-id="4f0c2-133">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
