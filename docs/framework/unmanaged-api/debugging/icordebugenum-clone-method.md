---
title: ICorDebugEnum::Clone, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugEnum.Clone
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEnum::Clone
helpviewer_keywords:
- Clone method, ICorDebugEnum interface [.NET Framework debugging]
- ICorDebugEnum::Clone method [.NET Framework debugging]
ms.assetid: 57eefaf3-75cf-4496-bc94-88c0706861b7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5d1226f64df379b5c40304221e9e66eebcdb17b4
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61989129"
---
# <a name="icordebugenumclone-method"></a><span data-ttu-id="2d61d-102">ICorDebugEnum::Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="2d61d-102">ICorDebugEnum::Clone Method</span></span>
<span data-ttu-id="2d61d-103">Crée une copie de cet objet ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="2d61d-103">Creates a copy of this ICorDebugEnum object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2d61d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d61d-104">Syntax</span></span>  
  
```  
HRESULT Clone (  
    [out] ICorDebugEnum **ppEnum  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d61d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d61d-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="2d61d-106">[out] Un pointeur vers l’adresse d’un `ICorDebugEnum` objet qui est une copie de ce `ICorDebugEnum` objet.</span><span class="sxs-lookup"><span data-stu-id="2d61d-106">[out] A pointer to the address of an `ICorDebugEnum` object that is a copy of this `ICorDebugEnum` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2d61d-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d61d-107">Requirements</span></span>  
 <span data-ttu-id="2d61d-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2d61d-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d61d-109">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2d61d-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2d61d-110">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2d61d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2d61d-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d61d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
