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
ms.openlocfilehash: 325db05cc322d85e836ca9ba62b6a169e8965241
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61766355"
---
# <a name="isymunmanagedvariablegetendoffset-method"></a><span data-ttu-id="5ee85-102">ISymUnmanagedVariable::GetEndOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="5ee85-102">ISymUnmanagedVariable::GetEndOffset Method</span></span>
<span data-ttu-id="5ee85-103">Obtient l’offset de fin de cette variable dans son parent.</span><span class="sxs-lookup"><span data-stu-id="5ee85-103">Gets the end offset of this variable within its parent.</span></span> <span data-ttu-id="5ee85-104">S’il s’agit d’une variable locale dans une portée, l’offset de fin est compris dans les offsets définis pour la portée.</span><span class="sxs-lookup"><span data-stu-id="5ee85-104">If this is a local variable within a scope, the end offset will fall within the offsets defined for the scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ee85-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ee85-105">Syntax</span></span>  
  
```  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5ee85-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ee85-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="5ee85-107">[out] Un pointeur vers un `ULONG32` qui reçoit l’offset de fin.</span><span class="sxs-lookup"><span data-stu-id="5ee85-107">[out] A pointer to a `ULONG32` that receives the end offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5ee85-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5ee85-108">Return Value</span></span>  
 <span data-ttu-id="5ee85-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5ee85-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ee85-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ee85-110">Requirements</span></span>  
 <span data-ttu-id="5ee85-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5ee85-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ee85-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ee85-112">See also</span></span>

- [<span data-ttu-id="5ee85-113">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="5ee85-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
- [<span data-ttu-id="5ee85-114">GetStartOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="5ee85-114">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getstartoffset-method.md)
