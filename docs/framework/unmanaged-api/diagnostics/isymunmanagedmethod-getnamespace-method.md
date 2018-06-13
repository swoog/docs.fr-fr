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
ms.openlocfilehash: 53a47cf67edb36b06c92be83cb23c2e1dd1e75cf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424428"
---
# <a name="isymunmanagedmethodgetnamespace-method"></a><span data-ttu-id="6d8fc-102">ISymUnmanagedMethod::GetNamespace, méthode</span><span class="sxs-lookup"><span data-stu-id="6d8fc-102">ISymUnmanagedMethod::GetNamespace Method</span></span>
<span data-ttu-id="6d8fc-103">Obtient l’espace de noms dans lequel cette méthode est définie.</span><span class="sxs-lookup"><span data-stu-id="6d8fc-103">Gets the namespace within which this method is defined.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d8fc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d8fc-104">Syntax</span></span>  
  
```  
HRESULT GetNamespace(  
   [out] ISymUnmanagedNamespace  **pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6d8fc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d8fc-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="6d8fc-106">[out] Un pointeur qui est défini à le [ISymUnmanagedNamespace](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="6d8fc-106">[out] A pointer that is set to the returned [ISymUnmanagedNamespace](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagednamespace-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6d8fc-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6d8fc-107">Return Value</span></span>  
 <span data-ttu-id="6d8fc-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="6d8fc-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d8fc-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6d8fc-109">Requirements</span></span>  
 <span data-ttu-id="6d8fc-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="6d8fc-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d8fc-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d8fc-111">See Also</span></span>  
 [<span data-ttu-id="6d8fc-112">ISymUnmanagedMethod, interface</span><span class="sxs-lookup"><span data-stu-id="6d8fc-112">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
