---
title: ISymUnmanagedWriter5::CloseMapTokensToSourceSpans, méthode
ms.date: 03/30/2017
ms.assetid: f8a0c0a2-a11d-436c-aa85-bc110215cfd6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6b3dea6b9710f1ee5ccf8c51261f59b2de026f5e
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59127775"
---
# <a name="isymunmanagedwriter5closemaptokenstosourcespans-method"></a><span data-ttu-id="2a46a-102">ISymUnmanagedWriter5::CloseMapTokensToSourceSpans, méthode</span><span class="sxs-lookup"><span data-stu-id="2a46a-102">ISymUnmanagedWriter5::CloseMapTokensToSourceSpans Method</span></span>
<span data-ttu-id="2a46a-103">Fermez la section de données personnalisé spécial pour l’étendue de jeton pour source des informations de mappage.</span><span class="sxs-lookup"><span data-stu-id="2a46a-103">Close the special custom data section for token-to-source span mapping information.</span></span> <span data-ttu-id="2a46a-104">Après sa fermeture, aucune information de mappage plus ne peut être ajoutée.</span><span class="sxs-lookup"><span data-stu-id="2a46a-104">After it is closed, no more mapping information can be added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2a46a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a46a-105">Syntax</span></span>  
  
```idl  
HRESULT CloseMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="2a46a-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2a46a-106">Return Value</span></span>  
 <span data-ttu-id="2a46a-107">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="2a46a-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2a46a-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a46a-108">Requirements</span></span>  
 <span data-ttu-id="2a46a-109">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="2a46a-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2a46a-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a46a-110">See also</span></span>

- [<span data-ttu-id="2a46a-111">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="2a46a-111">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
