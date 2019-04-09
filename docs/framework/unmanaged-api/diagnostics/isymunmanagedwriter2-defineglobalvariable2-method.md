---
title: ISymUnmanagedWriter2::DefineGlobalVariable2, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineGlobalVariable2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineGlobalVariable2
helpviewer_keywords:
- ISymUnmanagedWriter2::DefineGlobalVariable2 method [.NET Framework debugging]
- DefineGlobalVariable2 method [.NET Framework debugging]
ms.assetid: 04d569d6-a151-4957-9872-f3f694c3e4a9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a6bc6c52374ea047d2e76d346ee8bbc3faaa7bb2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59145221"
---
# <a name="isymunmanagedwriter2defineglobalvariable2-method"></a><span data-ttu-id="26133-102">ISymUnmanagedWriter2::DefineGlobalVariable2, méthode</span><span class="sxs-lookup"><span data-stu-id="26133-102">ISymUnmanagedWriter2::DefineGlobalVariable2 Method</span></span>
<span data-ttu-id="26133-103">Définit une variable globale unique.</span><span class="sxs-lookup"><span data-stu-id="26133-103">Defines a single global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26133-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26133-104">Syntax</span></span>  
  
```  
HRESULT DefineGlobalVariable2(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] mdSignature  sigToken,  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a><span data-ttu-id="26133-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26133-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="26133-106">[in] Le nom de variable global.</span><span class="sxs-lookup"><span data-stu-id="26133-106">[in] The global variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="26133-107">[in] Attributs de la variable globale.</span><span class="sxs-lookup"><span data-stu-id="26133-107">[in] The global variable attributes.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="26133-108">[in] Le jeton de métadonnées de la signature.</span><span class="sxs-lookup"><span data-stu-id="26133-108">[in] The metadata token of the signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="26133-109">[in] Le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="26133-109">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="26133-110">[in] La première adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="26133-110">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="26133-111">[in] La deuxième adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="26133-111">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="26133-112">[in] Troisième adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="26133-112">[in] The third address for the parameter specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="26133-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="26133-113">Return Value</span></span>  
 <span data-ttu-id="26133-114">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="26133-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26133-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26133-115">Requirements</span></span>  
 <span data-ttu-id="26133-116">**En-tête :** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="26133-116">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26133-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26133-117">See also</span></span>

- [<span data-ttu-id="26133-118">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="26133-118">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="26133-119">DefineGlobalVariable, méthode</span><span class="sxs-lookup"><span data-stu-id="26133-119">DefineGlobalVariable Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineglobalvariable-method.md)
