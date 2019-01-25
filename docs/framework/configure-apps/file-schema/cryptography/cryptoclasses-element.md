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
ms.openlocfilehash: e3bc8fbb103d59b825e07cc52b155f1ea8061f31
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54649373"
---
# <a name="ltcryptoclassesgt-element"></a><span data-ttu-id="86bf5-102">&lt;cryptoClasses&gt; élément</span><span class="sxs-lookup"><span data-stu-id="86bf5-102">&lt;cryptoClasses&gt; Element</span></span>
<span data-ttu-id="86bf5-103">Contient la liste des classes de chiffrement qui ont un mappage à un nom convivial dans l’élément [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md).</span><span class="sxs-lookup"><span data-stu-id="86bf5-103">Contains a list of cryptography classes that have a mapping to a friendly name in the [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) element.</span></span>  
  
 <span data-ttu-id="86bf5-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="86bf5-104">\<configuration></span></span>  
<span data-ttu-id="86bf5-105">\<mscorlib></span><span class="sxs-lookup"><span data-stu-id="86bf5-105">\<mscorlib></span></span>  
<span data-ttu-id="86bf5-106">\<cryptographySettings></span><span class="sxs-lookup"><span data-stu-id="86bf5-106">\<cryptographySettings></span></span>  
<span data-ttu-id="86bf5-107">\<cryptoNameMapping></span><span class="sxs-lookup"><span data-stu-id="86bf5-107">\<cryptoNameMapping></span></span>  
<span data-ttu-id="86bf5-108">\<cryptoClasses></span><span class="sxs-lookup"><span data-stu-id="86bf5-108">\<cryptoClasses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86bf5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86bf5-109">Syntax</span></span>  
  
```xml  
<cryptoClasses>   
</cryptoClasses>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="86bf5-110">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="86bf5-110">Attributes and Elements</span></span>  
 <span data-ttu-id="86bf5-111">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="86bf5-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="86bf5-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="86bf5-112">Attributes</span></span>  
 <span data-ttu-id="86bf5-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="86bf5-113">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="86bf5-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="86bf5-114">Child Elements</span></span>  
  
|<span data-ttu-id="86bf5-115">Élément</span><span class="sxs-lookup"><span data-stu-id="86bf5-115">Element</span></span>|<span data-ttu-id="86bf5-116">Description</span><span class="sxs-lookup"><span data-stu-id="86bf5-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="86bf5-117">\<cryptoClass></span><span class="sxs-lookup"><span data-stu-id="86bf5-117">\<cryptoClass></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptoclass-element.md)|<span data-ttu-id="86bf5-118">Contient une classe de chiffrement qui a un mappage à un nom convivial dans l’élément **\<nameEntry>**.</span><span class="sxs-lookup"><span data-stu-id="86bf5-118">Contains a cryptography class that has a mapping to a friendly name in the **\<nameEntry>** element.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="86bf5-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="86bf5-119">Parent Elements</span></span>  
  
|<span data-ttu-id="86bf5-120">Élément</span><span class="sxs-lookup"><span data-stu-id="86bf5-120">Element</span></span>|<span data-ttu-id="86bf5-121">Description</span><span class="sxs-lookup"><span data-stu-id="86bf5-121">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="86bf5-122">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="86bf5-122">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="86bf5-123">Contient des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="86bf5-123">Contains cryptography settings.</span></span>|  
|`cryptoNameMapping`|<span data-ttu-id="86bf5-124">Contient des mappages de classes à des noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="86bf5-124">Contains mappings of classes to friendly names.</span></span>|  
|`mscorlib`|<span data-ttu-id="86bf5-125">Contient le `cryptographySettings` élément.</span><span class="sxs-lookup"><span data-stu-id="86bf5-125">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="86bf5-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="86bf5-126">Example</span></span>  
 <span data-ttu-id="86bf5-127">L’exemple suivant montre comment utiliser le  **\<cryptoClass >** élément à référencer une classe de chiffrement et configurer le runtime.</span><span class="sxs-lookup"><span data-stu-id="86bf5-127">The following example shows how use the **\<cryptoClass>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="86bf5-128">Vous pouvez ensuite passer la chaîne « RSA » à la <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> méthode et l’utilisation du <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> méthode pour retourner un `MyCryptoRSAClass` objet.</span><span class="sxs-lookup"><span data-stu-id="86bf5-128">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="86bf5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86bf5-129">See also</span></span>
- <xref:System.Security.Cryptography>
- [<span data-ttu-id="86bf5-130">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="86bf5-130">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="86bf5-131">Schéma des paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="86bf5-131">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)
- [<span data-ttu-id="86bf5-132">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="86bf5-132">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
- [<span data-ttu-id="86bf5-133">System.Security.Cryptography.CryptoConfig.CreateFromName</span><span class="sxs-lookup"><span data-stu-id="86bf5-133">System.Security.Cryptography.CryptoConfig.CreateFromName</span></span>](Overload:System.Security.Cryptography.CryptoConfig.CreateFromName)
- [<span data-ttu-id="86bf5-134">Configuration des classes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="86bf5-134">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
