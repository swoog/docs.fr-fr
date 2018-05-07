---
title: ICorDebugProcess::IsOSSuspended, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.IsOSSuspended
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::IsOSSuspended
helpviewer_keywords:
- IsOSSuspended method [.NET Framework debugging]
- ICorDebugProcess::IsOSSuspended method [.NET Framework debugging]
ms.assetid: 83406cb2-5797-4402-872d-89c9516aefec
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2b65a621541f2b4a800f6b3708a6b257374c5866
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugprocessisossuspended-method"></a>ICorDebugProcess::IsOSSuspended, méthode
Obtient une valeur qui indique si le thread spécifié a été interrompu suite à l’arrêt de ce processus de débogueur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT IsOSSuspended(  
    [in]  DWORD threadID,  
    [out] BOOL  *pbSuspended);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `threadID`  
 [in] L’ID du thread en question.  
  
 `pbSuspended`  
 [out] Un pointeur vers une valeur booléenne qui est `true` si le thread spécifié a été suspendue ; sinon *`pbSuspended` est `false`.  
  
## <a name="remarks"></a>Notes  
 Quand le thread spécifié a été suspendu en raison de l’arrêt de ce processus de débogueur, le compteur de suspension Win32 du thread spécifié est incrémenté d’un. L’interface utilisateur (IU) du débogueur voudrez peut-être prendre en compte ces informations si elle affiche le système d’exploitation (OS) compteur de suspension du thread à l’utilisateur.  
  
 Le `IsOSSuspended` méthode de sens que dans le contexte de débogage non managé. Pendant le débogage managé, les threads sont en coopération suspendu au lieu du système d’exploitation suspendu.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
