---
title: ICorDebugModule::GetToken, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetToken
helpviewer_keywords:
- ICorDebugModule::GetToken method [.NET Framework debugging]
- GetToken method, ICorDebugModule interface [.NET Framework debugging]
ms.assetid: f759f87a-18ae-4c1a-8300-29b803432d0a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c28182feff8e4b7d49b7d068da1496d44fa2f917
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59150356"
---
# <a name="icordebugmodulegettoken-method"></a>ICorDebugModule::GetToken, méthode
Obtient le jeton pour l’entrée de table pour ce module.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetToken(  
    [out] mdModule *pToken  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pToken`  
 [out] Un pointeur vers le `mdModule` jeton qui référence les métadonnées du module.  
  
## <a name="remarks"></a>Notes  
 Le jeton peut être passé à la [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md), [IMetaDataImport2](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md), et [IMetaDataAssemblyImport](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interfaces d’importation de métadonnées.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions de .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Métadonnées](../../../../docs/framework/unmanaged-api/metadata/index.md)
