---
title: Authenticode (Informations de référence sur les API non managées)
ms.date: 03/30/2017
ms.assetid: 7e8cc303-6e77-4116-aa8b-7ea297a3a467
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 408219307015d5c39cb581b3884ed9810f4c0566
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59216344"
---
# <a name="authenticode-unmanaged-api-reference"></a>Authenticode (Informations de référence sur les API non managées)
Prend en charge le module de création et de vérification des licences XrML Authenticode.  
  
## <a name="in-this-section"></a>Dans cette section  
 [_AxlGetIssuerPublicKeyHash, fonction](../../../../docs/framework/unmanaged-api/authenticode/axlgetissuerpublickeyhash-function.md)  
 Récupère le hachage SHA-1 de la clé publique associée à la clé privée utilisée pour signer le certificat spécifié.  
  
 [_AxlPublicKeyBlobToPublicKeyToken, fonction](../../../../docs/framework/unmanaged-api/authenticode/axlpublickeyblobtopublickeytoken-function.md)  
 Calcule le jeton de clé publique de nom fort à partir d'un format CSP PUBLICKEYBLOB.  
  
 [_AxlRSAKeyValueToPublicKeyToken, fonction](../../../../docs/framework/unmanaged-api/authenticode/axlrsakeyvaluetopublickeytoken-function.md)  
 Convertit un modulo et un exposant en un jeton de clé publique de nom fort.  
  
 [CertFreeAuthenticodeSignerInfo, fonction](../../../../docs/framework/unmanaged-api/authenticode/certfreeauthenticodesignerinfo-function.md)  
 Libère les ressources allouées pour la structure AXL_AUTHENTICODE_SIGNER_INFO.  
  
 [CertFreeAuthenticodeTimestamperInfo, fonction](../../../../docs/framework/unmanaged-api/authenticode/certfreeauthenticodetimestamperinfo-function.md)  
 Libère les ressources allouées pour la structure AXL_AUTHENTICODE_TIMESTAMPER_INFO.  
  
 [CertTimestampAuthenticodeLicense, fonction](../../../../docs/framework/unmanaged-api/authenticode/certtimestampauthenticodelicense-function.md)  
 Effectue un horodatage d'une licence XrML Authenticode créée par CertCreateAuthenticodeLicense.  
  
 [CertVerifyAuthenticodeLicense, fonction](../../../../docs/framework/unmanaged-api/authenticode/certverifyauthenticodelicense-function.md)  
 Vérifie la validité d'une licence XrML Authenticode.  
  
 [AXL_AUTHENTICODE_SIGNER_INFO, structure](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-signer-info-structure.md)  
 Définit les informations du signataire Authenticode.  
  
 [AXL_AUTHENTICODE_TIMESTAMPER_INFO, structure](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-timestamper-info-structure.md)  
 Définit les informations de l'horodateur Authenticode.  
  
## <a name="see-also"></a>Voir aussi

- [Informations de référence sur les API non managées](../../../../docs/framework/unmanaged-api/index.md)
