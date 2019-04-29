---
title: ICorDebugInternalFrame::GetFrameType, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame.GetFrameType
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame::GetFrameType
helpviewer_keywords:
- GetFrameType method [.NET Framework debugging]
- ICorDebugInternalFrame::GetFrameType method [.NET Framework debugging]
ms.assetid: da278a29-dc2e-4bf7-96ce-801bdc4d7025
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a0b6f0550bad534379b562c3df9da9ab917f5270
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946336"
---
# <a name="icordebuginternalframegetframetype-method"></a><span data-ttu-id="ae2c8-102">ICorDebugInternalFrame::GetFrameType, méthode</span><span class="sxs-lookup"><span data-stu-id="ae2c8-102">ICorDebugInternalFrame::GetFrameType Method</span></span>
<span data-ttu-id="ae2c8-103">Obtient le type de ce frame interne.</span><span class="sxs-lookup"><span data-stu-id="ae2c8-103">Gets the type of this internal frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae2c8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae2c8-104">Syntax</span></span>  
  
```  
HRESULT GetFrameType (  
    [out] CorDebugInternalFrameType  *pType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ae2c8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae2c8-105">Parameters</span></span>  
 `pType`  
 <span data-ttu-id="ae2c8-106">[out] Un pointeur vers une valeur de l’énumération CorDebugInternalFrameType qui indique le type de frame interne représenté par cet `ICorDebugInternalFrame` objet.</span><span class="sxs-lookup"><span data-stu-id="ae2c8-106">[out] A pointer to a value of the CorDebugInternalFrameType enumeration that indicates the type of internal frame represented by this `ICorDebugInternalFrame` object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae2c8-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ae2c8-107">Remarks</span></span>  
 <span data-ttu-id="ae2c8-108">Le type de frame interne ne sera jamais STUBFRAME_NONE.</span><span class="sxs-lookup"><span data-stu-id="ae2c8-108">The internal frame type will never be STUBFRAME_NONE.</span></span> <span data-ttu-id="ae2c8-109">Débogueurs doivent ignorer correctement les types de frame interne non reconnu.</span><span class="sxs-lookup"><span data-stu-id="ae2c8-109">Debuggers should gracefully ignore unrecognized internal frame types.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae2c8-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae2c8-110">Requirements</span></span>  
 <span data-ttu-id="ae2c8-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ae2c8-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae2c8-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ae2c8-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ae2c8-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ae2c8-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ae2c8-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae2c8-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
