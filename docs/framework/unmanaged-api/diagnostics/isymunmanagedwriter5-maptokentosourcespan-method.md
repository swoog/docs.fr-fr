---
title: ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode
ms.date: 03/30/2017
ms.assetid: d0fbbf61-71c6-4fb1-8c9f-d619ca5d7d68
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cf061de3e75550e33ba67c1d624279b1673c5382
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57465334"
---
# <a name="isymunmanagedwriter5maptokentosourcespan-method"></a><span data-ttu-id="4a389-102">ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode</span><span class="sxs-lookup"><span data-stu-id="4a389-102">ISymUnmanagedWriter5::MapTokenToSourceSpan Method</span></span>
<span data-ttu-id="4a389-103">Cartes s’étendent sur le jeton de métadonnées donné à la ligne source donné dans le fichier source spécifié.</span><span class="sxs-lookup"><span data-stu-id="4a389-103">Maps the given metadata token to the given source line span in the specified source file.</span></span>  
  
 <span data-ttu-id="4a389-104">Doit être appelée entre les appels à [openmaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) et [closemaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span><span class="sxs-lookup"><span data-stu-id="4a389-104">Must be called between calls to [OpenMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) and [CloseMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a389-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a389-105">Syntax</span></span>  
  
```idl  
HRESULT MapTokenToSourceSpan(    [in] mdToken token,    [in] ISymUnmanagedDocumentWriter* document,    [in] ULONG32 line,    [in] ULONG32 column,    [in] ULONG32 endLine,    [in] ULONG32 endColumn);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4a389-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a389-106">Parameters</span></span>  
  
|<span data-ttu-id="4a389-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="4a389-107">Parameter</span></span>|<span data-ttu-id="4a389-108">Description</span><span class="sxs-lookup"><span data-stu-id="4a389-108">Description</span></span>|  
|---------------|-----------------|  
|`token`||  
|`document`||  
|`line`||  
|`column`||  
|`endLine`||  
|`endColumn`||  
  
## <a name="return-value"></a><span data-ttu-id="4a389-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4a389-109">Return Value</span></span>  
 <span data-ttu-id="4a389-110">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="4a389-110">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a389-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4a389-111">Requirements</span></span>  
 <span data-ttu-id="4a389-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="4a389-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a389-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a389-113">See also</span></span>
- [<span data-ttu-id="4a389-114">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="4a389-114">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
