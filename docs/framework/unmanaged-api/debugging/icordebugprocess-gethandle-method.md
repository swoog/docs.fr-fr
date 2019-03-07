---
title: ICorDebugProcess::GetHandle, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.GetHandle
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetHandle
helpviewer_keywords:
- GetHandle method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::GetHandle method [.NET Framework debugging]
ms.assetid: e7d3ecf5-09d2-4d94-abb6-ff3483deebb6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c5d81564a34ed8e7ef75840e3a174661c36f5411
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57498084"
---
# <a name="icordebugprocessgethandle-method"></a>ICorDebugProcess::GetHandle, méthode
Obtient un handle vers le processus.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetHandle([out] HPROCESS *phProcessHandle);  
```  
  
## <a name="parameters"></a>Paramètres  
 `phProcessHandle`  
 [out] Un pointeur vers un `HPROCESS` qui est le handle pour le processus.  
  
## <a name="remarks"></a>Notes  
 Le handle récupéré est détenu par l’interface de débogage. Le débogueur doit dupliquer le handle avant de l’utiliser.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
