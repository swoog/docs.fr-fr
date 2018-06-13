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
ms.openlocfilehash: ce9ce768e32434e0a1acd2fad67a0cdc99f49e18
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430144"
---
# <a name="isymunmanagedconstantgetsignature-method"></a><span data-ttu-id="0abee-102">ISymUnmanagedConstant::GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="0abee-102">ISymUnmanagedConstant::GetSignature Method</span></span>
<span data-ttu-id="0abee-103">Obtient la signature de la constante.</span><span class="sxs-lookup"><span data-stu-id="0abee-103">Gets the signature of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0abee-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0abee-104">Syntax</span></span>  
  
```  
HRESULT GetSignature(  
    [in]  ULONG32  cSig,  
    [out] ULONG32  *pcSig,  
    [out, size_is(cSig),  
        length_is(*pcSig)] BYTE sig[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0abee-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0abee-105">Parameters</span></span>  
 `cSig`  
 <span data-ttu-id="0abee-106">[in] La longueur de la mémoire tampon qui le `pcSig` paramètre pointe vers.</span><span class="sxs-lookup"><span data-stu-id="0abee-106">[in] The length of the buffer that the `pcSig` parameter points to.</span></span>  
  
 `pcSig`  
 <span data-ttu-id="0abee-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir la signature.</span><span class="sxs-lookup"><span data-stu-id="0abee-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the signature.</span></span>  
  
 `sig`  
 <span data-ttu-id="0abee-108">[out] Mémoire tampon qui stocke la signature.</span><span class="sxs-lookup"><span data-stu-id="0abee-108">[out] The buffer that stores the signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0abee-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0abee-109">Return Value</span></span>  
 <span data-ttu-id="0abee-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0abee-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0abee-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0abee-111">Requirements</span></span>  
 <span data-ttu-id="0abee-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="0abee-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0abee-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0abee-113">See Also</span></span>  
 [<span data-ttu-id="0abee-114">ISymUnmanagedConstant, interface</span><span class="sxs-lookup"><span data-stu-id="0abee-114">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)  
 [<span data-ttu-id="0abee-115">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="0abee-115">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getname-method.md)  
 [<span data-ttu-id="0abee-116">GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="0abee-116">GetValue Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getvalue-method.md)
