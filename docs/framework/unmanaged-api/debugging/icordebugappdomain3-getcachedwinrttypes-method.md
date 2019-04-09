---
title: ICorDebugAppDomain3::GetCachedWinRTTypes, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain3.GetCachedWinRTTypes
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypes
helpviewer_keywords:
- ICorDebugAppDomain3::GetCachedWinRTTypes method [.NET Framework debugging]
- GetCachedWinRTTypes method, ICorDebugAppDomain3 interface [.NET Framework debugging]
ms.assetid: 9afd0e04-a403-41e2-9528-a6dcbcdcbd4d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 73a08e83d67c973294938a030b95b906aec6be6d
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59126605"
---
# <a name="icordebugappdomain3getcachedwinrttypes-method"></a><span data-ttu-id="bb169-102">ICorDebugAppDomain3::GetCachedWinRTTypes, méthode</span><span class="sxs-lookup"><span data-stu-id="bb169-102">ICorDebugAppDomain3::GetCachedWinRTTypes Method</span></span>
<span data-ttu-id="bb169-103">Obtient un énumérateur pour toutes les mises en cache [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types.</span><span class="sxs-lookup"><span data-stu-id="bb169-103">Gets an enumerator for all cached [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb169-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb169-104">Syntax</span></span>  
  
```  
HRESULT GetCachedWinRTTypes (   
    [out] ICorDebugGuidToTypeEnum **ppGuidToTypeEnum)  
;  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb169-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb169-105">Parameters</span></span>  
 `ppGuidToTypeEnum`  
 <span data-ttu-id="bb169-106">[out] Un pointeur vers un [ICorDebugGuidToTypeEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-interface.md) objet d’interface qui peut énumérer les représentations sous forme managées de [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types actuellement chargés dans le domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="bb169-106">[out] A pointer to an [ICorDebugGuidToTypeEnum](../../../../docs/framework/unmanaged-api/debugging/icordebugguidtotypeenum-interface.md) interface object that can enumerate the managed representations of [!INCLUDE[wrt](../../../../includes/wrt-md.md)] types currently loaded in the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb169-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb169-107">Requirements</span></span>  
 **<span data-ttu-id="bb169-108">Plateformes :</span><span class="sxs-lookup"><span data-stu-id="bb169-108">Platforms:</span></span>** [!INCLUDE[wrt](../../../../includes/wrt-md.md)]  
  
 <span data-ttu-id="bb169-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bb169-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bb169-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bb169-110">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="bb169-111">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="bb169-111">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="bb169-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb169-112">See also</span></span>

- [<span data-ttu-id="bb169-113">ICorDebugAppDomain3, interface</span><span class="sxs-lookup"><span data-stu-id="bb169-113">ICorDebugAppDomain3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugappdomain3-interface.md)
