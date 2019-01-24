---
title: ISymUnmanagedScope::GetMethod, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetMethod
helpviewer_keywords:
- GetMethod method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetMethod method [.NET Framework debugging]
ms.assetid: a61866ee-221a-45b9-a1b7-395825b77872
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 12dd485f2b89dc76076410e76a132ff547681597
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616821"
---
# <a name="isymunmanagedscopegetmethod-method"></a><span data-ttu-id="fe4f4-102">ISymUnmanagedScope::GetMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="fe4f4-102">ISymUnmanagedScope::GetMethod Method</span></span>
<span data-ttu-id="fe4f4-103">Obtient la méthode qui contient cette étendue.</span><span class="sxs-lookup"><span data-stu-id="fe4f4-103">Gets the method that contains this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe4f4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe4f4-104">Syntax</span></span>  
  
```  
HRESULT GetMethod(  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fe4f4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe4f4-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="fe4f4-106">[out] Un pointeur vers le texte retourné [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fe4f4-106">[out] A pointer to the returned [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fe4f4-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fe4f4-107">Return Value</span></span>  
 <span data-ttu-id="fe4f4-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="fe4f4-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe4f4-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe4f4-109">Requirements</span></span>  
 <span data-ttu-id="fe4f4-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fe4f4-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe4f4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe4f4-111">See also</span></span>
- [<span data-ttu-id="fe4f4-112">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="fe4f4-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
