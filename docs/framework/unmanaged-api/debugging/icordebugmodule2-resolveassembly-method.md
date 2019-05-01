---
title: ICorDebugModule2::ResolveAssembly, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.ResolveAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::ResolveAssembly
helpviewer_keywords:
- ICorDebugModule2::ResolveAssembly method [.NET Framework debugging]
- ResolveAssembly method [.NET Framework debugging]
ms.assetid: ddf9085c-7161-44bd-9609-cd2732b9009f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fd899422287d34407778f67e5b4dfd2f33ffd00c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61994823"
---
# <a name="icordebugmodule2resolveassembly-method"></a>ICorDebugModule2::ResolveAssembly, méthode

Résout l’assembly référencé par le jeton de métadonnées spécifié.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT ResolveAssembly (
    [in]  mdToken             tkAssemblyRef,
    [out] ICorDebugAssembly   **ppAssembly
);
```

## <a name="parameters"></a>Paramètres

`tkAssemblyRef`\
[in] Un `mdToken` valeur qui fait référence à l’assembly.

`ppAssembly`\
[out] Pointeur vers l’adresse d’un objet ICorDebugAssembly qui représente l’assembly.

## <a name="remarks"></a>Notes

Si l’assembly n'est pas déjà chargé quand `ResolveAssembly` est appelée, un HRESULT valeur CORDBG_E_CANNOT_RESOLVE_ASSEMBLY est retournée.

## <a name="requirements"></a>Configuration requise

**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).

**En-tête :** CorDebug.idl, CorDebug.h

**Bibliothèque :** CorGuids.lib

**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
