---
title: ISymUnmanagedWriter5::OpenMapTokensToSourceSpans, méthode
ms.date: 03/30/2017
ms.assetid: 93ad2517-b0dc-464c-8688-a58a30eda18d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 82dc2ced988f7277c994eb9449e7c26efa5450b7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59222677"
---
# <a name="isymunmanagedwriter5openmaptokenstosourcespans-method"></a><span data-ttu-id="fbec4-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans, méthode</span><span class="sxs-lookup"><span data-stu-id="fbec4-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans Method</span></span>
<span data-ttu-id="fbec4-103">Ouvrez une section spéciale de données personnalisées pour émettre des informations de mappage de l’étendue de source de jeton dans.</span><span class="sxs-lookup"><span data-stu-id="fbec4-103">Open a special custom data section to emit token-to-source span mapping information into.</span></span> <span data-ttu-id="fbec4-104">Ouverture de cette section quand une méthode est déjà ouverte, ou vice versa, est une erreur.</span><span class="sxs-lookup"><span data-stu-id="fbec4-104">Opening this section when a method is already open, or vice versa, is an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fbec4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbec4-105">Syntax</span></span>  
  
```idl  
HRESULT OpenMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="fbec4-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fbec4-106">Return Value</span></span>  
 <span data-ttu-id="fbec4-107">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="fbec4-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fbec4-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbec4-108">Requirements</span></span>  
 <span data-ttu-id="fbec4-109">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fbec4-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fbec4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbec4-110">See also</span></span>

- [<span data-ttu-id="fbec4-111">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="fbec4-111">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
