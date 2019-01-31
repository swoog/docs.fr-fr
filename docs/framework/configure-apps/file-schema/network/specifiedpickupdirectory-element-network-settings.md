---
title: <specifiedPickupDirectory>, élément (paramètres réseau)
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#specifiedPickupDirectory
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp/specifiedPickupDirectory
helpviewer_keywords:
- specifiedPickupDirectory element
- <specifiedPickupDirectory> element
ms.assetid: 0121f49d-bff2-4bc6-af06-f1628dcd61f1
ms.openlocfilehash: 6abee1b01e690633dabfd225b30fcb9b8b408dad
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55270821"
---
# <a name="specifiedpickupdirectory-element-network-settings"></a><span data-ttu-id="1ed2d-102">\<specifiedPickupDirectory >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="1ed2d-102">\<specifiedPickupDirectory> Element (Network Settings)</span></span>
<span data-ttu-id="1ed2d-103">Configure le répertoire local pour un serveur SMTP Simple Mail Transport Protocol ().</span><span class="sxs-lookup"><span data-stu-id="1ed2d-103">Configures the local directory for a Simple Mail Transport Protocol (SMTP) server.</span></span>  
  
 <span data-ttu-id="1ed2d-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="1ed2d-104">\<configuration></span></span>  
<span data-ttu-id="1ed2d-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="1ed2d-105">\<system.net></span></span>  
<span data-ttu-id="1ed2d-106">\<mailSettings></span><span class="sxs-lookup"><span data-stu-id="1ed2d-106">\<mailSettings></span></span>  
<span data-ttu-id="1ed2d-107">\<smtp></span><span class="sxs-lookup"><span data-stu-id="1ed2d-107">\<smtp></span></span>  
<span data-ttu-id="1ed2d-108">\<specifiedPickupDirectory></span><span class="sxs-lookup"><span data-stu-id="1ed2d-108">\<specifiedPickupDirectory></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ed2d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ed2d-109">Syntax</span></span>  
  
```xml  
<specifiedPickupDirectory  
  pickupDirectoryLocation="directory"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="1ed2d-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="1ed2d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="1ed2d-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="1ed2d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="1ed2d-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="1ed2d-112">Attributes</span></span>  
  
|<span data-ttu-id="1ed2d-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="1ed2d-113">Attribute</span></span>|<span data-ttu-id="1ed2d-114">Description</span><span class="sxs-lookup"><span data-stu-id="1ed2d-114">Description</span></span>|  
|---------------|-----------------|  
|`pickupDirectoryLocation`|<span data-ttu-id="1ed2d-115">Le répertoire dans lequel les applications enregistrent e-mail pour un traitement ultérieur par le serveur SMTP.</span><span class="sxs-lookup"><span data-stu-id="1ed2d-115">The directory where applications save email for later processing by the SMTP server.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="1ed2d-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1ed2d-116">Child Elements</span></span>  
 <span data-ttu-id="1ed2d-117">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1ed2d-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="1ed2d-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1ed2d-118">Parent Elements</span></span>  
  
|<span data-ttu-id="1ed2d-119">Élément</span><span class="sxs-lookup"><span data-stu-id="1ed2d-119">Element</span></span>|<span data-ttu-id="1ed2d-120">Description</span><span class="sxs-lookup"><span data-stu-id="1ed2d-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="1ed2d-121">\<SMTP >, élément (paramètres réseau)</span><span class="sxs-lookup"><span data-stu-id="1ed2d-121">\<smtp> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|<span data-ttu-id="1ed2d-122">Configure les options d’envoi du courrier SMTP Simple Mail Transport Protocol ().</span><span class="sxs-lookup"><span data-stu-id="1ed2d-122">Configures Simple Mail Transport Protocol (SMTP) mail sending options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1ed2d-123">Notes</span><span class="sxs-lookup"><span data-stu-id="1ed2d-123">Remarks</span></span>  
 <span data-ttu-id="1ed2d-124">Le `specifiedPickupDirectory` attribut définit le répertoire dans lequel les applications enregistrent les messages électroniques à traiter par le serveur SMTP.</span><span class="sxs-lookup"><span data-stu-id="1ed2d-124">The `specifiedPickupDirectory` attribute sets the directory where applications save mail messages to be processed by the SMTP server.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1ed2d-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="1ed2d-125">Example</span></span>  
 <span data-ttu-id="1ed2d-126">L’exemple suivant indique c:\maildrop comme répertoire de collecte de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1ed2d-126">The following example specifies c:\maildrop as the mail pickup directory.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="SpecifiedPickupDirectory">  
        <specifiedPickupDirectory  
          pickupDirectoryLocation="c:\maildrop"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1ed2d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ed2d-127">See also</span></span>
- <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>
- <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>
- <xref:System.Net.Configuration.SmtpSpecifiedPickupDirectoryElement?displayProperty=nameWithType>
- [<span data-ttu-id="1ed2d-128">Schéma des paramètres réseau</span><span class="sxs-lookup"><span data-stu-id="1ed2d-128">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
