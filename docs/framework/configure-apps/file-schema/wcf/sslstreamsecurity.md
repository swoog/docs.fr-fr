---
title: '&lt;sslStreamSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 430a378b-a742-4858-8a12-9f9b235fd627
ms.openlocfilehash: ecc67c2b3972ccb5bc8a1fe9ae9b400292642d53
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50184489"
---
# <a name="ltsslstreamsecuritygt"></a><span data-ttu-id="4a6bb-102">&lt;sslStreamSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="4a6bb-102">&lt;sslStreamSecurity&gt;</span></span>
<span data-ttu-id="4a6bb-103">Représente un élément de liaison personnalisé qui prend en charge la sécurité de canal à l’aide d’un flux SSL.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-103">Represents a custom binding element that supports channel security using an SSL stream.</span></span>  
  
 <span data-ttu-id="4a6bb-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="4a6bb-104">\<system.serviceModel></span></span>  
<span data-ttu-id="4a6bb-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="4a6bb-105">\<bindings></span></span>  
<span data-ttu-id="4a6bb-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="4a6bb-106">\<customBinding></span></span>  
<span data-ttu-id="4a6bb-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="4a6bb-107">\<binding></span></span>  
<span data-ttu-id="4a6bb-108">\<sslStreamSecurity ></span><span class="sxs-lookup"><span data-stu-id="4a6bb-108">\<sslStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a6bb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a6bb-109">Syntax</span></span>  
  
```xml  
<sslStreamSecurity requireClientCertificate="Boolean"      sslProtocols="Ssl3|Tls|Tls11|Tls12" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4a6bb-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4a6bb-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4a6bb-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4a6bb-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="4a6bb-112">Attributes</span></span>  
  
|<span data-ttu-id="4a6bb-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="4a6bb-113">Attribute</span></span>|<span data-ttu-id="4a6bb-114">Description</span><span class="sxs-lookup"><span data-stu-id="4a6bb-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4a6bb-115">requireClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4a6bb-115">requireClientCertificate</span></span>|<span data-ttu-id="4a6bb-116">Valeur booléenne qui spécifie si un certificat client est requis pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-116">A Boolean value that specifies if a client certificate is required for this binding.</span></span> <span data-ttu-id="4a6bb-117">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-117">The default is `false`.</span></span>|  
|<span data-ttu-id="4a6bb-118">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="4a6bb-118">sslProtocols</span></span>|<span data-ttu-id="4a6bb-119">Valeur d'indicateur d'énumération SslProtocols qui spécifie les protocoles SSL pris en charge.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-119">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="4a6bb-120">La valeur par défaut est Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-120">The default is Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4a6bb-121">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4a6bb-121">Child Elements</span></span>  
 <span data-ttu-id="4a6bb-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-122">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4a6bb-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4a6bb-123">Parent Elements</span></span>  
  
|<span data-ttu-id="4a6bb-124">Élément</span><span class="sxs-lookup"><span data-stu-id="4a6bb-124">Element</span></span>|<span data-ttu-id="4a6bb-125">Description</span><span class="sxs-lookup"><span data-stu-id="4a6bb-125">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4a6bb-126">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="4a6bb-126">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="4a6bb-127">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4a6bb-127">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4a6bb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a6bb-128">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.SslStreamSecurityElement>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>  
 [<span data-ttu-id="4a6bb-129">Liaisons</span><span class="sxs-lookup"><span data-stu-id="4a6bb-129">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="4a6bb-130">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="4a6bb-130">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="4a6bb-131">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="4a6bb-131">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="4a6bb-132">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="4a6bb-132">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
