---
title: ISymUnmanagedAsyncMethod::GetKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: ba084444-9e68-4cde-9388-54b950670987
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f20039318d6e1230ccc0fbd203fc44686806bb2e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54604468"
---
# <a name="isymunmanagedasyncmethodgetkickoffmethod-method"></a><span data-ttu-id="a89a7-102">ISymUnmanagedAsyncMethod::GetKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="a89a7-102">ISymUnmanagedAsyncMethod::GetKickoffMethod Method</span></span>
<span data-ttu-id="a89a7-103">Consultez [definekickoffmethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="a89a7-103">See [DefineKickoffMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a89a7-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a89a7-104">Syntax</span></span>  
  
```idl  
HRESULT GetKickoffMethod(    [out, retval] mdToken* kickoffMethod);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a89a7-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a89a7-105">Parameters</span></span>  
  
|<span data-ttu-id="a89a7-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a89a7-106">Parameter</span></span>|<span data-ttu-id="a89a7-107">Description</span><span class="sxs-lookup"><span data-stu-id="a89a7-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="a89a7-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a89a7-108">Return Value</span></span>  
 <span data-ttu-id="a89a7-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="a89a7-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a89a7-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a89a7-110">Requirements</span></span>  
 <span data-ttu-id="a89a7-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="a89a7-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a89a7-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a89a7-112">See also</span></span>
- [<span data-ttu-id="a89a7-113">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="a89a7-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
