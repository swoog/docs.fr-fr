---
title: '&lt;windowsStreamSecurity&gt;'
ms.date: 03/30/2017
ms.assetid: 926bea29-90c7-4a26-9cf0-fb4aa44f6f70
ms.openlocfilehash: 6cce178910767d7fd197aff0d007b7cc3f4e60f3
ms.sourcegitcommit: 4ac80713f6faa220e5a119d5165308a58f7ccdc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/09/2019
ms.locfileid: "54151122"
---
# <a name="ltwindowsstreamsecuritygt"></a><span data-ttu-id="5e650-102">&lt;windowsStreamSecurity&gt;</span><span class="sxs-lookup"><span data-stu-id="5e650-102">&lt;windowsStreamSecurity&gt;</span></span>
<span data-ttu-id="5e650-103">Spécifiez les paramètres de sécurité de flux de données Windows pour la liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="5e650-103">Specify Windows stream security settings of the custom binding.</span></span>  
  
 <span data-ttu-id="5e650-104">\<system.serviceModel></span><span class="sxs-lookup"><span data-stu-id="5e650-104">\<system.serviceModel></span></span>  
<span data-ttu-id="5e650-105">\<liaisons ></span><span class="sxs-lookup"><span data-stu-id="5e650-105">\<bindings></span></span>  
<span data-ttu-id="5e650-106">\<customBinding ></span><span class="sxs-lookup"><span data-stu-id="5e650-106">\<customBinding></span></span>  
<span data-ttu-id="5e650-107">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5e650-107">\<binding></span></span>  
<span data-ttu-id="5e650-108">\<windowsStreamSecurity ></span><span class="sxs-lookup"><span data-stu-id="5e650-108">\<windowsStreamSecurity></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5e650-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e650-109">Syntax</span></span>  
  
```xml  
<windowsStreamSecurity protectionLevel="None/Sign/EncryptAndSign" />
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5e650-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="5e650-110">Attributes and Elements</span></span>  
 <span data-ttu-id="5e650-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5e650-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5e650-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="5e650-112">Attributes</span></span>  
  
|<span data-ttu-id="5e650-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="5e650-113">Attribute</span></span>|<span data-ttu-id="5e650-114">Description</span><span class="sxs-lookup"><span data-stu-id="5e650-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5e650-115">protectionLevel</span><span class="sxs-lookup"><span data-stu-id="5e650-115">protectionLevel</span></span>|<span data-ttu-id="5e650-116">Définit la sécurité au niveau du message.</span><span class="sxs-lookup"><span data-stu-id="5e650-116">Defines message-level security.</span></span> <span data-ttu-id="5e650-117">La signature des messages atténue le risque de modification par un tiers pendant le transfert.</span><span class="sxs-lookup"><span data-stu-id="5e650-117">Signing messages mitigates the risk of a third party tampering with the message while it is being transferred.</span></span> <span data-ttu-id="5e650-118">Le chiffrement garantit la confidentialité des données pendant le transport.</span><span class="sxs-lookup"><span data-stu-id="5e650-118">Encryption provides data-level privacy during transport.</span></span> <span data-ttu-id="5e650-119">Les valeurs valides sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e650-119">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="5e650-120">-None : Aucune protection.</span><span class="sxs-lookup"><span data-stu-id="5e650-120">-   None: No protection.</span></span><br /><span data-ttu-id="5e650-121">-Signe : Les messages sont signés.</span><span class="sxs-lookup"><span data-stu-id="5e650-121">-   Sign: Messages are signed.</span></span><br /><span data-ttu-id="5e650-122">-EncryptAndSign : Les messages sont signés et chiffrés.</span><span class="sxs-lookup"><span data-stu-id="5e650-122">-   EncryptAndSign: Messages are signed and encrypted.</span></span><br /><br /> <span data-ttu-id="5e650-123">La valeur par défaut est EncryptAndSign.</span><span class="sxs-lookup"><span data-stu-id="5e650-123">The default is EncryptAndSign.</span></span><br /><br /> <span data-ttu-id="5e650-124">Cet attribut est de type <xref:System.Net.Security.ProtectionLevel>.</span><span class="sxs-lookup"><span data-stu-id="5e650-124">This attribute is of type <xref:System.Net.Security.ProtectionLevel>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5e650-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5e650-125">Child Elements</span></span>  
 <span data-ttu-id="5e650-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="5e650-126">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5e650-127">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5e650-127">Parent Elements</span></span>  
  
|<span data-ttu-id="5e650-128">Élément</span><span class="sxs-lookup"><span data-stu-id="5e650-128">Element</span></span>|<span data-ttu-id="5e650-129">Description</span><span class="sxs-lookup"><span data-stu-id="5e650-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5e650-130">\<liaison ></span><span class="sxs-lookup"><span data-stu-id="5e650-130">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)|<span data-ttu-id="5e650-131">Définit toutes les fonctions de liaison d’une liaison personnalisée.</span><span class="sxs-lookup"><span data-stu-id="5e650-131">Defines all binding capabilities of the custom binding.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5e650-132">Notes</span><span class="sxs-lookup"><span data-stu-id="5e650-132">Remarks</span></span>  
 <span data-ttu-id="5e650-133">Les transports qui utilisent un protocole orienté flux de données, tel que TCP, et des canaux nommés prennent en charge les mises à niveau de transport basées sur le flux de données.</span><span class="sxs-lookup"><span data-stu-id="5e650-133">Transports that use a stream-oriented protocol such as TCP and named pipes support stream-based transport upgrades.</span></span> <span data-ttu-id="5e650-134">Plus spécifiquement, WCF fournit les mises à niveau de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="5e650-134">Specifically, WCF provides security upgrades.</span></span> <span data-ttu-id="5e650-135">La configuration de cette sécurité de transport est encapsulée par cet élément de configuration, ainsi que par [ \<sslStreamSecurity >](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md), ce qui peut être configuré et ajouté à une liaison personnalisée</span><span class="sxs-lookup"><span data-stu-id="5e650-135">The configuration of this transport security is encapsulated by this configuration element  as well as by [\<sslStreamSecurity>](../../../../../docs/framework/configure-apps/file-schema/wcf/sslstreamsecurity.md), which can be configured and added to a custom binding</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5e650-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e650-136">See Also</span></span>  
 <xref:System.ServiceModel.Channels.CustomBinding>  
 <xref:System.ServiceModel.Configuration.WindowsStreamSecurityElement>  
 <xref:System.ServiceModel.Channels.WindowsStreamSecurityBindingElement>  
 [<span data-ttu-id="5e650-137">Liaisons</span><span class="sxs-lookup"><span data-stu-id="5e650-137">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="5e650-138">Extension de liaisons</span><span class="sxs-lookup"><span data-stu-id="5e650-138">Extending Bindings</span></span>](../../../../../docs/framework/wcf/extending/extending-bindings.md)  
 [<span data-ttu-id="5e650-139">Liaisons personnalisées</span><span class="sxs-lookup"><span data-stu-id="5e650-139">Custom Bindings</span></span>](../../../../../docs/framework/wcf/extending/custom-bindings.md)  
 [<span data-ttu-id="5e650-140">\<customBinding></span><span class="sxs-lookup"><span data-stu-id="5e650-140">\<customBinding></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
