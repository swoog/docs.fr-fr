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
ms.openlocfilehash: 643666df9f93d1aa5e09579359ae0db87908f10b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33428331"
---
# <a name="isymunmanagedwriter3openmethod2-method"></a><span data-ttu-id="32b5b-102">ISymUnmanagedWriter3::OpenMethod2, méthode</span><span class="sxs-lookup"><span data-stu-id="32b5b-102">ISymUnmanagedWriter3::OpenMethod2 Method</span></span>
<span data-ttu-id="32b5b-103">Ouvre une méthode et fournit sa vraie section compensée dans l’image.</span><span class="sxs-lookup"><span data-stu-id="32b5b-103">Opens a method and provides its real section offset in the image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32b5b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32b5b-104">Syntax</span></span>  
  
```  
HRESULT OpenMethod2(   
    [in] mdMethodDef method,  
    [in] ULONG32 isect,  
    [in] ULONG32 offset);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="32b5b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32b5b-105">Parameters</span></span>  
 `method`  
 <span data-ttu-id="32b5b-106">[in] Le jeton de métadonnées pour la méthode à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="32b5b-106">[in] The metadata token for the method to be opened.</span></span>  
  
 `isect`  
 <span data-ttu-id="32b5b-107">[in] Le décalage de la section dans l’image.</span><span class="sxs-lookup"><span data-stu-id="32b5b-107">[in] The section offset in the image.</span></span>  
  
 `offset`  
 <span data-ttu-id="32b5b-108">[in] Le décalage de l’image.</span><span class="sxs-lookup"><span data-stu-id="32b5b-108">[in] The offset in the image.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="32b5b-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="32b5b-109">Return Value</span></span>  
 <span data-ttu-id="32b5b-110">S_OK si la méthode réussit ; Sinon, E_FAIL ou un autre code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="32b5b-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="32b5b-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="32b5b-111">Requirements</span></span>  
 <span data-ttu-id="32b5b-112">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="32b5b-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32b5b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32b5b-113">See Also</span></span>  
 [<span data-ttu-id="32b5b-114">ISymUnmanagedWriter3, interface</span><span class="sxs-lookup"><span data-stu-id="32b5b-114">ISymUnmanagedWriter3 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter3-interface.md)  
 [<span data-ttu-id="32b5b-115">OpenMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="32b5b-115">OpenMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)
