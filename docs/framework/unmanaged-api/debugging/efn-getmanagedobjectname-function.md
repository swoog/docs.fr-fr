---
title: _EFN_GetManagedObjectName, fonction
ms.date: 03/30/2017
api_name:
- _EFN_GetManagedObjectName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- _EFN_GetManagedObjectName
helpviewer_keywords:
- _EFN_GetManagedObjectName function [.NET Framework debugging]
ms.assetid: 6e7c6bee-7ced-495f-bf6c-2a5f0c716f7e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9f13fad537a6847ba6e19c939e72df86036e28ff
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402202"
---
# <a name="efngetmanagedobjectname-function"></a><span data-ttu-id="3b532-102">_EFN_GetManagedObjectName, fonction</span><span class="sxs-lookup"><span data-stu-id="3b532-102">_EFN_GetManagedObjectName Function</span></span>
<span data-ttu-id="3b532-103">Obtient le nom d’un type à l’aide du pointeur d’objet managé fourni.</span><span class="sxs-lookup"><span data-stu-id="3b532-103">Gets the name of a type using the provided managed object pointer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b532-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b532-104">Syntax</span></span>  
  
```  
HRESULT _EFN_GetManagedObjectName(  
    [in]  PDEBUG_CLIENT  Client,  
    [in]  ULONG64        objAddr,  
    [out] __out_ecount(cbName) PSTR szName,  
    [out] ULONG          cbName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3b532-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b532-105">Parameters</span></span>  
 `Client`  
 <span data-ttu-id="3b532-106">[in] Pointeur vers le client de débogage.</span><span class="sxs-lookup"><span data-stu-id="3b532-106">[in] A pointer to the debug client.</span></span>  
  
 `objAddr`  
 <span data-ttu-id="3b532-107">[in] Un pointeur d’objet managé.</span><span class="sxs-lookup"><span data-stu-id="3b532-107">[in] A managed object pointer.</span></span>  
  
 <span data-ttu-id="3b532-108">szName</span><span class="sxs-lookup"><span data-stu-id="3b532-108">szName</span></span>  
 <span data-ttu-id="3b532-109">[out] Le nom du type.</span><span class="sxs-lookup"><span data-stu-id="3b532-109">[out] The name of the type.</span></span>  
  
 `cbName`  
 <span data-ttu-id="3b532-110">[out] Le nombre de caractères disponibles dans la mémoire tampon de chaîne.</span><span class="sxs-lookup"><span data-stu-id="3b532-110">[out] The number of characters available in the string buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3b532-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3b532-111">Remarks</span></span>  
 <span data-ttu-id="3b532-112">S’il n’existe aucun code managé sur le thread actuellement dans le contexte, la fonction retourne les HRESULT SOS_E_NOMANAGEDCODE avec une valeur d’environnement 0xa0 et un code d’erreur de 0 x 1000.</span><span class="sxs-lookup"><span data-stu-id="3b532-112">If there is no managed code on the thread currently in context, the function returns HRESULT SOS_E_NOMANAGEDCODE with a facility value of 0xa0 and an error code of 0x1000.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b532-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3b532-113">Requirements</span></span>  
 <span data-ttu-id="3b532-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3b532-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b532-115">**En-tête :** SOS_Stacktrace.h</span><span class="sxs-lookup"><span data-stu-id="3b532-115">**Header:** SOS_Stacktrace.h</span></span>  
  
 <span data-ttu-id="3b532-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b532-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b532-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b532-117">See Also</span></span>  
 [<span data-ttu-id="3b532-118">Fonctions statiques globales de débogage</span><span class="sxs-lookup"><span data-stu-id="3b532-118">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
