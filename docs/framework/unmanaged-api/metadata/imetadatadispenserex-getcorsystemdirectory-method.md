---
title: IMetaDataDispenserEx::GetCORSystemDirectory, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.GetCORSystemDirectory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::GetCORSystemDirectory
helpviewer_keywords:
- IMetaDataDispenserEx::GetCORSystemDirectory method [.NET Framework metadata]
- GetCORSystemDirectory method [.NET Framework metadata]
ms.assetid: d9e0f3b6-e106-4820-bada-5bfba34ce360
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cf580f6d3fb18e729f3eca300aa817036eb61e4f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443428"
---
# <a name="imetadatadispenserexgetcorsystemdirectory-method"></a>IMetaDataDispenserEx::GetCORSystemDirectory, méthode
Obtient le répertoire qui contient le common language runtime (CLR) actuel. Cette méthode est prise en charge uniquement pour une utilisation par les débogueurs out-of-process. Si elle est appelée à partir d’un autre composant, elle retournera E_NOTIMPL.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetCORSystemDirectory (  
    [out] LPWSTR      szBuffer,   
    [in]  DWORD       cchBuffer,   
    [out] DWORD*      pchBuffer  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `szBuffer`  
 [out] La mémoire tampon pour recevoir le nom de répertoire.  
  
 `cchBuffer`  
 [in] La taille, en octets, de `szBuffer`.  
  
 `pchBuffer`  
 [out] Le nombre d’octets retournés dans `szBuffer`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateforme :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Cor.h  
  
 **Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IMetaDataDispenserEx, interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)  
 [IMetaDataDispenser, interface](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
