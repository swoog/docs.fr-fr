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
ms.openlocfilehash: 4a95008d98436161ac919ef307273bc797519f15
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59080616"
---
# <a name="efngetmanagedobjectname-function"></a><span data-ttu-id="b84ba-102">_EFN_GetManagedObjectName, fonction</span><span class="sxs-lookup"><span data-stu-id="b84ba-102">_EFN_GetManagedObjectName Function</span></span>
<span data-ttu-id="b84ba-103">Obtient le nom d’un type en utilisant le pointeur d’objet managé fourni.</span><span class="sxs-lookup"><span data-stu-id="b84ba-103">Gets the name of a type using the provided managed object pointer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b84ba-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b84ba-104">Syntax</span></span>  
  
```  
HRESULT _EFN_GetManagedObjectName(  
    [in]  PDEBUG_CLIENT  Client,  
    [in]  ULONG64        objAddr,  
    [out] __out_ecount(cbName) PSTR szName,  
    [out] ULONG          cbName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b84ba-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b84ba-105">Parameters</span></span>  
 `Client`  
 <span data-ttu-id="b84ba-106">[in] Pointeur vers le client de débogage.</span><span class="sxs-lookup"><span data-stu-id="b84ba-106">[in] A pointer to the debug client.</span></span>  
  
 `objAddr`  
 <span data-ttu-id="b84ba-107">[in] Un pointeur d’objet managé.</span><span class="sxs-lookup"><span data-stu-id="b84ba-107">[in] A managed object pointer.</span></span>  
  
 <span data-ttu-id="b84ba-108">szName</span><span class="sxs-lookup"><span data-stu-id="b84ba-108">szName</span></span>  
 <span data-ttu-id="b84ba-109">[out] Le nom du type.</span><span class="sxs-lookup"><span data-stu-id="b84ba-109">[out] The name of the type.</span></span>  
  
 `cbName`  
 <span data-ttu-id="b84ba-110">[out] Le nombre de caractères disponibles dans la mémoire tampon de chaîne.</span><span class="sxs-lookup"><span data-stu-id="b84ba-110">[out] The number of characters available in the string buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b84ba-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b84ba-111">Remarks</span></span>  
 <span data-ttu-id="b84ba-112">S’il n’existe aucun code managé sur le thread actuellement dans le contexte, la fonction retourne les HRESULT SOS_E_NOMANAGEDCODE avec une valeur de 0xa0 et un code d’erreur de 0 x 1000.</span><span class="sxs-lookup"><span data-stu-id="b84ba-112">If there is no managed code on the thread currently in context, the function returns HRESULT SOS_E_NOMANAGEDCODE with a facility value of 0xa0 and an error code of 0x1000.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b84ba-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b84ba-113">Requirements</span></span>  
 <span data-ttu-id="b84ba-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b84ba-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b84ba-115">**En-tête :** SOS_Stacktrace.h</span><span class="sxs-lookup"><span data-stu-id="b84ba-115">**Header:** SOS_Stacktrace.h</span></span>  
  
 **<span data-ttu-id="b84ba-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="b84ba-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="b84ba-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b84ba-117">See also</span></span>

- [<span data-ttu-id="b84ba-118">Fonctions statiques globales du débogage</span><span class="sxs-lookup"><span data-stu-id="b84ba-118">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
