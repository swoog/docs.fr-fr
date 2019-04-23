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
ms.openlocfilehash: 16e91a0c748e5b148e79dc73cf213b03c68c5021
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59103751"
---
# <a name="isymunmanagedencupdategetlocalvariables-method"></a><span data-ttu-id="05cda-102">ISymUnmanagedENCUpdate::GetLocalVariables, méthode</span><span class="sxs-lookup"><span data-stu-id="05cda-102">ISymUnmanagedENCUpdate::GetLocalVariables Method</span></span>
<span data-ttu-id="05cda-103">Obtient les variables locales.</span><span class="sxs-lookup"><span data-stu-id="05cda-103">Gets the local variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05cda-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05cda-104">Syntax</span></span>  
  
```  
HRESULT GetLocalVariables(  
    [in]  mdMethodDef  mdMethodToken,  
    [in]  ULONG        cLocals,  
    [out, size_is(cLocals), length_is(*pceltFetched)]  
        ISymUnmanagedVariable *rgLocals[],  
    [out] ULONG        *pceltFetched);  
```  
  
## <a name="parameters"></a><span data-ttu-id="05cda-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05cda-105">Parameters</span></span>  
 `mdMethodToken`  
 <span data-ttu-id="05cda-106">[in] Le jeton de métadonnées de la méthode.</span><span class="sxs-lookup"><span data-stu-id="05cda-106">[in] The metadata token of the method.</span></span>  
  
 `cLocals`  
 <span data-ttu-id="05cda-107">[in] Un `ULONG` qui indique la taille de la `rgLocals` paramètre.</span><span class="sxs-lookup"><span data-stu-id="05cda-107">[in] A `ULONG` that indicates the size of the `rgLocals` parameter.</span></span>  
  
 `rgLocals`  
 <span data-ttu-id="05cda-108">[out] Le tableau retourné [ISymUnmanagedVariable](isymunmanagedvariable-interface.md) instances.</span><span class="sxs-lookup"><span data-stu-id="05cda-108">[out] The returned array of [ISymUnmanagedVariable](isymunmanagedvariable-interface.md) instances.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="05cda-109">[out] Un pointeur vers un `ULONG` qui reçoit la taille de la `rgLocals` tampon nécessaire pour contenir les variables locales.</span><span class="sxs-lookup"><span data-stu-id="05cda-109">[out] A pointer to a `ULONG` that receives the size of the `rgLocals` buffer required to contain the locals.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="05cda-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="05cda-110">Return Value</span></span>  
 <span data-ttu-id="05cda-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="05cda-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05cda-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05cda-112">Requirements</span></span>  
 <span data-ttu-id="05cda-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="05cda-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05cda-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05cda-114">See also</span></span>

- [<span data-ttu-id="05cda-115">ISymUnmanagedENCUpdate, interface</span><span class="sxs-lookup"><span data-stu-id="05cda-115">ISymUnmanagedENCUpdate Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedencupdate-interface.md)
