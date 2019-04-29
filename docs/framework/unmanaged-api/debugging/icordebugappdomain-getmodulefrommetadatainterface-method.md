---
title: ICorDebugAppDomain::GetModuleFromMetaDataInterface, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetModuleFromMetaDataInterface
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetModuleFromMetaDataInterface
helpviewer_keywords:
- ICorDebugAppDomain::GetModuleFromMetaDatainterface method [.NET Framework debugging]
- GetModuleFromMetaDatainterface method [.NET Framework debugging]
ms.assetid: f35225b3-5dda-4d5a-913d-b3373e9ab81e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2eaa48dcc7dad2d66f1a60922c94193120b59b32
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61785155"
---
# <a name="icordebugappdomaingetmodulefrommetadatainterface-method"></a><span data-ttu-id="82932-102">ICorDebugAppDomain::GetModuleFromMetaDataInterface, méthode</span><span class="sxs-lookup"><span data-stu-id="82932-102">ICorDebugAppDomain::GetModuleFromMetaDataInterface Method</span></span>
<span data-ttu-id="82932-103">Obtient le module qui correspond à l’interface de métadonnées fourni.</span><span class="sxs-lookup"><span data-stu-id="82932-103">Gets the module that corresponds to the given metadata interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82932-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82932-104">Syntax</span></span>  
  
```  
HRESULT GetModuleFromMetaDataInterface (  
    [in] IUnknown           *pIMetaData,  
    [out] ICorDebugModule  **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="82932-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82932-105">Parameters</span></span>  
 `pIMetaData`  
 <span data-ttu-id="82932-106">[in] Un pointeur vers un objet qui est un de la [interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="82932-106">[in] A pointer to an object that is one of the [Metadata interfaces](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span></span>  
  
 `ppModule`  
 <span data-ttu-id="82932-107">[out] Pointeur vers l’adresse d’un objet ICorDebugModule qui représente le module correspondant à l’interface de métadonnées fourni.</span><span class="sxs-lookup"><span data-stu-id="82932-107">[out] A pointer to the address of an ICorDebugModule object that represents the module corresponding to the given metadata interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="82932-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82932-108">Requirements</span></span>  
 <span data-ttu-id="82932-109">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="82932-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82932-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="82932-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="82932-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="82932-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="82932-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="82932-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
