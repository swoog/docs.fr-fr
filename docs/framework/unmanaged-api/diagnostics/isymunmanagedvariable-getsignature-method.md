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
ms.openlocfilehash: 3cc616246812bb9643388d8ad57cf84bc387b55e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59136417"
---
# <a name="isymunmanagedvariablegetsignature-method"></a><span data-ttu-id="6f084-102">ISymUnmanagedVariable::GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="6f084-102">ISymUnmanagedVariable::GetSignature Method</span></span>
<span data-ttu-id="6f084-103">Obtient la signature de cette variable.</span><span class="sxs-lookup"><span data-stu-id="6f084-103">Gets the signature of this variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6f084-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f084-104">Syntax</span></span>  
  
```  
HRESULT GetSignature(  
    [in]  ULONG32  cSig,  
    [out] ULONG32  *pcSig,  
    [out, size_is(cSig),  
        length_is(*pcSig)] BYTE sig[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6f084-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f084-105">Parameters</span></span>  
 `cSig`  
 <span data-ttu-id="6f084-106">[in] La longueur de la mémoire tampon vers laquelle pointe le `sig` paramètre.</span><span class="sxs-lookup"><span data-stu-id="6f084-106">[in] The length of the buffer pointed to by the `sig` parameter.</span></span>  
  
 `pcSig`  
 <span data-ttu-id="6f084-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir la signature.</span><span class="sxs-lookup"><span data-stu-id="6f084-107">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the signature.</span></span>  
  
 `sig`  
 <span data-ttu-id="6f084-108">[out] La mémoire tampon qui stocke la signature.</span><span class="sxs-lookup"><span data-stu-id="6f084-108">[out] The buffer that stores the signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6f084-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6f084-109">Return Value</span></span>  
 <span data-ttu-id="6f084-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6f084-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6f084-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f084-111">Requirements</span></span>  
 <span data-ttu-id="6f084-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="6f084-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f084-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f084-113">See also</span></span>

- [<span data-ttu-id="6f084-114">ISymUnmanagedVariable, interface</span><span class="sxs-lookup"><span data-stu-id="6f084-114">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)
