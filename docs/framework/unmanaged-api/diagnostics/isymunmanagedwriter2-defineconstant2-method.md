---
title: ISymUnmanagedWriter2::DefineConstant2, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter2.DefineConstant2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter2::DefineConstant2
helpviewer_keywords:
- DefineConstant2 method [.NET Framework debugging]
- ISymUnmanagedWriter2::DefineConstant2 method [.NET Framework debugging]
ms.assetid: dd2bc956-7dbe-49fc-a646-daa0d267f2df
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c6f9f198fc1115aed7b531515ab07ddc35d36ba8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427334"
---
# <a name="isymunmanagedwriter2defineconstant2-method"></a><span data-ttu-id="ed025-102">ISymUnmanagedWriter2::DefineConstant2, méthode</span><span class="sxs-lookup"><span data-stu-id="ed025-102">ISymUnmanagedWriter2::DefineConstant2 Method</span></span>
<span data-ttu-id="ed025-103">Définit un nom pour une valeur constante.</span><span class="sxs-lookup"><span data-stu-id="ed025-103">Defines a name for a constant value.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed025-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed025-104">Syntax</span></span>  
  
```  
HRESULT DefineConstant2(  
    [in] const WCHAR  *name,  
    [in] VARIANT      value,  
    [in] mdSignature  sigToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ed025-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed025-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="ed025-106">[in] Nom de la constante.</span><span class="sxs-lookup"><span data-stu-id="ed025-106">[in] The constant name.</span></span>  
  
 `value`  
 <span data-ttu-id="ed025-107">[in] La valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="ed025-107">[in] The value of the constant.</span></span>  
  
 `sigToken`  
 <span data-ttu-id="ed025-108">[in] Le jeton de métadonnées de la constante.</span><span class="sxs-lookup"><span data-stu-id="ed025-108">[in] The metadata token of the constant.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ed025-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ed025-109">Return Value</span></span>  
 <span data-ttu-id="ed025-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ed025-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ed025-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ed025-111">Requirements</span></span>  
 <span data-ttu-id="ed025-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ed025-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed025-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed025-113">See Also</span></span>  
 [<span data-ttu-id="ed025-114">ISymUnmanagedWriter2, interface</span><span class="sxs-lookup"><span data-stu-id="ed025-114">ISymUnmanagedWriter2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter2-interface.md)  
 [<span data-ttu-id="ed025-115">DefineConstant, méthode</span><span class="sxs-lookup"><span data-stu-id="ed025-115">DefineConstant Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-defineconstant-method.md)
