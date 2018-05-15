---
title: '&lt;serviceAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 5d69e64f-f325-4d55-8e2d-0fb30f222dda
ms.openlocfilehash: 3b58214a1fd7a50fb1a9ab3dfee0a14870f8a476
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltserviceauthenticationmanagergt"></a><span data-ttu-id="f2c59-102">&lt;serviceAuthenticationManager&gt;</span><span class="sxs-lookup"><span data-stu-id="f2c59-102">&lt;serviceAuthenticationManager&gt;</span></span>
<span data-ttu-id="f2c59-103">Fournit un élément de configuration de flux de travail qui établit au niveau du service la validité d'une transmission, d'un message ou d'un expéditeur.</span><span class="sxs-lookup"><span data-stu-id="f2c59-103">Provides a workflow configuration element that establishes at the service level the validity of a transmission, message, or originator..</span></span>  
  
<span data-ttu-id="f2c59-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="f2c59-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="f2c59-105">\<comportements ></span><span class="sxs-lookup"><span data-stu-id="f2c59-105">\<behaviors></span></span>  
<span data-ttu-id="f2c59-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="f2c59-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="f2c59-107">\<comportement ></span><span class="sxs-lookup"><span data-stu-id="f2c59-107">\<behavior></span></span>  
<span data-ttu-id="f2c59-108">\<serviceAuthenticationManager ></span><span class="sxs-lookup"><span data-stu-id="f2c59-108">\<serviceAuthenticationManager></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2c59-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2c59-109">Syntax</span></span>  
  
```xml  
<behaviors>
  <serviceBehaviors>
    <behavior name="String">
      <serviceAuthenticationManager serviceAuthenticationManagerType="String" />
    </behavior>
  </serviceBehaviors>
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f2c59-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f2c59-110">Attributes and Elements</span></span>  
 <span data-ttu-id="f2c59-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="f2c59-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f2c59-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="f2c59-112">Attributes</span></span>  
  
|<span data-ttu-id="f2c59-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="f2c59-113">Attribute</span></span>|<span data-ttu-id="f2c59-114">Description</span><span class="sxs-lookup"><span data-stu-id="f2c59-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f2c59-115">serviceAuthenticationManagerType</span><span class="sxs-lookup"><span data-stu-id="f2c59-115">serviceAuthenticationManagerType</span></span>|<span data-ttu-id="f2c59-116">Chaîne qui spécifie le type de la stratégie d'authentification pour le comportement actuel.</span><span class="sxs-lookup"><span data-stu-id="f2c59-116">A string that specifies the type of the authentication policy for the current behavior.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f2c59-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f2c59-117">Child Elements</span></span>  
 <span data-ttu-id="f2c59-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f2c59-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="f2c59-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f2c59-119">Parent Elements</span></span>  
  
|<span data-ttu-id="f2c59-120">Élément</span><span class="sxs-lookup"><span data-stu-id="f2c59-120">Element</span></span>|<span data-ttu-id="f2c59-121">Description</span><span class="sxs-lookup"><span data-stu-id="f2c59-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="f2c59-122">\<behavior></span><span class="sxs-lookup"><span data-stu-id="f2c59-122">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="f2c59-123">Spécifie un élément de comportement.</span><span class="sxs-lookup"><span data-stu-id="f2c59-123">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f2c59-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2c59-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceAuthenticationElement>
