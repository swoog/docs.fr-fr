---
title: ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReaderSymbolSearchInfo.GetSymbolSearchInfoCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount
helpviewer_keywords:
- GetSymbolSearchInfoCount method [.NET Framework debugging]
- ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount method [.NET Framework debugging]
ms.assetid: 4068b6ec-525f-4446-8818-0296178cbd19
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 103444e0b4b17b6384473eac714fba025cee9a55
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426540"
---
# <a name="isymunmanagedreadersymbolsearchinfogetsymbolsearchinfocount-method"></a><span data-ttu-id="158ea-102">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount, méthode</span><span class="sxs-lookup"><span data-stu-id="158ea-102">ISymUnmanagedReaderSymbolSearchInfo::GetSymbolSearchInfoCount Method</span></span>
<span data-ttu-id="158ea-103">Obtient le nombre d’informations de la recherche de symbole.</span><span class="sxs-lookup"><span data-stu-id="158ea-103">Gets a count of symbol search information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="158ea-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="158ea-104">Syntax</span></span>  
  
```  
HRESULT GetSymbolSearchInfoCount(  
    [out] ULONG32 *pcSearchInfo);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="158ea-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="158ea-105">Parameters</span></span>  
 `pcSearchInfo`  
 <span data-ttu-id="158ea-106">[] out] pointeur vers un `ULONG32` qui reçoit la taille de la mémoire tampon requise pour contenir les informations de recherche.</span><span class="sxs-lookup"><span data-stu-id="158ea-106">]out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the search information.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="158ea-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="158ea-107">Return Value</span></span>  
 <span data-ttu-id="158ea-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="158ea-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="158ea-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="158ea-109">Requirements</span></span>  
 <span data-ttu-id="158ea-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="158ea-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="158ea-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="158ea-111">See Also</span></span>  
 [<span data-ttu-id="158ea-112">ISymUnmanagedReaderSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="158ea-112">ISymUnmanagedReaderSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreadersymbolsearchinfo-interface.md)
