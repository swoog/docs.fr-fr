---
title: ICorDebugThread2::GetActiveFunctions, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugThread2.GetActiveFunctions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread2::GetActiveFunctions
helpviewer_keywords:
- GetActiveFunctions method [.NET Framework debugging]
- ICorDebugThread2::GetActiveFunctions method [.NET Framework debugging]
ms.assetid: 27fae01a-ecec-423a-973e-24f8de55826c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f7ed7787f0302826cab67664780177f05e551199
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugthread2getactivefunctions-method"></a>ICorDebugThread2::GetActiveFunctions, méthode
Obtient des informations sur la fonction active dans chacun des frames de ce thread.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetActiveFunctions (  
    [in]   ULONG32             cFunctions,  
    [out]  ULONG32             *pcFunctions,  
    [in, out, size_is(cFunctions), length_is(*pcFunctions)]  
        COR_ACTIVE_FUNCTION    pFunctions[]  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `cFunctions`  
 [in] Taille du tableau `pFunctions`.  
  
 `pcFunctions`  
 [out] Un pointeur vers le nombre d’objets retournés dans le `pFunctions` tableau. Le nombre d’objets renvoyés est égal au nombre de frames managés sur la pile.  
  
 `pFunctions`  
 [dans, out] Tableau d’objets COR_ACTIVE_FUNCTION, dont chacun contient des informations sur les fonctions actives dans les frames de ce thread.  
  
 Le premier élément sera utilisé pour le frame terminal et ainsi de suite jusqu’à la racine de la pile.  
  
## <a name="remarks"></a>Notes  
 Si `pFunctions` a la valeur null en entrée, `GetActiveFunctions` retourne uniquement le nombre de fonctions qui se trouvent sur la pile. Autrement dit, si `pFunctions` a la valeur null en entrée, `GetActiveFunctions` retourne une valeur uniquement dans `pcFunctions`.  
  
 Le `GetActiveFunctions` méthode est une optimisation sur l’obtention des informations mêmes des frames dans une trace de pile et inclut uniquement les frames qui auraient eu un objet ICorDebugILFrame pour eux dans la trace de pile complet.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
