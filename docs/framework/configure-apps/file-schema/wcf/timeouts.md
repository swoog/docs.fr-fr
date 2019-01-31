---
title: <timeOuts>
ms.date: 03/30/2017
ms.assetid: 7fccd436-b326-48ec-8de1-c16817a09e0d
ms.openlocfilehash: 8a8a352380fe6eedb41ead089405e7b79fad29fe
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55272772"
---
# <a name="timeouts"></a><span data-ttu-id="dfb4c-101">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="dfb4c-101">\<timeOuts></span></span>
<span data-ttu-id="dfb4c-102">Représente un élément de configuration qui spécifie l'intervalle de temps pendant lequel l'ouverture ou la fermeture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-102">Represents a configuration element that specifies the interval of time allowed for the service host to open or close.</span></span>  
  
 <span data-ttu-id="dfb4c-103">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="dfb4c-103">\<system.ServiceModel></span></span>  
<span data-ttu-id="dfb4c-104">\<client></span><span class="sxs-lookup"><span data-stu-id="dfb4c-104">\<client></span></span>  
<span data-ttu-id="dfb4c-105">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="dfb4c-105">\<endpoint></span></span>  
<span data-ttu-id="dfb4c-106">\<host></span><span class="sxs-lookup"><span data-stu-id="dfb4c-106">\<host></span></span>  
<span data-ttu-id="dfb4c-107">\<timeOuts></span><span class="sxs-lookup"><span data-stu-id="dfb4c-107">\<timeOuts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfb4c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfb4c-108">Syntax</span></span>  
  
```xml  
<timeOuts closeTimeout="TimeSpan"
          openTimeout="TimeSpan" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dfb4c-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dfb4c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="dfb4c-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dfb4c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="dfb4c-111">Attributes</span></span>  
  
|<span data-ttu-id="dfb4c-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="dfb4c-112">Attribute</span></span>|<span data-ttu-id="dfb4c-113">Description</span><span class="sxs-lookup"><span data-stu-id="dfb4c-113">Description</span></span>|  
|---------------|-----------------|  
|`closeTimeout`|<span data-ttu-id="dfb4c-114">Valeur de type <xref:System.TimeSpan> qui spécifie l'intervalle de temps pendant lequel la fermeture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-114">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to close.</span></span>|  
|`openTimeout`|<span data-ttu-id="dfb4c-115">Valeur de type <xref:System.TimeSpan> qui spécifie l'intervalle de temps pendant lequel l'ouverture de l'hôte de service est autorisée.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-115">A <xref:System.TimeSpan> value that specifies the interval of time allowed for the service host to open.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dfb4c-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dfb4c-116">Child Elements</span></span>  
 <span data-ttu-id="dfb4c-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dfb4c-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dfb4c-118">Parent Elements</span></span>  
  
|<span data-ttu-id="dfb4c-119">Élément</span><span class="sxs-lookup"><span data-stu-id="dfb4c-119">Element</span></span>|<span data-ttu-id="dfb4c-120">Description</span><span class="sxs-lookup"><span data-stu-id="dfb4c-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="dfb4c-121">\<host></span><span class="sxs-lookup"><span data-stu-id="dfb4c-121">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="dfb4c-122">Élément de configuration qui spécifie des paramètres pour un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="dfb4c-122">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dfb4c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfb4c-123">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- [<span data-ttu-id="dfb4c-124">Hébergement</span><span class="sxs-lookup"><span data-stu-id="dfb4c-124">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
