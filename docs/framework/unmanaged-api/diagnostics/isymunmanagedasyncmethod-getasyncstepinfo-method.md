---
title: ISymUnmanagedAsyncMethod::GetAsyncStepInfo, méthode
ms.date: 03/30/2017
ms.assetid: 3ef5b4b8-4ac7-4906-849b-f932c5e3db07
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a26ff1e0b1bb4d0de662f0186dc2f7958b9707f2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33425377"
---
# <a name="isymunmanagedasyncmethodgetasyncstepinfo-method"></a><span data-ttu-id="bc4f0-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="bc4f0-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfo Method</span></span>
<span data-ttu-id="bc4f0-103">Consultez [defineasyncstepinfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="bc4f0-103">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc4f0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc4f0-104">Syntax</span></span>  
  
```idl  
HRESULT GetAsyncStepInfo(    [in] ULONG32 cStepInfo,    [out] ULONG32 *pcStepInfo,    [in, size_is(cStepInfo)] ULONG32 yieldOffsets[],    [in, size_is(cStepInfo)] ULONG32 breakpointOffset[],    [in, size_is(cStepInfo)] mdToken breakpointMethod[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bc4f0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc4f0-105">Parameters</span></span>  
  
|<span data-ttu-id="bc4f0-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="bc4f0-106">Parameter</span></span>|<span data-ttu-id="bc4f0-107">Description</span><span class="sxs-lookup"><span data-stu-id="bc4f0-107">Description</span></span>|  
|---------------|-----------------|  
|`cStepInfo`||  
|`pcStepInfo`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="bc4f0-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bc4f0-108">Return Value</span></span>  
 <span data-ttu-id="bc4f0-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="bc4f0-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bc4f0-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bc4f0-110">Requirements</span></span>  
 <span data-ttu-id="bc4f0-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="bc4f0-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc4f0-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc4f0-112">See Also</span></span>  
 [<span data-ttu-id="bc4f0-113">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="bc4f0-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
