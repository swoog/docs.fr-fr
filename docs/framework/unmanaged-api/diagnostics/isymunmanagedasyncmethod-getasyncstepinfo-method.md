---
title: ISymUnmanagedAsyncMethod::GetAsyncStepInfo, méthode
ms.date: 03/30/2017
ms.assetid: 3ef5b4b8-4ac7-4906-849b-f932c5e3db07
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3f7c72d0766580f9aa3aa678aacd872b804172a8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940216"
---
# <a name="isymunmanagedasyncmethodgetasyncstepinfo-method"></a><span data-ttu-id="ecee6-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="ecee6-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo Method</span></span>
<span data-ttu-id="ecee6-103">Consultez [defineasyncstepinfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="ecee6-103">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ecee6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ecee6-104">Syntax</span></span>  
  
```idl  
HRESULT GetAsyncStepInfo(    [in] ULONG32 cStepInfo,    [out] ULONG32 *pcStepInfo,    [in, size_is(cStepInfo)] ULONG32 yieldOffsets[],    [in, size_is(cStepInfo)] ULONG32 breakpointOffset[],    [in, size_is(cStepInfo)] mdToken breakpointMethod[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ecee6-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ecee6-105">Parameters</span></span>  
  
|<span data-ttu-id="ecee6-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ecee6-106">Parameter</span></span>|<span data-ttu-id="ecee6-107">Description</span><span class="sxs-lookup"><span data-stu-id="ecee6-107">Description</span></span>|  
|---------------|-----------------|  
|`cStepInfo`||  
|`pcStepInfo`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="ecee6-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ecee6-108">Return Value</span></span>  
 <span data-ttu-id="ecee6-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="ecee6-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ecee6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecee6-110">Requirements</span></span>  
 <span data-ttu-id="ecee6-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ecee6-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ecee6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecee6-112">See also</span></span>

- [<span data-ttu-id="ecee6-113">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="ecee6-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
