---
title: ICorDebugChain::GetActiveFrame, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetActiveFrame
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetActiveFrame
helpviewer_keywords:
- ICorDebugChain::GetActiveFrame method [.NET Framework debugging]
- GetActiveFrame method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 36887017-670b-4f21-b406-8fab956f84a3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c14b48a29993a65a0a0ab9fcb63bcb1e0d882042
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645368"
---
# <a name="icordebugchaingetactiveframe-method"></a>ICorDebugChain::GetActiveFrame, méthode
Obtient l’actif (autrement dit, plus récente) frame sur la chaîne.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetActiveFrame (  
    [out] ICorDebugFrame   **ppFrame  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppFrame`  
 [out] Un pointeur vers l’adresse d’un objet ICorDebugFrame qui représente l’actif (autrement dit, plus récente) frame sur la chaîne.  
  
## <a name="remarks"></a>Notes  
 Si aucun frame de pile managée est disponible, `ppFrame` a la valeur null.  
  
 Si le frame actif n’est pas disponible, l’appel réussira et `ppFrame` sera null. Cadres active ne sera pas disponibles pour les chaînes lancées en raison de CHAIN_ENTER_UNMANAGED et pour certaines chaînes lancées en raison de CHAIN_CLASS_INIT. Consultez l’énumération CorDebugChainReason.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
