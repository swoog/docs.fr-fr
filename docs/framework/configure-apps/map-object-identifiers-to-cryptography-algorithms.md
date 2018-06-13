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
manager: markl
ms.openlocfilehash: 7801c55cf6b3334347788013d9052038d5d2f3ec
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/03/2018
ms.locfileid: "32756616"
---
# <a name="mapping-object-identifiers-to-cryptography-algorithms"></a>Mappage d'identificateurs d'objet à des algorithmes de chiffrement
Les signatures numériques garantissent que les données ne sont pas falsifiées lors de l’envoi d’un programme à un autre. En règle générale, la signature numérique est calculée en appliquant une fonction mathématique au hachage des données à signer. Lors de la mise en forme une valeur de hachage à signer, certains algorithmes de signature numérique ajouter un identificateur d’objet ASN.1 (OID) dans le cadre de l’opération de mise en forme. L’OID identifie l’algorithme utilisé pour calculer le hachage. Vous pouvez mapper des algorithmes à des identificateurs d’objet pour étendre le mécanisme de chiffrement pour utiliser des algorithmes personnalisés. L’exemple suivant montre comment mapper un identificateur d’objet à un nouvel algorithme de hachage.  
  
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
  
 Le [ \<oidEntry > élément](../../../docs/framework/configure-apps/file-schema/cryptography/oidentry-element.md) contient deux attributs. Le **OID** attribut est le numéro d’identification de l’objet. Le **nom** attribut est la valeur de la **nom** attribut à partir de la [ \<nameEntry > élément](../../../docs/framework/configure-apps/file-schema/cryptography/nameentry-element.md). Il doit exister un mappage à partir d’un nom d’algorithme à une classe avant un identificateur d’objet peut être mappé à un nom simple.  
  
## <a name="see-also"></a>Voir aussi  
 [Configuration des classes de chiffrement](../../../docs/framework/configure-apps/configure-cryptography-classes.md)  
 [Cryptographic Services](../../../docs/standard/security/cryptographic-services.md)
