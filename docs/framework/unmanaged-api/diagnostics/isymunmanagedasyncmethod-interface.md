---
title: ISymUnmanagedAsyncMethod, interface
ms.date: 03/30/2017
ms.assetid: f2de5224-fd91-45de-9e58-bc600c6d22f1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3dd7b351de8e82f9fdbe623505f86b54f6eba68d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54694865"
---
# <a name="isymunmanagedasyncmethod-interface"></a><span data-ttu-id="6a454-102">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="6a454-102">ISymUnmanagedAsyncMethod Interface</span></span>
<span data-ttu-id="6a454-103">Cette interface est le complément de lecture de [isymunmanagedasyncmethodpropertieswriter, Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).</span><span class="sxs-lookup"><span data-stu-id="6a454-103">This interface is the reading complement to [ISymUnmanagedAsyncMethodPropertiesWriter Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a454-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a454-104">Syntax</span></span>  
  
```idl  
[object,uuid(B20D55B3-532E-4906-87E7-25BD5734ABD2),pointer_default(unique)]interface ISymUnmanagedAsyncMethod : IUnknown  
```  
  
## <a name="methods"></a><span data-ttu-id="6a454-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6a454-105">Methods</span></span>  
 <span data-ttu-id="6a454-106">Cette interface contient les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="6a454-106">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="6a454-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="6a454-107">Method</span></span>|<span data-ttu-id="6a454-108">Description</span><span class="sxs-lookup"><span data-stu-id="6a454-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6a454-109">GetAsyncStepInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="6a454-109">GetAsyncStepInfo Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-getasyncstepinfo-method.md)|<span data-ttu-id="6a454-110">Consultez [defineasyncstepinfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a454-110">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>|  
|[<span data-ttu-id="6a454-111">GetAsyncStepInfoCount, méthode</span><span class="sxs-lookup"><span data-stu-id="6a454-111">GetAsyncStepInfoCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-getasyncstepinfocount-method.md)|<span data-ttu-id="6a454-112">Consultez [defineasyncstepinfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a454-112">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>|  
|[<span data-ttu-id="6a454-113">GetCatchHandlerILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="6a454-113">GetCatchHandlerILOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-getcatchhandleriloffset-method.md)|<span data-ttu-id="6a454-114">Consultez [definecatchhandleriloffset, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a454-114">See [DefineCatchHandlerILOffset Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span></span>|  
|[<span data-ttu-id="6a454-115">GetKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="6a454-115">GetKickoffMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-getkickoffmethod-method.md)|<span data-ttu-id="6a454-116">Consultez [definekickoffmethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a454-116">See [DefineKickoffMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>|  
|[<span data-ttu-id="6a454-117">HasCatchHandlerILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="6a454-117">HasCatchHandlerILOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-hascatchhandleriloffset-method.md)|<span data-ttu-id="6a454-118">Consultez [definecatchhandleriloffset, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span><span class="sxs-lookup"><span data-stu-id="6a454-118">See [DefineCatchHandlerILOffset Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span></span>|  
|[<span data-ttu-id="6a454-119">IsAsyncMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="6a454-119">IsAsyncMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-isasyncmethod-method.md)|<span data-ttu-id="6a454-120">Vérifie si la méthode async informations ou pas.</span><span class="sxs-lookup"><span data-stu-id="6a454-120">Checks if the method has async information or not.</span></span><br /><br /> <span data-ttu-id="6a454-121">Si cette méthode retourne `FALSE` , il est impossible d’appeler toutes les autres méthodes dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="6a454-121">If this method returns `FALSE` then it is invalid to call any other methods in this interface.</span></span> <span data-ttu-id="6a454-122">Il s’agit de retour de tous les `E_UNEXPECTED` dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="6a454-122">They will all return `E_UNEXPECTED` in this case.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6a454-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6a454-123">Requirements</span></span>  
 <span data-ttu-id="6a454-124">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="6a454-124">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a454-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a454-125">See also</span></span>
- [<span data-ttu-id="6a454-126">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="6a454-126">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
