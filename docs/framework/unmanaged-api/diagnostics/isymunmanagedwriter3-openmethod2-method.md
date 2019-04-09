---
title: ISymUnmanagedWriter3::OpenMethod2, méthode
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3.OpenMethod2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3::OpenMethod2
helpviewer_keywords:
- ISymUnmanagedWriter3::OpenMethod2 method [.NET Framework debugging]
- OpenMethod2 method [.NET Framework debugging]
ms.assetid: 025e358c-448f-4423-a2f2-57acf437c8a5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a3dcb1327ad50761a8268e8adc7b1e976cae0b3a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59200296"
---
# <a name="isymunmanagedwriter3openmethod2-method"></a><span data-ttu-id="960ba-102">ISymUnmanagedWriter3::OpenMethod2, méthode</span><span class="sxs-lookup"><span data-stu-id="960ba-102">ISymUnmanagedWriter3::OpenMethod2 Method</span></span>
<span data-ttu-id="960ba-103">Ouvre une méthode et fournit son décalage de la section réel dans l’image.</span><span class="sxs-lookup"><span data-stu-id="960ba-103">Opens a method and provides its real section offset in the image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="960ba-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="960ba-104">Syntax</span></span>  
  
```  
HRESULT OpenMethod2(   
    [in] mdMethodDef method,  
    [in] ULONG32 isect,  
    [in] ULONG32 offset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="960ba-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="960ba-105">Parameters</span></span>  
 `method`  
 <span data-ttu-id="960ba-106">[in] Le jeton de métadonnées pour la méthode à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="960ba-106">[in] The metadata token for the method to be opened.</span></span>  
  
 `isect`  
 <span data-ttu-id="960ba-107">[in] Le décalage de la section dans l’image.</span><span class="sxs-lookup"><span data-stu-id="960ba-107">[in] The section offset in the image.</span></span>  
  
 `offset`  
 <span data-ttu-id="960ba-108">[in] Le décalage de l’image.</span><span class="sxs-lookup"><span data-stu-id="960ba-108">[in] The offset in the image.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="960ba-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="960ba-109">Return Value</span></span>  
 <span data-ttu-id="960ba-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="960ba-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="960ba-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="960ba-111">Requirements</span></span>  
 <span data-ttu-id="960ba-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="960ba-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="960ba-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="960ba-113">See also</span></span>

- [<span data-ttu-id="960ba-114">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="960ba-114">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)
- [<span data-ttu-id="960ba-115">OpenMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="960ba-115">OpenMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)
