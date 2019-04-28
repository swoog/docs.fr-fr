---
title: ICorDebugCode::GetCode, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetCode
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetCode
helpviewer_keywords:
- ICorDebugCode::GetCode method [.NET Framework debugging]
- GetCode method, ICorDebugCode interface [.NET Framework debugging]
ms.assetid: 7137e3d1-1dad-48d8-8c37-16ac816534d3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f396881ef16f63eaf198aec168e5e94ed887698b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61750319"
---
# <a name="icordebugcodegetcode-method"></a><span data-ttu-id="ce37c-102">ICorDebugCode::GetCode, méthode</span><span class="sxs-lookup"><span data-stu-id="ce37c-102">ICorDebugCode::GetCode Method</span></span>
<span data-ttu-id="ce37c-103">Obtient tout le code pour la fonction spécifiée, la mise en forme pour le code machine.</span><span class="sxs-lookup"><span data-stu-id="ce37c-103">Gets all the code for the specified function, formatted for disassembly.</span></span> <span data-ttu-id="ce37c-104">Cette méthode a été déconseillée dans le .NET Framework version 2.0.</span><span class="sxs-lookup"><span data-stu-id="ce37c-104">This method has been deprecated in the .NET Framework version 2.0.</span></span> <span data-ttu-id="ce37c-105">Utilisez [ICorDebugCode2::GetCodeChunks](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="ce37c-105">Use [ICorDebugCode2::GetCodeChunks](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce37c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce37c-106">Syntax</span></span>  
  
```  
HRESULT GetCode (  
    [in] ULONG32     startOffset,   
    [in] ULONG32     endOffset,  
    [in] ULONG32     cBufferAlloc,  
    [out, size_is(cBufferAlloc),  
        length_is(*pcBufferSize)] BYTE buffer[],  
    [out] ULONG32    *pcBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ce37c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce37c-107">Parameters</span></span>  
 `startOffset`  
 <span data-ttu-id="ce37c-108">[in] Le décalage du début de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ce37c-108">[in] The offset of the beginning of the function.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="ce37c-109">[in] Le décalage de la fin de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ce37c-109">[in] The offset of the end of the function.</span></span>  
  
 `cBufferAlloc`  
 <span data-ttu-id="ce37c-110">[in] La taille de la `buffer` de tableau dans lequel le code sera retourné.</span><span class="sxs-lookup"><span data-stu-id="ce37c-110">[in] The size of the `buffer` array into which the code will be returned.</span></span>  
  
 `buffer`  
 <span data-ttu-id="ce37c-111">[out] Tableau dans lequel le code sera retourné.</span><span class="sxs-lookup"><span data-stu-id="ce37c-111">[out] The array into which the code will be returned.</span></span>  
  
 `pcBufferSize`  
 <span data-ttu-id="ce37c-112">[out] Le nombre d’octets retournés.</span><span class="sxs-lookup"><span data-stu-id="ce37c-112">[out] The number of bytes returned.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ce37c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ce37c-113">Remarks</span></span>  
 <span data-ttu-id="ce37c-114">Si le code de fonction a été divisé en plusieurs segments, elles sont concaténées par ordre croissant d’offset natif.</span><span class="sxs-lookup"><span data-stu-id="ce37c-114">If the function's code has been divided into multiple chunks, they are concatenated in order of increasing native offset.</span></span> <span data-ttu-id="ce37c-115">Limites d’instruction ne sont pas vérifiées.</span><span class="sxs-lookup"><span data-stu-id="ce37c-115">Instruction boundaries are not checked.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce37c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce37c-116">Requirements</span></span>  
 <span data-ttu-id="ce37c-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ce37c-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ce37c-118">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ce37c-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ce37c-119">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ce37c-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ce37c-120">**Versions du .NET framework :** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="ce37c-120">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce37c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce37c-121">See also</span></span>

- [<span data-ttu-id="ce37c-122">GetCodeChunks, méthode</span><span class="sxs-lookup"><span data-stu-id="ce37c-122">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)
