---
title: <pnrpPeerResolver>
ms.date: 03/30/2017
ms.assetid: c1b34f3b-68e5-4911-a367-de49fb61dbc6
ms.openlocfilehash: 2404f00b2a3ba03e89c1e21fb25e13cabb8feed3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59214051"
---
# <a name="pnrppeerresolver"></a><span data-ttu-id="40516-101">\<pnrpPeerResolver></span><span class="sxs-lookup"><span data-stu-id="40516-101">\<pnrpPeerResolver></span></span>
<span data-ttu-id="40516-102">Spécifie que le programme de résolution PNRP (Peer Name Resolution Protocol) doit être utilisé comme un programme de résolution.</span><span class="sxs-lookup"><span data-stu-id="40516-102">Specifies that the PNRP (Peer Name Resolution Protocol) resolver is to be used as a resolver.</span></span> <span data-ttu-id="40516-103">Cet élément est facultatif parce que PNRP est le programme de résolution par défaut.</span><span class="sxs-lookup"><span data-stu-id="40516-103">This element is optional because PNRP is the default resolver.</span></span>  
  
 <span data-ttu-id="40516-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="40516-104">\<system.serviceModel></span></span>  
<span data-ttu-id="40516-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="40516-105">\<bindings></span></span>  
<span data-ttu-id="40516-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="40516-106">\<customBinding></span></span>  
<span data-ttu-id="40516-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="40516-107">\<binding></span></span>  
<span data-ttu-id="40516-108">\<pnrpResolver></span><span class="sxs-lookup"><span data-stu-id="40516-108">\<pnrpResolver></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="40516-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40516-109">Syntax</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="40516-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="40516-110">Attributes and Elements</span></span>  
 <span data-ttu-id="40516-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="40516-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="40516-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="40516-112">Attributes</span></span>  
  
|<span data-ttu-id="40516-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="40516-113">Attribute</span></span>|<span data-ttu-id="40516-114">Description</span><span class="sxs-lookup"><span data-stu-id="40516-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="40516-115">resolverType</span><span class="sxs-lookup"><span data-stu-id="40516-115">resolverType</span></span>|<span data-ttu-id="40516-116">Chaîne qui spécifie le programme de résolution à utiliser.</span><span class="sxs-lookup"><span data-stu-id="40516-116">A string that specifies the resolver to be used.</span></span> <span data-ttu-id="40516-117">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="40516-117">This attribute is optional.</span></span> <span data-ttu-id="40516-118">S'il n'est pas défini ou s'il a pour valeur une chaîne vide, PNRP est utilisé.</span><span class="sxs-lookup"><span data-stu-id="40516-118">If it is not set, or if it is set to an empty string, PNRP is used.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="40516-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="40516-119">Child Elements</span></span>  
 <span data-ttu-id="40516-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="40516-120">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="40516-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="40516-121">Parent Elements</span></span>  
  
|<span data-ttu-id="40516-122">Élément</span><span class="sxs-lookup"><span data-stu-id="40516-122">Element</span></span>|<span data-ttu-id="40516-123">Description</span><span class="sxs-lookup"><span data-stu-id="40516-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="40516-124">\<binding></span><span class="sxs-lookup"><span data-stu-id="40516-124">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="40516-125">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="40516-125">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="40516-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="40516-126">Example</span></span>  
  
```xml  
<pnrpResolver resolverType="String" />
```  
  
## <a name="see-also"></a><span data-ttu-id="40516-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40516-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.PnrpPeerResolverElement>
- <xref:System.ServiceModel.Channels.PnrpPeerResolverBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="40516-128">Liaisons</span><span class="sxs-lookup"><span data-stu-id="40516-128">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="40516-129">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="40516-129">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="40516-130">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="40516-130">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="40516-131">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="40516-131">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [<span data-ttu-id="40516-132">Programmes de résolution d'homologue</span><span class="sxs-lookup"><span data-stu-id="40516-132">Peer Resolvers</span></span>](../../../../../docs/framework/wcf/feature-details/peer-resolvers.md)
