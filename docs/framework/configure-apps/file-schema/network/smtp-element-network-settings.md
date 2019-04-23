---
title: <smtp>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp
- http://schemas.microsoft.com/.NetConfiguration/v2.0#smtp
helpviewer_keywords:
- <smtp> element
- smtp element
ms.assetid: 220b0329-e384-4e0c-86b4-0945ad17efd9
ms.openlocfilehash: 1b5f7406f995a86f0a192dbf3249c067dff570ea
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59140372"
---
# <a name="smtp-element-network-settings"></a><span data-ttu-id="ecd9c-102">\<SMTP >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="ecd9c-102">\<smtp> Element (Network Settings)</span></span>
<span data-ttu-id="ecd9c-103">Configure le format de remise, la méthode de remise et à partir de l’adresse pour l’envoi des e-mails.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-103">Configures the delivery format, delivery method, and from address for sending emails.</span></span>  
  
 <span data-ttu-id="ecd9c-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="ecd9c-104">\<configuration></span></span>  
<span data-ttu-id="ecd9c-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="ecd9c-105">\<system.net></span></span>  
<span data-ttu-id="ecd9c-106">\<mailSettings></span><span class="sxs-lookup"><span data-stu-id="ecd9c-106">\<mailSettings></span></span>  
<span data-ttu-id="ecd9c-107">\<smtp></span><span class="sxs-lookup"><span data-stu-id="ecd9c-107">\<smtp></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ecd9c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecd9c-108">Syntax</span></span>  
  
```xml  
<smtp  
  deliveryFormat="format"  
  deliveryMethod="method"  
  from="from address">
    <specifiedPickupDirectory>...</specifiedPickupDirectory>  
    <network>...</network>  
</smtp>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="ecd9c-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="ecd9c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="ecd9c-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="ecd9c-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="ecd9c-111">Attributes</span></span>  
  
|<span data-ttu-id="ecd9c-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="ecd9c-112">Attribute</span></span>|<span data-ttu-id="ecd9c-113">Description</span><span class="sxs-lookup"><span data-stu-id="ecd9c-113">Description</span></span>|  
|---------------|-----------------|  
|`deliveryFormat`|<span data-ttu-id="ecd9c-114">Spécifie le format de remise de messages électroniques sortants.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-114">Specifies the delivery format for outgoing emails.</span></span> <span data-ttu-id="ecd9c-115">Les valeurs acceptables sont SevenBit et International.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-115">Acceptable values are SevenBit and International.</span></span>|  
|`deliveryMethod`|<span data-ttu-id="ecd9c-116">Spécifie la méthode de remise pour les e-mails.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-116">Specifies the delivery method for emails.</span></span> <span data-ttu-id="ecd9c-117">Les valeurs acceptables sont réseau, PickupDirectoryFromIis et SpecifiedPickupDirectory.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-117">Acceptable values are Network, PickupDirectoryFromIis, and SpecifiedPickupDirectory.</span></span>|  
|`from`|<span data-ttu-id="ecd9c-118">Spécifie l’adresse d’origine de messages électroniques sortants.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-118">Specifies the from address for outgoing emails.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="ecd9c-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ecd9c-119">Child Elements</span></span>  
  
|<span data-ttu-id="ecd9c-120">Attribut</span><span class="sxs-lookup"><span data-stu-id="ecd9c-120">Attribute</span></span>|<span data-ttu-id="ecd9c-121">Description</span><span class="sxs-lookup"><span data-stu-id="ecd9c-121">Description</span></span>|  
|---------------|-----------------|  
|`specifiedPickupDirectory`|<span data-ttu-id="ecd9c-122">Configure le répertoire local pour un serveur SMTP Simple Mail Transport Protocol ().</span><span class="sxs-lookup"><span data-stu-id="ecd9c-122">Configures the local directory for a Simple Mail Transport Protocol (SMTP) server.</span></span>|  
|`network`|<span data-ttu-id="ecd9c-123">Configure les options de réseau pour un serveur SMTP externe.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-123">Configures the network options for an external SMTP server.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="ecd9c-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ecd9c-124">Parent Elements</span></span>  
  
|<span data-ttu-id="ecd9c-125">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ecd9c-125">**Element**</span></span>|<span data-ttu-id="ecd9c-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="ecd9c-126">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="ecd9c-127">\<mailSettings>, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="ecd9c-127">\<mailSettings> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/mailsettings-element-network-settings.md)|<span data-ttu-id="ecd9c-128">Configure les options d’envoi du courrier.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-128">Configures mail sending options.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="ecd9c-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="ecd9c-129">Example</span></span>  
 <span data-ttu-id="ecd9c-130">L’exemple suivant spécifie les paramètres SMTP appropriés pour envoyer un e-mail à l’aide des informations d’identification du réseau par défaut.</span><span class="sxs-lookup"><span data-stu-id="ecd9c-130">The following example specifies the appropriate SMTP parameters to send email using the default network credentials.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="Network" deliveryFormat="SevenBit"  from="ben@contoso.com">  
        <network  
          host="localhost"  
          port="25"  
          defaultCredentials="true"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="ecd9c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecd9c-131">See also</span></span>

- <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>
- <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>
- <xref:System.Net.Mail.SmtpDeliveryFormat>
- <xref:System.Net.Mail.SmtpDeliveryMethod>
- [<span data-ttu-id="ecd9c-132">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="ecd9c-132">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
