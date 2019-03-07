---
title: IMetaDataImport::GetPinvokeMap, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetPinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetPinvokeMap
helpviewer_keywords:
- IMetaDataImport::GetPinvokeMap method [.NET Framework metadata]
- GetPinvokeMap method [.NET Framework metadata]
ms.assetid: b8685c1e-b80c-4198-8eb3-748d6f48a99e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ec32b285713e3e506359c4c831eb076d2b47a967
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57499765"
---
# <a name="imetadataimportgetpinvokemap-method"></a>IMetaDataImport::GetPinvokeMap, méthode
Obtient un jeton ModuleRef pour représenter l'assembly cible d'un appel PInvoke.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetPinvokeMap (  
   [in]  mdToken       tk,  
   [out] DWORD         *pdwMappingFlags,  
   [out] LPWSTR        szImportName,  
   [in]  ULONG         cchImportName,  
   [out] ULONG         *pchImportName,  
   [out] mdModuleRef   *pmrImportDLL  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `tk`  
 [in] Jeton FieldDef ou MethodDef pour obtenir les métadonnées de mappage PInvoke.  
  
 `pdwMappingFlags`  
 [out] Pointeur vers les indicateurs utilisés pour le mappage. Cette valeur est un masque de bits à partir de la [CorPinvokeMap](../../../../docs/framework/unmanaged-api/metadata/corpinvokemap-enumeration.md) énumération.  
  
 `szImportName`  
 [out] Le nom de la DLL cible non managée.  
  
 `cchImportName`  
 [in] La taille en caractères larges de `szImportName`.  
  
 `pchImportName`  
 [out] Le nombre de caractères étendus retournés dans `szImportName`.  
  
 `pmrImportDLL`  
 [out] Pointeur vers un jeton ModuleRef qui représente la bibliothèque d’objets cible non managée.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi
- [IMetaDataImport, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
- [IMetaDataImport2, interface](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
