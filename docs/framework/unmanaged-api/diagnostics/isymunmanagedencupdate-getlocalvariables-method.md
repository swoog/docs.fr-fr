---
title: ISymUnmanagedENCUpdate::GetLocalVariables, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.GetLocalVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariables
helpviewer_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariables method [.NET Framework debugging]
- GetLocalVariables method [.NET Framework debugging]
ms.assetid: 5c8840be-ffea-447f-9c8d-178f1eaf8d06
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a53493d666cb16fcc9b407ca3a46072afa306b97
ms.sourcegitcommit: 35316b768394e56087483cde93f854ba607b63bc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2018
ms.locfileid: "52297554"
---
# <a name="isymunmanagedencupdategetlocalvariables-method"></a><span data-ttu-id="87734-102">ISymUnmanagedENCUpdate::GetLocalVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="87734-102">ISymUnmanagedENCUpdate::GetLocalVariables Method</span></span>
<span data-ttu-id="87734-103">Obtient les variables locales.</span><span class="sxs-lookup"><span data-stu-id="87734-103">Gets the local variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87734-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87734-104">Syntax</span></span>  
  
```  
HRESULT GetLocalVariables(  
    [in]  mdMethodDef  mdMethodToken,  
    [in]  ULONG        cLocals,  
    [out, size_is(cLocals), length_is(*pceltFetched)]  
        ISymUnmanagedVariable *rgLocals[],  
    [out] ULONG        *pceltFetched);  
```  
  
## <a name="parameters"></a><span data-ttu-id="87734-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87734-105">Parameters</span></span>  
 `mdMethodToken`  
 <span data-ttu-id="87734-106">[in] Le jeton de métadonnées de la méthode.</span><span class="sxs-lookup"><span data-stu-id="87734-106">[in] The metadata token of the method.</span></span>  
  
 `cLocals`  
 <span data-ttu-id="87734-107">[in] Un `ULONG` qui indique la taille de la `rgLocals` paramètre.</span><span class="sxs-lookup"><span data-stu-id="87734-107">[in] A `ULONG` that indicates the size of the `rgLocals` parameter.</span></span>  
  
 `rgLocals`  
 <span data-ttu-id="87734-108">[out] Le tableau retourné [ISymUnmanagedVariable](isymunmanagedvariable-interface.md) instances.</span><span class="sxs-lookup"><span data-stu-id="87734-108">[out] The returned array of [ISymUnmanagedVariable](isymunmanagedvariable-interface.md) instances.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="87734-109">[out] Un pointeur vers un `ULONG` qui reçoit la taille de la `rgLocals` tampon nécessaire pour contenir les variables locales.</span><span class="sxs-lookup"><span data-stu-id="87734-109">[out] A pointer to a `ULONG` that receives the size of the `rgLocals` buffer required to contain the locals.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="87734-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="87734-110">Return Value</span></span>  
 <span data-ttu-id="87734-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="87734-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="87734-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87734-112">Requirements</span></span>  
 <span data-ttu-id="87734-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="87734-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="87734-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87734-114">See Also</span></span>  
 [<span data-ttu-id="87734-115">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="87734-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
