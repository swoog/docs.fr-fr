---
title: ICorDebugVariableHome::GetArgumentIndex (méthode)
ms.date: 03/30/2017
api_name:
- ICorDebugVariableHome.GetArgumentIndex
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugVariableHome::GetArgumentIndex
helpviewer_keywords:
- ICorDebugVariableHome::GetArgumentIndex method [.NET Framework debugging]
- GetArgumentIndex method, ICorDebugVariableHome interface [.NET Framework debugging]
ms.assetid: e86fcc72-388d-4009-ab21-8f9c3323e9a3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2457dff3063e47f1fb9d040caac1bc08441e1739
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57366827"
---
# <a name="icordebugvariablehomegetargumentindex-method"></a><span data-ttu-id="58e33-102">ICorDebugVariableHome::GetArgumentIndex (méthode)</span><span class="sxs-lookup"><span data-stu-id="58e33-102">ICorDebugVariableHome::GetArgumentIndex Method</span></span>

<span data-ttu-id="58e33-103">Obtient l’index d’un argument de fonction.</span><span class="sxs-lookup"><span data-stu-id="58e33-103">Gets the index of a function argument.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e33-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58e33-104">Syntax</span></span>

```cpp
HRESULT GetArgumentIndex(
    [out] ULONG32* pArgumentIndex
);
```

## <a name="parameters"></a><span data-ttu-id="58e33-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58e33-105">Parameters</span></span>

`pArgumentIndex`\
<span data-ttu-id="58e33-106">[out] Pointeur vers l’index de l’argument.</span><span class="sxs-lookup"><span data-stu-id="58e33-106">[out] A pointer to the argument index.</span></span>

## <a name="return-value"></a><span data-ttu-id="58e33-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="58e33-107">Return Value</span></span>

<span data-ttu-id="58e33-108">La méthode retourne les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="58e33-108">The method returns the following values.</span></span>

|<span data-ttu-id="58e33-109">Value</span><span class="sxs-lookup"><span data-stu-id="58e33-109">Value</span></span>|<span data-ttu-id="58e33-110">Description</span><span class="sxs-lookup"><span data-stu-id="58e33-110">Description</span></span>|
|-----------|-----------------|
|`S_OK`|<span data-ttu-id="58e33-111">L’appel de méthode a retourné un index d’argument valide.</span><span class="sxs-lookup"><span data-stu-id="58e33-111">The method call returned a valid argument index.</span></span>|
|`E_FAIL`|<span data-ttu-id="58e33-112">Actuel [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instance représente une variable locale.</span><span class="sxs-lookup"><span data-stu-id="58e33-112">The current [ICorDebugVariableHome](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md) instance represents a local variable.</span></span>|

## <a name="remarks"></a><span data-ttu-id="58e33-113">Notes</span><span class="sxs-lookup"><span data-stu-id="58e33-113">Remarks</span></span>

<span data-ttu-id="58e33-114">L’index de l’argument peut être utilisé pour récupérer des métadonnées pour cet argument.</span><span class="sxs-lookup"><span data-stu-id="58e33-114">The argument index can be used to retrieve metadata for this argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e33-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="58e33-115">Requirements</span></span>

<span data-ttu-id="58e33-116">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="58e33-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="58e33-117">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="58e33-117">**Header:** CorDebug.idl, CorDebug.h</span></span>

<span data-ttu-id="58e33-118">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58e33-118">**Library:** CorGuids.lib</span></span>

<span data-ttu-id="58e33-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58e33-119">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="58e33-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58e33-120">See also</span></span>

- [<span data-ttu-id="58e33-121">ICorDebugVariableHome, interface</span><span class="sxs-lookup"><span data-stu-id="58e33-121">ICorDebugVariableHome Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablehome-interface.md)
