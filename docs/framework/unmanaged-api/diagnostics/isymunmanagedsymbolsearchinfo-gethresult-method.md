---
title: ISymUnmanagedSymbolSearchInfo::GetHRESULT, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo.GetHRESULT
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetHRESULT
helpviewer_keywords:
- ISymUnmanagedSymbolSearchInfo::GetHRESULT method [.NET Framework debugging]
- GetHRESULT method [.NET Framework debugging]
ms.assetid: 6999dc3d-65d7-4bf6-bb0a-6efc0fc72588
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 15f85a6f5ab418692d747cc9ad415c637d7b96e2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54614364"
---
# <a name="isymunmanagedsymbolsearchinfogethresult-method"></a><span data-ttu-id="50f33-102">ISymUnmanagedSymbolSearchInfo::GetHRESULT, méthode</span><span class="sxs-lookup"><span data-stu-id="50f33-102">ISymUnmanagedSymbolSearchInfo::GetHRESULT Method</span></span>
<span data-ttu-id="50f33-103">Obtient le HRESULT.</span><span class="sxs-lookup"><span data-stu-id="50f33-103">Gets the HRESULT.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50f33-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50f33-104">Syntax</span></span>  
  
```  
HRESULT GetHRESULT(  
    [out] HRESULT *phr);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="50f33-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50f33-105">Parameters</span></span>  
 `phr`  
 <span data-ttu-id="50f33-106">[out] Pointeur vers la valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="50f33-106">[out] A pointer to the HRESULT.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="50f33-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="50f33-107">Return Value</span></span>  
 <span data-ttu-id="50f33-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="50f33-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50f33-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="50f33-109">Requirements</span></span>  
 <span data-ttu-id="50f33-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="50f33-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50f33-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50f33-111">See also</span></span>
- [<span data-ttu-id="50f33-112">ISymUnmanagedSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="50f33-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
