---
title: <sslStreamSecurity>
ms.date: 03/30/2017
ms.assetid: 430a378b-a742-4858-8a12-9f9b235fd627
ms.openlocfilehash: 67ec30b2bf3c322b949700789ce942e4281b77a4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61757987"
---
# <a name="sslstreamsecurity"></a><span data-ttu-id="42b6e-101">\<sslStreamSecurity></span><span class="sxs-lookup"><span data-stu-id="42b6e-101">\<sslStreamSecurity></span></span>
<span data-ttu-id="42b6e-102">Représente un élément de liaison personnalisé qui prend en charge la sécurité de canal à l'aide d'un flux SSL.</span><span class="sxs-lookup"><span data-stu-id="42b6e-102">Represents a custom binding element that supports channel security using an SSL stream.</span></span>  
  
 <span data-ttu-id="42b6e-103">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="42b6e-103">\<system.serviceModel></span></span>  
<span data-ttu-id="42b6e-104">\<bindings></span><span class="sxs-lookup"><span data-stu-id="42b6e-104">\<bindings></span></span>  
<span data-ttu-id="42b6e-105">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="42b6e-105">\<customBinding></span></span>  
<span data-ttu-id="42b6e-106">\<binding></span><span class="sxs-lookup"><span data-stu-id="42b6e-106">\<binding></span></span>  
<span data-ttu-id="42b6e-107">\<sslStreamSecurity></span><span class="sxs-lookup"><span data-stu-id="42b6e-107">\<sslStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="42b6e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42b6e-108">Syntax</span></span>  
  
```xml  
<sslStreamSecurity requireClientCertificate="Boolean"
                   sslProtocols="Ssl3|Tls|Tls11|Tls12" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="42b6e-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="42b6e-109">Attributes and Elements</span></span>  
 <span data-ttu-id="42b6e-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="42b6e-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="42b6e-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="42b6e-111">Attributes</span></span>  
  
|<span data-ttu-id="42b6e-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="42b6e-112">Attribute</span></span>|<span data-ttu-id="42b6e-113">Description</span><span class="sxs-lookup"><span data-stu-id="42b6e-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="42b6e-114">requireClientCertificate</span><span class="sxs-lookup"><span data-stu-id="42b6e-114">requireClientCertificate</span></span>|<span data-ttu-id="42b6e-115">Valeur booléenne qui spécifie si un certificat client est requis pour cette liaison.</span><span class="sxs-lookup"><span data-stu-id="42b6e-115">A Boolean value that specifies if a client certificate is required for this binding.</span></span> <span data-ttu-id="42b6e-116">La valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="42b6e-116">The default is `false`.</span></span>|  
|<span data-ttu-id="42b6e-117">sslProtocols</span><span class="sxs-lookup"><span data-stu-id="42b6e-117">sslProtocols</span></span>|<span data-ttu-id="42b6e-118">Valeur d'indicateur d'énumération SslProtocols qui spécifie les protocoles SSL pris en charge.</span><span class="sxs-lookup"><span data-stu-id="42b6e-118">A SslProtocols enum flag value that specifies which SslProtocols are supported.</span></span> <span data-ttu-id="42b6e-119">La valeur par défaut est Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span><span class="sxs-lookup"><span data-stu-id="42b6e-119">The default is Ssl3&#124;Tls&#124;Tls11&#124;Tls12.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="42b6e-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="42b6e-120">Child Elements</span></span>  
 <span data-ttu-id="42b6e-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="42b6e-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="42b6e-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="42b6e-122">Parent Elements</span></span>  
  
|<span data-ttu-id="42b6e-123">Élément</span><span class="sxs-lookup"><span data-stu-id="42b6e-123">Element</span></span>|<span data-ttu-id="42b6e-124">Description</span><span class="sxs-lookup"><span data-stu-id="42b6e-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="42b6e-125">\<binding></span><span class="sxs-lookup"><span data-stu-id="42b6e-125">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="42b6e-126">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="42b6e-126">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="42b6e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42b6e-127">See also</span></span>

- <xref:System.ServiceModel.Configuration.SslStreamSecurityElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- <xref:System.ServiceModel.Channels.SslStreamSecurityBindingElement>
- [<span data-ttu-id="42b6e-128">Liaisons</span><span class="sxs-lookup"><span data-stu-id="42b6e-128">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)
- [<span data-ttu-id="42b6e-129">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="42b6e-129">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [<span data-ttu-id="42b6e-130">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="42b6e-130">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [<span data-ttu-id="42b6e-131">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="42b6e-131">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
