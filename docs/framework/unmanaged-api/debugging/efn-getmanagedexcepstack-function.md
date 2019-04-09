---
title: _EFN_GetManagedExcepStack, fonction
ms.date: 03/30/2017
api_name:
- _EFN_GetManagedExcepStack
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- _EFN_GetManagedExcepStack
helpviewer_keywords:
- _EFN_GetManagedExcepStack function [.NET Framework debugging]
ms.assetid: 21ceed9e-62b2-4024-b027-6d095109955a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7e201b9a350c030da59e2b6ed27f84f570c8e621
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59126657"
---
# <a name="efngetmanagedexcepstack-function"></a><span data-ttu-id="86e0e-102">_EFN_GetManagedExcepStack, fonction</span><span class="sxs-lookup"><span data-stu-id="86e0e-102">_EFN_GetManagedExcepStack Function</span></span>
<span data-ttu-id="86e0e-103">Retourne une version de chaîne de la trace de pile contenue dans une adresse d'objet exception managée donnée.</span><span class="sxs-lookup"><span data-stu-id="86e0e-103">Given a managed exception object address, returns a string version of the stack trace contained inside.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="86e0e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86e0e-104">Syntax</span></span>  
  
```  
HRESULT _EFN_GetManagedExcepStack(  
    [in]  PDEBUG_CLIENT Client,  
    [in]  ULONG64       StackObjAddr,  
    [out] __out_ecount(cbString) PSTR szStackString,  
    [out] ULONG         cbString  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="86e0e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86e0e-105">Parameters</span></span>  
 `Client`  
 <span data-ttu-id="86e0e-106">[in] Le client en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="86e0e-106">[in] The client being debugged.</span></span>  
  
 `StackObjAddr`  
 <span data-ttu-id="86e0e-107">[in] Un pointeur d’objet managé, dérivé <xref:System.Exception>.</span><span class="sxs-lookup"><span data-stu-id="86e0e-107">[in] A managed object pointer, derived from <xref:System.Exception>.</span></span>  
  
 <span data-ttu-id="86e0e-108">szStackString</span><span class="sxs-lookup"><span data-stu-id="86e0e-108">szStackString</span></span>  
 <span data-ttu-id="86e0e-109">[out] La chaîne retournée.</span><span class="sxs-lookup"><span data-stu-id="86e0e-109">[out] The returned string.</span></span>  
  
 `cbString`  
 <span data-ttu-id="86e0e-110">[out] Le nombre de caractères disponibles dans la mémoire tampon de chaîne.</span><span class="sxs-lookup"><span data-stu-id="86e0e-110">[out] The number of characters available in the string buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="86e0e-111">Notes</span><span class="sxs-lookup"><span data-stu-id="86e0e-111">Remarks</span></span>  
 <span data-ttu-id="86e0e-112">S’il n’existe aucun code managé sur le thread actuellement dans le contexte, la fonction retourne les HRESULT SOS_E_NOMANAGEDCODE avec une valeur de 0xa0 et un code d’erreur de 0 x 1000.</span><span class="sxs-lookup"><span data-stu-id="86e0e-112">If there is no managed code on the thread currently in context, the function returns HRESULT SOS_E_NOMANAGEDCODE with a facility value of 0xa0 and an error code of 0x1000.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="86e0e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86e0e-113">Requirements</span></span>  
 <span data-ttu-id="86e0e-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="86e0e-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="86e0e-115">**En-tête :** SOS_Stacktrace.h</span><span class="sxs-lookup"><span data-stu-id="86e0e-115">**Header:** SOS_Stacktrace.h</span></span>  
  
 **<span data-ttu-id="86e0e-116">Version du .NET framework :</span><span class="sxs-lookup"><span data-stu-id="86e0e-116">.NET Framework Version:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="86e0e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86e0e-117">See also</span></span>

- [<span data-ttu-id="86e0e-118">Fonctions statiques globales du débogage</span><span class="sxs-lookup"><span data-stu-id="86e0e-118">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
