---
title: ISymUnmanagedAsyncMethod::IsAsyncMethod, méthode
ms.date: 03/30/2017
ms.assetid: 670a7653-dac6-4171-98ee-d669e3adf4b2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e5cddf34f1a6277e966901c9692bff63e26a3b8e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59136732"
---
# <a name="isymunmanagedasyncmethodisasyncmethod-method"></a><span data-ttu-id="590e5-102">ISymUnmanagedAsyncMethod::IsAsyncMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="590e5-102">ISymUnmanagedAsyncMethod::IsAsyncMethod Method</span></span>
<span data-ttu-id="590e5-103">Vérifie si la méthode async informations ou pas.</span><span class="sxs-lookup"><span data-stu-id="590e5-103">Checks if the method has async information or not.</span></span>  
  
 <span data-ttu-id="590e5-104">Si cette méthode retourne `FALSE` , il est impossible d’appeler toutes les autres méthodes dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="590e5-104">If this method returns `FALSE` then it is invalid to call any other methods in this interface.</span></span> <span data-ttu-id="590e5-105">Il s’agit de retour de tous les `E_UNEXPECTED` dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="590e5-105">They will all return `E_UNEXPECTED` in this case.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="590e5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="590e5-106">Syntax</span></span>  
  
```idl  
HRESULT IsAsyncMethod(    [out, retval] BOOL* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="590e5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="590e5-107">Parameters</span></span>  
  
|<span data-ttu-id="590e5-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="590e5-108">Parameter</span></span>|<span data-ttu-id="590e5-109">Description</span><span class="sxs-lookup"><span data-stu-id="590e5-109">Description</span></span>|  
|---------------|-----------------|  
|`pRetVal`||  
  
## <a name="return-value"></a><span data-ttu-id="590e5-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="590e5-110">Return Value</span></span>  
 <span data-ttu-id="590e5-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="590e5-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="590e5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="590e5-112">Requirements</span></span>  
 <span data-ttu-id="590e5-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="590e5-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="590e5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="590e5-114">See also</span></span>

- [<span data-ttu-id="590e5-115">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="590e5-115">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
