---
title: ISymUnmanagedVariable::GetEndOffset, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetEndOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetEndOffset
helpviewer_keywords:
- ISymUnmanagedVariable::GetEndOffset method [.NET Framework debugging]
- GetEndOffset method, ISymUnmanagedVariable interface [.NET Framework debugging]
ms.assetid: e5d777c5-d450-4c0f-999c-b3953ee22cfb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a4c474b2ea9bc80be156c8e1424eabe3d2384666
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54585265"
---
# <a name="isymunmanagedvariablegetendoffset-method"></a><span data-ttu-id="b7558-102">ISymUnmanagedVariable::GetEndOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="b7558-102">ISymUnmanagedVariable::GetEndOffset Method</span></span>
<span data-ttu-id="b7558-103">Obtient l’offset de fin de cette variable dans son parent.</span><span class="sxs-lookup"><span data-stu-id="b7558-103">Gets the end offset of this variable within its parent.</span></span> <span data-ttu-id="b7558-104">S’il s’agit d’une variable locale dans une portée, l’offset de fin est compris dans les offsets définis pour la portée.</span><span class="sxs-lookup"><span data-stu-id="b7558-104">If this is a local variable within a scope, the end offset will fall within the offsets defined for the scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7558-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7558-105">Syntax</span></span>  
  
```  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b7558-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7558-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="b7558-107">[out] Un pointeur vers un `ULONG32` qui reçoit l’offset de fin.</span><span class="sxs-lookup"><span data-stu-id="b7558-107">[out] A pointer to a `ULONG32` that receives the end offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b7558-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b7558-108">Return Value</span></span>  
 <span data-ttu-id="b7558-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b7558-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7558-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b7558-110">Requirements</span></span>  
 <span data-ttu-id="b7558-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b7558-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7558-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7558-112">See also</span></span>
- [<span data-ttu-id="b7558-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="b7558-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
- [<span data-ttu-id="b7558-114">GetStartOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="b7558-114">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getstartoffset-method.md)
