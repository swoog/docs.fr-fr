---
title: ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReaderSymbolSearchInfo.GetSymbolSearchInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo
helpviewer_keywords:
- GetSymbolSearchInfo method [.NET Framework debugging]
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo method [.NET Framework debugging]
ms.assetid: 40fcdbc5-3bb2-41e9-b995-40984c209a7f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 628d6fac45b046d9e8f26ad8777c38450da27a1d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427416"
---
# <a name="isymunmanagedreadersymbolsearchinfogetsymbolsearchinfo-method"></a><span data-ttu-id="3e4d1-102">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="3e4d1-102">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfo Method</span></span>
<span data-ttu-id="3e4d1-103">Obtient les informations de la recherche de symbole.</span><span class="sxs-lookup"><span data-stu-id="3e4d1-103">Gets symbol search information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e4d1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e4d1-104">Syntax</span></span>  
  
```  
HRESULT GetSymbolSearchInfo(  
    [in]  ULONG32  cSearchInfo,  
    [out] ULONG32  *pcSearchInfo,  
    [out, size_is(cSearchInfo), length_is(*pcSearchInfo)]  
        ISymUnmanagedSymbolSearchInfo **rgpSearchInfo);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3e4d1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e4d1-105">Parameters</span></span>  
 `cSearchInfo`  
 <span data-ttu-id="3e4d1-106">[in] A `ULONG32` qui indique la taille de `rgpSearchInfo`.</span><span class="sxs-lookup"><span data-stu-id="3e4d1-106">[in] A `ULONG32` that indicates the size of `rgpSearchInfo`.</span></span>  
  
 `pcSearchInfo`  
 <span data-ttu-id="3e4d1-107">[out] Un pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les informations de recherche.</span><span class="sxs-lookup"><span data-stu-id="3e4d1-107">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the search information.</span></span>  
  
 `rgpSearchInfo`  
 <span data-ttu-id="3e4d1-108">[out] Un pointeur qui est défini à le [ISymUnmanagedSymbolSearchInfo](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="3e4d1-108">[out] A pointer that is set to the returned [ISymUnmanagedSymbolSearchInfo](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3e4d1-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3e4d1-109">Return Value</span></span>  
 <span data-ttu-id="3e4d1-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3e4d1-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e4d1-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3e4d1-111">Requirements</span></span>  
 <span data-ttu-id="3e4d1-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="3e4d1-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e4d1-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e4d1-113">See Also</span></span>  
 [<span data-ttu-id="3e4d1-114">ISymUnmanagedReaderSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="3e4d1-114">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreadersymbolsearchinfo-interface.md)
