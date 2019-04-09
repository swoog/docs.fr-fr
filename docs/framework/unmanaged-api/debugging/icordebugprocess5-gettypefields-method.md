---
title: ICorDebugProcess5::GetTypeFields, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess5.GetTypeFields
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::GetTypeFields
helpviewer_keywords:
- GetTypeFields method, ICorDebugProcess5 interface [.NET Framework debugging]
- ICorDebugProcess5::GetTypeFields method [.NET Framework debugging]
ms.assetid: 6a0ad3ee-dacb-47e9-abae-4536bcc4804b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c2725c62105e92996bb2d8e79e8ff504904e9c7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59107950"
---
# <a name="icordebugprocess5gettypefields-method"></a><span data-ttu-id="aeb12-102">ICorDebugProcess5::GetTypeFields, méthode</span><span class="sxs-lookup"><span data-stu-id="aeb12-102">ICorDebugProcess5::GetTypeFields Method</span></span>
<span data-ttu-id="aeb12-103">Fournit des informations sur les champs qui appartiennent à un type.</span><span class="sxs-lookup"><span data-stu-id="aeb12-103">Provides information about the fields that belong to a type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aeb12-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aeb12-104">Syntax</span></span>  
  
```  
HRESULT GetTypeFields(  
    [in] COR_TYPEID id,  
    [in] ULONG32 celt,  
    [out] COR_FIELD fields[],   
    [out] ULONG32 *pceltNeeded  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="aeb12-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aeb12-105">Parameters</span></span>  
 `id`  
 <span data-ttu-id="aeb12-106">[in] L’identificateur du type dont les informations de champ sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="aeb12-106">[in] The identifier of the type whose field information is retrieved.</span></span>  
  
 `celt`  
 <span data-ttu-id="aeb12-107">[in] Le nombre de [COR_FIELD](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md) objets dont les informations de champ doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="aeb12-107">[in] The number of [COR_FIELD](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md) objects whose field information is to be retrieved.</span></span>  
  
 `fields`  
 <span data-ttu-id="aeb12-108">[out] Un tableau de [COR_FIELD](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md) objets qui fournissent des informations sur les champs qui appartiennent au type.</span><span class="sxs-lookup"><span data-stu-id="aeb12-108">[out] An array of [COR_FIELD](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md) objects that provide information about the fields that belong to the type.</span></span>  
  
 `pceltNeeded`  
 <span data-ttu-id="aeb12-109">[out] Un pointeur vers le nombre de [COR_FIELD](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md) objets inclus dans `fields`.</span><span class="sxs-lookup"><span data-stu-id="aeb12-109">[out] A pointer to the number of [COR_FIELD](../../../../docs/framework/unmanaged-api/debugging/cor-field-structure.md) objects included in `fields`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aeb12-110">Notes</span><span class="sxs-lookup"><span data-stu-id="aeb12-110">Remarks</span></span>  
 <span data-ttu-id="aeb12-111">Le `celt` paramètre qui spécifie le nombre de champs dont la méthode utilise pour remplir les informations de champ `fields`, doit correspondre à la valeur de la `COR_TYPE_LAYOUT::numFields` champ.</span><span class="sxs-lookup"><span data-stu-id="aeb12-111">The `celt` parameter, which specifies the number of fields whose field information the method uses to populate `fields`, should correspond to the value of the `COR_TYPE_LAYOUT::numFields` field.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aeb12-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aeb12-112">Requirements</span></span>  
 <span data-ttu-id="aeb12-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aeb12-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aeb12-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="aeb12-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="aeb12-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aeb12-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="aeb12-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="aeb12-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="aeb12-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aeb12-117">See also</span></span>

- [<span data-ttu-id="aeb12-118">ICorDebugProcess5, interface</span><span class="sxs-lookup"><span data-stu-id="aeb12-118">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)
- [<span data-ttu-id="aeb12-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="aeb12-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
