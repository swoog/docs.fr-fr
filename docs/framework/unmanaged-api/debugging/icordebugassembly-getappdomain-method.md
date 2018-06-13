---
title: ICorDebugAssembly::GetAppDomain, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly.GetAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly::GetAppDomain
helpviewer_keywords:
- ICorDebugAssembly::GetAppDomain method [.NET Framework debugging]
- GetAppDomain method, ICorDebugAssembly interface [.NET Framework debugging]
ms.assetid: 14e18510-23ac-4cba-9f96-c86147a2df9d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e22d112d1414b13033f73723821e5e4b5764e1c8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401977"
---
# <a name="icordebugassemblygetappdomain-method"></a><span data-ttu-id="2bd11-102">ICorDebugAssembly::GetAppDomain, méthode</span><span class="sxs-lookup"><span data-stu-id="2bd11-102">ICorDebugAssembly::GetAppDomain Method</span></span>
<span data-ttu-id="2bd11-103">Obtient un pointeur d’interface vers le domaine d’application qui contient cette `ICorDebugAssembly` instance.</span><span class="sxs-lookup"><span data-stu-id="2bd11-103">Gets an interface pointer to the application domain that contains this `ICorDebugAssembly` instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2bd11-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bd11-104">Syntax</span></span>  
  
```  
HRESULT GetAppDomain (  
    [out] ICorDebugAppDomain  **ppAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2bd11-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bd11-105">Parameters</span></span>  
 `ppAppDomain`  
 <span data-ttu-id="2bd11-106">[out] Pointeur vers l’adresse d’une interface ICorDebugAppDomain qui représente le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="2bd11-106">[out] A pointer to the address of an ICorDebugAppDomain interface that represents the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2bd11-107">Notes</span><span class="sxs-lookup"><span data-stu-id="2bd11-107">Remarks</span></span>  
 <span data-ttu-id="2bd11-108">Si cet assembly est l’assembly système, `GetAppDomain` retourne la valeur null.</span><span class="sxs-lookup"><span data-stu-id="2bd11-108">If this assembly is the system assembly, `GetAppDomain` returns null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2bd11-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2bd11-109">Requirements</span></span>  
 <span data-ttu-id="2bd11-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2bd11-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2bd11-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2bd11-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2bd11-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2bd11-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2bd11-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2bd11-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
