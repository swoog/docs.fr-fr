---
title: '&lt;mailSettings&gt; élément (paramètres réseau)'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#mailSettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings
helpviewer_keywords:
- mailSettings element
- <mailSettings> element
ms.assetid: 54f0f153-17e5-4f49-afdc-deadb940c9c1
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 5bc7cc649b18a5330d056bbddfe96db4ecca2ec8
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32746421"
---
# <a name="ltmailsettingsgt-element-network-settings"></a><span data-ttu-id="4a7b9-102">&lt;mailSettings&gt; élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="4a7b9-102">&lt;mailSettings&gt; Element (Network Settings)</span></span>
<span data-ttu-id="4a7b9-103">Configure les options d’envoi du courrier.</span><span class="sxs-lookup"><span data-stu-id="4a7b9-103">Configures mail sending options.</span></span>  

<span data-ttu-id="4a7b9-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="4a7b9-104">\<configuration></span></span>  
<span data-ttu-id="4a7b9-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="4a7b9-105">\<system.net></span></span>  
<span data-ttu-id="4a7b9-106">\<mailSettings ></span><span class="sxs-lookup"><span data-stu-id="4a7b9-106">\<mailSettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a7b9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a7b9-107">Syntax</span></span>  
  
```xml  
<mailSettings>
  <smtp> … </smtp>  
</mailSettings>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4a7b9-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="4a7b9-108">Attributes and Elements</span></span>  
 <span data-ttu-id="4a7b9-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="4a7b9-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4a7b9-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="4a7b9-110">Attributes</span></span>  
 <span data-ttu-id="4a7b9-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4a7b9-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="4a7b9-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4a7b9-112">Child Elements</span></span>  
  
|<span data-ttu-id="4a7b9-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="4a7b9-113">Attribute</span></span>|<span data-ttu-id="4a7b9-114">Description</span><span class="sxs-lookup"><span data-stu-id="4a7b9-114">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="4a7b9-115">\<SMTP >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="4a7b9-115">\<smtp> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|<span data-ttu-id="4a7b9-116">Configure les options de Simple Mail Transport Protocol.</span><span class="sxs-lookup"><span data-stu-id="4a7b9-116">Configures Simple Mail Transport Protocol options.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="4a7b9-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4a7b9-117">Parent Elements</span></span>  
  
|<span data-ttu-id="4a7b9-118">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4a7b9-118">**Element**</span></span>|<span data-ttu-id="4a7b9-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="4a7b9-119">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="4a7b9-120">\<system.Net>, élément (Paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="4a7b9-120">\<system.Net> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="4a7b9-121">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="4a7b9-121">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="4a7b9-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="4a7b9-122">Example</span></span>  
 <span data-ttu-id="4a7b9-123">L’exemple suivant spécifie les paramètres SMTP appropriés pour envoyer un courrier électronique à l’aide des informations d’identification de réseau par défaut.</span><span class="sxs-lookup"><span data-stu-id="4a7b9-123">The following example specifies the appropriate SMTP parameters to send email using the default network credentials.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="network">  
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
  
## <a name="see-also"></a><span data-ttu-id="4a7b9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a7b9-124">See Also</span></span>  
 <xref:System.Net.Mail.SmtpClient>  
 [<span data-ttu-id="4a7b9-125">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="4a7b9-125">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
