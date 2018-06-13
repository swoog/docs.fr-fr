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
ms.openlocfilehash: 8ab9773a5056dbfba422a9a53c7cd877e4c29abe
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404597"
---
# <a name="icordebugappdomaingetmodulefrommetadatainterface-method"></a><span data-ttu-id="02d4c-102">ICorDebugAppDomain::GetModuleFromMetaDataInterface, méthode</span><span class="sxs-lookup"><span data-stu-id="02d4c-102">ICorDebugAppDomain::GetModuleFromMetaDataInterface Method</span></span>
<span data-ttu-id="02d4c-103">Obtient le module qui correspond à l’interface de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="02d4c-103">Gets the module that corresponds to the given metadata interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="02d4c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02d4c-104">Syntax</span></span>  
  
```  
HRESULT GetModuleFromMetaDataInterface (  
    [in] IUnknown           *pIMetaData,  
    [out] ICorDebugModule  **ppModule  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="02d4c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02d4c-105">Parameters</span></span>  
 `pIMetaData`  
 <span data-ttu-id="02d4c-106">[in] Un pointeur vers un objet qui est un de le [interfaces de métadonnées](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="02d4c-106">[in] A pointer to an object that is one of the [Metadata interfaces](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md).</span></span>  
  
 `ppModule`  
 <span data-ttu-id="02d4c-107">[out] Pointeur vers l’adresse d’un objet ICorDebugModule qui représente le module correspondant à l’interface de métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="02d4c-107">[out] A pointer to the address of an ICorDebugModule object that represents the module corresponding to the given metadata interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="02d4c-108">Spécifications</span><span class="sxs-lookup"><span data-stu-id="02d4c-108">Requirements</span></span>  
 <span data-ttu-id="02d4c-109">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="02d4c-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="02d4c-110">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="02d4c-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="02d4c-111">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="02d4c-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="02d4c-112">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="02d4c-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
