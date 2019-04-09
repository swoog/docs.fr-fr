---
title: ICorDebugModule3::CreateReaderForInMemorySymbols, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule3.CreateReaderForInMemorySymbols
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule3::CreateReaderForInMemorySymbols
helpviewer_keywords:
- CreateReaderForInMemorySymbols method, ICorDebugModule3 interface [.NET Framework debugging]
- ICorDebugModule3::CreateReaderForInMemorySymbols method [.NET Framework debugging]
ms.assetid: af317171-d66d-4114-89eb-063554c74940
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ccfe83707b6354c42a4c3c81e911918b2ea79ec4
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59108912"
---
# <a name="icordebugmodule3createreaderforinmemorysymbols-method"></a><span data-ttu-id="68f0e-102">ICorDebugModule3::CreateReaderForInMemorySymbols, méthode</span><span class="sxs-lookup"><span data-stu-id="68f0e-102">ICorDebugModule3::CreateReaderForInMemorySymbols Method</span></span>
<span data-ttu-id="68f0e-103">Crée un lecteur de symboles de débogage pour un module dynamique.</span><span class="sxs-lookup"><span data-stu-id="68f0e-103">Creates a debug symbol reader for a dynamic module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68f0e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68f0e-104">Syntax</span></span>  
  
```  
HRESULT CreateReaderForInMemorySymbols (  
      [in] REFIID riid,  
      [out][iid_is(riid)] void **    ppObj  
```  
  
## <a name="parameters"></a><span data-ttu-id="68f0e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68f0e-105">Parameters</span></span>  
 <span data-ttu-id="68f0e-106">riid</span><span class="sxs-lookup"><span data-stu-id="68f0e-106">riid</span></span>  
 <span data-ttu-id="68f0e-107">[in] IID de l’interface COM à retourner.</span><span class="sxs-lookup"><span data-stu-id="68f0e-107">[in] The IID of the COM interface to return.</span></span> <span data-ttu-id="68f0e-108">En règle générale, il s’agit d’un [ISymUnmanagedReader Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md).</span><span class="sxs-lookup"><span data-stu-id="68f0e-108">Typically, this is an [ISymUnmanagedReader Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-interface.md).</span></span>  
  
 <span data-ttu-id="68f0e-109">ppObj</span><span class="sxs-lookup"><span data-stu-id="68f0e-109">ppObj</span></span>  
 <span data-ttu-id="68f0e-110">[out] Pointeur vers un pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="68f0e-110">[out] Pointer to a pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="68f0e-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="68f0e-111">Return Value</span></span>  
 <span data-ttu-id="68f0e-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="68f0e-112">S_OK</span></span>  
 <span data-ttu-id="68f0e-113">Le lecteur a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="68f0e-113">Successfully created the reader.</span></span>  
  
 <span data-ttu-id="68f0e-114">CORDBG_E_MODULE_LOADED_FROM_DISK</span><span class="sxs-lookup"><span data-stu-id="68f0e-114">CORDBG_E_MODULE_LOADED_FROM_DISK</span></span>  
 <span data-ttu-id="68f0e-115">Le module n’est pas un module en mémoire ou dynamique.</span><span class="sxs-lookup"><span data-stu-id="68f0e-115">The module is not an in-memory or dynamic module.</span></span>  
  
 <span data-ttu-id="68f0e-116">CORDBG_E_SYMBOLS_NOT_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="68f0e-116">CORDBG_E_SYMBOLS_NOT_AVAILABLE</span></span>  
 <span data-ttu-id="68f0e-117">Symboles n’ont pas été fournis par l’application ou ne sont pas encore disponibles.</span><span class="sxs-lookup"><span data-stu-id="68f0e-117">Symbols have not been supplied by the application or are not yet available.</span></span>  
  
 <span data-ttu-id="68f0e-118">E_FAIL (ou autres codes de retour E_)</span><span class="sxs-lookup"><span data-stu-id="68f0e-118">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="68f0e-119">Impossible de créer le lecteur.</span><span class="sxs-lookup"><span data-stu-id="68f0e-119">Unable to create the reader.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="68f0e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="68f0e-120">Remarks</span></span>  
 <span data-ttu-id="68f0e-121">Cette méthode peut également être utilisée pour créer un objet lecteur de symboles pour les modules en mémoire (non dynamique), mais uniquement une fois que les symboles sont tout d’abord disponibles (indiqué par le [UpdateModuleSymbols, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-updatemodulesymbols-method.md) rappel).</span><span class="sxs-lookup"><span data-stu-id="68f0e-121">This method can also be used to create a symbol reader object for in-memory (non-dynamic) modules, but only after the symbols are first available (indicated by the [UpdateModuleSymbols Method](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-updatemodulesymbols-method.md) callback).</span></span>  
  
 <span data-ttu-id="68f0e-122">Cette méthode retourne une nouvelle instance de lecteur chaque fois qu’elle est appelée (comme [CComPtrBase::CoCreateInstance](/cpp/atl/reference/ccomptrbase-class#cocreateinstance)).</span><span class="sxs-lookup"><span data-stu-id="68f0e-122">This method returns a new reader instance every time it is called (like [CComPtrBase::CoCreateInstance](/cpp/atl/reference/ccomptrbase-class#cocreateinstance)).</span></span> <span data-ttu-id="68f0e-123">Par conséquent, le débogueur doit mettre en cache le résultat et demander une nouvelle instance uniquement lorsque les données sous-jacentes peuvent avoir changé (autrement dit, quand un [LoadClass, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md) reçu de rappel).</span><span class="sxs-lookup"><span data-stu-id="68f0e-123">Therefore, the debugger should cache the result and request a new instance only when the underlying data may have changed (that is, when a [LoadClass Method](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md) callback is received).</span></span>  
  
 <span data-ttu-id="68f0e-124">Modules dynamiques n’ont pas de symboles disponibles jusqu'à ce que le premier type a été chargé (comme indiqué par le [LoadClass, méthode](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md) rappel).</span><span class="sxs-lookup"><span data-stu-id="68f0e-124">Dynamic modules do not have any symbols available until the first type has been loaded (as indicated by the [LoadClass Method](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-loadclass-method.md) callback).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="68f0e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68f0e-125">Requirements</span></span>  
 <span data-ttu-id="68f0e-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="68f0e-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68f0e-127">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="68f0e-127">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="68f0e-128">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="68f0e-128">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="68f0e-129">**Versions du .NET framework :** 4.5, 4, 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="68f0e-129">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68f0e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68f0e-130">See also</span></span>

- [<span data-ttu-id="68f0e-131">ICorDebugRemoteTarget, interface</span><span class="sxs-lookup"><span data-stu-id="68f0e-131">ICorDebugRemoteTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugremotetarget-interface.md)
- [<span data-ttu-id="68f0e-132">ICorDebug, interface</span><span class="sxs-lookup"><span data-stu-id="68f0e-132">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)

- [<span data-ttu-id="68f0e-133">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="68f0e-133">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
