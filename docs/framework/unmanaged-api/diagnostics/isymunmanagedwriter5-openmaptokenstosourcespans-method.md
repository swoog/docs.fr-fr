---
title: ISymUnmanagedWriter5::OpenMapTokensToSourceSpans, méthode
ms.date: 03/30/2017
ms.assetid: 93ad2517-b0dc-464c-8688-a58a30eda18d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d3bc8b00b568f96cd55b7811f310d34c1ff700d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33428646"
---
# <a name="isymunmanagedwriter5openmaptokenstosourcespans-method"></a><span data-ttu-id="2ccfe-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans, méthode</span><span class="sxs-lookup"><span data-stu-id="2ccfe-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans Method</span></span>
<span data-ttu-id="2ccfe-103">Ouvrez une section spéciale de données personnalisé pour émettre des informations de mappage de span à source de jeton dans.</span><span class="sxs-lookup"><span data-stu-id="2ccfe-103">Open a special custom data section to emit token-to-source span mapping information into.</span></span> <span data-ttu-id="2ccfe-104">Ouverture de cette section lorsqu’une méthode est déjà ouverte, ou vice versa, est une erreur.</span><span class="sxs-lookup"><span data-stu-id="2ccfe-104">Opening this section when a method is already open, or vice versa, is an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2ccfe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ccfe-105">Syntax</span></span>  
  
```idl  
HRESULT OpenMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="2ccfe-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2ccfe-106">Return Value</span></span>  
 <span data-ttu-id="2ccfe-107">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="2ccfe-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2ccfe-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2ccfe-108">Requirements</span></span>  
 <span data-ttu-id="2ccfe-109">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2ccfe-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ccfe-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ccfe-110">See Also</span></span>  
 [<span data-ttu-id="2ccfe-111">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="2ccfe-111">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
