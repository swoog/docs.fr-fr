---
title: '&lt;useManagedPresentation&gt;'
ms.date: 03/30/2017
ms.assetid: 17a0dd77-af54-41db-a9d0-4b17ff42878f
ms.openlocfilehash: a60e1e16b9b41cc5df4ded51cc05d6109dd7b3dc
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54147705"
---
# <a name="ltusemanagedpresentationgt"></a><span data-ttu-id="4fc82-102">&lt;useManagedPresentation&gt;</span><span class="sxs-lookup"><span data-stu-id="4fc82-102">&lt;useManagedPresentation&gt;</span></span>
<span data-ttu-id="4fc82-103">Élément de liaison utilisé pour communiquer avec un service d’émission de jeton de sécurité CardSpace qui prend en charge le profil CardSpace de WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="4fc82-103">A binding element used to communicate with a CardSpace Security Token Service that supports the CardSpace profile of WS-Trust.</span></span> <span data-ttu-id="4fc82-104">Cet élément n'a aucun attribut et est présent en tant que commutateur vide.</span><span class="sxs-lookup"><span data-stu-id="4fc82-104">This element has no attribute and is present as an empty switch.</span></span>  
  
 <span data-ttu-id="4fc82-105">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4fc82-105">\<system.serviceModel></span></span>  
<span data-ttu-id="4fc82-106">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="4fc82-106">\<bindings></span></span>  
<span data-ttu-id="4fc82-107">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="4fc82-107">\<customBinding></span></span>  
<span data-ttu-id="4fc82-108">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="4fc82-108">\<binding></span></span>  
<span data-ttu-id="4fc82-109">\<useManagedPresentation ></span><span class="sxs-lookup"><span data-stu-id="4fc82-109">\<useManagedPresentation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4fc82-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fc82-110">Syntax</span></span>  
  
```xml  
<useManagedPresentation />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4fc82-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4fc82-111">Attributes and Elements</span></span>  
 <span data-ttu-id="4fc82-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4fc82-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4fc82-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="4fc82-113">Attributes</span></span>  
 <span data-ttu-id="4fc82-114">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4fc82-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4fc82-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4fc82-115">Child Elements</span></span>  
 <span data-ttu-id="4fc82-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4fc82-116">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4fc82-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4fc82-117">Parent Elements</span></span>  
  
|<span data-ttu-id="4fc82-118">Élément</span><span class="sxs-lookup"><span data-stu-id="4fc82-118">Element</span></span>|<span data-ttu-id="4fc82-119">Description</span><span class="sxs-lookup"><span data-stu-id="4fc82-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4fc82-120">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="4fc82-120">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="4fc82-121">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4fc82-121">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4fc82-122">Notes</span><span class="sxs-lookup"><span data-stu-id="4fc82-122">Remarks</span></span>  
 <span data-ttu-id="4fc82-123">Cet élément est utilisé par un fournisseur d'identité pour exprimer dans sa stratégie le fait qu'il prend en charge le profil CardSpace de WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="4fc82-123">This element is used by an identity provider to express in its policy the fact that it supports the CardSpace profile of WS-Trust.</span></span> <span data-ttu-id="4fc82-124">Les fournisseurs d'identité qui publient une telle assertion de stratégie doivent être en mesure de publier des jetons selon ce profil CardSpace.</span><span class="sxs-lookup"><span data-stu-id="4fc82-124">Identity providers that publish such a policy assertion should be able to issue tokens based on that CardSpace profile.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4fc82-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fc82-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.UseManagedPresentationElement>  
 <xref:System.ServiceModel.Channels.UseManagedPresentationBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="4fc82-126">Liaisons</span><span class="sxs-lookup"><span data-stu-id="4fc82-126">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="4fc82-127">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="4fc82-127">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="4fc82-128">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="4fc82-128">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="4fc82-129">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4fc82-129">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
