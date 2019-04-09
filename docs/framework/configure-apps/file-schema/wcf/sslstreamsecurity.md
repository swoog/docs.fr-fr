---
title: <sslStreamSecurity>
ms.date: 03/30/2017
ms.assetid: 430a378b-a742-4858-8a12-9f9b235fd627
ms.openlocfilehash: 67ec30b2bf3c322b949700789ce942e4281b77a4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59204443"
---
# <a name="sslstreamsecurity"></a><span data-ttu-id="625e6-101">\<sslStreamSecurity></span><span class="sxs-lookup"><span data-stu-id="625e6-101">\<sslStreamSecurity></span></span>
<span data-ttu-id="625e6-102">Représente un élément de liaison personnalisé qui prend en charge la sécurité de canal à l'aide d'un flux SSL.</span><span class="sxs-lookup"><span data-stu-id="625e6-102">Represents a custom binding element that supports channel security using an SSL stream.</span></span>  
  
 <span data-ttu-id="625e6-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="625e6-103">\<system.serviceModel></span></span>  
<span data-ttu-id="625e6-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="625e6-104">\<bindings></span></span>  
<span data-ttu-id="625e6-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="625e6-105">\<customBinding></span></span>  
<span data-ttu-id="625e6-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="625e6-106">\<binding></span></span>  
<span data-ttu-id="625e6-107">\<sslStreamSecurity></span><span class="sxs-lookup"><span data-stu-id="625e6-107">\<sslStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="625e6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="625e6-108">Syntax</span></span>  
  
```xml  
<sslStreamSecurity requireClientCertificate="Boolean"
                   sslProtocols="Ssl3|Tls|Tls11|Tls12" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="625e6-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="625e6-109">Attributes and Elements</span></span>  
 <span data-ttu-id="625e6-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="625e6-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="625e6-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="625e6-111">Attributes</span></span>  
  
|<span data-ttu-id="625e6-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="625e6-112">Attribute</span></span>|<span data-ttu-id="625e6-113">Description</span><span class="sxs-lookup"><span data-stu-id="625e6-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="625e6-114">requireClientCertificate</span><span class="sxs-lookup"><span data-stu-id="625e6-114">requireClientCertificate</span></span>|<span data-ttu-id="625e6-115">Valeur booléenne qui spécifie si un certificat client est requis pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="625e6-115">A Boolean value that specifies if a client certificate is required for this binding.</span></span> <span data-ttu-id="625e6-116">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="625e6-116">The default is `false`.</span></span>|  
|<span data-ttu-id="625e6-117">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="625e6-117">sslProtocols</span></span>|<span data-ttu-id="625e6-118">Valeur d'indicateur d'énumération SslProtocols qui spécifie les protocoles SSL pris en charge.</span><span class="sxs-lookup"><span data-stu-id="625e6-118">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="625e6-119">La valeur par défaut est Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span><span class="sxs-lookup"><span data-stu-id="625e6-119">The default is Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="625e6-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="625e6-120">Child Elements</span></span>  
 <span data-ttu-id="625e6-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="625e6-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="625e6-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="625e6-122">Parent Elements</span></span>  
  
|<span data-ttu-id="625e6-123">Élément</span><span class="sxs-lookup"><span data-stu-id="625e6-123">Element</span></span>|<span data-ttu-id="625e6-124">Description</span><span class="sxs-lookup"><span data-stu-id="625e6-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="625e6-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="625e6-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="625e6-126">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="625e6-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="625e6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="625e6-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.SslStreamSecurityElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>
- [<span data-ttu-id="625e6-128">Liaisons</span><span class="sxs-lookup"><span data-stu-id="625e6-128">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="625e6-129">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="625e6-129">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="625e6-130">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="625e6-130">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="625e6-131">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="625e6-131">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
