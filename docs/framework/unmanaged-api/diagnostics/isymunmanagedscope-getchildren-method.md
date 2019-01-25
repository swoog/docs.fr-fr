---
title: ISymUnmanagedScope::GetChildren, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetChildren
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetChildren
helpviewer_keywords:
- ISymUnmanagedScope::GetChildren method [.NET Framework debugging]
- GetChildren method [.NET Framework debugging]
ms.assetid: 0bed524e-cc48-4bf0-b9fa-25d665e63ddb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f9bd6ae34903798a29f8666dfdba3e102fae28db
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54584556"
---
# <a name="isymunmanagedscopegetchildren-method"></a><span data-ttu-id="e15c4-102">ISymUnmanagedScope::GetChildren, méthode</span><span class="sxs-lookup"><span data-stu-id="e15c4-102">ISymUnmanagedScope::GetChildren Method</span></span>
<span data-ttu-id="e15c4-103">Obtient les enfants de cette étendue.</span><span class="sxs-lookup"><span data-stu-id="e15c4-103">Gets the children of this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e15c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e15c4-104">Syntax</span></span>  
  
```  
HRESULT GetChildren(  
    [in]  ULONG32  cChildren,  
    [out] ULONG32  *pcChildren,  
    [out, size_is(cChildren),  
        length_is(*pcChildren)] ISymUnmanagedScope* children[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e15c4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e15c4-105">Parameters</span></span>  
 `cChildren`  
 <span data-ttu-id="e15c4-106">[in] Un `ULONG32` qui indique la taille de la `children` tableau.</span><span class="sxs-lookup"><span data-stu-id="e15c4-106">[in] A `ULONG32` that indicates the size of the `children` array.</span></span>  
  
 `pcChildren`  
 <span data-ttu-id="e15c4-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les enfants.</span><span class="sxs-lookup"><span data-stu-id="e15c4-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the children.</span></span>  
  
 `children`  
 <span data-ttu-id="e15c4-108">[out] Le tableau retourné d’enfants.</span><span class="sxs-lookup"><span data-stu-id="e15c4-108">[out] The returned array of children.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e15c4-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e15c4-109">Return Value</span></span>  
 <span data-ttu-id="e15c4-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e15c4-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e15c4-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e15c4-111">Requirements</span></span>  
 <span data-ttu-id="e15c4-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e15c4-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e15c4-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e15c4-113">See also</span></span>
- [<span data-ttu-id="e15c4-114">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="e15c4-114">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
- [<span data-ttu-id="e15c4-115">GetParent, méthode</span><span class="sxs-lookup"><span data-stu-id="e15c4-115">GetParent Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getparent-method.md)
