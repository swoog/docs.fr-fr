---
title: ICorDebugThread::GetProcess, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread.GetProcess
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetProcess
helpviewer_keywords:
- ICorDebugThread::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 163816e7-0739-4566-b3df-cd256be8b8a4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b41c7eeccad8b3f685c81e6afc23eaf19d862182
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33417610"
---
# <a name="icordebugthreadgetprocess-method"></a>ICorDebugThread::GetProcess, méthode
Obtient un pointeur d’interface vers le processus qui ICorDebugThread fait partie.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetProcess (  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `ppProcess`  
 [out] Pointeur vers l’adresse d’un objet d’interface ICorDebugProcess qui représente le processus.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
