---
title: ICLRMetadataLocator, interface
ms.date: 03/30/2017
api_name:
- ICLRMetadataLocator
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRMetadataLocator
helpviewer_keywords:
- ICLRMetadataLocator interface [.NET Framework debugging]
ms.assetid: 43c944f4-406a-4df6-981e-0eabb33dd5d0
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e5dd77783c03d6a61d0b5831e44db97a731d8074
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55825886"
---
# <a name="iclrmetadatalocator-interface"></a><span data-ttu-id="33415-102">ICLRMetadataLocator, interface</span><span class="sxs-lookup"><span data-stu-id="33415-102">ICLRMetadataLocator Interface</span></span>
<span data-ttu-id="33415-103">Utilisé par la couche de services d’accès aux données pour localiser les métadonnées des assemblys dans un processus cible.</span><span class="sxs-lookup"><span data-stu-id="33415-103">Used by the data access services layer to locate metadata of assemblies in a target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="33415-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="33415-104">Methods</span></span>  
  
|<span data-ttu-id="33415-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="33415-105">Method</span></span>|<span data-ttu-id="33415-106">Description</span><span class="sxs-lookup"><span data-stu-id="33415-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="33415-107">GetMetadata, méthode</span><span class="sxs-lookup"><span data-stu-id="33415-107">GetMetadata Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrmetadatalocator-getmetadata-method.md)|<span data-ttu-id="33415-108">Récupère les métadonnées d’une image à partir du processus cible.</span><span class="sxs-lookup"><span data-stu-id="33415-108">Retrieves the metadata of an image from the target process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="33415-109">Notes</span><span class="sxs-lookup"><span data-stu-id="33415-109">Remarks</span></span>  
 <span data-ttu-id="33415-110">Le client API (c'est-à-dire le débogueur) doit implémenter cette interface comme il convient pour le processus cible particulier.</span><span class="sxs-lookup"><span data-stu-id="33415-110">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="33415-111">Par exemple, l’implémentation pour un processus actif serait différente de celui d’un vidage de mémoire.</span><span class="sxs-lookup"><span data-stu-id="33415-111">For example, the implementation for a live process would be different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="33415-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="33415-112">Requirements</span></span>  
 <span data-ttu-id="33415-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="33415-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="33415-114">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="33415-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="33415-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="33415-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="33415-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="33415-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33415-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33415-117">See also</span></span>
- [<span data-ttu-id="33415-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="33415-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
