---
title: ISymUnmanagedMethod::GetRootScope, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetRootScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetRootScope
helpviewer_keywords:
- ISymUnmanagedMethod::GetRootScope method [.NET Framework debugging]
- GetRootScope method [.NET Framework debugging]
ms.assetid: 7d58caac-2e75-4dfa-9249-32d8a624b247
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7c77be0dde950693d3943e41c392dcdcd9bc995e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59096073"
---
# <a name="isymunmanagedmethodgetrootscope-method"></a><span data-ttu-id="8fb51-102">ISymUnmanagedMethod::GetRootScope, méthode</span><span class="sxs-lookup"><span data-stu-id="8fb51-102">ISymUnmanagedMethod::GetRootScope Method</span></span>
<span data-ttu-id="8fb51-103">Obtient la portée lexicale racine au sein de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8fb51-103">Gets the root lexical scope within this method.</span></span> <span data-ttu-id="8fb51-104">Cette portée englobe la totalité de la méthode.</span><span class="sxs-lookup"><span data-stu-id="8fb51-104">This scope encloses the entire method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8fb51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fb51-105">Syntax</span></span>  
  
```  
HRESULT GetRootScope(  
    [out, retval] ISymUnmanagedScope** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8fb51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fb51-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="8fb51-107">[out] Un pointeur qui est défini à retourné [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="8fb51-107">[out] A pointer that is set to the returned [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8fb51-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8fb51-108">Return Value</span></span>  
 <span data-ttu-id="8fb51-109">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8fb51-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8fb51-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fb51-110">Requirements</span></span>  
 <span data-ttu-id="8fb51-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="8fb51-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fb51-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fb51-112">See also</span></span>

- [<span data-ttu-id="8fb51-113">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="8fb51-113">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
