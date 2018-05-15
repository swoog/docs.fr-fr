---
title: '&lt;privacyNoticeAt&gt;'
ms.date: 03/30/2017
ms.assetid: 4cc96942-4eb9-4241-b2fd-45aa239915e8
ms.openlocfilehash: 2914a3716b9e2adb6ebc47fd73ccee027a3b65da
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
---
# <a name="ltprivacynoticeatgt"></a><span data-ttu-id="58109-102">&lt;privacyNoticeAt&gt;</span><span class="sxs-lookup"><span data-stu-id="58109-102">&lt;privacyNoticeAt&gt;</span></span>
<span data-ttu-id="58109-103">Représente un élément de configuration qui spécifie un avis de confidentialité utilisé dans la liaison `wsFederationHttp`.</span><span class="sxs-lookup"><span data-stu-id="58109-103">Represents a configuration element that specifies a privacy notice used in `wsFederationHttp` binding.</span></span>  
  
 <span data-ttu-id="58109-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="58109-104">\<system.serviceModel></span></span>  
<span data-ttu-id="58109-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="58109-105">\<bindings></span></span>  
<span data-ttu-id="58109-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="58109-106">\<customBinding></span></span>  
<span data-ttu-id="58109-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="58109-107">\<binding></span></span>  
<span data-ttu-id="58109-108">\<privacyNotice ></span><span class="sxs-lookup"><span data-stu-id="58109-108">\<privacyNotice></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="58109-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58109-109">Syntax</span></span>  
  
```xml  
<privacyNotice url="String"  
        version="Integer" />  
```  
  
## <a name="type"></a><span data-ttu-id="58109-110">Type</span><span class="sxs-lookup"><span data-stu-id="58109-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="58109-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="58109-111">Attributes and Elements</span></span>  
 <span data-ttu-id="58109-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="58109-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="58109-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="58109-113">Attributes</span></span>  
  
|<span data-ttu-id="58109-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="58109-114">Attribute</span></span>|<span data-ttu-id="58109-115">Description</span><span class="sxs-lookup"><span data-stu-id="58109-115">Description</span></span>|  
|---------------|-----------------|  
|`url`|<span data-ttu-id="58109-116">Chaîne qui spécifie l'URI dans lequel l'information préalable de confidentialité est située.</span><span class="sxs-lookup"><span data-stu-id="58109-116">A string that specifies the URI at which the privacy notice is located.</span></span>|  
|`version`|<span data-ttu-id="58109-117">Entier qui spécifie la version de cet avis de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="58109-117">An integer that specifies the version of this privacy notice.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="58109-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="58109-118">Child Elements</span></span>  
 <span data-ttu-id="58109-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="58109-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="58109-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="58109-120">Parent Elements</span></span>  
  
|<span data-ttu-id="58109-121">Élément</span><span class="sxs-lookup"><span data-stu-id="58109-121">Element</span></span>|<span data-ttu-id="58109-122">Description</span><span class="sxs-lookup"><span data-stu-id="58109-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="58109-123">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="58109-123">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="58109-124">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="58109-124">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="58109-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58109-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PrivacyNoticeElement>  
 <xref:System.ServiceModel.Channels.PrivacyNoticeBindingElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 [<span data-ttu-id="58109-126">Liaisons</span><span class="sxs-lookup"><span data-stu-id="58109-126">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="58109-127">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="58109-127">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="58109-128">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="58109-128">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="58109-129">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="58109-129">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
