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
ms.openlocfilehash: 9f35e3c9327a3945e6ddce85be52b757294b39aa
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429721"
---
# <a name="isymunmanagedwriter2defineglobalvariable2-method"></a><span data-ttu-id="940ba-102">ISymUnmanagedWriter2::DefineGlobalVariable2, méthode</span><span class="sxs-lookup"><span data-stu-id="940ba-102">ISymUnmanagedWriter2::DefineGlobalVariable2 Method</span></span>
<span data-ttu-id="940ba-103">Définit une variable globale unique.</span><span class="sxs-lookup"><span data-stu-id="940ba-103">Defines a single global variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="940ba-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="940ba-104">Syntax</span></span>  
  
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
  
#### <a name="parameters"></a><span data-ttu-id="940ba-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="940ba-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="940ba-106">[in] Le nom de variable global.</span><span class="sxs-lookup"><span data-stu-id="940ba-106">[in] The global variable name.</span></span>  
  
 `attributes`  
 <span data-ttu-id="940ba-107">[in] Attributs de la variable globales.</span><span class="sxs-lookup"><span data-stu-id="940ba-107">[in] The global variable attributes.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="940ba-108">[in] Le jeton de métadonnées de la signature.</span><span class="sxs-lookup"><span data-stu-id="940ba-108">[in] The metadata token of the signature.</span></span>  
  
 `addrKind`  
 <span data-ttu-id="940ba-109">[in] Le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="940ba-109">[in] The address type.</span></span>  
  
 `addr1`  
 <span data-ttu-id="940ba-110">[in] La première adresse de la spécification du paramètre.</span><span class="sxs-lookup"><span data-stu-id="940ba-110">[in] The first address for the parameter specification.</span></span>  
  
 `addr2`  
 <span data-ttu-id="940ba-111">[in] La deuxième adresse de la spécification du paramètre.</span><span class="sxs-lookup"><span data-stu-id="940ba-111">[in] The second address for the parameter specification.</span></span>  
  
 `addr3`  
 <span data-ttu-id="940ba-112">[in] Troisième adresse de la spécification du paramètre.</span><span class="sxs-lookup"><span data-stu-id="940ba-112">[in] The third address for the parameter specification.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="940ba-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="940ba-113">Return Value</span></span>  
 <span data-ttu-id="940ba-114">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="940ba-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="940ba-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="940ba-115">Requirements</span></span>  
 <span data-ttu-id="940ba-116">**En-tête :** CorSym.idl</span><span class="sxs-lookup"><span data-stu-id="940ba-116">**Header:** CorSym.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="940ba-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="940ba-117">See Also</span></span>  
 [<span data-ttu-id="940ba-118">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="940ba-118">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)  
 [<span data-ttu-id="940ba-119">DefineGlobalVariable, méthode</span><span class="sxs-lookup"><span data-stu-id="940ba-119">DefineGlobalVariable Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineglobalvariable-method.md)
