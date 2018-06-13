---
title: ISymUnmanagedAsyncMethod::IsAsyncMethod, méthode
ms.date: 03/30/2017
ms.assetid: 670a7653-dac6-4171-98ee-d669e3adf4b2
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3f5bf8252986ffa90ea5380d5342595cb91e5419
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424939"
---
# <a name="isymunmanagedasyncmethodisasyncmethod-method"></a><span data-ttu-id="3b57f-102">ISymUnmanagedAsyncMethod::IsAsyncMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="3b57f-102">ISymUnmanagedAsyncMethod::IsAsyncMethod Method</span></span>
<span data-ttu-id="3b57f-103">Vérifie si la méthode async informations ou non.</span><span class="sxs-lookup"><span data-stu-id="3b57f-103">Checks if the method has async information or not.</span></span>  
  
 <span data-ttu-id="3b57f-104">Si cette méthode retourne `FALSE` , il est interdit d’appeler d’autres méthodes dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="3b57f-104">If this method returns `FALSE` then it is invalid to call any other methods in this interface.</span></span> <span data-ttu-id="3b57f-105">Ils seront retournent tous les `E_UNEXPECTED` dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="3b57f-105">They will all return `E_UNEXPECTED` in this case.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b57f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b57f-106">Syntax</span></span>  
  
```idl  
HRESULT IsAsyncMethod(    [out, retval] BOOL* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3b57f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b57f-107">Parameters</span></span>  
  
|<span data-ttu-id="3b57f-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3b57f-108">Parameter</span></span>|<span data-ttu-id="3b57f-109">Description</span><span class="sxs-lookup"><span data-stu-id="3b57f-109">Description</span></span>|  
|---------------|-----------------|  
|`pRetVal`||  
  
## <a name="return-value"></a><span data-ttu-id="3b57f-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3b57f-110">Return Value</span></span>  
 <span data-ttu-id="3b57f-111">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="3b57f-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b57f-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b57f-112">Requirements</span></span>  
 <span data-ttu-id="3b57f-113">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="3b57f-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b57f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b57f-114">See Also</span></span>  
 [<span data-ttu-id="3b57f-115">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="3b57f-115">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
