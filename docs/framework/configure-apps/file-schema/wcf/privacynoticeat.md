---
title: <privacyNoticeAt>
ms.date: 03/30/2017
ms.assetid: 4cc96942-4eb9-4241-b2fd-45aa239915e8
ms.openlocfilehash: e2ce2111e4bb26cc6a51b4a772b1d8a4d3238c70
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59200764"
---
# <a name="privacynoticeat"></a><span data-ttu-id="820e1-101">\<privacyNoticeAt></span><span class="sxs-lookup"><span data-stu-id="820e1-101">\<privacyNoticeAt></span></span>
<span data-ttu-id="820e1-102">Représente un élément de configuration qui spécifie un avis de confidentialité utilisé dans la liaison `wsFederationHttp`.</span><span class="sxs-lookup"><span data-stu-id="820e1-102">Represents a configuration element that specifies a privacy notice used in `wsFederationHttp` binding.</span></span>  
  
 <span data-ttu-id="820e1-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="820e1-103">\<system.serviceModel></span></span>  
<span data-ttu-id="820e1-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="820e1-104">\<bindings></span></span>  
<span data-ttu-id="820e1-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="820e1-105">\<customBinding></span></span>  
<span data-ttu-id="820e1-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="820e1-106">\<binding></span></span>  
<span data-ttu-id="820e1-107">\<privacyNotice></span><span class="sxs-lookup"><span data-stu-id="820e1-107">\<privacyNotice></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="820e1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="820e1-108">Syntax</span></span>  
  
```xml  
<privacyNotice url="String"
               version="Integer" />
```  
  
## <a name="type"></a><span data-ttu-id="820e1-109">Type</span><span class="sxs-lookup"><span data-stu-id="820e1-109">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="820e1-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="820e1-110">Attributes and Elements</span></span>  
 <span data-ttu-id="820e1-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="820e1-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="820e1-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="820e1-112">Attributes</span></span>  
  
|<span data-ttu-id="820e1-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="820e1-113">Attribute</span></span>|<span data-ttu-id="820e1-114">Description</span><span class="sxs-lookup"><span data-stu-id="820e1-114">Description</span></span>|  
|---------------|-----------------|  
|`url`|<span data-ttu-id="820e1-115">Chaîne qui spécifie l'URI dans lequel l'information préalable de confidentialité est située.</span><span class="sxs-lookup"><span data-stu-id="820e1-115">A string that specifies the URI at which the privacy notice is located.</span></span>|  
|`version`|<span data-ttu-id="820e1-116">Entier qui spécifie la version de cet avis de confidentialité.</span><span class="sxs-lookup"><span data-stu-id="820e1-116">An integer that specifies the version of this privacy notice.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="820e1-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="820e1-117">Child Elements</span></span>  
 <span data-ttu-id="820e1-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="820e1-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="820e1-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="820e1-119">Parent Elements</span></span>  
  
|<span data-ttu-id="820e1-120">Élément</span><span class="sxs-lookup"><span data-stu-id="820e1-120">Element</span></span>|<span data-ttu-id="820e1-121">Description</span><span class="sxs-lookup"><span data-stu-id="820e1-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="820e1-122">\<binding></span><span class="sxs-lookup"><span data-stu-id="820e1-122">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="820e1-123">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="820e1-123">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="820e1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="820e1-124">See also</span></span>

- <xref:System.ServiceModel.Configuration.PrivacyNoticeElement>
- <xref:System.ServiceModel.Channels.PrivacyNoticeBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [<span data-ttu-id="820e1-125">Liaisons</span><span class="sxs-lookup"><span data-stu-id="820e1-125">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="820e1-126">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="820e1-126">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="820e1-127">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="820e1-127">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="820e1-128">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="820e1-128">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
