---
title: ISymUnmanagedWriter5::OpenMapTokensToSourceSpans, méthode
ms.date: 03/30/2017
ms.assetid: 93ad2517-b0dc-464c-8688-a58a30eda18d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 82dc2ced988f7277c994eb9449e7c26efa5450b7
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59222677"
---
# <a name="isymunmanagedwriter5openmaptokenstosourcespans-method"></a><span data-ttu-id="ae409-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans, méthode</span><span class="sxs-lookup"><span data-stu-id="ae409-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans Method</span></span>
<span data-ttu-id="ae409-103">Ouvrez une section spéciale de données personnalisées pour émettre des informations de mappage de l’étendue de source de jeton dans.</span><span class="sxs-lookup"><span data-stu-id="ae409-103">Open a special custom data section to emit token-to-source span mapping information into.</span></span> <span data-ttu-id="ae409-104">Ouverture de cette section quand une méthode est déjà ouverte, ou vice versa, est une erreur.</span><span class="sxs-lookup"><span data-stu-id="ae409-104">Opening this section when a method is already open, or vice versa, is an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae409-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae409-105">Syntax</span></span>  
  
```idl  
HRESULT OpenMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="ae409-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ae409-106">Return Value</span></span>  
 <span data-ttu-id="ae409-107">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="ae409-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae409-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae409-108">Requirements</span></span>  
 <span data-ttu-id="ae409-109">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ae409-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae409-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae409-110">See also</span></span>

- [<span data-ttu-id="ae409-111">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="ae409-111">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
