---
title: ICorDebugModule::GetProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetProcess
helpviewer_keywords:
- GetProcess method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetProcess method [.NET Framework debugging]
ms.assetid: 5e13446c-0271-446c-924a-9072c0e6eeae
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 97cecd66462cf6a88012b13dec82dbf617891dd5
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57493841"
---
# <a name="icordebugmodulegetprocess-method"></a>ICorDebugModule::GetProcess, méthode
Obtient le processus contenant de ce module.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetProcess (  
    [out] ICorDebugProcess **ppProcess  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppProcess`  
 [out] Pointeur vers l’adresse d’un objet ICorDebugProcess qui représente le processus qui contient ce module.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
