---
title: _EFN_GetManagedObjectFieldInfo, fonction
ms.date: 03/30/2017
api_name:
- _EFN_GetManagedObjectFieldInfo
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- _EFN_GetManagedObjectFieldInfo
helpviewer_keywords:
- _EFN_GetManagedObjectFieldInfo function [.NET Framework debugging]
ms.assetid: 3b93bcff-62a4-47b2-babc-6bcf4216119a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c6195d9666afa8fba3f77322366e4709634e53bb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405242"
---
# <a name="efngetmanagedobjectfieldinfo-function"></a><span data-ttu-id="6119b-102">_EFN_GetManagedObjectFieldInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="6119b-102">_EFN_GetManagedObjectFieldInfo Function</span></span>
<span data-ttu-id="6119b-103">Obtient l'offset du début d'un objet jusqu'à un champ, ainsi que la valeur du champ, à l'aide du pointeur d'objet et du nom de champ fournis.</span><span class="sxs-lookup"><span data-stu-id="6119b-103">Gets the offset from the start of an object to a field and the field's value, using the provided object pointer and field name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6119b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6119b-104">Syntax</span></span>  
  
```  
HRESULT _EFN_GetManagedObjectFieldInfo(  
    [in]  PDEBUG_CLIENT Client,  
    [in]  ULONG64       objAddr,  
    [in]  __out_ecount (mdNameLen) PSTR szFieldName,  
    [out] PULONG64      pValue,  
    [out] PULONG        pOffset  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6119b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6119b-105">Parameters</span></span>  
 `Client`  
 <span data-ttu-id="6119b-106">[in] Pointeur vers le client de débogage.</span><span class="sxs-lookup"><span data-stu-id="6119b-106">[in] A pointer to the debug client.</span></span>  
  
 `objAddr`  
 <span data-ttu-id="6119b-107">[in] Un pointeur d’objet managé.</span><span class="sxs-lookup"><span data-stu-id="6119b-107">[in] A managed object pointer.</span></span>  
  
 <span data-ttu-id="6119b-108">szFieldName</span><span class="sxs-lookup"><span data-stu-id="6119b-108">szFieldName</span></span>  
 <span data-ttu-id="6119b-109">[in] Un pointeur d’objet managé pour le nom du champ.</span><span class="sxs-lookup"><span data-stu-id="6119b-109">[in] A managed object pointer to the field name.</span></span>  
  
 `pValue`  
 <span data-ttu-id="6119b-110">[out] La valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="6119b-110">[out] The field value.</span></span> <span data-ttu-id="6119b-111">Ce paramètre peut avoir la valeur Null.</span><span class="sxs-lookup"><span data-stu-id="6119b-111">This parameter can be null.</span></span>  
  
 `pOffset`  
 <span data-ttu-id="6119b-112">[out] Le décalage à partir de `objAddr` au champ.</span><span class="sxs-lookup"><span data-stu-id="6119b-112">[out] The offset from `objAddr` to the field.</span></span> <span data-ttu-id="6119b-113">Ce paramètre peut avoir la valeur Null.</span><span class="sxs-lookup"><span data-stu-id="6119b-113">This parameter can be null.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6119b-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6119b-114">Remarks</span></span>  
 <span data-ttu-id="6119b-115">Si le décalage est 0, aucun offset n’est écrit.</span><span class="sxs-lookup"><span data-stu-id="6119b-115">If the offset is 0, no offset is written.</span></span>  
  
 <span data-ttu-id="6119b-116">S’il n’existe aucun code managé sur le thread actuellement dans le contexte, la fonction retourne les HRESULT SOS_E_NOMANAGEDCODE avec une valeur d’environnement 0xa0 et un code d’erreur de 0 x 1000.</span><span class="sxs-lookup"><span data-stu-id="6119b-116">If there is no managed code on the thread currently in context, the function returns HRESULT SOS_E_NOMANAGEDCODE with a facility value of 0xa0 and an error code of 0x1000.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6119b-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6119b-117">Requirements</span></span>  
 <span data-ttu-id="6119b-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6119b-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6119b-119">**En-tête :** SOS_Stacktrace.h</span><span class="sxs-lookup"><span data-stu-id="6119b-119">**Header:** SOS_Stacktrace.h</span></span>  
  
 <span data-ttu-id="6119b-120">**Version du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6119b-120">**.NET Framework Version:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6119b-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6119b-121">See Also</span></span>  
 [<span data-ttu-id="6119b-122">Fonctions statiques globales de débogage</span><span class="sxs-lookup"><span data-stu-id="6119b-122">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
