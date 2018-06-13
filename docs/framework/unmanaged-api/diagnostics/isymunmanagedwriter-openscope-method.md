---
title: ISymUnmanagedWriter::OpenScope, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.OpenScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::OpenScope
helpviewer_keywords:
- OpenScope method, ISymUnmanagedWriter interface [.NET Framework debugging]
- ISymUnmanagedWriter::OpenScope method [.NET Framework debugging]
ms.assetid: dbea0644-3873-4329-90b8-624163e87467
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 6aad2df19ec5563d8d48b0c286ab888a727c21ac
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33428158"
---
# <a name="isymunmanagedwriteropenscope-method"></a><span data-ttu-id="26f82-102">ISymUnmanagedWriter::OpenScope, méthode</span><span class="sxs-lookup"><span data-stu-id="26f82-102">ISymUnmanagedWriter::OpenScope Method</span></span>
<span data-ttu-id="26f82-103">Ouvre une nouvelle portée lexicale dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="26f82-103">Opens a new lexical scope in the current method.</span></span> <span data-ttu-id="26f82-104">La portée devient la nouvelle portée actuelle et est placée sur une pile d’étendues.</span><span class="sxs-lookup"><span data-stu-id="26f82-104">The scope becomes the new current scope and is pushed onto a stack of scopes.</span></span> <span data-ttu-id="26f82-105">Les portées doivent former une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="26f82-105">Scopes must form a hierarchy.</span></span> <span data-ttu-id="26f82-106">Frères ne sont pas autorisées à chevaucher.</span><span class="sxs-lookup"><span data-stu-id="26f82-106">Siblings are not allowed to overlap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26f82-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26f82-107">Syntax</span></span>  
  
```  
HRESULT OpenScope(  
    [in] ULONG32 startOffset,  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="26f82-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26f82-108">Parameters</span></span>  
 `startOffset`  
 <span data-ttu-id="26f82-109">[in] Le décalage de la première instruction dans la portée lexicale, en octets, à partir du début de la méthode.</span><span class="sxs-lookup"><span data-stu-id="26f82-109">[in] The offset of the first instruction in the lexical scope, in bytes, from the beginning of the method.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="26f82-110">[out] Un pointeur vers un `ULONG32` qui reçoit l’identificateur de portée.</span><span class="sxs-lookup"><span data-stu-id="26f82-110">[out] A pointer to a `ULONG32` that receives the scope identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="26f82-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="26f82-111">Return Value</span></span>  
 <span data-ttu-id="26f82-112">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="26f82-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="26f82-113">Notes</span><span class="sxs-lookup"><span data-stu-id="26f82-113">Remarks</span></span>  
 <span data-ttu-id="26f82-114">`ISymUnmanagedWriter::OpenScope` Retourne un identificateur de portée opaque qui peut être utilisé avec [ISymUnmanagedWriter::SetScopeRange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md) pour définir une étendue de début et de fin décalage ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="26f82-114">`ISymUnmanagedWriter::OpenScope` returns an opaque scope identifier that can be used with [ISymUnmanagedWriter::SetScopeRange](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-setscoperange-method.md) to define a scope's starting and ending offset at a later time.</span></span> <span data-ttu-id="26f82-115">Dans ce cas, les offsets passés à `ISymUnmanagedWriter::OpenScope` et [ISymUnmanagedWriter::CloseScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closescope-method.md) sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="26f82-115">In this case, the offsets passed to `ISymUnmanagedWriter::OpenScope` and [ISymUnmanagedWriter::CloseScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-closescope-method.md) are ignored.</span></span> <span data-ttu-id="26f82-116">Les identificateurs de portée sont valides uniquement dans la méthode actuelle.</span><span class="sxs-lookup"><span data-stu-id="26f82-116">Scope identifiers are valid only in the current method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26f82-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="26f82-117">Requirements</span></span>  
 <span data-ttu-id="26f82-118">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="26f82-118">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26f82-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26f82-119">See Also</span></span>  
 [<span data-ttu-id="26f82-120">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="26f82-120">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
