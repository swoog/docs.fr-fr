---
title: ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode
ms.date: 03/30/2017
ms.assetid: d0fbbf61-71c6-4fb1-8c9f-d619ca5d7d68
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 08c219dd033b39fc07159875b184cdf70e3aa3ed
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61937863"
---
# <a name="isymunmanagedwriter5maptokentosourcespan-method"></a><span data-ttu-id="db1f3-102">ISymUnmanagedWriter5::MapTokenToSourceSpan, méthode</span><span class="sxs-lookup"><span data-stu-id="db1f3-102">ISymUnmanagedWriter5::MapTokenToSourceSpan Method</span></span>
<span data-ttu-id="db1f3-103">Cartes s’étendent sur le jeton de métadonnées donné à la ligne source donné dans le fichier source spécifié.</span><span class="sxs-lookup"><span data-stu-id="db1f3-103">Maps the given metadata token to the given source line span in the specified source file.</span></span>  
  
 <span data-ttu-id="db1f3-104">Doit être appelée entre les appels à [openmaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) et [closemaptokenstosourcespans, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span><span class="sxs-lookup"><span data-stu-id="db1f3-104">Must be called between calls to [OpenMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-openmaptokenstosourcespans-method.md) and [CloseMapTokensToSourceSpans Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-closemaptokenstosourcespans-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db1f3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db1f3-105">Syntax</span></span>  
  
```idl  
HRESULT MapTokenToSourceSpan(    [in] mdToken token,    [in] ISymUnmanagedDocumentWriter* document,    [in] ULONG32 line,    [in] ULONG32 column,    [in] ULONG32 endLine,    [in] ULONG32 endColumn);  
```  
  
## <a name="parameters"></a><span data-ttu-id="db1f3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db1f3-106">Parameters</span></span>  
  
|<span data-ttu-id="db1f3-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="db1f3-107">Parameter</span></span>|<span data-ttu-id="db1f3-108">Description</span><span class="sxs-lookup"><span data-stu-id="db1f3-108">Description</span></span>|  
|---------------|-----------------|  
|`token`||  
|`document`||  
|`line`||  
|`column`||  
|`endLine`||  
|`endColumn`||  
  
## <a name="return-value"></a><span data-ttu-id="db1f3-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="db1f3-109">Return Value</span></span>  
 <span data-ttu-id="db1f3-110">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="db1f3-110">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="db1f3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db1f3-111">Requirements</span></span>  
 <span data-ttu-id="db1f3-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="db1f3-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db1f3-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db1f3-113">See also</span></span>

- [<span data-ttu-id="db1f3-114">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="db1f3-114">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
