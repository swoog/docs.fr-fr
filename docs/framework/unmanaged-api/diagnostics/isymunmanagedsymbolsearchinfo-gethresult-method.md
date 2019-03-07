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
ms.openlocfilehash: dd24289f7e670684effa553f930af9aec92e5730
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57469598"
---
# <a name="isymunmanagedsymbolsearchinfogethresult-method"></a><span data-ttu-id="47cf4-102">ISymUnmanagedSymbolSearchInfo::GetHRESULT, méthode</span><span class="sxs-lookup"><span data-stu-id="47cf4-102">ISymUnmanagedSymbolSearchInfo::GetHRESULT Method</span></span>
<span data-ttu-id="47cf4-103">Obtient le HRESULT.</span><span class="sxs-lookup"><span data-stu-id="47cf4-103">Gets the HRESULT.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47cf4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47cf4-104">Syntax</span></span>  
  
```  
HRESULT GetHRESULT(  
    [out] HRESULT *phr);  
```  
  
## <a name="parameters"></a><span data-ttu-id="47cf4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47cf4-105">Parameters</span></span>  
 `phr`  
 <span data-ttu-id="47cf4-106">[out] Pointeur vers la valeur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="47cf4-106">[out] A pointer to the HRESULT.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="47cf4-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="47cf4-107">Return Value</span></span>  
 <span data-ttu-id="47cf4-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="47cf4-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="47cf4-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="47cf4-109">Requirements</span></span>  
 <span data-ttu-id="47cf4-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="47cf4-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47cf4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47cf4-111">See also</span></span>
- [<span data-ttu-id="47cf4-112">ISymUnmanagedSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="47cf4-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
