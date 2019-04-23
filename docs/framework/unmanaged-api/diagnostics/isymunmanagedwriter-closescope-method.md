---
title: ISymUnmanagedWriter::CloseScope, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseScope
helpviewer_keywords:
- CloseScope method [.NET Framework debugging]
- ISymUnmanagedWriter::CloseScope method [.NET Framework debugging]
ms.assetid: 6dade525-7770-4cb4-bafd-4bb995ad0d87
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9ab30e1f80be71b42a131afe68e38f0b2731ae60
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59212945"
---
# <a name="isymunmanagedwriterclosescope-method"></a><span data-ttu-id="554de-102">ISymUnmanagedWriter::CloseScope, méthode</span><span class="sxs-lookup"><span data-stu-id="554de-102">ISymUnmanagedWriter::CloseScope Method</span></span>
<span data-ttu-id="554de-103">Ferme la portée lexicale actuelle.</span><span class="sxs-lookup"><span data-stu-id="554de-103">Closes the current lexical scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="554de-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="554de-104">Syntax</span></span>  
  
```  
HRESULT CloseScope(  
    [in] ULONG32 endOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="554de-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="554de-105">Parameters</span></span>  
 `endOffset`  
 <span data-ttu-id="554de-106">[in] Le décalage à partir du début de la méthode du point à la fin de la dernière instruction dans la portée lexicale, en octets.</span><span class="sxs-lookup"><span data-stu-id="554de-106">[in] The offset from the beginning of the method of the point at the end of the last instruction in the lexical scope, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="554de-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="554de-107">Return Value</span></span>  
 <span data-ttu-id="554de-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="554de-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="554de-109">Notes</span><span class="sxs-lookup"><span data-stu-id="554de-109">Remarks</span></span>  
 <span data-ttu-id="554de-110">Une fois qu’une portée est fermée, plus aucune variable ne peut être définie qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="554de-110">Once a scope is closed, no more variables can be defined within it.</span></span>  
  
 <span data-ttu-id="554de-111">[ISymUnmanagedWriter::OpenScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md) retourne un identificateur de portée opaque qui peut être utilisé avec [ISymUnmanagedWriter::SetScopeRange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md) pour définir ultérieurement une étendue de démarrage et de fin de décalage.</span><span class="sxs-lookup"><span data-stu-id="554de-111">[ISymUnmanagedWriter::OpenScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md) returns an opaque scope identifier that can be used with [ISymUnmanagedWriter::SetScopeRange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md) to later define a scope's starting and ending offset.</span></span> <span data-ttu-id="554de-112">Dans ce cas, les offsets passés à `ISymUnmanagedWriter::OpenScope` et `ISymUnmanagedWriter::CloseScope` sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="554de-112">In this case, the offsets passed to `ISymUnmanagedWriter::OpenScope` and `ISymUnmanagedWriter::CloseScope` are ignored.</span></span> <span data-ttu-id="554de-113">Les identificateurs de portée sont valides uniquement dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="554de-113">Scope identifiers are valid only in the current method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="554de-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="554de-114">Requirements</span></span>  
 <span data-ttu-id="554de-115">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="554de-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="554de-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="554de-116">See also</span></span>

- [<span data-ttu-id="554de-117">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="554de-117">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
