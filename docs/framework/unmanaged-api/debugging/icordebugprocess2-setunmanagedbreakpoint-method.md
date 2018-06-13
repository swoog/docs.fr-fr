---
title: ICorDebugProcess2::SetUnmanagedBreakpoint, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess2.SetUnmanagedBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess2::SetUnmanagedBreakpoint
helpviewer_keywords:
- ICorDebugProcess2::SetUnmanagedBreakpoint method [.NET Framework debugging]
- SetUnmanagedBreakpoint method [.NET Framework debugging]
ms.assetid: 93829d15-d942-4e2d-b7a4-dfc9d7fb96be
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d4326c6d8a3ee780cf63652badc8c527f55a075c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420815"
---
# <a name="icordebugprocess2setunmanagedbreakpoint-method"></a>ICorDebugProcess2::SetUnmanagedBreakpoint, méthode
Définit un point d’arrêt non managé à l’offset d’image native spécifié.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT SetUnmanagedBreakpoint (  
    [in]  CORDB_ADDRESS    address,  
    [in]  ULONG32          bufsize,  
    [out, size_is(bufsize), length_is(*bufLen)]   
        BYTE               buffer[],  
    [out] ULONG32          *bufLen  
);  
```  
  
#### <a name="parameters"></a>Paramètres  
 `address`  
 [in] A `CORDB_ADDRESS` objet qui spécifie le décalage de l’image native.  
  
 `bufsize`  
 [in] La taille, en octets, de le `buffer` tableau.  
  
 `buffer`  
 [out] Tableau qui contient le code d’opération qui est remplacé par le point d’arrêt.  
  
 `bufLen`  
 [out] Un pointeur vers le nombre d’octets retournés dans le `buffer` tableau.  
  
## <a name="remarks"></a>Notes  
 Si le décalage de l’image native est dans le common language runtime (CLR), le point d’arrêt sera ignoré. Ainsi, le CLR afin d’éviter la distribution d’un point d’arrêt hors-bande, lorsque le point d’arrêt est défini par le débogueur.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
