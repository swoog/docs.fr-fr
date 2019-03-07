---
title: ISymUnmanagedWriter::DefineConstant, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineConstant
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineConstant
helpviewer_keywords:
- DefineConstant method [.NET Framework debugging]
- ISymUnmanagedWriter::DefineConstant method [.NET Framework debugging]
ms.assetid: 9e986986-2223-4d5f-b040-85d716146924
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 4d19b77633ba9c35dfedad047248b69643861644
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468986"
---
# <a name="isymunmanagedwriterdefineconstant-method"></a><span data-ttu-id="b09a9-102">ISymUnmanagedWriter::DefineConstant, méthode</span><span class="sxs-lookup"><span data-stu-id="b09a9-102">ISymUnmanagedWriter::DefineConstant Method</span></span>
<span data-ttu-id="b09a9-103">Définit un nom pour une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="b09a9-103">Defines a name for a constant value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b09a9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b09a9-104">Syntax</span></span>  
  
```  
HRESULT DefineConstant(  
    [in] const WCHAR *name,  
    [in] VARIANT value,  
    [in] ULONG32 cSig,  
    [in, size_is(cSig)] unsigned char signature[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b09a9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b09a9-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="b09a9-106">[in] Un pointeur vers un `WCHAR` qui définit le nom de constante.</span><span class="sxs-lookup"><span data-stu-id="b09a9-106">[in] A pointer to a `WCHAR` that defines the constant name.</span></span>  
  
 `value`  
 <span data-ttu-id="b09a9-107">[in] La valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="b09a9-107">[in] The value of the constant.</span></span>  
  
 `cSig`  
 <span data-ttu-id="b09a9-108">[in] Taille du tableau `signature`.</span><span class="sxs-lookup"><span data-stu-id="b09a9-108">[in] The size of the `signature` array.</span></span>  
  
 `signature`  
 <span data-ttu-id="b09a9-109">[in] La signature de type pour la constante.</span><span class="sxs-lookup"><span data-stu-id="b09a9-109">[in] The type signature for the constant.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b09a9-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b09a9-110">Return Value</span></span>  
 <span data-ttu-id="b09a9-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b09a9-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b09a9-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b09a9-112">Requirements</span></span>  
 <span data-ttu-id="b09a9-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="b09a9-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b09a9-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b09a9-114">See also</span></span>
- [<span data-ttu-id="b09a9-115">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="b09a9-115">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="b09a9-116">DefineConstant2, méthode</span><span class="sxs-lookup"><span data-stu-id="b09a9-116">DefineConstant2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineconstant2-method.md)
