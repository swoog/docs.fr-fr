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
ms.openlocfilehash: 067be401b793c227d8b5caa2706f84a59d3a09df
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57499041"
---
# <a name="isymunmanagedwriter2defineglobalvariable2-method"></a><span data-ttu-id="389f0-102">ISymUnmanagedWriter2::DefineGlobalVariable2, méthode</span><span class="sxs-lookup"><span data-stu-id="389f0-102">ISymUnmanagedWriter2::DefineGlobalVariable2 Method</span></span>
<span data-ttu-id="389f0-103">Définit une variable globale unique.</span><span class="sxs-lookup"><span data-stu-id="389f0-103">Defines a single global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="389f0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="389f0-104">Syntax</span></span>  
  
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
  
## <a name="parameters"></a><span data-ttu-id="389f0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="389f0-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="389f0-106">[in] Le nom de variable global.</span><span class="sxs-lookup"><span data-stu-id="389f0-106">[in] The global variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="389f0-107">[in] Attributs de la variable globale.</span><span class="sxs-lookup"><span data-stu-id="389f0-107">[in] The global variable attributes.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="389f0-108">[in] Le jeton de métadonnées de la signature.</span><span class="sxs-lookup"><span data-stu-id="389f0-108">[in] The metadata token of the signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="389f0-109">[in] Le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="389f0-109">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="389f0-110">[in] La première adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="389f0-110">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="389f0-111">[in] La deuxième adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="389f0-111">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="389f0-112">[in] Troisième adresse de la spécification de paramètre.</span><span class="sxs-lookup"><span data-stu-id="389f0-112">[in] The third address for the parameter specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="389f0-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="389f0-113">Return Value</span></span>  
 <span data-ttu-id="389f0-114">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="389f0-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="389f0-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="389f0-115">Requirements</span></span>  
 <span data-ttu-id="389f0-116">**En-tête :** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="389f0-116">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="389f0-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="389f0-117">See also</span></span>
- [<span data-ttu-id="389f0-118">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="389f0-118">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)
- [<span data-ttu-id="389f0-119">DefineGlobalVariable, méthode</span><span class="sxs-lookup"><span data-stu-id="389f0-119">DefineGlobalVariable Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineglobalvariable-method.md)
