---
title: CreateAssemblyEnum, fonction
ms.date: 03/30/2017
api_name:
- CreateAssemblyEnum
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateAssemblyEnum
helpviewer_keywords:
- CreateAssemblyEnum function [.NET Framework fusion]
ms.assetid: 3506df38-6cea-42f6-946e-4287863bcfb3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b2098d5d9ce1c01f232cf2904c1fd3e990dfbe2e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432114"
---
# <a name="createassemblyenum-function"></a>CreateAssemblyEnum, fonction
Obtient un pointeur vers un [IAssemblyEnum](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md) instance qui peut énumérer les objets dans l’assembly avec l’objet [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT CreateAssemblyEnum (  
    [out] IAssemblyEnum  **pEnum,  
    [in]  IUnknown       *pUnkReserved,  
    [in]  IAssemblyName  *pName,  
    [in]  DWORD          dwFlags,  
    [in]  LPVOID         pvReserved  
 );  
```  
  
#### <a name="parameters"></a>Paramètres  
 `pEnum`  
 [out] Pointeur vers un emplacement de mémoire qui contient l’élément demandé `IAssemblyEnum` pointeur.  
  
 `pUnkReserved`  
 [in] Réservé pour une future extensibilité. `pUnkReserved` doit être une référence null.  
  
 `pName`  
 [in] Le `IAssemblyName` de l’assembly demandé. Ce nom est utilisé pour filtrer l’énumération. Il peut être null pour énumérer tous les assemblys dans le global assembly cache.  
  
 `dwFlags`  
 [in] Indicateurs permettant de modifier le comportement de l’énumérateur. Ce paramètre contient exactement un bit de le [ASM_CACHE_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cache-flags-enumeration.md) énumération.  
  
 `pvReserved`  
 [in] Réservé pour une future extensibilité. `pvReserved` doit être une référence null.  
  
## <a name="remarks"></a>Notes  
 Le `dwFlags` paramètre contient exactement un bit de le `ASM_CACHE_FLAGS` énumération.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** Fusion.h  
  
 **Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [IAssemblyEnum, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyenum-interface.md)  
 [IAssemblyName, interface](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [Fonctions statiques globales de fusion](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
