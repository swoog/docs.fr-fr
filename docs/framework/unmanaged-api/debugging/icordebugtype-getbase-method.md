---
title: ICorDebugType::GetBase, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugType.GetBase
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugType::GetBase
helpviewer_keywords:
- ICorDebugType::GetBase method [.NET Framework debugging]
- GetBase method [.NET Framework debugging]
ms.assetid: f24e1af9-c220-4f79-ae62-4153ec17ea81
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1d04bc67013a2227f295ac3a41be027b9f9b04e2
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57478724"
---
# <a name="icordebugtypegetbase-method"></a>ICorDebugType::GetBase, méthode
Obtient un pointeur d’interface vers ICorDebugType qui représente le type de base, s’il en existe, du type représenté par ce `ICorDebugType`.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetBase (  
    [out] ICorDebugType   **pBase  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `pBase`  
 [out] Un pointeur vers l’adresse d’un `ICorDebugType` objet qui représente le type de base.  
  
## <a name="remarks"></a>Notes  
 Recherche le type de base pour un type est utile d’implémenter des fonctionnalités communes du débogueur, telles que l’impression de tous les champs d’un objet ou de ses classes parentes.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
