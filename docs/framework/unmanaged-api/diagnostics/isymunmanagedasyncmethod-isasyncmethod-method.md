---
title: ISymUnmanagedAsyncMethod::IsAsyncMethod, méthode
ms.date: 03/30/2017
ms.assetid: 670a7653-dac6-4171-98ee-d669e3adf4b2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 460d6781405b6042262d50e1aa79ee8c77f781a7
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57489720"
---
# <a name="isymunmanagedasyncmethodisasyncmethod-method"></a><span data-ttu-id="785fe-102">ISymUnmanagedAsyncMethod::IsAsyncMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="785fe-102">ISymUnmanagedAsyncMethod::IsAsyncMethod Method</span></span>
<span data-ttu-id="785fe-103">Vérifie si la méthode async informations ou pas.</span><span class="sxs-lookup"><span data-stu-id="785fe-103">Checks if the method has async information or not.</span></span>  
  
 <span data-ttu-id="785fe-104">Si cette méthode retourne `FALSE` , il est impossible d’appeler toutes les autres méthodes dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="785fe-104">If this method returns `FALSE` then it is invalid to call any other methods in this interface.</span></span> <span data-ttu-id="785fe-105">Il s’agit de retour de tous les `E_UNEXPECTED` dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="785fe-105">They will all return `E_UNEXPECTED` in this case.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="785fe-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="785fe-106">Syntax</span></span>  
  
```idl  
HRESULT IsAsyncMethod(    [out, retval] BOOL* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="785fe-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="785fe-107">Parameters</span></span>  
  
|<span data-ttu-id="785fe-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="785fe-108">Parameter</span></span>|<span data-ttu-id="785fe-109">Description</span><span class="sxs-lookup"><span data-stu-id="785fe-109">Description</span></span>|  
|---------------|-----------------|  
|`pRetVal`||  
  
## <a name="return-value"></a><span data-ttu-id="785fe-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="785fe-110">Return Value</span></span>  
 <span data-ttu-id="785fe-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="785fe-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="785fe-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="785fe-112">Requirements</span></span>  
 <span data-ttu-id="785fe-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="785fe-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="785fe-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="785fe-114">See also</span></span>
- [<span data-ttu-id="785fe-115">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="785fe-115">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
