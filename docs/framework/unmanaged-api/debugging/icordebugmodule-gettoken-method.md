---
title: ICorDebugModule::GetToken, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugModule.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::GetToken
helpviewer_keywords:
- ICorDebugModule::GetToken method [.NET Framework debugging]
- GetToken method, ICorDebugModule interface [.NET Framework debugging]
ms.assetid: f759f87a-18ae-4c1a-8300-29b803432d0a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5bfeb9bf282f8b6fc076cf3a5ae71b2375b8a90d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57487201"
---
# <a name="icordebugmodulegettoken-method"></a><span data-ttu-id="d0c20-102">ICorDebugModule::GetToken, méthode</span><span class="sxs-lookup"><span data-stu-id="d0c20-102">ICorDebugModule::GetToken Method</span></span>
<span data-ttu-id="d0c20-103">Obtient le jeton pour l’entrée de table pour ce module.</span><span class="sxs-lookup"><span data-stu-id="d0c20-103">Gets the token for the table entry for this module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0c20-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0c20-104">Syntax</span></span>  
  
```  
HRESULT GetToken(  
    [out] mdModule *pToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d0c20-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0c20-105">Parameters</span></span>  
 `pToken`  
 <span data-ttu-id="d0c20-106">[out] Un pointeur vers le `mdModule` jeton qui référence les métadonnées du module.</span><span class="sxs-lookup"><span data-stu-id="d0c20-106">[out] A pointer to the `mdModule` token that references the module's metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d0c20-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d0c20-107">Remarks</span></span>  
 <span data-ttu-id="d0c20-108">Le jeton peut être passé à la [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md), [IMetaDataImport2](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md), et [IMetaDataAssemblyImport](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interfaces d’importation de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d0c20-108">The token can be passed to the [IMetaDataImport](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md), [IMetaDataImport2](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md), and [IMetaDataAssemblyImport](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) metadata import interfaces.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0c20-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d0c20-109">Requirements</span></span>  
 <span data-ttu-id="d0c20-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d0c20-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0c20-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d0c20-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d0c20-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d0c20-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d0c20-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0c20-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0c20-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0c20-114">See also</span></span>
- [<span data-ttu-id="d0c20-115">Métadonnées</span><span class="sxs-lookup"><span data-stu-id="d0c20-115">Metadata</span></span>](../../../../docs/framework/unmanaged-api/metadata/index.md)
