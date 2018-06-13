---
title: '&lt;cryptographySettings&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptographySettings
helpviewer_keywords:
- cryptographySettings element
- <cryptographySettings> element
ms.assetid: 6201b7da-bcb7-49f7-b9f5-ba1fe05573b9
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 14b510df192dcff1f005eec4f029aa0f26b967a4
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32751933"
---
# <a name="ltcryptographysettingsgt-element"></a><span data-ttu-id="b9649-102">&lt;cryptographySettings&gt; élément</span><span class="sxs-lookup"><span data-stu-id="b9649-102">&lt;cryptographySettings&gt; Element</span></span>
<span data-ttu-id="b9649-103">Contient des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="b9649-103">Contains cryptography settings.</span></span>  
  
 <span data-ttu-id="b9649-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="b9649-104">\<configuration></span></span>  
<span data-ttu-id="b9649-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="b9649-105">\<mscorlib></span></span>  
<span data-ttu-id="b9649-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="b9649-106">\<cryptographySettings></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9649-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9649-107">Syntax</span></span>  
  
```xml  
      <cryptographySettings>   
</cryptographySettings>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="b9649-108">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="b9649-108">Attributes and Elements</span></span>  
 <span data-ttu-id="b9649-109">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="b9649-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="b9649-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="b9649-110">Attributes</span></span>  
 <span data-ttu-id="b9649-111">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b9649-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="b9649-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b9649-112">Child Elements</span></span>  
  
|<span data-ttu-id="b9649-113">Élément</span><span class="sxs-lookup"><span data-stu-id="b9649-113">Element</span></span>|<span data-ttu-id="b9649-114">Description</span><span class="sxs-lookup"><span data-stu-id="b9649-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="b9649-115">\<cryptoNameMapping ></span><span class="sxs-lookup"><span data-stu-id="b9649-115">\<cryptoNameMapping></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptonamemapping-element.md)|<span data-ttu-id="b9649-116">Contient des mappages de classes à des noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="b9649-116">Contains mappings of classes to friendly names.</span></span>|  
|[<span data-ttu-id="b9649-117">\<oidMap ></span><span class="sxs-lookup"><span data-stu-id="b9649-117">\<oidMap></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidmap-element.md)|<span data-ttu-id="b9649-118">Contient les mappages de d’identificateur d’objet ASN.1 aux classes.</span><span class="sxs-lookup"><span data-stu-id="b9649-118">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="b9649-119">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="b9649-119">Parent Elements</span></span>  
  
|<span data-ttu-id="b9649-120">Élément</span><span class="sxs-lookup"><span data-stu-id="b9649-120">Element</span></span>|<span data-ttu-id="b9649-121">Description</span><span class="sxs-lookup"><span data-stu-id="b9649-121">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="b9649-122">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b9649-122">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`mscorlib`|<span data-ttu-id="b9649-123">Contient le `cryptographySettings` élément.</span><span class="sxs-lookup"><span data-stu-id="b9649-123">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="b9649-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="b9649-124">Example</span></span>  
 <span data-ttu-id="b9649-125">L’exemple suivant montre comment utiliser le  **\<cryptographySettings >** élément doit contenir les mappages de noms de chiffrement et les mappages de l’OID.</span><span class="sxs-lookup"><span data-stu-id="b9649-125">The following example shows how use the **\<cryptographySettings>** element to contain cryptography name mappings and OID mappings.</span></span> <span data-ttu-id="b9649-126">Cet exemple configure l’exécution afin que <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> retourne un `MyHashClass` objet et la `MyCryptoClass` classe correspond à l’OID 1.3.36.2.1.</span><span class="sxs-lookup"><span data-stu-id="b9649-126">This example configures the runtime so that <xref:System.Security.Cryptography.HashAlgorithm.Create%2A?displayProperty=nameWithType> returns a `MyHashClass` object and the `MyCryptoClass` class maps to the object identifier 1.3.36.2.1.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyHash="MyHashClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="System.Security.Cryptography.HashAlgorithm"  
                       class="MyHash"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"   name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="b9649-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9649-127">See Also</span></span>  
 [<span data-ttu-id="b9649-128">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="b9649-128">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="b9649-129">Schéma des paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="b9649-129">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [<span data-ttu-id="b9649-130">Services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="b9649-130">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
