---
title: ISymUnmanagedReader2::GetMethodByVersionPreRemap, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2.GetMethodByVersionPreRemap
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2::GetMethodByVersionPreRemap
helpviewer_keywords:
- GetMethodByVersionPreRemap method [.NET Framework debugging]
- ISymUnmanagedReader2::GetMethodByVersionPreRemap method [.NET Framework debugging]
ms.assetid: 0d144ed4-bdb0-4cac-960c-cb90f4dca173
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bcd200b7fa431f193dd202c3c2a690aa22ec8e32
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59135177"
---
# <a name="isymunmanagedreader2getmethodbyversionpreremap-method"></a><span data-ttu-id="9a980-102">ISymUnmanagedReader2::GetMethodByVersionPreRemap, méthode</span><span class="sxs-lookup"><span data-stu-id="9a980-102">ISymUnmanagedReader2::GetMethodByVersionPreRemap Method</span></span>
<span data-ttu-id="9a980-103">Obtient une méthode de lecteur de symboles, étant donné un jeton de méthode et un numéro de version modifier et continuer.</span><span class="sxs-lookup"><span data-stu-id="9a980-103">Gets a symbol reader method, given a method token and an edit-and-continue version number.</span></span> <span data-ttu-id="9a980-104">Numéros de version commencent à 1 et sont incrémentés à chaque fois que la méthode est modifiée suite à une opération modifier et continuer.</span><span class="sxs-lookup"><span data-stu-id="9a980-104">Version numbers start at 1 and are incremented each time the method is changed as a result of an edit-and-continue operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a980-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a980-105">Syntax</span></span>  
  
```  
HRESULT GetMethodByVersionPreRemap(  
    [in]  mdMethodDef token,  
    [in]  int version,  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a980-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a980-106">Parameters</span></span>  
 `token`  
 <span data-ttu-id="9a980-107">[in] Le jeton de métadonnées de méthode.</span><span class="sxs-lookup"><span data-stu-id="9a980-107">[in] The method metadata token.</span></span>  
  
 `version`  
 <span data-ttu-id="9a980-108">[in] La version de la méthode.</span><span class="sxs-lookup"><span data-stu-id="9a980-108">[in] The method version.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="9a980-109">[out] Un pointeur vers le texte retourné [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="9a980-109">[out] A pointer to the returned [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9a980-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9a980-110">Return Value</span></span>  
 <span data-ttu-id="9a980-111">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9a980-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a980-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a980-112">Requirements</span></span>  
 <span data-ttu-id="9a980-113">**En-tête :** CorSym.idl.</span><span class="sxs-lookup"><span data-stu-id="9a980-113">**Header:** CorSym.idl.</span></span> <span data-ttu-id="9a980-114">CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9a980-114">CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a980-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a980-115">See also</span></span>

- [<span data-ttu-id="9a980-116">ISymUnmanagedReader2, interface</span><span class="sxs-lookup"><span data-stu-id="9a980-116">ISymUnmanagedReader2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)
