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
ms.openlocfilehash: 7f470dbe4ef2ef0d5f2204ccbdd5fb64730f9a2c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59159755"
---
# <a name="isymunmanagedwriterdefineconstant-method"></a><span data-ttu-id="89680-102">ISymUnmanagedWriter::DefineConstant, méthode</span><span class="sxs-lookup"><span data-stu-id="89680-102">ISymUnmanagedWriter::DefineConstant Method</span></span>
<span data-ttu-id="89680-103">Définit un nom pour une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="89680-103">Defines a name for a constant value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="89680-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89680-104">Syntax</span></span>  
  
```  
HRESULT DefineConstant(  
    [in] const WCHAR *name,  
    [in] VARIANT value,  
    [in] ULONG32 cSig,  
    [in, size_is(cSig)] unsigned char signature[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="89680-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89680-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="89680-106">[in] Un pointeur vers un `WCHAR` qui définit le nom de constante.</span><span class="sxs-lookup"><span data-stu-id="89680-106">[in] A pointer to a `WCHAR` that defines the constant name.</span></span>  
  
 `value`  
 <span data-ttu-id="89680-107">[in] La valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="89680-107">[in] The value of the constant.</span></span>  
  
 `cSig`  
 <span data-ttu-id="89680-108">[in] Taille du tableau `signature`.</span><span class="sxs-lookup"><span data-stu-id="89680-108">[in] The size of the `signature` array.</span></span>  
  
 `signature`  
 <span data-ttu-id="89680-109">[in] La signature de type pour la constante.</span><span class="sxs-lookup"><span data-stu-id="89680-109">[in] The type signature for the constant.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="89680-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="89680-110">Return Value</span></span>  
 <span data-ttu-id="89680-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="89680-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="89680-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89680-112">Requirements</span></span>  
 <span data-ttu-id="89680-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="89680-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89680-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89680-114">See also</span></span>

- [<span data-ttu-id="89680-115">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="89680-115">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
- [<span data-ttu-id="89680-116">DefineConstant2, méthode</span><span class="sxs-lookup"><span data-stu-id="89680-116">DefineConstant2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-defineconstant2-method.md)
