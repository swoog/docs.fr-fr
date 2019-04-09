---
title: ISymUnmanagedWriter::SetScopeRange, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.SetScopeRange
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::SetScopeRange
helpviewer_keywords:
- SetScopeRange method [.NET Framework debugging]
- ISymUnmanagedWriter::SetScopeRange method [.NET Framework debugging]
ms.assetid: d4d98676-444b-46ca-bfe6-0d827385cd22
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7d7fe8f36c7a5dbe6e715402fd7253092b64e68e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59078965"
---
# <a name="isymunmanagedwritersetscoperange-method"></a><span data-ttu-id="bdf11-102">ISymUnmanagedWriter::SetScopeRange, méthode</span><span class="sxs-lookup"><span data-stu-id="bdf11-102">ISymUnmanagedWriter::SetScopeRange Method</span></span>
<span data-ttu-id="bdf11-103">Définit la plage d'offsets pour la portée lexicale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bdf11-103">Defines the offset range for the specified lexical scope.</span></span> <span data-ttu-id="bdf11-104">La portée devient la nouvelle portée actuelle et est envoyée à une pile d’étendues.</span><span class="sxs-lookup"><span data-stu-id="bdf11-104">The scope becomes the new current scope and is pushed onto a stack of scopes.</span></span> <span data-ttu-id="bdf11-105">Les portées doivent former une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="bdf11-105">Scopes must form a hierarchy.</span></span> <span data-ttu-id="bdf11-106">Frères ne sont pas autorisées à chevaucher.</span><span class="sxs-lookup"><span data-stu-id="bdf11-106">Siblings are not allowed to overlap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdf11-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdf11-107">Syntax</span></span>  
  
```  
HRESULT OpenScope(  
    [in] ULONG32  scopeID,  
    [in] ULONG32  startOffset,  
    [in] ULONG32  endOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bdf11-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdf11-108">Parameters</span></span>  
 `scopeId`  
 <span data-ttu-id="bdf11-109">[in] L’identificateur de portée pour la portée.</span><span class="sxs-lookup"><span data-stu-id="bdf11-109">[in] The scope identifier for the scope.</span></span>  
  
 `startOffset`  
 <span data-ttu-id="bdf11-110">[in] Offset, en octets, de la première instruction dans la portée lexicale à partir du début de la méthode.</span><span class="sxs-lookup"><span data-stu-id="bdf11-110">[in] The offset, in bytes, of the first instruction in the lexical scope from the beginning of the method.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="bdf11-111">[in] Offset, en octets, de la dernière instruction dans la portée lexicale à partir du début de la méthode.</span><span class="sxs-lookup"><span data-stu-id="bdf11-111">[in] The offset, in bytes, of the last instruction in the lexical scope from the beginning of the method.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bdf11-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bdf11-112">Return Value</span></span>  
 <span data-ttu-id="bdf11-113">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="bdf11-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bdf11-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bdf11-114">Remarks</span></span>  
 <span data-ttu-id="bdf11-115">[ISymUnmanagedWriter::OpenScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md) retourne un identificateur de portée opaque qui peut être utilisé avec `ISymUnmanagedWriter::SetScopeRange` pour définir une étendue de démarrage et de fin de décalage à partir d’une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="bdf11-115">[ISymUnmanagedWriter::OpenScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openscope-method.md) returns an opaque scope identifier that can be used with `ISymUnmanagedWriter::SetScopeRange` to define a scope's starting and ending offset at a later time.</span></span> <span data-ttu-id="bdf11-116">Dans ce cas, les offsets passés à `ISymUnmanagedWriter::OpenScope` et [ISymUnmanagedWriter::CloseScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closescope-method.md) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="bdf11-116">In this case, the offsets passed to `ISymUnmanagedWriter::OpenScope` and [ISymUnmanagedWriter::CloseScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closescope-method.md) are ignored.</span></span> <span data-ttu-id="bdf11-117">Identificateurs d’étendue sont uniquement valides dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="bdf11-117">Scope identifiers are only valid in the current method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdf11-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bdf11-118">Requirements</span></span>  
 <span data-ttu-id="bdf11-119">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="bdf11-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdf11-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bdf11-120">See also</span></span>

- [<span data-ttu-id="bdf11-121">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="bdf11-121">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
