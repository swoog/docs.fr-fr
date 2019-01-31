---
title: <sslStreamSecurity>
ms.date: 03/30/2017
ms.assetid: 430a378b-a742-4858-8a12-9f9b235fd627
ms.openlocfilehash: f66569f36dc61a063b79a088dcbc405126a074d8
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55284594"
---
# <a name="sslstreamsecurity"></a><span data-ttu-id="de94c-101">\<sslStreamSecurity></span><span class="sxs-lookup"><span data-stu-id="de94c-101">\<sslStreamSecurity></span></span>
<span data-ttu-id="de94c-102">Représente un élément de liaison personnalisé qui prend en charge la sécurité de canal à l’aide d’un flux SSL.</span><span class="sxs-lookup"><span data-stu-id="de94c-102">Represents a custom binding element that supports channel security using an SSL stream.</span></span>  
  
 <span data-ttu-id="de94c-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="de94c-103">\<system.serviceModel></span></span>  
<span data-ttu-id="de94c-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="de94c-104">\<bindings></span></span>  
<span data-ttu-id="de94c-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="de94c-105">\<customBinding></span></span>  
<span data-ttu-id="de94c-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="de94c-106">\<binding></span></span>  
<span data-ttu-id="de94c-107">\<sslStreamSecurity></span><span class="sxs-lookup"><span data-stu-id="de94c-107">\<sslStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="de94c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de94c-108">Syntax</span></span>  
  
```xml  
<sslStreamSecurity requireClientCertificate="Boolean"
                   sslProtocols="Ssl3|Tls|Tls11|Tls12" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="de94c-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="de94c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="de94c-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="de94c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="de94c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="de94c-111">Attributes</span></span>  
  
|<span data-ttu-id="de94c-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="de94c-112">Attribute</span></span>|<span data-ttu-id="de94c-113">Description</span><span class="sxs-lookup"><span data-stu-id="de94c-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="de94c-114">requireClientCertificate</span><span class="sxs-lookup"><span data-stu-id="de94c-114">requireClientCertificate</span></span>|<span data-ttu-id="de94c-115">Valeur booléenne qui spécifie si un certificat client est requis pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="de94c-115">A Boolean value that specifies if a client certificate is required for this binding.</span></span> <span data-ttu-id="de94c-116">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="de94c-116">The default is `false`.</span></span>|  
|<span data-ttu-id="de94c-117">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="de94c-117">sslProtocols</span></span>|<span data-ttu-id="de94c-118">Valeur d'indicateur d'énumération SslProtocols qui spécifie les protocoles SSL pris en charge.</span><span class="sxs-lookup"><span data-stu-id="de94c-118">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="de94c-119">La valeur par défaut est Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span><span class="sxs-lookup"><span data-stu-id="de94c-119">The default is Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="de94c-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="de94c-120">Child Elements</span></span>  
 <span data-ttu-id="de94c-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="de94c-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="de94c-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="de94c-122">Parent Elements</span></span>  
  
|<span data-ttu-id="de94c-123">Élément</span><span class="sxs-lookup"><span data-stu-id="de94c-123">Element</span></span>|<span data-ttu-id="de94c-124">Description</span><span class="sxs-lookup"><span data-stu-id="de94c-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="de94c-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="de94c-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="de94c-126">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="de94c-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="de94c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de94c-127">See also</span></span>
- <xref:System.ServiceModel.Configuration.SslStreamSecurityElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>
- [<span data-ttu-id="de94c-128">Liaisons</span><span class="sxs-lookup"><span data-stu-id="de94c-128">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="de94c-129">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="de94c-129">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="de94c-130">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="de94c-130">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="de94c-131">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="de94c-131">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
