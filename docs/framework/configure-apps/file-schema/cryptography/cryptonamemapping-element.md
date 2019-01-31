---
title: Élément <cryptoNameMapping>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptoNameMapping
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/cryptoNameMapping
helpviewer_keywords:
- <cryptoNameMapping> element
- cryptoNameMapping element
ms.assetid: c59c9494-149b-4ce6-b38d-371f896ae85c
ms.openlocfilehash: ff3300f57fd4681875e2791610cc5a0d0dcba31b
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55281474"
---
# <a name="cryptonamemapping-element"></a><span data-ttu-id="9f25f-102">\<cryptoNameMapping> Element</span><span class="sxs-lookup"><span data-stu-id="9f25f-102">\<cryptoNameMapping> Element</span></span>
<span data-ttu-id="9f25f-103">Contient des mappages de classes à des noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="9f25f-103">Contains mappings of classes to friendly names.</span></span>  
  
 <span data-ttu-id="9f25f-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="9f25f-104">\<configuration></span></span>  
<span data-ttu-id="9f25f-105">\<mscorlib></span><span class="sxs-lookup"><span data-stu-id="9f25f-105">\<mscorlib></span></span>  
<span data-ttu-id="9f25f-106">\<cryptographySettings></span><span class="sxs-lookup"><span data-stu-id="9f25f-106">\<cryptographySettings></span></span>  
<span data-ttu-id="9f25f-107">\<cryptoNameMapping></span><span class="sxs-lookup"><span data-stu-id="9f25f-107">\<cryptoNameMapping></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f25f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f25f-108">Syntax</span></span>  
  
```xml  
      <cryptoNameMapping>   
</cryptoNameMapping>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9f25f-109">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="9f25f-109">Attributes and Elements</span></span>  
 <span data-ttu-id="9f25f-110">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="9f25f-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9f25f-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="9f25f-111">Attributes</span></span>  
 <span data-ttu-id="9f25f-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9f25f-112">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="9f25f-113">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9f25f-113">Child Elements</span></span>  
  
|<span data-ttu-id="9f25f-114">Élément</span><span class="sxs-lookup"><span data-stu-id="9f25f-114">Element</span></span>|<span data-ttu-id="9f25f-115">Description</span><span class="sxs-lookup"><span data-stu-id="9f25f-115">Description</span></span>|  
|-------------|-----------------|  
|`cryptoClasses`|<span data-ttu-id="9f25f-116">Contient la liste des classes de chiffrement qui ont un mappage à un nom convivial dans l’élément **\<nameEntry>**.</span><span class="sxs-lookup"><span data-stu-id="9f25f-116">Contains a list of cryptography classes that have a mapping to a friendly name in the **\<nameEntry>** element.</span></span>|  
|`nameEntry`|<span data-ttu-id="9f25f-117">Mappe un nom de classe à un nom d’algorithme convivial, ce qui permet à une classe d’avoir plusieurs noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="9f25f-117">Maps a class name to a friendly algorithm name, which allows one class to have many friendly names.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9f25f-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9f25f-118">Parent Elements</span></span>  
  
|<span data-ttu-id="9f25f-119">Élément</span><span class="sxs-lookup"><span data-stu-id="9f25f-119">Element</span></span>|<span data-ttu-id="9f25f-120">Description</span><span class="sxs-lookup"><span data-stu-id="9f25f-120">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="9f25f-121">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9f25f-121">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="9f25f-122">Contient des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="9f25f-122">Contains cryptography settings.</span></span>|  
|`cryptoNameMapping`|<span data-ttu-id="9f25f-123">Contient des mappages de classes à des noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="9f25f-123">Contains mappings of classes to friendly names.</span></span>|  
|`mscorlib`|<span data-ttu-id="9f25f-124">Contient le \<cryptographySettings > élément.</span><span class="sxs-lookup"><span data-stu-id="9f25f-124">Contains the \<cryptographySettings> element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="9f25f-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="9f25f-125">Example</span></span>  
 <span data-ttu-id="9f25f-126">L’exemple suivant montre comment utiliser le  **\<cryptoNameMapping >** élément à référencer une classe de chiffrement et configurer le runtime.</span><span class="sxs-lookup"><span data-stu-id="9f25f-126">The following example shows how to use the **\<cryptoNameMapping>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="9f25f-127">Vous pouvez ensuite passer la chaîne « RSA » à la <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> méthode et l’utilisation du <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> méthode pour retourner un `MyCryptoRSAClass` objet.</span><span class="sxs-lookup"><span data-stu-id="9f25f-127">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass   MyCryptoRSA="MyCryptoRSAClass, MyAssembly  
                  Culture=neutral, PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="RSA" class="MyCryptoRSA"/>  
            <nameEntry name="System.Security.Cryptography.AsymmetricAlgorithm"  
                       class="MyCryptoRSA"/>  
         </cryptoNameMapping>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9f25f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f25f-128">See also</span></span>
- [<span data-ttu-id="9f25f-129">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="9f25f-129">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="9f25f-130">Schéma des paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="9f25f-130">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)
- [<span data-ttu-id="9f25f-131">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="9f25f-131">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)
- [<span data-ttu-id="9f25f-132">Configuration des classes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="9f25f-132">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
