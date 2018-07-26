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
manager: markl
ms.openlocfilehash: a9afd992a12392ae0ad1c27eea305cb7e367686d
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/06/2018
ms.locfileid: "37874414"
---
# <a name="ltmailsettingsgt-element-network-settings"></a><span data-ttu-id="0a095-102">&lt;mailSettings&gt; , élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="0a095-102">&lt;mailSettings&gt; Element (Network Settings)</span></span>
<span data-ttu-id="0a095-103">Configure les options d’envoi du courrier.</span><span class="sxs-lookup"><span data-stu-id="0a095-103">Configures mail sending options.</span></span>  

<span data-ttu-id="0a095-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="0a095-104">\<configuration></span></span>  
<span data-ttu-id="0a095-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="0a095-105">\<system.net></span></span>  
<span data-ttu-id="0a095-106">\<mailSettings ></span><span class="sxs-lookup"><span data-stu-id="0a095-106">\<mailSettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a095-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a095-107">Syntax</span></span>  
  
```xml  
<mailSettings>
  <smtp> … </smtp>  
</mailSettings>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0a095-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0a095-108">Attributes and Elements</span></span>  
 <span data-ttu-id="0a095-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="0a095-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0a095-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="0a095-110">Attributes</span></span>  
 <span data-ttu-id="0a095-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0a095-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0a095-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0a095-112">Child Elements</span></span>  
  
|<span data-ttu-id="0a095-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="0a095-113">Attribute</span></span>|<span data-ttu-id="0a095-114">Description</span><span class="sxs-lookup"><span data-stu-id="0a095-114">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="0a095-115">\<SMTP >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="0a095-115">\<smtp> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|<span data-ttu-id="0a095-116">Configure les options de Simple Mail Transport Protocol.</span><span class="sxs-lookup"><span data-stu-id="0a095-116">Configures Simple Mail Transport Protocol options.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0a095-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0a095-117">Parent Elements</span></span>  
  
|<span data-ttu-id="0a095-118">**Élément**</span><span class="sxs-lookup"><span data-stu-id="0a095-118">**Element**</span></span>|<span data-ttu-id="0a095-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="0a095-119">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="0a095-120">\<system.Net>, élément (Paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="0a095-120">\<system.Net> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="0a095-121">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="0a095-121">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="0a095-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="0a095-122">Example</span></span>  
 <span data-ttu-id="0a095-123">L’exemple suivant spécifie les paramètres SMTP appropriés pour envoyer un e-mail à l’aide des informations d’identification du réseau par défaut.</span><span class="sxs-lookup"><span data-stu-id="0a095-123">The following example specifies the appropriate SMTP parameters to send email using the default network credentials.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="0a095-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a095-124">See Also</span></span>  
 <xref:System.Net.Mail.SmtpClient>  
 [<span data-ttu-id="0a095-125">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="0a095-125">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
