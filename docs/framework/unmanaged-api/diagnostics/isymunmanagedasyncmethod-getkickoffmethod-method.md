---
title: ISymUnmanagedAsyncMethod::GetKickoffMethod, méthode
ms.date: 03/30/2017
ms.assetid: ba084444-9e68-4cde-9388-54b950670987
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e2f055dc19bf7f40036283102d8cc4549555b992
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424766"
---
# <a name="isymunmanagedasyncmethodgetkickoffmethod-method"></a><span data-ttu-id="08037-102">ISymUnmanagedAsyncMethod::GetKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="08037-102">ISymUnmanagedAsyncMethod::GetKickoffMethod Method</span></span>
<span data-ttu-id="08037-103">Consultez [definekickoffmethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="08037-103">See [DefineKickoffMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08037-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08037-104">Syntax</span></span>  
  
```idl  
HRESULT GetKickoffMethod(    [out, retval] mdToken* kickoffMethod);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="08037-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08037-105">Parameters</span></span>  
  
|<span data-ttu-id="08037-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="08037-106">Parameter</span></span>|<span data-ttu-id="08037-107">Description</span><span class="sxs-lookup"><span data-stu-id="08037-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="08037-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="08037-108">Return Value</span></span>  
 <span data-ttu-id="08037-109">Retourne `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="08037-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08037-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="08037-110">Requirements</span></span>  
 <span data-ttu-id="08037-111">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="08037-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08037-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08037-112">See Also</span></span>  
 [<span data-ttu-id="08037-113">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="08037-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
