---
title: ICorDebugAssembly2::IsFullyTrusted, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly2.IsFullyTrusted
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly2::IsFullyTrusted
helpviewer_keywords:
- ICorDebugAssembly2::IsFullyTrusted method [.NET Framework debugging]
- IsFullyTrusted method [.NET Framework debugging]
ms.assetid: 26cbd27d-12bf-444a-8197-ccd14d37dda3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bd3b977a894f8cb1fc9a866f5a43265d917db513
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645563"
---
# <a name="icordebugassembly2isfullytrusted-method"></a>ICorDebugAssembly2::IsFullyTrusted, méthode
Obtient une valeur qui indique si l’assembly a été accordé une confiance totale par le système de sécurité du runtime.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsFullyTrusted(  
    [out] BOOL *pbFullyTrusted  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pbFullyTrusted`  
 [out] `true` si l’assembly a été accordé une confiance totale par le système de sécurité du runtime ; sinon, `false`.  
  
## <a name="remarks"></a>Notes  
 Cette méthode retourne un HRESULT de CORDBG_E_NOTREADY si la stratégie de sécurité pour l’assembly n'a pas encore été résolue, autrement dit, si aucun code dans l’assembly a encore été exécuté.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
