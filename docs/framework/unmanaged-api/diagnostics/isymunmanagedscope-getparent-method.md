---
title: ISymUnmanagedScope::GetParent, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetParent
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetParent
helpviewer_keywords:
- GetParent method [.NET Framework debugging]
- ISymUnmanagedScope::GetParent method [.NET Framework debugging]
ms.assetid: c7963c87-6ec5-49b3-a5cd-e0fe0c43f9b4
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 634f30186c552f0e5330dd94f78c585da7d450c9
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57493828"
---
# <a name="isymunmanagedscopegetparent-method"></a><span data-ttu-id="fb2f0-102">ISymUnmanagedScope::GetParent, méthode</span><span class="sxs-lookup"><span data-stu-id="fb2f0-102">ISymUnmanagedScope::GetParent Method</span></span>
<span data-ttu-id="fb2f0-103">Obtient la portée parente de cette étendue.</span><span class="sxs-lookup"><span data-stu-id="fb2f0-103">Gets the parent scope of this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb2f0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb2f0-104">Syntax</span></span>  
  
```  
HRESULT GetParent(  
    [out, retval] ISymUnmanagedScope** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fb2f0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb2f0-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="fb2f0-106">[out] Un pointeur vers le texte retourné [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fb2f0-106">[out] A pointer to the returned [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fb2f0-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fb2f0-107">Return Value</span></span>  
 <span data-ttu-id="fb2f0-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fb2f0-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fb2f0-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fb2f0-109">Requirements</span></span>  
 <span data-ttu-id="fb2f0-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fb2f0-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb2f0-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb2f0-111">See also</span></span>
- [<span data-ttu-id="fb2f0-112">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="fb2f0-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
- [<span data-ttu-id="fb2f0-113">GetChildren, méthode</span><span class="sxs-lookup"><span data-stu-id="fb2f0-113">GetChildren Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getchildren-method.md)
