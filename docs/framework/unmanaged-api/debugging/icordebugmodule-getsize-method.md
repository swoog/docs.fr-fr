---
title: ICorDebugModule::GetSize, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugModule interface [.NET Framework debugging]
- ICorDebugModule::GetSize method [.NET Framework debugging]
ms.assetid: 5c68375d-145d-46ef-a7c8-2dc4257472de
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f0d741bda5426dee1292df0e6fd9107cc2f44c8a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33413317"
---
# <a name="icordebugmodulegetsize-method"></a><span data-ttu-id="4937a-102">ICorDebugModule::GetSize, méthode</span><span class="sxs-lookup"><span data-stu-id="4937a-102">ICorDebugModule::GetSize Method</span></span>
<span data-ttu-id="4937a-103">Obtient la taille, en octets, du module.</span><span class="sxs-lookup"><span data-stu-id="4937a-103">Gets the size, in bytes, of the module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4937a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4937a-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
    [out] ULONG32 *pcBytes  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4937a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4937a-105">Parameters</span></span>  
 `pcBytes`  
 <span data-ttu-id="4937a-106">[out] La taille du module en octets.</span><span class="sxs-lookup"><span data-stu-id="4937a-106">[out] The size of the module in bytes.</span></span>  
  
 <span data-ttu-id="4937a-107">Si le module a été généré à partir du Générateur d’images natives (NGen.exe), la taille du module sera zéro.</span><span class="sxs-lookup"><span data-stu-id="4937a-107">If the module was produced from the native image generator (NGen.exe), the size of the module will be zero.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4937a-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4937a-108">Requirements</span></span>  
 <span data-ttu-id="4937a-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4937a-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4937a-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4937a-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4937a-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4937a-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4937a-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4937a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
