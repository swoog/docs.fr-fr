---
title: ISymUnmanagedAsyncMethod::GetAsyncStepInfo, méthode
ms.date: 03/30/2017
ms.assetid: 3ef5b4b8-4ac7-4906-849b-f932c5e3db07
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fa87188765450e84fc2417be8530ff43c88c237c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54666226"
---
# <a name="isymunmanagedasyncmethodgetasyncstepinfo-method"></a><span data-ttu-id="fe84e-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="fe84e-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo Method</span></span>
<span data-ttu-id="fe84e-103">Consultez [defineasyncstepinfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="fe84e-103">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe84e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe84e-104">Syntax</span></span>  
  
```idl  
HRESULT GetAsyncStepInfo(    [in] ULONG32 cStepInfo,    [out] ULONG32 *pcStepInfo,    [in, size_is(cStepInfo)] ULONG32 yieldOffsets[],    [in, size_is(cStepInfo)] ULONG32 breakpointOffset[],    [in, size_is(cStepInfo)] mdToken breakpointMethod[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fe84e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe84e-105">Parameters</span></span>  
  
|<span data-ttu-id="fe84e-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="fe84e-106">Parameter</span></span>|<span data-ttu-id="fe84e-107">Description</span><span class="sxs-lookup"><span data-stu-id="fe84e-107">Description</span></span>|  
|---------------|-----------------|  
|`cStepInfo`||  
|`pcStepInfo`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="fe84e-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fe84e-108">Return Value</span></span>  
 <span data-ttu-id="fe84e-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="fe84e-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe84e-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe84e-110">Requirements</span></span>  
 <span data-ttu-id="fe84e-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fe84e-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe84e-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe84e-112">See also</span></span>
- [<span data-ttu-id="fe84e-113">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="fe84e-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
