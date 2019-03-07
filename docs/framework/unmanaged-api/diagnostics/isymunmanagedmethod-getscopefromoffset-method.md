---
title: ISymUnmanagedMethod::GetScopeFromOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetScopeFromOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetScopeFromOffset
helpviewer_keywords:
- GetScopeFromOffset method [.NET Framework debugging]
- ISymUnmanagedMethod::GetScopeFromOffset method [.NET Framework debugging]
ms.assetid: d14cf210-81f8-46e1-8b19-6ddec0ba8b11
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b036c5cff5300377580fe22dc254911fbdd79715
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57503123"
---
# <a name="isymunmanagedmethodgetscopefromoffset-method"></a><span data-ttu-id="9c0ee-102">ISymUnmanagedMethod::GetScopeFromOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="9c0ee-102">ISymUnmanagedMethod::GetScopeFromOffset Method</span></span>
<span data-ttu-id="9c0ee-103">Obtient la portée lexicale la plus englobante dans cette méthode qui englobe l’offset donné.</span><span class="sxs-lookup"><span data-stu-id="9c0ee-103">Gets the most enclosing lexical scope within this method that encloses the given offset.</span></span> <span data-ttu-id="9c0ee-104">Cela peut être utilisé pour démarrer la recherche de variables locales.</span><span class="sxs-lookup"><span data-stu-id="9c0ee-104">This can be used to start local variable searches.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9c0ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c0ee-105">Syntax</span></span>  
  
```  
HRESULT GetScopeFromOffset(  
    [in]  ULONG32 offset,  
    [out, retval] ISymUnmanagedScope**  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9c0ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9c0ee-106">Parameters</span></span>  
 `offset`  
 <span data-ttu-id="9c0ee-107">[in] Un `ULONG` qui contient l’offset.</span><span class="sxs-lookup"><span data-stu-id="9c0ee-107">[in] A `ULONG` that contains the offset.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="9c0ee-108">[out] Un pointeur qui est défini à retourné [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="9c0ee-108">[out] A pointer that is set to the returned [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9c0ee-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9c0ee-109">Return Value</span></span>  
 <span data-ttu-id="9c0ee-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9c0ee-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9c0ee-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9c0ee-111">Requirements</span></span>  
 <span data-ttu-id="9c0ee-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9c0ee-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c0ee-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9c0ee-113">See also</span></span>
- [<span data-ttu-id="9c0ee-114">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="9c0ee-114">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
