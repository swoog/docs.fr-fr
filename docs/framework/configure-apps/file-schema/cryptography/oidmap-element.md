---
title: '&lt;oidMap&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#oidMap
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/oidMap
helpviewer_keywords:
- <oidMap> element
- oidMap element
ms.assetid: 7f0c2246-c070-4748-b96a-2f66a296c539
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 4ec2ba884f0f60182dd59bb6a4491e223f43ce1a
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47196614"
---
# <a name="ltoidmapgt-element"></a><span data-ttu-id="a8eef-102">&lt;oidMap&gt; élément</span><span class="sxs-lookup"><span data-stu-id="a8eef-102">&lt;oidMap&gt; Element</span></span>
<span data-ttu-id="a8eef-103">Contient des mappages d’identificateur (OID) d’objet ASN.1 aux classes.</span><span class="sxs-lookup"><span data-stu-id="a8eef-103">Contains ASN.1 object identifier (OID) mappings to classes.</span></span>  
  
 <span data-ttu-id="a8eef-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="a8eef-104">\<configuration></span></span>  
<span data-ttu-id="a8eef-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="a8eef-105">\<mscorlib></span></span>  
<span data-ttu-id="a8eef-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="a8eef-106">\<cryptographySettings></span></span>  
<span data-ttu-id="a8eef-107">\<oidMap ></span><span class="sxs-lookup"><span data-stu-id="a8eef-107">\<oidMap></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8eef-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8eef-108">Syntax</span></span>  
  
```xml  
<oidMap>   
</oidMap>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a8eef-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="a8eef-109">Attributes and Elements</span></span>  
 <span data-ttu-id="a8eef-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="a8eef-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a8eef-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="a8eef-111">Attributes</span></span>  
 <span data-ttu-id="a8eef-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a8eef-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="a8eef-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a8eef-113">Child Elements</span></span>  
  
|<span data-ttu-id="a8eef-114">Élément</span><span class="sxs-lookup"><span data-stu-id="a8eef-114">Element</span></span>|<span data-ttu-id="a8eef-115">Description</span><span class="sxs-lookup"><span data-stu-id="a8eef-115">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a8eef-116">\<oidEntry ></span><span class="sxs-lookup"><span data-stu-id="a8eef-116">\<oidEntry></span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md)|<span data-ttu-id="a8eef-117">Mappe un OID ASN.1 à un nom convivial.</span><span class="sxs-lookup"><span data-stu-id="a8eef-117">Maps an ASN.1 OID to a friendly name.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="a8eef-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a8eef-118">Parent Elements</span></span>  
  
|<span data-ttu-id="a8eef-119">Élément</span><span class="sxs-lookup"><span data-stu-id="a8eef-119">Element</span></span>|<span data-ttu-id="a8eef-120">Description</span><span class="sxs-lookup"><span data-stu-id="a8eef-120">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="a8eef-121">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="a8eef-121">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="a8eef-122">Contient des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="a8eef-122">Contains cryptography settings.</span></span>|  
|`mscorlib`|<span data-ttu-id="a8eef-123">Contient le `cryptographySettings` élément.</span><span class="sxs-lookup"><span data-stu-id="a8eef-123">Contains the `cryptographySettings` element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="a8eef-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="a8eef-124">Example</span></span>  
 <span data-ttu-id="a8eef-125">L’exemple suivant montre comment utiliser le  **\<oidMap >** élément doit contenir un mappage d’un OID pour l’algorithme de hachage RIPEMD-160 à une implémentation de cet algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="a8eef-125">The following example shows how to use the **\<oidMap>** element to contain a mapping of an OID for the RIPEMD-160 hash algorithm to an implementation of that hash algorithm.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCrypto="MyCryptoClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RIPEMD-160" class="MyCrypto"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.36.3.2.1"  name="MyCryptoClass"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a8eef-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8eef-126">See Also</span></span>  
 [<span data-ttu-id="a8eef-127">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="a8eef-127">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="a8eef-128">Schéma des paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="a8eef-128">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [<span data-ttu-id="a8eef-129">Services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="a8eef-129">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)  
 [<span data-ttu-id="a8eef-130">Configuration des classes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="a8eef-130">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)  
 [<span data-ttu-id="a8eef-131">Mappage d'identificateurs d'objet à des algorithmes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="a8eef-131">Mapping Object Identifiers to Cryptography Algorithms</span></span>](../../../../../docs/framework/configure-apps/map-object-identifiers-to-cryptography-algorithms.md)
