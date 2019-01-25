---
title: ISymUnmanagedConstant::GetSignature, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetSignature
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetSignature
helpviewer_keywords:
- GetSignature method, ISymUnmanagedConstant interface [.NET Framework debugging]
- ISymUnmanagedConstant::GetSignature method [.NET Framework debugging]
ms.assetid: 3eb41151-a228-43e3-ba8f-e6dd3ceb8542
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 86c64f7c56555619ead495e1e935e7bea86ac6ec
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54495446"
---
# <a name="isymunmanagedconstantgetsignature-method"></a><span data-ttu-id="e786c-102">ISymUnmanagedConstant::GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="e786c-102">ISymUnmanagedConstant::GetSignature Method</span></span>
<span data-ttu-id="e786c-103">Obtient la signature de la constante.</span><span class="sxs-lookup"><span data-stu-id="e786c-103">Gets the signature of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e786c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e786c-104">Syntax</span></span>  
  
```  
HRESULT GetSignature(  
    [in]  ULONG32  cSig,  
    [out] ULONG32  *pcSig,  
    [out, size_is(cSig),  
        length_is(*pcSig)] BYTE sig[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e786c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e786c-105">Parameters</span></span>  
 `cSig`  
 <span data-ttu-id="e786c-106">[in] La longueur de la mémoire tampon qui le `pcSig` paramètre pointe vers.</span><span class="sxs-lookup"><span data-stu-id="e786c-106">[in] The length of the buffer that the `pcSig` parameter points to.</span></span>  
  
 `pcSig`  
 <span data-ttu-id="e786c-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir la signature.</span><span class="sxs-lookup"><span data-stu-id="e786c-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the signature.</span></span>  
  
 `sig`  
 <span data-ttu-id="e786c-108">[out] La mémoire tampon qui stocke la signature.</span><span class="sxs-lookup"><span data-stu-id="e786c-108">[out] The buffer that stores the signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e786c-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e786c-109">Return Value</span></span>  
 <span data-ttu-id="e786c-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e786c-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e786c-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e786c-111">Requirements</span></span>  
 <span data-ttu-id="e786c-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e786c-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e786c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e786c-113">See also</span></span>
- [<span data-ttu-id="e786c-114">ISymUnmanagedConstant, interface</span><span class="sxs-lookup"><span data-stu-id="e786c-114">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)
- [<span data-ttu-id="e786c-115">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="e786c-115">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getname-method.md)
- [<span data-ttu-id="e786c-116">GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="e786c-116">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getvalue-method.md)
