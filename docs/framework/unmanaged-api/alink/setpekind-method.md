---
title: SetPEKind, méthode
ms.date: 03/30/2017
api_name:
- IALink2.SetPEKind
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- SetPEKind
helpviewer_keywords:
- SetPEKind method
ms.assetid: 050e77ee-3014-45c0-9e29-2ebe29347b0d
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e568050a5cc94da865d656adc8a775024dab836c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57500042"
---
# <a name="setpekind-method"></a>SetPEKind, méthode
Détermine le type de fichier exécutable portable, spécifiques à l’ordinateur ou indépendant de l’ordinateur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetPEKind(  
    mdAssembly AssemblyID,  
    mdToken FileToken,  
    DWORD dwPEKind,  
    DWORD dwMachine  
) PURE;   
```  
  
## <a name="parameters"></a>Paramètres  
 `AssemblyID`  
 ID de l’assembly.  
  
 `FileToken`  
 Jeton du fichier pour lequel le type PE doit être défini. Peut être NULL si `AssemblyID` n’indique pas un netmodule indépendant.  
  
 `dwPEKind`  
 Le type de PE, comme indiqué par le [CorPEKind, énumération](../../../../docs/framework/unmanaged-api/metadata/corpekind-enumeration.md).  
  
 `dwMachine`  
 L’architecture d’ordinateur cible, comme indiqué dans l’en-tête NT.  
  
## <a name="return-value"></a>Valeur de retour  
 Retourne S_OK si la méthode réussit.  
  
## <a name="requirements"></a>Spécifications  
 Nécessite alink.h.  
  
## <a name="see-also"></a>Voir aussi
- [GetPEKind, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getpekind-method.md)
- [IALink2, interface](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [IALink, interface](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [API ALink](../../../../docs/framework/unmanaged-api/alink/index.md)
