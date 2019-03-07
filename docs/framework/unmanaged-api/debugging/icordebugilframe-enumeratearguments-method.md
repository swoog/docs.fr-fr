---
title: ICorDebugILFrame::EnumerateArguments, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame.EnumerateArguments
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame::EnumerateArguments
helpviewer_keywords:
- ICorDebugILFrame::EnumerateArguments method [.NET Framework debugging]
- EnumerateArguments method [.NET Framework debugging]
ms.assetid: 00ac81e2-a774-422a-bd88-54a4b3c99f73
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 49d7fb1de0b2ea63c1a766023b23acc42e027af8
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57475656"
---
# <a name="icordebugilframeenumeratearguments-method"></a>ICorDebugILFrame::EnumerateArguments, méthode
Obtient un énumérateur pour les arguments dans ce frame.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT EnumerateArguments (  
    [out] ICorDebugValueEnum    **ppValueEnum  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppValueEnum`  
 [out] Pointeur vers l’adresse d’un objet ICorDebugValueEnum qui est l’énumérateur pour les arguments dans ce frame.  
  
## <a name="remarks"></a>Notes  
 `EnumerateArguments` Obtient un énumérateur qui peut répertorier les arguments disponibles dans le frame d’appel représenté par cet objet ICorDebugILFrame. La liste inclut les arguments sont [vararg](/cpp/windows/vararg) (autrement dit, un nombre variable d’arguments), ainsi que les arguments qui ne sont pas `vararg`.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
