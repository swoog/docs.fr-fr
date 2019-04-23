---
title: ISymUnmanagedSymbolSearchInfo::GetSearchPath, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo.GetSearchPath
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetSearchPath
helpviewer_keywords:
- GetSearchPath method [.NET Framework debugging]
- ISymUnmanagedSymbolSearchInfo::GetSearchPath method [.NET Framework debugging]
ms.assetid: b588d470-53c2-4492-be8c-957323eaca0b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 649f44bd7966b9ca89d2d040b7eede662404aa0f
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59093551"
---
# <a name="isymunmanagedsymbolsearchinfogetsearchpath-method"></a><span data-ttu-id="e6a2f-102">ISymUnmanagedSymbolSearchInfo::GetSearchPath, méthode</span><span class="sxs-lookup"><span data-stu-id="e6a2f-102">ISymUnmanagedSymbolSearchInfo::GetSearchPath Method</span></span>
<span data-ttu-id="e6a2f-103">Obtient le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="e6a2f-103">Gets the search path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6a2f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6a2f-104">Syntax</span></span>  
  
```  
HRESULT GetSearchPathLength(  
    [out] ULONG32 *pcchPath);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6a2f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6a2f-105">Parameters</span></span>  
 `pcchPath`  
 <span data-ttu-id="e6a2f-106">[out] Un pointeur vers un `ULONG32` qui reçoit la taille, en caractères, de la mémoire tampon requise pour contenir le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="e6a2f-106">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the search path.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e6a2f-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e6a2f-107">Return Value</span></span>  
 <span data-ttu-id="e6a2f-108">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e6a2f-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6a2f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6a2f-109">Requirements</span></span>  
 <span data-ttu-id="e6a2f-110">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="e6a2f-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6a2f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6a2f-111">See also</span></span>

- [<span data-ttu-id="e6a2f-112">ISymUnmanagedSymbolSearchInfo, interface</span><span class="sxs-lookup"><span data-stu-id="e6a2f-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
