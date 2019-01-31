---
title: <mailSettings>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#mailSettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings
helpviewer_keywords:
- mailSettings element
- <mailSettings> element
ms.assetid: 54f0f153-17e5-4f49-afdc-deadb940c9c1
ms.openlocfilehash: 0e71284e914dac2d28448f3d8bd4bdc7a9f6b325
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55277613"
---
# <a name="mailsettings-element-network-settings"></a><span data-ttu-id="39d1e-102">\<mailSettings >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="39d1e-102">\<mailSettings> Element (Network Settings)</span></span>
<span data-ttu-id="39d1e-103">Configure les options d’envoi du courrier.</span><span class="sxs-lookup"><span data-stu-id="39d1e-103">Configures mail sending options.</span></span>  

<span data-ttu-id="39d1e-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="39d1e-104">\<configuration></span></span>  
<span data-ttu-id="39d1e-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="39d1e-105">\<system.net></span></span>  
<span data-ttu-id="39d1e-106">\<mailSettings></span><span class="sxs-lookup"><span data-stu-id="39d1e-106">\<mailSettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="39d1e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39d1e-107">Syntax</span></span>  
  
```xml  
<mailSettings>
  <smtp>...</smtp>  
</mailSettings>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="39d1e-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="39d1e-108">Attributes and Elements</span></span>  
 <span data-ttu-id="39d1e-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="39d1e-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="39d1e-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="39d1e-110">Attributes</span></span>  
 <span data-ttu-id="39d1e-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="39d1e-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="39d1e-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="39d1e-112">Child Elements</span></span>  
  
|<span data-ttu-id="39d1e-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="39d1e-113">Attribute</span></span>|<span data-ttu-id="39d1e-114">Description</span><span class="sxs-lookup"><span data-stu-id="39d1e-114">Description</span></span>|  
|---------------|-----------------|  
|[<span data-ttu-id="39d1e-115">\<SMTP >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="39d1e-115">\<smtp> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|<span data-ttu-id="39d1e-116">Configure les options de Simple Mail Transport Protocol.</span><span class="sxs-lookup"><span data-stu-id="39d1e-116">Configures Simple Mail Transport Protocol options.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="39d1e-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="39d1e-117">Parent Elements</span></span>  
  
|<span data-ttu-id="39d1e-118">**Élément**</span><span class="sxs-lookup"><span data-stu-id="39d1e-118">**Element**</span></span>|<span data-ttu-id="39d1e-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="39d1e-119">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="39d1e-120">\<system.Net>, élément (Paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="39d1e-120">\<system.Net> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/system-net-element-network-settings.md)|<span data-ttu-id="39d1e-121">Contient des paramètres qui spécifient la manière dont .NET Framework se connecte au réseau.</span><span class="sxs-lookup"><span data-stu-id="39d1e-121">Contains settings that specify how the .NET Framework connects to the network.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="39d1e-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="39d1e-122">Example</span></span>  
 <span data-ttu-id="39d1e-123">L’exemple suivant spécifie les paramètres SMTP appropriés pour envoyer un e-mail à l’aide des informations d’identification du réseau par défaut.</span><span class="sxs-lookup"><span data-stu-id="39d1e-123">The following example specifies the appropriate SMTP parameters to send email using the default network credentials.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="39d1e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39d1e-124">See also</span></span>
- <xref:System.Net.Mail.SmtpClient>
- [<span data-ttu-id="39d1e-125">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="39d1e-125">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
