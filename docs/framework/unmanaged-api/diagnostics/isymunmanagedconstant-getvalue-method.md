---
title: ISymUnmanagedConstant::GetValue, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetValue
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetValue
helpviewer_keywords:
- GetValue method, ISymUnmanagedConstant interface [.NET Framework debugging]
- ISymUnmanagedConstant::GetValue method [.NET Framework debugging]
ms.assetid: 0036fc10-e768-47a8-b9cf-bf47faf8d194
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f51a41e8f00a0cf88b11078468ba5a8511fd1391
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424737"
---
# <a name="isymunmanagedconstantgetvalue-method"></a><span data-ttu-id="4f7f9-102">ISymUnmanagedConstant::GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="4f7f9-102">ISymUnmanagedConstant::GetValue Method</span></span>
<span data-ttu-id="4f7f9-103">Obtient la valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="4f7f9-103">Gets the value of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4f7f9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f7f9-104">Syntax</span></span>  
  
```  
HRESULT GetValue(  
    [out]  VARIANT* pValue  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4f7f9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f7f9-105">Parameters</span></span>  
 `pValue`  
 <span data-ttu-id="4f7f9-106">[out] Pointeur vers une variable qui reçoit la valeur.</span><span class="sxs-lookup"><span data-stu-id="4f7f9-106">[out] A pointer to a variable that receives the value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4f7f9-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4f7f9-107">Return Value</span></span>  
 <span data-ttu-id="4f7f9-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4f7f9-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4f7f9-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4f7f9-109">Requirements</span></span>  
 <span data-ttu-id="4f7f9-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="4f7f9-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4f7f9-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f7f9-111">See Also</span></span>  
 [<span data-ttu-id="4f7f9-112">ISymUnmanagedConstant, interface</span><span class="sxs-lookup"><span data-stu-id="4f7f9-112">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)  
 [<span data-ttu-id="4f7f9-113">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="4f7f9-113">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getname-method.md)  
 [<span data-ttu-id="4f7f9-114">GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="4f7f9-114">GetSignature Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getsignature-method.md)
