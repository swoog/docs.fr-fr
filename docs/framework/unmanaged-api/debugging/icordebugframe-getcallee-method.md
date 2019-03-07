---
title: ICorDebugFrame::GetCallee, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetCallee
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetCallee
helpviewer_keywords:
- ICorDebugFrame::GetCallee method [.NET Framework debugging]
- GetCallee method, ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 92d8136d-0436-4c7e-a6b2-80765f892a0d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a179b68e2196eeadc712ae8f7d023b2943533335
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471067"
---
# <a name="icordebugframegetcallee-method"></a>ICorDebugFrame::GetCallee, méthode
Obtient un pointeur vers l’objet ICorDebugFrame dans la chaîne actuelle qui a appelé ce frame.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetCallee (  
    [out] ICorDebugFrame     **ppFrame  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppFrame`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugFrame` objet qui représente le frame appelé. Cette valeur est null si le frame appelant est le plus profond frame dans la chaîne actuelle.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
