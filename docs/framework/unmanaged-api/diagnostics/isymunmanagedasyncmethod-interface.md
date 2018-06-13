---
title: ISymUnmanagedAsyncMethod, interface
ms.date: 03/30/2017
ms.assetid: f2de5224-fd91-45de-9e58-bc600c6d22f1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cefad27d8b9314b45dec6100e35a54990fb591c2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427997"
---
# <a name="isymunmanagedasyncmethod-interface"></a><span data-ttu-id="f8dee-102">ISymUnmanagedAsyncMethod, interface</span><span class="sxs-lookup"><span data-stu-id="f8dee-102">ISymUnmanagedAsyncMethod Interface</span></span>
<span data-ttu-id="f8dee-103">Cette interface est le complément de la lecture à [isymunmanagedasyncmethodpropertieswriter, Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f8dee-103">This interface is the reading complement to [ISymUnmanagedAsyncMethodPropertiesWriter Interface](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f8dee-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8dee-104">Syntax</span></span>  
  
```idl  
[object,uuid(B20D55B3-532E-4906-87E7-25BD5734ABD2),pointer_default(unique)]interface ISymUnmanagedAsyncMethod : IUnknown  
```  
  
## <a name="methods"></a><span data-ttu-id="f8dee-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f8dee-105">Methods</span></span>  
 <span data-ttu-id="f8dee-106">Cette interface contient les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f8dee-106">This interface contains the following methods:</span></span>  
  
|<span data-ttu-id="f8dee-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="f8dee-107">Method</span></span>|<span data-ttu-id="f8dee-108">Description</span><span class="sxs-lookup"><span data-stu-id="f8dee-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="f8dee-109">GetAsyncStepInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="f8dee-109">GetAsyncStepInfo Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-getasyncstepinfo-method.md)|<span data-ttu-id="f8dee-110">Consultez [defineasyncstepinfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8dee-110">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>|  
|[<span data-ttu-id="f8dee-111">GetAsyncStepInfoCount, méthode</span><span class="sxs-lookup"><span data-stu-id="f8dee-111">GetAsyncStepInfoCount Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-getasyncstepinfocount-method.md)|<span data-ttu-id="f8dee-112">Consultez [defineasyncstepinfo, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8dee-112">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>|  
|[<span data-ttu-id="f8dee-113">GetCatchHandlerILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="f8dee-113">GetCatchHandlerILOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-getcatchhandleriloffset-method.md)|<span data-ttu-id="f8dee-114">Consultez [definecatchhandleriloffset, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8dee-114">See [DefineCatchHandlerILOffset Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span></span>|  
|[<span data-ttu-id="f8dee-115">GetKickoffMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="f8dee-115">GetKickoffMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-getkickoffmethod-method.md)|<span data-ttu-id="f8dee-116">Consultez [definekickoffmethod, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8dee-116">See [DefineKickoffMethod Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>|  
|[<span data-ttu-id="f8dee-117">HasCatchHandlerILOffset, méthode</span><span class="sxs-lookup"><span data-stu-id="f8dee-117">HasCatchHandlerILOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-hascatchhandleriloffset-method.md)|<span data-ttu-id="f8dee-118">Consultez [definecatchhandleriloffset, méthode](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8dee-118">See [DefineCatchHandlerILOffset Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-definecatchhandleriloffset-method.md).</span></span>|  
|[<span data-ttu-id="f8dee-119">IsAsyncMethod, méthode</span><span class="sxs-lookup"><span data-stu-id="f8dee-119">IsAsyncMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-isasyncmethod-method.md)|<span data-ttu-id="f8dee-120">Vérifie si la méthode async informations ou non.</span><span class="sxs-lookup"><span data-stu-id="f8dee-120">Checks if the method has async information or not.</span></span><br /><br /> <span data-ttu-id="f8dee-121">Si cette méthode retourne `FALSE` , il est interdit d’appeler d’autres méthodes dans cette interface.</span><span class="sxs-lookup"><span data-stu-id="f8dee-121">If this method returns `FALSE` then it is invalid to call any other methods in this interface.</span></span> <span data-ttu-id="f8dee-122">Ils seront retournent tous les `E_UNEXPECTED` dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="f8dee-122">They will all return `E_UNEXPECTED` in this case.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f8dee-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f8dee-123">Requirements</span></span>  
 <span data-ttu-id="f8dee-124">**En-tête :** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="f8dee-124">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8dee-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8dee-125">See Also</span></span>  
 [<span data-ttu-id="f8dee-126">Interfaces du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="f8dee-126">Diagnostics Symbol Store Interfaces</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-interfaces.md)
