---
title: '&lt;délais d’attente&gt;'
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: 1f0638f85177d2acb6f61e3246a1a5ee9a4e2f5c
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32752999"
---
# <a name="lttimeoutsgt"></a><span data-ttu-id="a6fee-102">&lt;délais d’attente&gt;</span><span class="sxs-lookup"><span data-stu-id="a6fee-102">&lt;timeOuts&gt;</span></span>
<span data-ttu-id="a6fee-103">Représente un élément de configuration qui spécifie l'intervalle de temps pendant lequel l'ouverture ou la fermeture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="a6fee-103">Represents a configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>  
  
 <span data-ttu-id="a6fee-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="a6fee-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="a6fee-105">\<client></span><span class="sxs-lookup"><span data-stu-id="a6fee-105">\<client></span></span>  
<span data-ttu-id="a6fee-106">\<point de terminaison ></span><span class="sxs-lookup"><span data-stu-id="a6fee-106">\<endpoint></span></span>  
<span data-ttu-id="a6fee-107">\<hôte ></span><span class="sxs-lookup"><span data-stu-id="a6fee-107">\<host></span></span>  
<span data-ttu-id="a6fee-108">\<délais d’attente ></span><span class="sxs-lookup"><span data-stu-id="a6fee-108">\<timeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6fee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6fee-109">Syntax</span></span>  
  
```xml  
<timeOuts closeTimeout="TimeSpan"  
   openTimeout="TimeSpan" >  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a6fee-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a6fee-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a6fee-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a6fee-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a6fee-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="a6fee-112">Attributes</span></span>  
  
|<span data-ttu-id="a6fee-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="a6fee-113">Attribute</span></span>|<span data-ttu-id="a6fee-114">Description</span><span class="sxs-lookup"><span data-stu-id="a6fee-114">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="a6fee-115">Valeur de type <xref:System.TimeSpan> qui spécifie l'intervalle de temps pendant lequel la fermeture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="a6fee-115">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to close.</span></span>|  
|`openTimeout`|<span data-ttu-id="a6fee-116">Valeur de type <xref:System.TimeSpan> qui spécifie l'intervalle de temps pendant lequel l'ouverture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="a6fee-116">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to open.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a6fee-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a6fee-117">Child Elements</span></span>  
 <span data-ttu-id="a6fee-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a6fee-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a6fee-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a6fee-119">Parent Elements</span></span>  
  
|<span data-ttu-id="a6fee-120">Élément</span><span class="sxs-lookup"><span data-stu-id="a6fee-120">Element</span></span>|<span data-ttu-id="a6fee-121">Description</span><span class="sxs-lookup"><span data-stu-id="a6fee-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a6fee-122">\<hôte ></span><span class="sxs-lookup"><span data-stu-id="a6fee-122">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="a6fee-123">Élément de configuration qui spécifie des paramètres pour un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="a6fee-123">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a6fee-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6fee-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 [<span data-ttu-id="a6fee-125">Hébergement</span><span class="sxs-lookup"><span data-stu-id="a6fee-125">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
