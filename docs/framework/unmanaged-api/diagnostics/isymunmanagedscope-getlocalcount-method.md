---
title: ISymUnmanagedScope::GetLocalCount, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetLocalCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetLocalCount
helpviewer_keywords:
- GetLocalCount method [.NET Framework debugging]
- ISymUnmanagedScope::GetLocalCount method [.NET Framework debugging]
ms.assetid: 3ede8fb5-f655-4088-8e19-9c53812588a8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 809b9033c784954374065a901f34f7542f41e7ab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549939"
---
# <a name="isymunmanagedscopegetlocalcount-method"></a><span data-ttu-id="9f508-102">ISymUnmanagedScope::GetLocalCount, méthode</span><span class="sxs-lookup"><span data-stu-id="9f508-102">ISymUnmanagedScope::GetLocalCount Method</span></span>
<span data-ttu-id="9f508-103">Obtient le nombre des variables locales définies dans cette portée.</span><span class="sxs-lookup"><span data-stu-id="9f508-103">Gets a count of the local variables defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f508-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f508-104">Syntax</span></span>  
  
```  
HRESULT GetLocalCount(  
    [out, retval] ULONG32 *pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9f508-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f508-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="9f508-106">[out] Un pointeur vers un `ULONG32` qui reçoit le nombre de variables locales.</span><span class="sxs-lookup"><span data-stu-id="9f508-106">[out] A pointer to a `ULONG32` that receives the count of local variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9f508-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9f508-107">Return Value</span></span>  
 <span data-ttu-id="9f508-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9f508-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f508-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f508-109">Requirements</span></span>  
 <span data-ttu-id="9f508-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9f508-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f508-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f508-111">See also</span></span>
- [<span data-ttu-id="9f508-112">ISymUnmanagedScope, interface</span><span class="sxs-lookup"><span data-stu-id="9f508-112">ISymUnmanagedScope Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedscope-interface.md)
