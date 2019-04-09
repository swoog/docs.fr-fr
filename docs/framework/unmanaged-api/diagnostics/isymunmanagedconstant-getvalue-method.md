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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59204664"
---
# <a name="isymunmanagedconstantgetvalue-method"></a><span data-ttu-id="db2c0-102">ISymUnmanagedConstant::GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="db2c0-102">ISymUnmanagedConstant::GetValue Method</span></span>
<span data-ttu-id="db2c0-103">Obtient la valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="db2c0-103">Gets the value of the constant.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db2c0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db2c0-104">Syntax</span></span>  
  
```  
HRESULT GetValue(  
    [out]  VARIANT* pValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="db2c0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db2c0-105">Parameters</span></span>  
 `pValue`  
 <span data-ttu-id="db2c0-106">[out] Pointeur vers une variable qui reçoit la valeur.</span><span class="sxs-lookup"><span data-stu-id="db2c0-106">[out] A pointer to a variable that receives the value.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="db2c0-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="db2c0-107">Return Value</span></span>  
 <span data-ttu-id="db2c0-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="db2c0-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db2c0-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db2c0-109">Requirements</span></span>  
 <span data-ttu-id="db2c0-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="db2c0-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db2c0-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db2c0-111">See also</span></span>

- [<span data-ttu-id="db2c0-112">ISymUnmanagedConstant, interface</span><span class="sxs-lookup"><span data-stu-id="db2c0-112">ISymUnmanagedConstant Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-interface.md)
- [<span data-ttu-id="db2c0-113">GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="db2c0-113">GetName Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getname-method.md)
- [<span data-ttu-id="db2c0-114">GetSignature, méthode</span><span class="sxs-lookup"><span data-stu-id="db2c0-114">GetSignature Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedconstant-getsignature-method.md)
