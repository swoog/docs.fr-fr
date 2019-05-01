---
title: ISymUnmanagedWriter5::OpenMapTokensToSourceSpans, méthode
ms.date: 03/30/2017
ms.assetid: 93ad2517-b0dc-464c-8688-a58a30eda18d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 82dc2ced988f7277c994eb9449e7c26efa5450b7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61968582"
---
# <a name="isymunmanagedwriter5openmaptokenstosourcespans-method"></a><span data-ttu-id="cdb76-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans, méthode</span><span class="sxs-lookup"><span data-stu-id="cdb76-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans Method</span></span>
<span data-ttu-id="cdb76-103">Ouvrez une section spéciale de données personnalisées pour émettre des informations de mappage de l’étendue de source de jeton dans.</span><span class="sxs-lookup"><span data-stu-id="cdb76-103">Open a special custom data section to emit token-to-source span mapping information into.</span></span> <span data-ttu-id="cdb76-104">Ouverture de cette section quand une méthode est déjà ouverte, ou vice versa, est une erreur.</span><span class="sxs-lookup"><span data-stu-id="cdb76-104">Opening this section when a method is already open, or vice versa, is an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cdb76-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdb76-105">Syntax</span></span>  
  
```idl  
HRESULT OpenMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="cdb76-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cdb76-106">Return Value</span></span>  
 <span data-ttu-id="cdb76-107">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="cdb76-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cdb76-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdb76-108">Requirements</span></span>  
 <span data-ttu-id="cdb76-109">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="cdb76-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdb76-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdb76-110">See also</span></span>

- [<span data-ttu-id="cdb76-111">ISymUnmanagedWriter5, interface</span><span class="sxs-lookup"><span data-stu-id="cdb76-111">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
