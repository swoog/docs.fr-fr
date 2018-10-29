---
title: '&lt;windowsStreamSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 926bea29-90c7-4a26-9cf0-fb4aa44f6f70
ms.openlocfilehash: e117c30ba2583158ee21fd11ff4a38b094c18fd9
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50197630"
---
# <a name="ltwindowsstreamsecuritygt"></a><span data-ttu-id="798d8-102">&lt;windowsStreamSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="798d8-102">&lt;windowsStreamSecurity&gt;</span></span>
<span data-ttu-id="798d8-103">Spécifiez les paramètres de sécurité de flux de données Windows pour la liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="798d8-103">Specify Windows stream security settings of the custom binding.</span></span>  
  
 <span data-ttu-id="798d8-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="798d8-104">\<system.serviceModel></span></span>  
<span data-ttu-id="798d8-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="798d8-105">\<bindings></span></span>  
<span data-ttu-id="798d8-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="798d8-106">\<customBinding></span></span>  
<span data-ttu-id="798d8-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="798d8-107">\<binding></span></span>  
<span data-ttu-id="798d8-108">\<windowsStreamSecurity ></span><span class="sxs-lookup"><span data-stu-id="798d8-108">\<windowsStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="798d8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="798d8-109">Syntax</span></span>  
  
```xml  
<windowsStreamSecurity protectionLevel="None/Sign/EncryptAndSign"/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="798d8-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="798d8-110">Attributes and Elements</span></span>  
 <span data-ttu-id="798d8-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="798d8-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="798d8-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="798d8-112">Attributes</span></span>  
  
|<span data-ttu-id="798d8-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="798d8-113">Attribute</span></span>|<span data-ttu-id="798d8-114">Description</span><span class="sxs-lookup"><span data-stu-id="798d8-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="798d8-115">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="798d8-115">protectionLevel</span></span>|<span data-ttu-id="798d8-116">Définit la sécurité au niveau du message.</span><span class="sxs-lookup"><span data-stu-id="798d8-116">Defines message-level security.</span></span> <span data-ttu-id="798d8-117">La signature des messages atténue le risque de modification par un tiers pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="798d8-117">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="798d8-118">Le chiffrement garantit la confidentialité des données pendant le transport.</span><span class="sxs-lookup"><span data-stu-id="798d8-118">Encryption provides data-level privacy during transport.</span></span> <span data-ttu-id="798d8-119">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="798d8-119">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="798d8-120">-None : Aucune protection.</span><span class="sxs-lookup"><span data-stu-id="798d8-120">-   None: No protection.</span></span><br /><span data-ttu-id="798d8-121">-Signe : Les Messages sont signés.</span><span class="sxs-lookup"><span data-stu-id="798d8-121">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="798d8-122">-EncryptAndSign : Les Messages sont signés et chiffrés.</span><span class="sxs-lookup"><span data-stu-id="798d8-122">-   EncryptAndSign: Messages are signed and encrypted.</span></span><br /><br /> <span data-ttu-id="798d8-123">La valeur par défaut est EncryptAndSign.</span><span class="sxs-lookup"><span data-stu-id="798d8-123">The default is EncryptAndSign.</span></span><br /><br /> <span data-ttu-id="798d8-124">Cet attribut est de type <xref:System.Net.Security.ProtectionLevel>.</span><span class="sxs-lookup"><span data-stu-id="798d8-124">This attribute is of type <xref:System.Net.Security.ProtectionLevel>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="798d8-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="798d8-125">Child Elements</span></span>  
 <span data-ttu-id="798d8-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="798d8-126">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="798d8-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="798d8-127">Parent Elements</span></span>  
  
|<span data-ttu-id="798d8-128">Élément</span><span class="sxs-lookup"><span data-stu-id="798d8-128">Element</span></span>|<span data-ttu-id="798d8-129">Description</span><span class="sxs-lookup"><span data-stu-id="798d8-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="798d8-130">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="798d8-130">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="798d8-131">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="798d8-131">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="798d8-132">Notes</span><span class="sxs-lookup"><span data-stu-id="798d8-132">Remarks</span></span>  
 <span data-ttu-id="798d8-133">Les transports qui utilisent un protocole orienté flux de données, tel que TCP, et des canaux nommés prennent en charge les mises à niveau de transport basées sur le flux de données.</span><span class="sxs-lookup"><span data-stu-id="798d8-133">Transports that use a stream-oriented protocol such as TCP and named pipes support stream-based transport upgrades.</span></span> <span data-ttu-id="798d8-134">Plus spécifiquement, WCF fournit les mises à niveau de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="798d8-134">Specifically, WCF provides security upgrades.</span></span> <span data-ttu-id="798d8-135">La configuration de cette sécurité de transport est encapsulée par cet élément de configuration, ainsi que par [ \<sslStreamSecurity >](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md), ce qui peut être configuré et ajouté à une liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="798d8-135">The configuration of this transport security is encapsulated by this configuration element  as well as by [\<sslStreamSecurity>](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md), which can be configured and added to a custom binding</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="798d8-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="798d8-136">See Also</span></span>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Configuration.WindowsStreamSecurityElement>  
 <xref:System.ServiceModel.Channels.WindowsStreamSecurityBindingElement>  
 [<span data-ttu-id="798d8-137">Liaisons</span><span class="sxs-lookup"><span data-stu-id="798d8-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="798d8-138">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="798d8-138">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="798d8-139">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="798d8-139">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="798d8-140">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="798d8-140">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
