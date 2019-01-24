---
title: '&lt;timeOuts&gt;'
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: 42f4db1d954834cbfa3c526328cca45443751506
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54629655"
---
# <a name="lttimeoutsgt"></a><span data-ttu-id="0aba4-102">&lt;timeOuts&gt;</span><span class="sxs-lookup"><span data-stu-id="0aba4-102">&lt;timeOuts&gt;</span></span>
<span data-ttu-id="0aba4-103">Représente un élément de configuration qui spécifie l'intervalle de temps pendant lequel l'ouverture ou la fermeture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="0aba4-103">Represents a configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>  
  
 <span data-ttu-id="0aba4-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="0aba4-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0aba4-105">\<client></span><span class="sxs-lookup"><span data-stu-id="0aba4-105">\<client></span></span>  
<span data-ttu-id="0aba4-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="0aba4-106">\<endpoint></span></span>  
<span data-ttu-id="0aba4-107">\<host></span><span class="sxs-lookup"><span data-stu-id="0aba4-107">\<host></span></span>  
<span data-ttu-id="0aba4-108">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="0aba4-108">\<timeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0aba4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0aba4-109">Syntax</span></span>  
  
```xml  
<timeOuts closeTimeout="TimeSpan"
          openTimeout="TimeSpan" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0aba4-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0aba4-110">Attributes and Elements</span></span>  
 <span data-ttu-id="0aba4-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0aba4-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0aba4-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="0aba4-112">Attributes</span></span>  
  
|<span data-ttu-id="0aba4-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="0aba4-113">Attribute</span></span>|<span data-ttu-id="0aba4-114">Description</span><span class="sxs-lookup"><span data-stu-id="0aba4-114">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="0aba4-115">Valeur de type <xref:System.TimeSpan> qui spécifie l'intervalle de temps pendant lequel la fermeture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="0aba4-115">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to close.</span></span>|  
|`openTimeout`|<span data-ttu-id="0aba4-116">Valeur de type <xref:System.TimeSpan> qui spécifie l'intervalle de temps pendant lequel l'ouverture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="0aba4-116">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to open.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0aba4-117">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0aba4-117">Child Elements</span></span>  
 <span data-ttu-id="0aba4-118">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0aba4-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="0aba4-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0aba4-119">Parent Elements</span></span>  
  
|<span data-ttu-id="0aba4-120">Élément</span><span class="sxs-lookup"><span data-stu-id="0aba4-120">Element</span></span>|<span data-ttu-id="0aba4-121">Description</span><span class="sxs-lookup"><span data-stu-id="0aba4-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0aba4-122">\<host></span><span class="sxs-lookup"><span data-stu-id="0aba4-122">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="0aba4-123">Élément de configuration qui spécifie des paramètres pour un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="0aba4-123">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0aba4-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aba4-124">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="0aba4-125">Hébergement</span><span class="sxs-lookup"><span data-stu-id="0aba4-125">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
