---
title: '&lt;add&gt; de &lt;baseAddress&gt;'
ms.date: 03/30/2017
ms.assetid: 1bd7426f-5f4f-43fc-b8e9-de842219aa32
ms.openlocfilehash: 31edf570a7374a4b4fe31760d35ec196ecfcb3c6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54553566"
---
# <a name="ltaddgt-of-ltbaseaddressesgt"></a><span data-ttu-id="d9834-102">&lt;add&gt; de &lt;baseAddress&gt;</span><span class="sxs-lookup"><span data-stu-id="d9834-102">&lt;add&gt; of &lt;baseAddresses&gt;</span></span>
<span data-ttu-id="d9834-103">Représente un élément de configuration qui spécifie les adresses de base utilisées par l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="d9834-103">Represents a configuration element that specifies the base addresses used by the service host.</span></span>  
  
 <span data-ttu-id="d9834-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="d9834-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="d9834-105">\<client></span><span class="sxs-lookup"><span data-stu-id="d9834-105">\<client></span></span>  
<span data-ttu-id="d9834-106">\<endpoint></span><span class="sxs-lookup"><span data-stu-id="d9834-106">\<endpoint></span></span>  
<span data-ttu-id="d9834-107">\<host></span><span class="sxs-lookup"><span data-stu-id="d9834-107">\<host></span></span>  
<span data-ttu-id="d9834-108">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="d9834-108">\<baseAddresses></span></span>  
<span data-ttu-id="d9834-109">\<baseAddress></span><span class="sxs-lookup"><span data-stu-id="d9834-109">\<baseAddress></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9834-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9834-110">Syntax</span></span>  
  
```xml  
<add baseAddress="string" />
```  
  
## <a name="type"></a><span data-ttu-id="d9834-111">Type</span><span class="sxs-lookup"><span data-stu-id="d9834-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d9834-112">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d9834-112">Attributes and Elements</span></span>  
 <span data-ttu-id="d9834-113">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d9834-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d9834-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="d9834-114">Attributes</span></span>  
  
|<span data-ttu-id="d9834-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="d9834-115">Attribute</span></span>|<span data-ttu-id="d9834-116">Description</span><span class="sxs-lookup"><span data-stu-id="d9834-116">Description</span></span>|  
|---------------|-----------------|  
|`baseAddress`|<span data-ttu-id="d9834-117">Chaîne indiquant une adresse de base utilisée par l'hôte de service.</span><span class="sxs-lookup"><span data-stu-id="d9834-117">A string that specifies a base address used by the service host.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d9834-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d9834-118">Child Elements</span></span>  
 <span data-ttu-id="d9834-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d9834-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d9834-120">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d9834-120">Parent Elements</span></span>  
  
|<span data-ttu-id="d9834-121">Élément</span><span class="sxs-lookup"><span data-stu-id="d9834-121">Element</span></span>|<span data-ttu-id="d9834-122">Description</span><span class="sxs-lookup"><span data-stu-id="d9834-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d9834-123">\<baseAddresses></span><span class="sxs-lookup"><span data-stu-id="d9834-123">\<baseAddresses></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/baseaddresses.md)|<span data-ttu-id="d9834-124">Collection d'éléments `baseAddress`.</span><span class="sxs-lookup"><span data-stu-id="d9834-124">A collection of `baseAddress` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d9834-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9834-125">See also</span></span>
- <xref:System.ServiceModel.Configuration.HostElement>
- <xref:System.ServiceModel.ServiceHost>
- <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>
- [<span data-ttu-id="d9834-126">Hébergement</span><span class="sxs-lookup"><span data-stu-id="d9834-126">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
