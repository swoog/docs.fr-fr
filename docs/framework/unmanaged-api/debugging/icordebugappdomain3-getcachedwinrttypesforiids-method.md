---
title: ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3.GetCachedWinRTTypesForIIDs
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs
helpviewer_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs method, [.NET Framework debugging]
- GetCachedWinRTTypesForIIDs method, ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 23682ca0-1bcf-48e6-996e-69f7ba337682
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ed1d7ad95b7c8474121994d0f54557c1c36cb531
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61917374"
---
# <a name="icordebugappdomain3getcachedwinrttypesforiids-method"></a>ICorDebugAppDomain3::GetCachedWinRTTypesForIIDs, méthode
Obtient un énumérateur pour la mise en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types dans un domaine d’application basés sur leurs identificateurs de l’interface.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetCachedWinRTTypesForIIDs (   
    [in]  ULONG32            cReqTypes,  
    [in]  GUID                *iidsToResolve,  
    [out] ICorDebugTypeEnum   **ppTypesEnum  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `cReqTypes`  
 [in] Le nombre de types requis.  
  
 `iidsToResolve`  
 [in] Un pointeur vers un tableau qui contient les identificateurs d’interface correspondant à des représentations managées de le [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types à récupérer.  
  
 `ppTypesEnum`  
 [out] Un pointeur vers l’adresse d’un objet d’interface « ICorDebugTypeEnum » qui permet l’énumération de la mise en cache géré les représentations sous forme de la [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types récupérés, basé sur les identificateurs d’interface dans `iidsToResolve`.  
  
## <a name="remarks"></a>Notes  
 Si la méthode ne parvient pas à récupérer des informations pour un identificateur d’interface spécifique, l’entrée correspondante dans la collection « ICorDebugTypeEnum » est d’un type de `ELEMENT_TYPE_END` pour les erreurs en raison de problèmes de récupération des données, ou `ELEMENT_TYPE_VOID` pour interface inconnue identificateurs.  
  
## <a name="requirements"></a>Configuration requise  
 **Plateformes :** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [ICorDebugAppDomain3, interface](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-interface.md)
