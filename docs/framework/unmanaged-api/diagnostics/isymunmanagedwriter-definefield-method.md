---
title: ISymUnmanagedWriter::DefineField, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineField
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineField
helpviewer_keywords:
- ISymUnmanagedWriter::DefineField method [.NET Framework debugging]
- DefineField method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: c6a1f797-dbf4-40f5-ab99-d9b4bfb26148
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5a385e42ae3a494f6d2196e21b552c6b5679dda9
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468882"
---
# <a name="isymunmanagedwriterdefinefield-method"></a><span data-ttu-id="886b7-102">ISymUnmanagedWriter::DefineField, méthode</span><span class="sxs-lookup"><span data-stu-id="886b7-102">ISymUnmanagedWriter::DefineField Method</span></span>
<span data-ttu-id="886b7-103">Définit une variable unique qui n’est pas dans une méthode.</span><span class="sxs-lookup"><span data-stu-id="886b7-103">Defines a single variable that is not within a method.</span></span> <span data-ttu-id="886b7-104">Cette méthode est utilisée pour certains champs dans les classes, les champs de bits et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="886b7-104">This method is used for certain fields in classes, bit fields, and so on.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="886b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="886b7-105">Syntax</span></span>  
  
```  
HRESULT DefineField(  
    [in] mdTypeDef    parent,  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      cSig,  
    [in, size_is(cSig)] unsigned char signature[],  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a><span data-ttu-id="886b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="886b7-106">Parameters</span></span>  
 `parent`  
 <span data-ttu-id="886b7-107">[in] Le type de métadonnées ou la méthode jeton.</span><span class="sxs-lookup"><span data-stu-id="886b7-107">[in] The metadata type or method token.</span></span>  
  
 `name`  
 <span data-ttu-id="886b7-108">[in] Le nom du champ.</span><span class="sxs-lookup"><span data-stu-id="886b7-108">[in] The field name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="886b7-109">[in] Les attributs de champ.</span><span class="sxs-lookup"><span data-stu-id="886b7-109">[in] The field attributes.</span></span>  
  
 `cSig`  
 <span data-ttu-id="886b7-110">[in] Un `ULONG32` qui est la taille, en caractères, de la mémoire tampon requise pour contenir la signature de champ.</span><span class="sxs-lookup"><span data-stu-id="886b7-110">[in] A `ULONG32` that is the size, in characters, of the buffer required to contain the field signature.</span></span>  
  
 `signature`  
 <span data-ttu-id="886b7-111">[in] Le tableau de signatures de champ.</span><span class="sxs-lookup"><span data-stu-id="886b7-111">[in] The array of field signatures.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="886b7-112">[in] Le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="886b7-112">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="886b7-113">[in] La première adresse de la spécification de champ.</span><span class="sxs-lookup"><span data-stu-id="886b7-113">[in] The first address for the field specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="886b7-114">[in] La deuxième adresse de la spécification de champ.</span><span class="sxs-lookup"><span data-stu-id="886b7-114">[in] The second address for the field specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="886b7-115">[in] Troisième adresse de la spécification de champ.</span><span class="sxs-lookup"><span data-stu-id="886b7-115">[in] The third address for the field specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="886b7-116">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="886b7-116">Return Value</span></span>  
 <span data-ttu-id="886b7-117">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="886b7-117">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="886b7-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="886b7-118">Requirements</span></span>  
 <span data-ttu-id="886b7-119">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="886b7-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="886b7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="886b7-120">See also</span></span>
- [<span data-ttu-id="886b7-121">ISymUnmanagedWriter, interface</span><span class="sxs-lookup"><span data-stu-id="886b7-121">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
