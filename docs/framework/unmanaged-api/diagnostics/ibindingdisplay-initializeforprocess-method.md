---
title: IBindingDisplay::InitializeForProcess, méthode
ms.date: 03/30/2017
api_name:
- IBindingDisplay.InitializeForProcess
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IBindingDisplay::InitializeForProcess
helpviewer_keywords:
- IBindingDisplay::InitializeForProcess method [.NET Framework debugging]
- InitializeForProcess method [.NET Framework debugging]
ms.assetid: 59417acb-4e59-46ad-acfe-d827e6ab6078
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: aabad159b521207fed976636ae8b9e338f09ac42
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57466178"
---
# <a name="ibindingdisplayinitializeforprocess-method"></a><span data-ttu-id="748a1-102">IBindingDisplay::InitializeForProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="748a1-102">IBindingDisplay::InitializeForProcess Method</span></span>
<span data-ttu-id="748a1-103">Initialise le [IBindingDisplay](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="748a1-103">Initializes the [IBindingDisplay](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="748a1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="748a1-104">Syntax</span></span>  
  
```  
HRESULT InitializeForProcess (  
    [in] ULONG32   pid  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="748a1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="748a1-105">Parameters</span></span>  
 `pid`  
 <span data-ttu-id="748a1-106">[in] L’identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="748a1-106">[in] The process identifier.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="748a1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="748a1-107">Remarks</span></span>  
 <span data-ttu-id="748a1-108">Le débogueur appelle la `InitializeForProcess` méthode au moment de la création pour initialiser l’affichage de la liaison.</span><span class="sxs-lookup"><span data-stu-id="748a1-108">The debugger calls the `InitializeForProcess` method at creation time to initialize the binding display.</span></span> <span data-ttu-id="748a1-109">`InitializeForProcess` doit être appelée au moment de la création avant toute autre méthode sur `IBindingDisplay` est appelée.</span><span class="sxs-lookup"><span data-stu-id="748a1-109">`InitializeForProcess` must be called at creation time before any other method on `IBindingDisplay` is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="748a1-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="748a1-110">Requirements</span></span>  
 <span data-ttu-id="748a1-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="748a1-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="748a1-112">**En-tête :** BindingDisplay.h</span><span class="sxs-lookup"><span data-stu-id="748a1-112">**Header:** BindingDisplay.h</span></span>  
  
 <span data-ttu-id="748a1-113">**Bibliothèque :** BindingDisplay.idl</span><span class="sxs-lookup"><span data-stu-id="748a1-113">**Library:** BindingDisplay.idl</span></span>  
  
 <span data-ttu-id="748a1-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="748a1-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="748a1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="748a1-115">See also</span></span>
- [<span data-ttu-id="748a1-116">IBindingDisplay, interface</span><span class="sxs-lookup"><span data-stu-id="748a1-116">IBindingDisplay Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md)
