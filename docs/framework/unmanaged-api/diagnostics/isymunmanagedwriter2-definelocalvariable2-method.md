---
title: ISymUnmanagedWriter2::DefineLocalVariable2, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineLocalVariable2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineLocalVariable2
helpviewer_keywords:
- ISymUnmanagedWriter2::DefineLocalVariable2 method [.NET Framework debugging]
- DefineLocalVariable2 method [.NET Framework debugging]
ms.assetid: e774eefe-858c-4362-8d2d-28ebf2ba1a24
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2caa9b48fc92a1b2e82f574d37d99758e19382c7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61777967"
---
# <a name="isymunmanagedwriter2definelocalvariable2-method"></a><span data-ttu-id="c32fa-102">ISymUnmanagedWriter2::DefineLocalVariable2, méthode</span><span class="sxs-lookup"><span data-stu-id="c32fa-102">ISymUnmanagedWriter2::DefineLocalVariable2 Method</span></span>
<span data-ttu-id="c32fa-103">Définit une variable unique dans la portée lexicale actuelle.</span><span class="sxs-lookup"><span data-stu-id="c32fa-103">Defines a single variable in the current lexical scope.</span></span> <span data-ttu-id="c32fa-104">Cette méthode peut être appelée plusieurs fois pour une variable du même nom qui a plusieurs maisons tout au long d’une étendue.</span><span class="sxs-lookup"><span data-stu-id="c32fa-104">This method can be called multiple times for a variable of the same name that has multiple homes throughout a scope.</span></span> <span data-ttu-id="c32fa-105">Dans ce cas, toutefois, les valeurs de la `startOffset` et `endOffset` paramètres ne doivent pas se chevaucher.</span><span class="sxs-lookup"><span data-stu-id="c32fa-105">In this case, however, the values of the `startOffset` and `endOffset` parameters must not overlap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c32fa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c32fa-106">Syntax</span></span>  
  
```  
HRESULT DefineLocalVariable2(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] mdSignature  sigToken,  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3,  
    [in] ULONG32      startOffset,  
    [in] ULONG32      endOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c32fa-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c32fa-107">Parameters</span></span>  
 `name`  
 <span data-ttu-id="c32fa-108">[in] Le nom de variable locale.</span><span class="sxs-lookup"><span data-stu-id="c32fa-108">[in] The local variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="c32fa-109">[in] Attributs de variable locale.</span><span class="sxs-lookup"><span data-stu-id="c32fa-109">[in] The local variable attributes.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="c32fa-110">[in] Le jeton de métadonnées de la signature.</span><span class="sxs-lookup"><span data-stu-id="c32fa-110">[in] The metadata token of the signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="c32fa-111">[in] Le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="c32fa-111">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="c32fa-112">[in] La première adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c32fa-112">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="c32fa-113">[in] La deuxième adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c32fa-113">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="c32fa-114">[in] Troisième adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c32fa-114">[in] The third address for the parameter specification.</span></span>  
  
 `startOffset`  
 <span data-ttu-id="c32fa-115">[in] Offset de début pour la variable.</span><span class="sxs-lookup"><span data-stu-id="c32fa-115">[in] The start offset for the variable.</span></span> <span data-ttu-id="c32fa-116">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="c32fa-116">This parameter is optional.</span></span> <span data-ttu-id="c32fa-117">Si la valeur est 0, ce paramètre est ignoré et la variable est définie dans l’ensemble de la portée.</span><span class="sxs-lookup"><span data-stu-id="c32fa-117">If it is 0, this parameter is ignored and the variable is defined throughout the entire scope.</span></span> <span data-ttu-id="c32fa-118">Dans le cas d’une valeur différente de zéro, la variable est comprise entre les offsets de la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="c32fa-118">If it is a nonzero value, the variable falls within the offsets of the current scope.</span></span>  
  
 `endOffset`  
 <span data-ttu-id="c32fa-119">[in] Offset de fin pour la variable.</span><span class="sxs-lookup"><span data-stu-id="c32fa-119">[in] The end offset for the variable.</span></span> <span data-ttu-id="c32fa-120">Ce paramètre est optionnel.</span><span class="sxs-lookup"><span data-stu-id="c32fa-120">This parameter is optional.</span></span> <span data-ttu-id="c32fa-121">Si la valeur est 0, ce paramètre est ignoré et la variable est définie dans l’ensemble de la portée.</span><span class="sxs-lookup"><span data-stu-id="c32fa-121">If it is 0, this parameter is ignored and the variable is defined throughout the entire scope.</span></span> <span data-ttu-id="c32fa-122">Dans le cas d’une valeur différente de zéro, la variable est comprise entre les offsets de la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="c32fa-122">If it is a nonzero value, the variable falls within the offsets of the current scope.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c32fa-123">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c32fa-123">Return Value</span></span>  
 <span data-ttu-id="c32fa-124">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c32fa-124">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c32fa-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c32fa-125">Requirements</span></span>  
 <span data-ttu-id="c32fa-126">**En-tête :** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="c32fa-126">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c32fa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c32fa-127">See also</span></span>

- [<span data-ttu-id="c32fa-128">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="c32fa-128">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="c32fa-129">DefineLocalVariable, méthode</span><span class="sxs-lookup"><span data-stu-id="c32fa-129">DefineLocalVariable Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-definelocalvariable-method.md)
