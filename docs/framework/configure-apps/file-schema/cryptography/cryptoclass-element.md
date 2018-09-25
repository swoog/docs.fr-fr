---
title: '&lt;cryptoClass&gt; élément'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/mscorlib/cryptographySettings/cryptoNameMapping/cryptoClasses/cryptoClass
- http://schemas.microsoft.com/.NetConfiguration/v2.0#cryptoClass
helpviewer_keywords:
- cryptoClass element
- <cryptoClass> element
ms.assetid: 03db52ef-010e-44ea-b6fd-b9c900ecad50
author: mcleblanc
ms.author: markl
ms.openlocfilehash: e74cc5fa99473562b158cd5068fb8bbaeb6a4a17
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47083911"
---
# <a name="ltcryptoclassgt-element"></a><span data-ttu-id="dcf44-102">&lt;cryptoClass&gt; élément</span><span class="sxs-lookup"><span data-stu-id="dcf44-102">&lt;cryptoClass&gt; Element</span></span>
<span data-ttu-id="dcf44-103">Contient une classe de chiffrement qui a un mappage à un nom convivial dans l’élément [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md).</span><span class="sxs-lookup"><span data-stu-id="dcf44-103">Contains a cryptography class that has a mapping to a friendly name in the [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) element.</span></span>  
  
 <span data-ttu-id="dcf44-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="dcf44-104">\<configuration></span></span>  
<span data-ttu-id="dcf44-105">\<mscorlib ></span><span class="sxs-lookup"><span data-stu-id="dcf44-105">\<mscorlib></span></span>  
<span data-ttu-id="dcf44-106">\<cryptographySettings ></span><span class="sxs-lookup"><span data-stu-id="dcf44-106">\<cryptographySettings></span></span>  
<span data-ttu-id="dcf44-107">\<cryptoNameMapping ></span><span class="sxs-lookup"><span data-stu-id="dcf44-107">\<cryptoNameMapping></span></span>  
<span data-ttu-id="dcf44-108">\<cryptoClasses ></span><span class="sxs-lookup"><span data-stu-id="dcf44-108">\<cryptoClasses></span></span>  
<span data-ttu-id="dcf44-109">\<cryptoClass ></span><span class="sxs-lookup"><span data-stu-id="dcf44-109">\<cryptoClass></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcf44-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcf44-110">Syntax</span></span>  
  
```xml  
<cryptoClass customClassName="fully qualified type name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="dcf44-111">Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="dcf44-111">Attributes and Elements</span></span>  
 <span data-ttu-id="dcf44-112">Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.</span><span class="sxs-lookup"><span data-stu-id="dcf44-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="dcf44-113">Attributs</span><span class="sxs-lookup"><span data-stu-id="dcf44-113">Attributes</span></span>  
  
|<span data-ttu-id="dcf44-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="dcf44-114">Attribute</span></span>|<span data-ttu-id="dcf44-115">Description</span><span class="sxs-lookup"><span data-stu-id="dcf44-115">Description</span></span>|  
|---------------|-----------------|  
|`customClassName`|<span data-ttu-id="dcf44-116">Attribut requis.</span><span class="sxs-lookup"><span data-stu-id="dcf44-116">Required attribute.</span></span><br /><br /> <span data-ttu-id="dcf44-117">Contient les informations pour la classe de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="dcf44-117">Contains the information for the cryptography class.</span></span> <span data-ttu-id="dcf44-118">Utilisez cet attribut pour fournir un nom court pour votre classe.</span><span class="sxs-lookup"><span data-stu-id="dcf44-118">Use this attribute to provide a short name for your class.</span></span> <span data-ttu-id="dcf44-119">Vous devez spécifier une chaîne conforme aux exigences spécifiées dans [spécifiant des noms de types qualifiés complets](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span><span class="sxs-lookup"><span data-stu-id="dcf44-119">You must specify a string that meets the requirements specified in [Specifying Fully Qualified Type Names](../../../../../docs/framework/reflection-and-codedom/specifying-fully-qualified-type-names.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="dcf44-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dcf44-120">Child Elements</span></span>  
 <span data-ttu-id="dcf44-121">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dcf44-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="dcf44-122">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dcf44-122">Parent Elements</span></span>  
  
|<span data-ttu-id="dcf44-123">Élément</span><span class="sxs-lookup"><span data-stu-id="dcf44-123">Element</span></span>|<span data-ttu-id="dcf44-124">Description</span><span class="sxs-lookup"><span data-stu-id="dcf44-124">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="dcf44-125">Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="dcf44-125">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`cryptoClasses`|<span data-ttu-id="dcf44-126">Contient la liste des classes de chiffrement qui ont un mappage à un nom convivial dans l’élément [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md).</span><span class="sxs-lookup"><span data-stu-id="dcf44-126">Contains a list of cryptography classes that have a mapping to a friendly name in the [\<nameEntry>](../../../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md) element.</span></span>|  
|`cryptographySettings`|<span data-ttu-id="dcf44-127">Contient des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="dcf44-127">Contains cryptography settings.</span></span>|  
|`cryptoNameMapping`|<span data-ttu-id="dcf44-128">Contient des mappages de classes à des noms conviviaux.</span><span class="sxs-lookup"><span data-stu-id="dcf44-128">Contains mappings of classes to friendly names.</span></span>|  
|`mscorlib`|<span data-ttu-id="dcf44-129">Contient l’élément [\<cryptographySettings>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptographysettings-element.md).</span><span class="sxs-lookup"><span data-stu-id="dcf44-129">Contains the [\<cryptographySettings>](../../../../../docs/framework/configure-apps/file-schema/cryptography/cryptographysettings-element.md) element.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="dcf44-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="dcf44-130">Example</span></span>  
 <span data-ttu-id="dcf44-131">L’exemple suivant montre comment utiliser le  **\<cryptoClass >** élément à référencer une classe de chiffrement et configurer le runtime.</span><span class="sxs-lookup"><span data-stu-id="dcf44-131">The following example shows how use the **\<cryptoClass>** element to reference a cryptography class and to configure the runtime.</span></span> <span data-ttu-id="dcf44-132">Vous pouvez ensuite passer la chaîne « RSA » à la <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> méthode et l’utilisation du <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> méthode pour retourner un `MyCryptoRSAClass` objet.</span><span class="sxs-lookup"><span data-stu-id="dcf44-132">You can then pass the string "RSA" to the <xref:System.Security.Cryptography.CryptoConfig.CreateFromName%2A?displayProperty=nameWithType> method and use the <xref:System.Security.Cryptography.AsymmetricAlgorithm.Create%2A> method to return a `MyCryptoRSAClass` object.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="dcf44-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcf44-133">See Also</span></span>  
 [<span data-ttu-id="dcf44-134">Schéma des fichiers de configuration</span><span class="sxs-lookup"><span data-stu-id="dcf44-134">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="dcf44-135">Schéma des paramètres de chiffrement</span><span class="sxs-lookup"><span data-stu-id="dcf44-135">Cryptography Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/cryptography/index.md)  
 [<span data-ttu-id="dcf44-136">Services de chiffrement</span><span class="sxs-lookup"><span data-stu-id="dcf44-136">Cryptographic Services</span></span>](../../../../../docs/standard/security/cryptographic-services.md)  
 [<span data-ttu-id="dcf44-137">Configuration des classes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="dcf44-137">Configuring Cryptography Classes</span></span>](../../../../../docs/framework/configure-apps/configure-cryptography-classes.md)
