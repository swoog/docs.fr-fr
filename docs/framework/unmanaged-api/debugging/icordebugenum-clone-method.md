---
title: ICorDebugEnum::Clone, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEnum.Clone
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum::Clone
helpviewer_keywords:
- Clone method, ICorDebugEnum interface [.NET Framework debugging]
- ICorDebugEnum::Clone method [.NET Framework debugging]
ms.assetid: 57eefaf3-75cf-4496-bc94-88c0706861b7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d1226f64df379b5c40304221e9e66eebcdb17b4
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57479231"
---
# <a name="icordebugenumclone-method"></a>ICorDebugEnum::Clone, méthode
Crée une copie de cet objet ICorDebugEnum.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT Clone (  
    [out] ICorDebugEnum **ppEnum  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppEnum`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugEnum` objet qui est une copie de ce `ICorDebugEnum` objet.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
