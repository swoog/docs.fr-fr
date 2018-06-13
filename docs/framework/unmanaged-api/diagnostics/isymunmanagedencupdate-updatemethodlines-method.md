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
ms.openlocfilehash: 50d9ac08b01a67df68ff077721ff5421fbc27707
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424272"
---
# <a name="isymunmanagedencupdateupdatemethodlines-method"></a><span data-ttu-id="3e4b8-102">ISymUnmanagedENCUpdate::UpdateMethodLines, méthode</span><span class="sxs-lookup"><span data-stu-id="3e4b8-102">ISymUnmanagedENCUpdate::UpdateMethodLines Method</span></span>
<span data-ttu-id="3e4b8-103">Permet de mettre à jour les informations de ligne pour une méthode qui n’a pas été recompilée, mais dont les lignes ont été déplacées indépendamment.</span><span class="sxs-lookup"><span data-stu-id="3e4b8-103">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="3e4b8-104">Un delta pour chaque instruction est autorisée.</span><span class="sxs-lookup"><span data-stu-id="3e4b8-104">A delta for each statement is allowed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e4b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e4b8-105">Syntax</span></span>  
  
```  
HRESULT UpdateMethodLines(  
    [in]  mdMethodDef  mdMethodToken,  
    [in, size_is(cDeltas)] INT32*  pDeltas,  
    [in]  ULONG        cDeltas);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3e4b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e4b8-106">Parameters</span></span>  
 `mdMethodToken`  
 <span data-ttu-id="3e4b8-107">[in] Les métadonnées du jeton de méthode.</span><span class="sxs-lookup"><span data-stu-id="3e4b8-107">[in] The metadata of the method token.</span></span>  
  
 `pDeltas`  
 <span data-ttu-id="3e4b8-108">[in] Un tableau de `INT32` les valeurs qui indiquent les deltas pour chaque point de séquence dans la méthode.</span><span class="sxs-lookup"><span data-stu-id="3e4b8-108">[in] An array of `INT32` values that indicates deltas for each sequence point in the method.</span></span>  
  
 `cDeltas`  
 <span data-ttu-id="3e4b8-109">[in] A `ULONG` contenant la taille de la `pDeltas` paramètre.</span><span class="sxs-lookup"><span data-stu-id="3e4b8-109">[in] A `ULONG` containing the size of the `pDeltas` parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3e4b8-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3e4b8-110">Return Value</span></span>  
 <span data-ttu-id="3e4b8-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3e4b8-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e4b8-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3e4b8-112">Requirements</span></span>  
 <span data-ttu-id="3e4b8-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="3e4b8-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e4b8-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e4b8-114">See Also</span></span>  
 [<span data-ttu-id="3e4b8-115">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="3e4b8-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
