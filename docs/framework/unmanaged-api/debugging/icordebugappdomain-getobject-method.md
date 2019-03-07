---
title: ICorDebugAppDomain::GetObject, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetObject
api_location:
- corguids.lib
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetObject
helpviewer_keywords:
- ICorDebugAppDomain::GetObject method [.NET Framework debugging]
- GetObject method, ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: 78232e6f-ae18-4cfa-a6cd-e79471cf9d76
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0ca9792df69f859e20f1d9e40754d1cec138945d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57480024"
---
# <a name="icordebugappdomaingetobject-method"></a>ICorDebugAppDomain::GetObject, méthode
Obtient un pointeur d’interface vers le domaine d’application du common language runtime (CLR).  
  
## <a name="syntax"></a>Syntaxe  
  
```  
HRESULT GetObject (  
    [out] ICorDebugValue   **ppObject  
);  
```  
  
## <a name="parameters"></a>Paramètres  
 `ppObject`  
 [out] Pointeur vers l’adresse d’un objet d’interface ICorDebugValue qui représente le domaine d’application CLR.  
  
## <a name="return-value"></a>Valeur de retour  
 Si un géré <xref:System.AppDomain?displayProperty=nameWithType> objet n’a pas été construit pour ce domaine d’application, la méthode retourne `S_FALSE` et place `NULL` dans `*ppObject`.  
  
## <a name="remarks"></a>Notes  
 Chaque domaine d’application dans un processus peut avoir un géré <xref:System.AppDomain?displayProperty=nameWithType> objet dans le runtime qui le représente. Cette fonction obtient un objet d’interface ICorDebugValue qui correspond à cet gérés <xref:System.AppDomain?displayProperty=nameWithType> objet.  
  
## <a name="requirements"></a>Spécifications  
 **Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).  
  
 **En-tête :** CorDebug.idl, CorDebug.h  
  
 **Bibliothèque :** CorGuids.lib  
  
 **Versions du .NET Framework :** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]
