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
ms.openlocfilehash: 0a18689563cb3d5fb8460893f9a429507cf93b8f
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57486964"
---
# <a name="isymunmanagedscopegetmethod-method"></a><span data-ttu-id="54169-102">ISymUnmanagedScope::GetMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="54169-102">ISymUnmanagedScope::GetMethod Method</span></span>
<span data-ttu-id="54169-103">Obtient la méthode qui contient cette étendue.</span><span class="sxs-lookup"><span data-stu-id="54169-103">Gets the method that contains this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54169-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54169-104">Syntax</span></span>  
  
```  
HRESULT GetMethod(  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="54169-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54169-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="54169-106">[out] Un pointeur vers le texte retourné [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="54169-106">[out] A pointer to the returned [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="54169-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="54169-107">Return Value</span></span>  
 <span data-ttu-id="54169-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="54169-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="54169-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="54169-109">Requirements</span></span>  
 <span data-ttu-id="54169-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="54169-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54169-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54169-111">See also</span></span>
- [<span data-ttu-id="54169-112">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="54169-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
