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
ms.openlocfilehash: d90aeb22a945f4fa1576009c700c420704dd891b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59144779"
---
# <a name="isymunmanagedscopegetparent-method"></a><span data-ttu-id="0bf73-102">ISymUnmanagedScope::GetParent, méthode</span><span class="sxs-lookup"><span data-stu-id="0bf73-102">ISymUnmanagedScope::GetParent Method</span></span>
<span data-ttu-id="0bf73-103">Obtient la portée parente de cette étendue.</span><span class="sxs-lookup"><span data-stu-id="0bf73-103">Gets the parent scope of this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0bf73-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bf73-104">Syntax</span></span>  
  
```  
HRESULT GetParent(  
    [out, retval] ISymUnmanagedScope** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0bf73-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bf73-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="0bf73-106">[out] Un pointeur vers le texte retourné [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="0bf73-106">[out] A pointer to the returned [ISymUnmanagedScope](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0bf73-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0bf73-107">Return Value</span></span>  
 <span data-ttu-id="0bf73-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0bf73-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0bf73-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bf73-109">Requirements</span></span>  
 <span data-ttu-id="0bf73-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="0bf73-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0bf73-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bf73-111">See also</span></span>

- [<span data-ttu-id="0bf73-112">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="0bf73-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
- [<span data-ttu-id="0bf73-113">GetChildren, méthode</span><span class="sxs-lookup"><span data-stu-id="0bf73-113">GetChildren Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-getchildren-method.md)
