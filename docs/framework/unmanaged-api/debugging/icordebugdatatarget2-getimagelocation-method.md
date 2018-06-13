---
title: ICorDebugDataTarget2::GetImageLocation, méthode
ms.date: 03/30/2017
ms.assetid: 696afe71-5852-478d-a33f-b2d2dbc4b91f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c6962c8063479b3b0279d771b1b0cd1df63f696b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33416414"
---
# <a name="icordebugdatatarget2getimagelocation-method"></a>ICorDebugDataTarget2::GetImageLocation, méthode
Retourne le chemin d’accès d’un module à partir de l’adresse de base du module.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetImageLocation(    [in] CORDB_ADDRESS baseAddress,  
    [in] ULONG32 cchName,  
    [out] ULONG32 *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `baseAddress`  
 [in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente l’adresse de base du module.  
  
 `cchName`  
 [in] Nombre de caractères dans la mémoire tampon qui reçoit le chemin d’accès du module.  
  
 `pcchName`  
 [out] Pointeur vers le nombre de caractères écrits dans la mémoire tampon `szName`.  
  
 `szName`  
 [out] Chemin d’accès du module.  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Cette méthode est uniquement disponible avec .NET Native.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugDataTarget2, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)  
 [Interfaces de débogage](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
