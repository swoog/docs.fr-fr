---
title: ISymUnmanagedENCUpdate::UpdateMethodLines, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.UpdateMethodLines
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::UpdateMethodLines
helpviewer_keywords:
- UpdateMethodLines method [.NET Framework debugging]
- ISymUnmanagedENCUpdate::UpdateMethodLines method [.NET Framework debugging]
ms.assetid: 275ef87b-0b53-49f9-af6b-58506335dc06
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 226d9aa75d0a9e4d6cef92e2d2edacb6e98cf34e
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57473055"
---
# <a name="isymunmanagedencupdateupdatemethodlines-method"></a><span data-ttu-id="12aab-102">ISymUnmanagedENCUpdate::UpdateMethodLines, méthode</span><span class="sxs-lookup"><span data-stu-id="12aab-102">ISymUnmanagedENCUpdate::UpdateMethodLines Method</span></span>
<span data-ttu-id="12aab-103">Permet la mise à jour les informations de ligne pour une méthode qui n’a pas été compilé, mais dont les lignes ont été déplacées indépendamment.</span><span class="sxs-lookup"><span data-stu-id="12aab-103">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="12aab-104">Un delta pour chaque instruction est autorisé.</span><span class="sxs-lookup"><span data-stu-id="12aab-104">A delta for each statement is allowed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12aab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12aab-105">Syntax</span></span>  
  
```  
HRESULT UpdateMethodLines(  
    [in]  mdMethodDef  mdMethodToken,  
    [in, size_is(cDeltas)] INT32*  pDeltas,  
    [in]  ULONG        cDeltas);  
```  
  
## <a name="parameters"></a><span data-ttu-id="12aab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12aab-106">Parameters</span></span>  
 `mdMethodToken`  
 <span data-ttu-id="12aab-107">[in] Les métadonnées du jeton de méthode.</span><span class="sxs-lookup"><span data-stu-id="12aab-107">[in] The metadata of the method token.</span></span>  
  
 `pDeltas`  
 <span data-ttu-id="12aab-108">[in] Un tableau de `INT32` les valeurs qui indiquent les deltas pour chaque point de séquence dans la méthode.</span><span class="sxs-lookup"><span data-stu-id="12aab-108">[in] An array of `INT32` values that indicates deltas for each sequence point in the method.</span></span>  
  
 `cDeltas`  
 <span data-ttu-id="12aab-109">[in] Un `ULONG` contenant la taille de la `pDeltas` paramètre.</span><span class="sxs-lookup"><span data-stu-id="12aab-109">[in] A `ULONG` containing the size of the `pDeltas` parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="12aab-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="12aab-110">Return Value</span></span>  
 <span data-ttu-id="12aab-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="12aab-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="12aab-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="12aab-112">Requirements</span></span>  
 <span data-ttu-id="12aab-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="12aab-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12aab-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12aab-114">See also</span></span>
- [<span data-ttu-id="12aab-115">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="12aab-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
