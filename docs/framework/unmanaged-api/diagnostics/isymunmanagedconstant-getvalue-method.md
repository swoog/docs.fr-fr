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
ms.openlocfilehash: 75cc16f44ddf29b161c758718b697cc2aaba8e08
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940021"
---
# <a name="isymunmanagedconstantgetvalue-method"></a><span data-ttu-id="44c62-102">ISymUnmanagedConstant::GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="44c62-102">ISymUnmanagedConstant::GetValue Method</span></span>
<span data-ttu-id="44c62-103">Obtient la valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="44c62-103">Gets the value of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44c62-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44c62-104">Syntax</span></span>  
  
```  
HRESULT GetValue(  
    [out]  VARIANT* pValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="44c62-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44c62-105">Parameters</span></span>  
 `pValue`  
 <span data-ttu-id="44c62-106">[out] Pointeur vers une variable qui reçoit la valeur.</span><span class="sxs-lookup"><span data-stu-id="44c62-106">[out] A pointer to a variable that receives the value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="44c62-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="44c62-107">Return Value</span></span>  
 <span data-ttu-id="44c62-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="44c62-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="44c62-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44c62-109">Requirements</span></span>  
 <span data-ttu-id="44c62-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="44c62-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44c62-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44c62-111">See also</span></span>

- [<span data-ttu-id="44c62-112">ISymUnmanagedConstant, interface</span><span class="sxs-lookup"><span data-stu-id="44c62-112">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)
- [<span data-ttu-id="44c62-113">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="44c62-113">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getname-method.md)
- [<span data-ttu-id="44c62-114">GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="44c62-114">GetSignature Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getsignature-method.md)
