---
title: '&lt;ServiceCertificate&gt;'
ms.date: 03/30/2017
ms.assetid: 42c7f291-2ec3-43c5-8872-35897ff3c660
author: BrucePerlerMS
ms.openlocfilehash: 008d2269a72759117658e27ec130cc8cf62cfdfa
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47400411"
---
# <a name="ltservicecertificategt"></a><span data-ttu-id="20413-102">&lt;ServiceCertificate&gt;</span><span class="sxs-lookup"><span data-stu-id="20413-102">&lt;serviceCertificate&gt;</span></span>
<span data-ttu-id="20413-103">Configure le certificat X.509 qui est utilisé pour chiffrer et déchiffrer les jetons.</span><span class="sxs-lookup"><span data-stu-id="20413-103">Configures the X.509 certificate that is used to encrypt and decrypt tokens.</span></span>  
  
 <span data-ttu-id="20413-104">\<system.identityModel.services ></span><span class="sxs-lookup"><span data-stu-id="20413-104">\<system.identityModel.services></span></span>  
<span data-ttu-id="20413-105">\<federationConfiguration ></span><span class="sxs-lookup"><span data-stu-id="20413-105">\<federationConfiguration></span></span>  
<span data-ttu-id="20413-106">\<serviceCertificate ></span><span class="sxs-lookup"><span data-stu-id="20413-106">\<serviceCertificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20413-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20413-107">Syntax</span></span>  
  
```xml  
<system.identityModel.services>  
  <federationConfiguration>  
    <serviceCertificate>  
    </serviceCertificate>  
  </federationConfiguration>  
</system.identityModel.services>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="20413-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="20413-108">Attributes and Elements</span></span>  
 <span data-ttu-id="20413-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="20413-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="20413-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="20413-110">Attributes</span></span>  
 <span data-ttu-id="20413-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="20413-111">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="20413-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="20413-112">Child Elements</span></span>  
  
|<span data-ttu-id="20413-113">Élément</span><span class="sxs-lookup"><span data-stu-id="20413-113">Element</span></span>|<span data-ttu-id="20413-114">Description</span><span class="sxs-lookup"><span data-stu-id="20413-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="20413-115">\<certificateReference ></span><span class="sxs-lookup"><span data-stu-id="20413-115">\<certificateReference></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatereference.md)|<span data-ttu-id="20413-116">Spécifie les paramètres qui sont utilisés pour rechercher et valider le certificat X.509 dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="20413-116">Specifies settings that are used to find and validate an X.509 certificate in a certificate store.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="20413-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="20413-117">Parent Elements</span></span>  
  
|<span data-ttu-id="20413-118">Élément</span><span class="sxs-lookup"><span data-stu-id="20413-118">Element</span></span>|<span data-ttu-id="20413-119">Description</span><span class="sxs-lookup"><span data-stu-id="20413-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="20413-120">\<federationConfiguration></span><span class="sxs-lookup"><span data-stu-id="20413-120">\<federationConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/federationconfiguration.md)|<span data-ttu-id="20413-121">Contient les paramètres qui configurent le <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) et le <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span><span class="sxs-lookup"><span data-stu-id="20413-121">Contains the settings that configure the <xref:System.IdentityModel.Services.WSFederationAuthenticationModule> (WSFAM) and the <xref:System.IdentityModel.Services.SessionAuthenticationModule> (SAM).</span></span>|  
  
## <a name="example"></a><span data-ttu-id="20413-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="20413-122">Example</span></span>  
 <span data-ttu-id="20413-123">Le code XML suivant illustre l’utilisation de la \<serviceCertificate > élément.</span><span class="sxs-lookup"><span data-stu-id="20413-123">The following XML shows the use of the \<serviceCertificate> element.</span></span> <span data-ttu-id="20413-124">Le code XML provient de la `CustomToken` exemple.</span><span class="sxs-lookup"><span data-stu-id="20413-124">The XML is taken from the `CustomToken` sample.</span></span>  
  
```xml  
<serviceCertificate>  
  <certificateReference x509FindType="FindBySubjectName" findValue="localhost" storeLocation="LocalMachine" storeName="My"/>  
</serviceCertificate>  
```
