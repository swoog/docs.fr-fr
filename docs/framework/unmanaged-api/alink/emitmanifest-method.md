---
title: EmitManifest, méthode
ms.date: 03/30/2017
api_name:
- EmitManifest
- IALink.EmitManifest
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- EmitManifest
helpviewer_keywords:
- EmitManifest method
ms.assetid: fdebc1f3-b62e-4d9e-b775-8ccaa8ecb250
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9217a045a8ddf6ad41adcc71a9568a05fe3fb334
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54565541"
---
# <a name="emitmanifest-method"></a>EmitManifest, méthode
Émet le manifeste final. Appelez cette méthode après l’importation de tous les autres fichiers et la définition de toutes les options. N’appelez pas cette méthode pour les modules indépendants.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EmitManifest(  
    mdAssembly   AssemblyID,  
    DWORD*       pdwReserveSize,  
    mdAssembly*  ptkManifest  
) PURE;  
```  
  
#### <a name="parameters"></a>Paramètres  
 `AssemblyID`  
 ID de l’assembly.  
  
 `pdwReserveSize`  
 Reçoit la taille à réserver dans le fichier d’assembly, récupérée à partir de [StrongNameSignatureSize, fonction](../../../../docs/framework/unmanaged-api/strong-naming/strongnamesignaturesize-function.md).  
  
 `ptkManifest`  
 Si vous le souhaitez reçoit le jeton de manifeste d’assembly.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Spécifications  
 Nécessite alink.h.  
  
## <a name="see-also"></a>Voir aussi
- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
