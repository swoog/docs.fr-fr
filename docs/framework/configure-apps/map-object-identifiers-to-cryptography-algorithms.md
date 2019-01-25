---
title: Mappage d'identificateurs d'objet à des algorithmes de chiffrement
ms.date: 03/30/2017
helpviewer_keywords:
- digital signatures
- identifiers, mapping object identifiers
- cryptographic algorithms
- mapping object identifiers
- cryptography, mapping object identifiers
ms.assetid: c9673f81-bf9e-47fd-bc6f-6bc1c1c4c15e
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 1bb5c6b46ff0f75082b0b7b631a197dd64156cf9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672862"
---
# <a name="mapping-object-identifiers-to-cryptography-algorithms"></a><span data-ttu-id="f74a8-102">Mappage d'identificateurs d'objet à des algorithmes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="f74a8-102">Mapping Object Identifiers to Cryptography Algorithms</span></span>
<span data-ttu-id="f74a8-103">Les signatures numériques garantissent que les données ne sont pas falsifiées lorsqu’elles sont envoyées à partir d’un programme vers un autre.</span><span class="sxs-lookup"><span data-stu-id="f74a8-103">Digital signatures ensure that data is not tampered with when it is sent from one program to another.</span></span> <span data-ttu-id="f74a8-104">En règle générale, la signature numérique est calculée en appliquant une fonction mathématique au hachage des données à signer.</span><span class="sxs-lookup"><span data-stu-id="f74a8-104">Typically the digital signature is computed by applying a mathematical function to the hash of the data to be signed.</span></span> <span data-ttu-id="f74a8-105">Lors de la mise en forme une valeur de hachage à signer, certains algorithmes de signature numérique d’ajouter un identificateur d’objet ASN.1 (OID) dans le cadre de l’opération de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="f74a8-105">When formatting a hash value to be signed, some digital signature algorithms append an ASN.1 Object Identifier (OID) as part of the formatting operation.</span></span> <span data-ttu-id="f74a8-106">L’OID identifie l’algorithme qui a été utilisé pour calculer le hachage.</span><span class="sxs-lookup"><span data-stu-id="f74a8-106">The OID identifies the algorithm that was used to compute the hash.</span></span> <span data-ttu-id="f74a8-107">Vous pouvez mapper des algorithmes à des identificateurs d’objet pour étendre le mécanisme de chiffrement pour utiliser des algorithmes personnalisés.</span><span class="sxs-lookup"><span data-stu-id="f74a8-107">You can map algorithms to object identifiers to extend the cryptography mechanism to use custom algorithms.</span></span> <span data-ttu-id="f74a8-108">L’exemple suivant montre comment mapper un identificateur d’objet à un nouvel algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="f74a8-108">The following example shows how to map an object identifier to a new hash algorithm.</span></span>  
  
```xml  
<configuration>  
   <mscorlib>  
      <cryptographySettings>  
         <cryptoNameMapping>  
            <cryptoClasses>  
               <cryptoClass MyNewHash="MyNewHashClass, MyAssembly  
                  Culture='en', PublicKeyToken=a5d015c7d5a0b012,  
                  Version=1.0.0.0"/>  
            </cryptoClasses>  
            <nameEntry name="NewHash" class="MyNewHash"/>  
         </cryptoNameMapping>  
         <oidMap>  
            <oidEntry OID="1.3.14.33.42.46"  name="NewHash"/>  
         </oidMap>  
      </cryptographySettings>  
   </mscorlib>  
</configuration>  
```  
  
 <span data-ttu-id="f74a8-109">Le [ \<oidEntry > élément](../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md) contient deux attributs.</span><span class="sxs-lookup"><span data-stu-id="f74a8-109">The [\<oidEntry> element](../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md) contains two attributes.</span></span> <span data-ttu-id="f74a8-110">Le **OID** attribut est le numéro de l’identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="f74a8-110">The **OID** attribute is the object identifier number.</span></span> <span data-ttu-id="f74a8-111">Le **nom** attribut est la valeur de la **nom** attribut à partir de la [ \<nameEntry > élément](../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md).</span><span class="sxs-lookup"><span data-stu-id="f74a8-111">The **name** attribute is the value of the **name** attribute from the [\<nameEntry> element](../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md).</span></span> <span data-ttu-id="f74a8-112">Il doit être un mappage à partir d’un nom d’algorithme à une classe avant un identificateur d’objet peut être mappé à un nom simple.</span><span class="sxs-lookup"><span data-stu-id="f74a8-112">There must be a mapping from an algorithm name to a class before an object identifier can be mapped to a simple name.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f74a8-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f74a8-113">See also</span></span>
- [<span data-ttu-id="f74a8-114">Configuration des classes de chiffrement</span><span class="sxs-lookup"><span data-stu-id="f74a8-114">Configuring Cryptography Classes</span></span>](../../../docs/framework/configure-apps/configure-cryptography-classes.md)
- [<span data-ttu-id="f74a8-115">Cryptographic Services</span><span class="sxs-lookup"><span data-stu-id="f74a8-115">Cryptographic Services</span></span>](../../../docs/standard/security/cryptographic-services.md)
