---
title: ICorDebugManagedCallback::UpdateModuleSymbols, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.UpdateModuleSymbols
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::UpdateModuleSymbols
helpviewer_keywords:
- UpdateModuleSymbols method [.NET Framework debugging]
- ICorDebugManagedCallback::UpdateModuleSymbols method [.NET Framework debugging]
ms.assetid: 0863f644-58e8-45a0-b0c3-a28e99b20938
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 581ea4f974bfec3961a32cd7c9985a5e45d2bddd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59209981"
---
# <a name="icordebugmanagedcallbackupdatemodulesymbols-method"></a><span data-ttu-id="bdb43-102">ICorDebugManagedCallback::UpdateModuleSymbols, méthode</span><span class="sxs-lookup"><span data-stu-id="bdb43-102">ICorDebugManagedCallback::UpdateModuleSymbols Method</span></span>
<span data-ttu-id="bdb43-103">Notifie le débogueur que les symboles pour un module du common language runtime ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="bdb43-103">Notifies the debugger that the symbols for a common language runtime module have changed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdb43-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdb43-104">Syntax</span></span>  
  
```  
HRESULT UpdateModuleSymbols (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugModule    *pModule,  
    [in] IStream            *pSymbolStream  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bdb43-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdb43-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="bdb43-106">[in] Pointeur vers un objet ICorDebugAppDomain qui représente le domaine d’application contenant le module dans lequel les symboles ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="bdb43-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain containing the module in which the symbols have changed.</span></span>  
  
 `pModule`  
 <span data-ttu-id="bdb43-107">[in] Pointeur vers un objet ICorDebugModule qui représente le module dans lequel les symboles ont été modifiés.</span><span class="sxs-lookup"><span data-stu-id="bdb43-107">[in] A pointer to an ICorDebugModule object that represents the module in which the symbols have changed.</span></span>  
  
 `pSymbolStream`  
 <span data-ttu-id="bdb43-108">[in] Un pointeur vers un COM Win32 `IStream` objet qui contient les symboles modifiés.</span><span class="sxs-lookup"><span data-stu-id="bdb43-108">[in] A pointer to a Win32 COM `IStream` object that contains the modified symbols.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bdb43-109">Notes</span><span class="sxs-lookup"><span data-stu-id="bdb43-109">Remarks</span></span>  
 <span data-ttu-id="bdb43-110">Cette méthode offre la possibilité de mettre à jour l’affichage du débogueur des symboles d’un module en appelant [ISymUnmanagedReader::UpdateSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-updatesymbolstore-method.md) ou [ISymUnmanagedReader::ReplaceSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-replacesymbolstore-method.md).</span><span class="sxs-lookup"><span data-stu-id="bdb43-110">This method provides an opportunity to update the debugger's view of a module's symbols by calling [ISymUnmanagedReader::UpdateSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-updatesymbolstore-method.md) or [ISymUnmanagedReader::ReplaceSymbolStore](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader-replacesymbolstore-method.md).</span></span>  
  
 <span data-ttu-id="bdb43-111">Ce rappel peut se produire plusieurs fois pour le même module.</span><span class="sxs-lookup"><span data-stu-id="bdb43-111">This callback can occur multiple times for the same module.</span></span>  
  
 <span data-ttu-id="bdb43-112">Un débogueur doit tenter de lier indépendants des points d’arrêt au niveau de la source.</span><span class="sxs-lookup"><span data-stu-id="bdb43-112">A debugger should try to bind unbound source-level breakpoints.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdb43-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdb43-113">Requirements</span></span>  
 <span data-ttu-id="bdb43-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bdb43-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bdb43-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bdb43-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bdb43-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bdb43-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bdb43-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bdb43-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdb43-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdb43-118">See also</span></span>

- [<span data-ttu-id="bdb43-119">ICorDebugManagedCallback, interface</span><span class="sxs-lookup"><span data-stu-id="bdb43-119">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
