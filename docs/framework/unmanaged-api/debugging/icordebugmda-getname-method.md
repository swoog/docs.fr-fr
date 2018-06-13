---
title: ICorDebugMDA::GetName, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetName
helpviewer_keywords:
- ICorDebugMDA::GetName method [.NET Framework debugging]
- GetName method, ICorDebugMDA interface [.NET Framework debugging]
ms.assetid: 885bf5e8-00b7-4cd7-9d8d-e720d47918c4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8c9f76f2c3b2ecf3ac5805dea8f8243f0b74ad48
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417831"
---
# <a name="icordebugmdagetname-method"></a>ICorDebugMDA::GetName, méthode
Obtient une chaîne contenant le nom de l’assistant débogage managé (MDA) représenté par [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetName (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `cchName`  
 [in] Taille du tableau `szName`.  
  
 `pcchName`  
 [out] Pointeur vers la longueur du nom.  
  
 `szName`  
 [out] Tableau dans lequel stocker le nom.  
  
## <a name="remarks"></a>Notes  
 Les noms d’Assistant Débogage MANAGÉ sont des valeurs uniques. Le `GetName` méthode constitue une alternative de performance appropriée pour obtenir le flux XML et extraire le nom du flux s’appuyant sur le schéma.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi  
 [ICorDebugMDA, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)  
 [Diagnostic d’erreurs avec les Assistants Débogage managé](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
