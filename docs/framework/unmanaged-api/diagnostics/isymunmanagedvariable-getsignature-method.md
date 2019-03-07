---
title: ISymUnmanagedVariable::GetSignature, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetSignature
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetSignature
helpviewer_keywords:
- GetSignature method, ISymUnmanagedVariable interface [.NET Framework debugging]
- ISymUnmanagedVariable::GetSignature method [.NET Framework debugging]
ms.assetid: 78c1ba28-a410-4360-805c-23a95408964a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0f28d6ec882afb21c3c204e141b1b6d883793004
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57499054"
---
# <a name="isymunmanagedvariablegetsignature-method"></a><span data-ttu-id="d8bd5-102">ISymUnmanagedVariable::GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="d8bd5-102">ISymUnmanagedVariable::GetSignature Method</span></span>
<span data-ttu-id="d8bd5-103">Obtient la signature de cette variable.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-103">Gets the signature of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8bd5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8bd5-104">Syntax</span></span>  
  
```  
HRESULT GetSignature(  
    [in]  ULONG32  cSig,  
    [out] ULONG32  *pcSig,  
    [out, size_is(cSig),  
        length_is(*pcSig)] BYTE sig[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d8bd5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8bd5-105">Parameters</span></span>  
 `cSig`  
 <span data-ttu-id="d8bd5-106">[in] La longueur de la mémoire tampon vers laquelle pointe le `sig` paramètre.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-106">[in] The length of the buffer pointed to by the `sig` parameter.</span></span>  
  
 `pcSig`  
 <span data-ttu-id="d8bd5-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir la signature.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the signature.</span></span>  
  
 `sig`  
 <span data-ttu-id="d8bd5-108">[out] La mémoire tampon qui stocke la signature.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-108">[out] The buffer that stores the signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d8bd5-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d8bd5-109">Return Value</span></span>  
 <span data-ttu-id="d8bd5-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8bd5-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8bd5-111">Requirements</span></span>  
 <span data-ttu-id="d8bd5-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d8bd5-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8bd5-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8bd5-113">See also</span></span>
- [<span data-ttu-id="d8bd5-114">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="d8bd5-114">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
