---
title: ICorDebugArrayValue::GetDimensions, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugArrayValue.GetDimensions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetDimensions
helpviewer_keywords:
- ICorDebugArrayValue::GetDimensions method [.NET Framework debugging]
- GetDimensions method [.NET Framework debugging]
ms.assetid: 6c116592-134b-4ef2-a319-680e92d013aa
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a52075f33d594787c516f84b65b3319991380907
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61645693"
---
# <a name="icordebugarrayvaluegetdimensions-method"></a>ICorDebugArrayValue::GetDimensions, méthode
Obtient le nombre d’éléments dans chaque dimension de ce tableau.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetDimensions (  
    [in] ULONG32         cdim,  
    [out, size_is(cdim), length_is(cdim)]   
        ULONG32          dims[]  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `cdim`  
 [in] Le nombre de dimensions de cet objet ICorDebugArrayValue.  
  
 Cette valeur est également la taille de la `dims` tableau car sa taille est égale au nombre de dimensions de la `ICorDebugArrayValue` objet.  
  
 `dims`  
 [out] Tableau d’entiers, chacun d’eux spécifie le nombre d’éléments dans une dimension dans ce `ICorDebugArrayValue` objet.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
