---
title: '&lt;cryptoClasses&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/cryptoNameMapping/cryptoClasses
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptoClasses
helpviewer_keywords:
- <cryptoClasses> element
- cryptoClasses element
ms.assetid: 290d5f96-946d-4f02-babb-1d31ec0b8295
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 8363351efd0b6cbcfee5b137cf9f222e16dcc425
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188740"
---
# <a name="ltcryptoclassesgt-element"></a><span data-ttu-id="d1c9d-102">&lt;cryptoClasses&gt; élément</span><span class="sxs-lookup"><span data-stu-id="d1c9d-102">&lt;cryptoClasses&gt; Element</span></span>
<span data-ttu-id="d1c9d-103">Contient la liste des classes de chiffrement qui ont un mappage à un nom convivial dans l’élément [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md).</span><span class="sxs-lookup"><span data-stu-id="d1c9d-103">Contains a list of cryptography classes that have a mapping to a friendly name in the [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) element.</span></span>  
  
 <span data-ttu-id="d1c9d-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="d1c9d-104">\<configuration></span></span>  
<span data-ttu-id="d1c9d-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="d1c9d-105">\<mscorlib></span></span>  
<span data-ttu-id="d1c9d-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="d1c9d-106">\<cryptographySettings></span></span>  
<span data-ttu-id="d1c9d-107">\<cryptoNameMapping ></span><span class="sxs-lookup"><span data-stu-id="d1c9d-107">\<cryptoNameMapping></span></span>  
<span data-ttu-id="d1c9d-108">\<cryptoClasses ></span><span class="sxs-lookup"><span data-stu-id="d1c9d-108">\<cryptoClasses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1c9d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1c9d-109">Syntax</span></span>  
  
```xml  
<cryptoClasses>   
</cryptoClasses>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d1c9d-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="d1c9d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="d1c9d-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d1c9d-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="d1c9d-112">Attributes</span></span>  
 <span data-ttu-id="d1c9d-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="d1c9d-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d1c9d-114">Child Elements</span></span>  
  
|<span data-ttu-id="d1c9d-115">Élément</span><span class="sxs-lookup"><span data-stu-id="d1c9d-115">Element</span></span>|<span data-ttu-id="d1c9d-116">Description</span><span class="sxs-lookup"><span data-stu-id="d1c9d-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d1c9d-117">\<cryptoClass ></span><span class="sxs-lookup"><span data-stu-id="d1c9d-117">\<cryptoClass></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclass-element.md)|<span data-ttu-id="d1c9d-118">Contient une classe de chiffrement qui a un mappage à un nom convivial dans l’élément **\<nameEntry>**.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-118">Contains a cryptography class that has a mapping to a friendly name in the **\<nameEntry>** element.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="d1c9d-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d1c9d-119">Parent Elements</span></span>  
  
|<span data-ttu-id="d1c9d-120">Élément</span><span class="sxs-lookup"><span data-stu-id="d1c9d-120">Element</span></span>|<span data-ttu-id="d1c9d-121">Description</span><span class="sxs-lookup"><span data-stu-id="d1c9d-121">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="d1c9d-122">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-122">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="d1c9d-123">Contient des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-123">Contains cryptography settings.</span></span>|  
|`cryptoNameMapping`|<span data-ttu-id="d1c9d-124">Contient des mappages de classes à des noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-124">Contains mappings of classes to friendly names.</span></span>|  
|`mscorlib`|<span data-ttu-id="d1c9d-125">Contient le `cryptographySettings` élément.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-125">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="d1c9d-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="d1c9d-126">Example</span></span>  
 <span data-ttu-id="d1c9d-127">L’exemple suivant montre comment utiliser le  **\<cryptoClass >** élément à référencer une classe de chiffrement et configurer le runtime.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-127">The following example shows how use the **\<cryptoClass>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="d1c9d-128">Vous pouvez ensuite passer la chaîne « RSA » à la <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> méthode et l’utilisation du <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> méthode pour retourner un `MyCryptoRSAClass` objet.</span><span class="sxs-lookup"><span data-stu-id="d1c9d-128">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCryptoRSA="MyCryptoRSAClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
               <!-- Other cryptography classes go here. -->  
            </cryptoClasses>  
            <nameEntry name="RSA" class="MyCryptoRSA"/>  
            <nameEntry name="System.Security.Cryptography.AsymmetricAlgorithm"  
                       class="MyCryptoRSA"/>  
             <!-- Mappings to other cryptography classes go here. -->  
         </cryptoNameMapping>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="d1c9d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1c9d-129">See Also</span></span>  
- <xref:System.Security.Cryptography>  
- [<span data-ttu-id="d1c9d-130">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="d1c9d-130">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
- [<span data-ttu-id="d1c9d-131">Schéma des paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="d1c9d-131">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
- [<span data-ttu-id="d1c9d-132">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="d1c9d-132">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)  
- [<span data-ttu-id="d1c9d-133">System.Security.Cryptography.CryptoConfig.CreateFromName</span><span class="sxs-lookup"><span data-stu-id="d1c9d-133">System.Security.Cryptography.CryptoConfig.CreateFromName</span></span>](Overload:System.Security.Cryptography.CryptoConfig.CreateFromName)  
- [<span data-ttu-id="d1c9d-134">Configuration des classes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="d1c9d-134">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
