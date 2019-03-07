---
title: ISymUnmanagedAsyncMethod::GetKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: ba084444-9e68-4cde-9388-54b950670987
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 84aef2b26e008d1a3c6d95d7ec1e130ab0594a11
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57484548"
---
# <a name="isymunmanagedasyncmethodgetkickoffmethod-method"></a><span data-ttu-id="dfa30-102">ISymUnmanagedAsyncMethod::GetKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="dfa30-102">ISymUnmanagedAsyncMethod::GetKickoffMethod Method</span></span>
<span data-ttu-id="dfa30-103">Consultez [definekickoffmethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="dfa30-103">See [DefineKickoffMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dfa30-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfa30-104">Syntax</span></span>  
  
```idl  
HRESULT GetKickoffMethod(    [out, retval] mdToken* kickoffMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dfa30-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfa30-105">Parameters</span></span>  
  
|<span data-ttu-id="dfa30-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="dfa30-106">Parameter</span></span>|<span data-ttu-id="dfa30-107">Description</span><span class="sxs-lookup"><span data-stu-id="dfa30-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="dfa30-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dfa30-108">Return Value</span></span>  
 <span data-ttu-id="dfa30-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="dfa30-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dfa30-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dfa30-110">Requirements</span></span>  
 <span data-ttu-id="dfa30-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="dfa30-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dfa30-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfa30-112">See also</span></span>
- [<span data-ttu-id="dfa30-113">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="dfa30-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
