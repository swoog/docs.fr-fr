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
ms.openlocfilehash: 954b1d91f33fe9a7e4df1ef51ee3666047836a17
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59099961"
---
# <a name="isymunmanagedscopegetmethod-method"></a><span data-ttu-id="d37e9-102">ISymUnmanagedScope::GetMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="d37e9-102">ISymUnmanagedScope::GetMethod Method</span></span>
<span data-ttu-id="d37e9-103">Obtient la méthode qui contient cette étendue.</span><span class="sxs-lookup"><span data-stu-id="d37e9-103">Gets the method that contains this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d37e9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d37e9-104">Syntax</span></span>  
  
```  
HRESULT GetMethod(  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d37e9-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d37e9-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="d37e9-106">[out] Un pointeur vers le texte retourné [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="d37e9-106">[out] A pointer to the returned [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d37e9-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d37e9-107">Return Value</span></span>  
 <span data-ttu-id="d37e9-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d37e9-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d37e9-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d37e9-109">Requirements</span></span>  
 <span data-ttu-id="d37e9-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d37e9-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d37e9-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d37e9-111">See also</span></span>

- [<span data-ttu-id="d37e9-112">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="d37e9-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
