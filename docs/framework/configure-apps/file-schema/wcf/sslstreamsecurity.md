---
title: '&lt;sslStreamSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 430a378b-a742-4858-8a12-9f9b235fd627
author: BrucePerlerMS
ms.openlocfilehash: 6eacf1833ecf980696d75c5dbcaaba3ba6403d92
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47087448"
---
# <a name="ltsslstreamsecuritygt"></a><span data-ttu-id="31d79-102">&lt;sslStreamSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="31d79-102">&lt;sslStreamSecurity&gt;</span></span>
<span data-ttu-id="31d79-103">Représente un élément de liaison personnalisé qui prend en charge la sécurité de canal à l’aide d’un flux SSL.</span><span class="sxs-lookup"><span data-stu-id="31d79-103">Represents a custom binding element that supports channel security using an SSL stream.</span></span>  
  
 <span data-ttu-id="31d79-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="31d79-104">\<system.serviceModel></span></span>  
<span data-ttu-id="31d79-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="31d79-105">\<bindings></span></span>  
<span data-ttu-id="31d79-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="31d79-106">\<customBinding></span></span>  
<span data-ttu-id="31d79-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="31d79-107">\<binding></span></span>  
<span data-ttu-id="31d79-108">\<sslStreamSecurity ></span><span class="sxs-lookup"><span data-stu-id="31d79-108">\<sslStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="31d79-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31d79-109">Syntax</span></span>  
  
```xml  
<sslStreamSecurity requireClientCertificate="Boolean"      sslProtocols="Ssl3|Tls|Tls11|Tls12" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="31d79-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="31d79-110">Attributes and Elements</span></span>  
 <span data-ttu-id="31d79-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="31d79-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="31d79-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="31d79-112">Attributes</span></span>  
  
|<span data-ttu-id="31d79-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="31d79-113">Attribute</span></span>|<span data-ttu-id="31d79-114">Description</span><span class="sxs-lookup"><span data-stu-id="31d79-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="31d79-115">requireClientCertificate</span><span class="sxs-lookup"><span data-stu-id="31d79-115">requireClientCertificate</span></span>|<span data-ttu-id="31d79-116">Valeur booléenne qui spécifie si un certificat client est requis pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="31d79-116">A Boolean value that specifies if a client certificate is required for this binding.</span></span> <span data-ttu-id="31d79-117">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="31d79-117">The default is `false`.</span></span>|  
|<span data-ttu-id="31d79-118">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="31d79-118">sslProtocols</span></span>|<span data-ttu-id="31d79-119">Valeur d'indicateur d'énumération SslProtocols qui spécifie les protocoles SSL pris en charge.</span><span class="sxs-lookup"><span data-stu-id="31d79-119">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="31d79-120">La valeur par défaut est Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span><span class="sxs-lookup"><span data-stu-id="31d79-120">The default is Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="31d79-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="31d79-121">Child Elements</span></span>  
 <span data-ttu-id="31d79-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="31d79-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="31d79-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="31d79-123">Parent Elements</span></span>  
  
|<span data-ttu-id="31d79-124">Élément</span><span class="sxs-lookup"><span data-stu-id="31d79-124">Element</span></span>|<span data-ttu-id="31d79-125">Description</span><span class="sxs-lookup"><span data-stu-id="31d79-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="31d79-126">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="31d79-126">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="31d79-127">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="31d79-127">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="31d79-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31d79-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.SslStreamSecurityElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>  
 [<span data-ttu-id="31d79-129">Liaisons</span><span class="sxs-lookup"><span data-stu-id="31d79-129">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="31d79-130">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="31d79-130">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="31d79-131">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="31d79-131">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="31d79-132">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="31d79-132">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
