---
title: ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode
ms.date: 03/30/2017
ms.assetid: d0fbbf61-71c6-4fb1-8c9f-d619ca5d7d68
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 158ff204d57c3b08ced91d397ef71f24c5f44248
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54499208"
---
# <a name="isymunmanagedwriter5maptokentosourcespan-method"></a><span data-ttu-id="bc0e6-102">ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode</span><span class="sxs-lookup"><span data-stu-id="bc0e6-102">ISymUnmanagedWriter5::MapTokenToSourceSpan Method</span></span>
<span data-ttu-id="bc0e6-103">Cartes s’étendent sur le jeton de métadonnées donné à la ligne source donné dans le fichier source spécifié.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-103">Maps the given metadata token to the given source line span in the specified source file.</span></span>  
  
 <span data-ttu-id="bc0e6-104">Doit être appelée entre les appels à [openmaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) et [closemaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span><span class="sxs-lookup"><span data-stu-id="bc0e6-104">Must be called between calls to [OpenMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) and [CloseMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc0e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc0e6-105">Syntax</span></span>  
  
```idl  
HRESULT MapTokenToSourceSpan(    [in] mdToken token,    [in] ISymUnmanagedDocumentWriter* document,    [in] ULONG32 line,    [in] ULONG32 column,    [in] ULONG32 endLine,    [in] ULONG32 endColumn);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bc0e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc0e6-106">Parameters</span></span>  
  
|<span data-ttu-id="bc0e6-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="bc0e6-107">Parameter</span></span>|<span data-ttu-id="bc0e6-108">Description</span><span class="sxs-lookup"><span data-stu-id="bc0e6-108">Description</span></span>|  
|---------------|-----------------|  
|`token`||  
|`document`||  
|`line`||  
|`column`||  
|`endLine`||  
|`endColumn`||  
  
## <a name="return-value"></a><span data-ttu-id="bc0e6-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bc0e6-109">Return Value</span></span>  
 <span data-ttu-id="bc0e6-110">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="bc0e6-110">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bc0e6-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bc0e6-111">Requirements</span></span>  
 <span data-ttu-id="bc0e6-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="bc0e6-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc0e6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc0e6-113">See also</span></span>
- [<span data-ttu-id="bc0e6-114">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="bc0e6-114">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
