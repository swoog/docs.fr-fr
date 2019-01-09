---
title: '&lt;serviceAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 5d69e64f-f325-4d55-8e2d-0fb30f222dda
ms.openlocfilehash: 3456ffa952372b014d579b5c420f7c44222fdad5
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54145352"
---
# <a name="ltserviceauthenticationmanagergt"></a><span data-ttu-id="b6d04-102">&lt;serviceAuthenticationManager&gt;</span><span class="sxs-lookup"><span data-stu-id="b6d04-102">&lt;serviceAuthenticationManager&gt;</span></span>
<span data-ttu-id="b6d04-103">Fournit un élément de configuration de flux de travail qui établit au niveau du service la validité d'une transmission, d'un message ou d'un donneur d'ordre.</span><span class="sxs-lookup"><span data-stu-id="b6d04-103">Provides a workflow configuration element that establishes at the service level the validity of a transmission, message, or originator.</span></span>  
  
<span data-ttu-id="b6d04-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="b6d04-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="b6d04-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="b6d04-105">\<behaviors></span></span>  
<span data-ttu-id="b6d04-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="b6d04-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="b6d04-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="b6d04-107">\<behavior></span></span>  
<span data-ttu-id="b6d04-108">\<serviceAuthenticationManager ></span><span class="sxs-lookup"><span data-stu-id="b6d04-108">\<serviceAuthenticationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6d04-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6d04-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceAuthenticationManager serviceAuthenticationManagerType="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b6d04-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b6d04-110">Attributes and Elements</span></span>  
 <span data-ttu-id="b6d04-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b6d04-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b6d04-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="b6d04-112">Attributes</span></span>  
  
|<span data-ttu-id="b6d04-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="b6d04-113">Attribute</span></span>|<span data-ttu-id="b6d04-114">Description</span><span class="sxs-lookup"><span data-stu-id="b6d04-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="b6d04-115">serviceAuthenticationManagerType</span><span class="sxs-lookup"><span data-stu-id="b6d04-115">serviceAuthenticationManagerType</span></span>|<span data-ttu-id="b6d04-116">Chaîne qui spécifie le type de la stratégie d'authentification pour le comportement actuel.</span><span class="sxs-lookup"><span data-stu-id="b6d04-116">A string that specifies the type of the authentication policy for the current behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="b6d04-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b6d04-117">Child Elements</span></span>  
 <span data-ttu-id="b6d04-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b6d04-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="b6d04-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b6d04-119">Parent Elements</span></span>  
  
|<span data-ttu-id="b6d04-120">Élément</span><span class="sxs-lookup"><span data-stu-id="b6d04-120">Element</span></span>|<span data-ttu-id="b6d04-121">Description</span><span class="sxs-lookup"><span data-stu-id="b6d04-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b6d04-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="b6d04-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="b6d04-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="b6d04-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b6d04-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6d04-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceAuthenticationElement>
