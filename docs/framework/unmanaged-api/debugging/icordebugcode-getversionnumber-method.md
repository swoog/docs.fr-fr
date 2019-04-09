---
title: ICorDebugCode::GetVersionNumber, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetVersionNumber
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetVersionNumber
helpviewer_keywords:
- GetVersionNumber method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetVersionNumber method [.NET Framework debugging]
ms.assetid: c8e02518-679f-4e9f-8a28-ba4a89a3876f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 003b29501e8f22ed9010a9f16a4f7ee67bce03a8
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59098947"
---
# <a name="icordebugcodegetversionnumber-method"></a><span data-ttu-id="a43cb-102">ICorDebugCode::GetVersionNumber, méthode</span><span class="sxs-lookup"><span data-stu-id="a43cb-102">ICorDebugCode::GetVersionNumber Method</span></span>
<span data-ttu-id="a43cb-103">Obtient le nombre de base 1 qui identifie la version du code qui représente « ICorDebugCode ».</span><span class="sxs-lookup"><span data-stu-id="a43cb-103">Gets the one-based number that identifies the version of the code that this "ICorDebugCode" represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a43cb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a43cb-104">Syntax</span></span>  
  
```  
HRESULT GetVersionNumber (  
    [out] ULONG32    *nVersion  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a43cb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a43cb-105">Parameters</span></span>  
 `nVersion`  
 <span data-ttu-id="a43cb-106">[out] Pointeur vers le numéro de version du code.</span><span class="sxs-lookup"><span data-stu-id="a43cb-106">[out] A pointer to the version number of the code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a43cb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a43cb-107">Remarks</span></span>  
 <span data-ttu-id="a43cb-108">Le numéro de version est incrémenté chaque fois qu’une opération modifier et continuer de (EnC) est exécutée sur le code.</span><span class="sxs-lookup"><span data-stu-id="a43cb-108">The version number is incremented each time an edit-and-continue (EnC) operation is performed on the code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a43cb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a43cb-109">Requirements</span></span>  
 <span data-ttu-id="a43cb-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a43cb-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a43cb-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a43cb-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a43cb-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a43cb-112">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="a43cb-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="a43cb-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="a43cb-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a43cb-114">See also</span></span>
