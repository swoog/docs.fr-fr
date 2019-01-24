---
title: ISymUnmanagedMethod::GetNamespace, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetNamespace
helpviewer_keywords:
- ISymUnmanagedMethod::GetNamespace method [.NET Framework debugging]
- GetNamespace method [.NET Framework debugging]
ms.assetid: 7fbbac42-b966-406d-9ae9-67bf3aea74ce
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a2bba44af50607772f2a52203a47e21d8699f78b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54716150"
---
# <a name="isymunmanagedmethodgetnamespace-method"></a><span data-ttu-id="0fb73-102">ISymUnmanagedMethod::GetNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="0fb73-102">ISymUnmanagedMethod::GetNamespace Method</span></span>
<span data-ttu-id="0fb73-103">Obtient l’espace de noms dans lequel cette méthode est définie.</span><span class="sxs-lookup"><span data-stu-id="0fb73-103">Gets the namespace within which this method is defined.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fb73-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fb73-104">Syntax</span></span>  
  
```  
HRESULT GetNamespace(  
   [out] ISymUnmanagedNamespace  **pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0fb73-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0fb73-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="0fb73-106">[out] Un pointeur qui est défini à retourné [ISymUnmanagedNamespace](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="0fb73-106">[out] A pointer that is set to the returned [ISymUnmanagedNamespace](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0fb73-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0fb73-107">Return Value</span></span>  
 <span data-ttu-id="0fb73-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0fb73-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fb73-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0fb73-109">Requirements</span></span>  
 <span data-ttu-id="0fb73-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="0fb73-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fb73-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fb73-111">See also</span></span>
- [<span data-ttu-id="0fb73-112">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="0fb73-112">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
