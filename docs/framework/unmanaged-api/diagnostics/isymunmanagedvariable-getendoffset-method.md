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
ms.openlocfilehash: e0f11614c6fa15034ef5fa3d68e41a936a9ff764
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427855"
---
# <a name="isymunmanagedvariablegetendoffset-method"></a><span data-ttu-id="b11b4-102">ISymUnmanagedVariable::GetEndOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="b11b4-102">ISymUnmanagedVariable::GetEndOffset Method</span></span>
<span data-ttu-id="b11b4-103">Obtient l’offset de fin de cette variable dans son parent.</span><span class="sxs-lookup"><span data-stu-id="b11b4-103">Gets the end offset of this variable within its parent.</span></span> <span data-ttu-id="b11b4-104">S’il s’agit d’une variable locale dans une portée, l’offset de fin est compris dans les offsets définis pour la portée.</span><span class="sxs-lookup"><span data-stu-id="b11b4-104">If this is a local variable within a scope, the end offset will fall within the offsets defined for the scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b11b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b11b4-105">Syntax</span></span>  
  
```  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b11b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b11b4-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="b11b4-107">[out] Un pointeur vers un `ULONG32` qui reçoit l’offset de fin.</span><span class="sxs-lookup"><span data-stu-id="b11b4-107">[out] A pointer to a `ULONG32` that receives the end offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b11b4-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b11b4-108">Return Value</span></span>  
 <span data-ttu-id="b11b4-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b11b4-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b11b4-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b11b4-110">Requirements</span></span>  
 <span data-ttu-id="b11b4-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b11b4-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b11b4-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b11b4-112">See Also</span></span>  
 [<span data-ttu-id="b11b4-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="b11b4-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)  
 [<span data-ttu-id="b11b4-114">GetStartOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="b11b4-114">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getstartoffset-method.md)
