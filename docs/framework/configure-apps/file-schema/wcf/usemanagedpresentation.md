---
title: <useManagedPresentation>
ms.date: 03/30/2017
ms.assetid: 17a0dd77-af54-41db-a9d0-4b17ff42878f
ms.openlocfilehash: eedf0ce6cf75b8fb56daf98f2005e66162ce10d8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59155647"
---
# <a name="usemanagedpresentation"></a><span data-ttu-id="ba089-101">\<useManagedPresentation></span><span class="sxs-lookup"><span data-stu-id="ba089-101">\<useManagedPresentation></span></span>
<span data-ttu-id="ba089-102">Élément de liaison utilisé pour communiquer avec un service d’émission de jeton de sécurité CardSpace qui prend en charge le profil CardSpace de WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="ba089-102">A binding element used to communicate with a CardSpace Security Token Service that supports the CardSpace profile of WS-Trust.</span></span> <span data-ttu-id="ba089-103">Cet élément n'a aucun attribut et est présent en tant que commutateur vide.</span><span class="sxs-lookup"><span data-stu-id="ba089-103">This element has no attribute and is present as an empty switch.</span></span>  
  
 <span data-ttu-id="ba089-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="ba089-104">\<system.serviceModel></span></span>  
<span data-ttu-id="ba089-105">\<bindings></span><span class="sxs-lookup"><span data-stu-id="ba089-105">\<bindings></span></span>  
<span data-ttu-id="ba089-106">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="ba089-106">\<customBinding></span></span>  
<span data-ttu-id="ba089-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="ba089-107">\<binding></span></span>  
<span data-ttu-id="ba089-108">\<useManagedPresentation></span><span class="sxs-lookup"><span data-stu-id="ba089-108">\<useManagedPresentation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ba089-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba089-109">Syntax</span></span>  
  
```xml  
<useManagedPresentation />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ba089-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ba089-110">Attributes and Elements</span></span>  
 <span data-ttu-id="ba089-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ba089-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ba089-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="ba089-112">Attributes</span></span>  
 <span data-ttu-id="ba089-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ba089-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="ba089-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ba089-114">Child Elements</span></span>  
 <span data-ttu-id="ba089-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ba089-115">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="ba089-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ba089-116">Parent Elements</span></span>  
  
|<span data-ttu-id="ba089-117">Élément</span><span class="sxs-lookup"><span data-stu-id="ba089-117">Element</span></span>|<span data-ttu-id="ba089-118">Description</span><span class="sxs-lookup"><span data-stu-id="ba089-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="ba089-119">\<binding></span><span class="sxs-lookup"><span data-stu-id="ba089-119">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="ba089-120">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="ba089-120">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ba089-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ba089-121">Remarks</span></span>  
 <span data-ttu-id="ba089-122">Cet élément est utilisé par un fournisseur d'identité pour exprimer dans sa stratégie le fait qu'il prend en charge le profil CardSpace de WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="ba089-122">This element is used by an identity provider to express in its policy the fact that it supports the CardSpace profile of WS-Trust.</span></span> <span data-ttu-id="ba089-123">Les fournisseurs d'identité qui publient une telle assertion de stratégie doivent être en mesure de publier des jetons selon ce profil CardSpace.</span><span class="sxs-lookup"><span data-stu-id="ba089-123">Identity providers that publish such a policy assertion should be able to issue tokens based on that CardSpace profile.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ba089-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba089-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.UseManagedPresentationElement>
- <xref:System.ServiceModel.Channels.UseManagedPresentationBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="ba089-125">Liaisons</span><span class="sxs-lookup"><span data-stu-id="ba089-125">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="ba089-126">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="ba089-126">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="ba089-127">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="ba089-127">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="ba089-128">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="ba089-128">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
