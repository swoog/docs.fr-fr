---
title: '&lt;mailSettings&gt; , élément (paramètres réseau)'
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
ms.openlocfilehash: f3a706edaeba551139368568a7467e0cdab3524c
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47208592"
---
# <a name="ltmailsettingsgt-element-network-settings"></a><span data-ttu-id="c05ff-102">&lt;mailSettings&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="c05ff-102">&lt;mailSettings&gt; Element (Network Settings)</span></span>
<span data-ttu-id="c05ff-103">Configure les options d’envoi du courrier.</span><span class="sxs-lookup"><span data-stu-id="c05ff-103">Configures mail sending options.</span></span>  

<span data-ttu-id="c05ff-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="c05ff-104">\<configuration></span></span>  
<span data-ttu-id="c05ff-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="c05ff-105">\<system.net></span></span>  
<span data-ttu-id="c05ff-106">\<mailSettings ></span><span class="sxs-lookup"><span data-stu-id="c05ff-106">\<mailSettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c05ff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c05ff-107">Syntax</span></span>  
  
```xml  
<mailSettings>
  <smtp> … </smtp>  
</mailSettings>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c05ff-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="c05ff-108">Attributes and Elements</span></span>  
 <span data-ttu-id="c05ff-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="c05ff-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c05ff-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="c05ff-110">Attributes</span></span>  
 <span data-ttu-id="c05ff-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c05ff-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="c05ff-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c05ff-112">Child Elements</span></span>  
  
|<span data-ttu-id="c05ff-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="c05ff-113">Attribute</span></span>|<span data-ttu-id="c05ff-114">Description</span><span class="sxs-lookup"><span data-stu-id="c05ff-114">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="c05ff-115">\<SMTP >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="c05ff-115">\<smtp> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|<span data-ttu-id="c05ff-116">Configure les options de Simple Mail Transport Protocol.</span><span class="sxs-lookup"><span data-stu-id="c05ff-116">Configures Simple Mail Transport Protocol options.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c05ff-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c05ff-117">Parent Elements</span></span>  
  
|<span data-ttu-id="c05ff-118">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c05ff-118">**Element**</span></span>|<span data-ttu-id="c05ff-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="c05ff-119">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="c05ff-120">\<system.Net>, élément (Paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="c05ff-120">\<system.Net> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="c05ff-121">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="c05ff-121">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c05ff-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="c05ff-122">Example</span></span>  
 <span data-ttu-id="c05ff-123">L’exemple suivant spécifie les paramètres SMTP appropriés pour envoyer un e-mail à l’aide des informations d’identification du réseau par défaut.</span><span class="sxs-lookup"><span data-stu-id="c05ff-123">The following example specifies the appropriate SMTP parameters to send email using the default network credentials.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="Network">  
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
  
## <a name="see-also"></a><span data-ttu-id="c05ff-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c05ff-124">See Also</span></span>  
 <xref:System.Net.Mail.SmtpClient>  
 [<span data-ttu-id="c05ff-125">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="c05ff-125">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
