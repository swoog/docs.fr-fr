---
title: IBindingDisplay::GetCurrentDisplay, méthode
ms.date: 03/30/2017
api_name:
- IBindingDisplay.GetCurrentDisplay
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IBindingDisplay::GetCurrentDisplay
helpviewer_keywords:
- IBindingDisplay::GetCurrentDisplay method [.NET Framework debugging]
- GetCurrentDisplay method [.NET Framework debugging]
ms.assetid: d28eeea4-c4e0-40d4-91de-198d98cfa13c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f8e585942cf6b7e368351fde3181402990201d6c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33426278"
---
# <a name="ibindingdisplaygetcurrentdisplay-method"></a><span data-ttu-id="6015a-102">IBindingDisplay::GetCurrentDisplay, méthode</span><span class="sxs-lookup"><span data-stu-id="6015a-102">IBindingDisplay::GetCurrentDisplay Method</span></span>
<span data-ttu-id="6015a-103">Retourne les informations d’affichage de liaison actuel.</span><span class="sxs-lookup"><span data-stu-id="6015a-103">Returns the current binding display information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6015a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6015a-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentDisplay (  
    [out, retval] SAFEARRAY(struct BindingDisplayTabControl) *display  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6015a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6015a-105">Parameters</span></span>  
 `display`  
 <span data-ttu-id="6015a-106">[out, retval] Pointeur vers un safearray qui contient les informations d’affichage de liaison.</span><span class="sxs-lookup"><span data-stu-id="6015a-106">[out, retval] A pointer to a safearray containing the binding display information.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6015a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6015a-107">Remarks</span></span>  
 <span data-ttu-id="6015a-108">Le [IBindingDisplay::InitializeForProcess](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-initializeforprocess-method.md) méthode doit avoir précédemment réussi et que le programme doit être arrêté par un débogueur.</span><span class="sxs-lookup"><span data-stu-id="6015a-108">The [IBindingDisplay::InitializeForProcess](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-initializeforprocess-method.md) method must have previously succeeded, and the program must be stopped by a debugger.</span></span>  
  
 <span data-ttu-id="6015a-109">L’appelant doit libérer retourné `SAFEARRAY` mémoire à l’aide de [SafeArrayDestroy](http://msdn.microsoft.com/library/fc94f7e7-b903-4c78-905c-54df1f8d13fa).</span><span class="sxs-lookup"><span data-stu-id="6015a-109">The caller must deallocate the returned `SAFEARRAY` memory by using [SafeArrayDestroy](http://msdn.microsoft.com/library/fc94f7e7-b903-4c78-905c-54df1f8d13fa).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6015a-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6015a-110">Requirements</span></span>  
 <span data-ttu-id="6015a-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6015a-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6015a-112">**En-tête :** BindingDisplay.h</span><span class="sxs-lookup"><span data-stu-id="6015a-112">**Header:** BindingDisplay.h</span></span>  
  
 <span data-ttu-id="6015a-113">**Bibliothèque :** BindingDisplay.idl</span><span class="sxs-lookup"><span data-stu-id="6015a-113">**Library:** BindingDisplay.idl</span></span>  
  
 <span data-ttu-id="6015a-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6015a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6015a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6015a-115">See Also</span></span>  
 [<span data-ttu-id="6015a-116">IBindingDisplay, interface</span><span class="sxs-lookup"><span data-stu-id="6015a-116">IBindingDisplay Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-interface.md)  
 [<span data-ttu-id="6015a-117">InitializeForProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="6015a-117">InitializeForProcess Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/ibindingdisplay-initializeforprocess-method.md)
