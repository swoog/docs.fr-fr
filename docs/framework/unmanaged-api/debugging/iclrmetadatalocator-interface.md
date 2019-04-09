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
ms.openlocfilehash: ddc0429a6fa921e8e6ba3c55f3efe5373bea9576
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59123771"
---
# <a name="iclrmetadatalocator-interface"></a><span data-ttu-id="4ffd4-102">ICLRMetadataLocator, interface</span><span class="sxs-lookup"><span data-stu-id="4ffd4-102">ICLRMetadataLocator Interface</span></span>
<span data-ttu-id="4ffd4-103">Utilisé par la couche de services d’accès aux données pour localiser les métadonnées des assemblys dans un processus cible.</span><span class="sxs-lookup"><span data-stu-id="4ffd4-103">Used by the data access services layer to locate metadata of assemblies in a target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4ffd4-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4ffd4-104">Methods</span></span>  
  
|<span data-ttu-id="4ffd4-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="4ffd4-105">Method</span></span>|<span data-ttu-id="4ffd4-106">Description</span><span class="sxs-lookup"><span data-stu-id="4ffd4-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4ffd4-107">GetMetaData, méthode</span><span class="sxs-lookup"><span data-stu-id="4ffd4-107">GetMetadata Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrmetadatalocator-getmetadata-method.md)|<span data-ttu-id="4ffd4-108">Récupère les métadonnées d’une image à partir du processus cible.</span><span class="sxs-lookup"><span data-stu-id="4ffd4-108">Retrieves the metadata of an image from the target process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4ffd4-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4ffd4-109">Remarks</span></span>  
 <span data-ttu-id="4ffd4-110">Le client API (c'est-à-dire le débogueur) doit implémenter cette interface comme il convient pour le processus cible particulier.</span><span class="sxs-lookup"><span data-stu-id="4ffd4-110">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="4ffd4-111">Par exemple, l’implémentation pour un processus actif serait différente de celui d’un vidage de mémoire.</span><span class="sxs-lookup"><span data-stu-id="4ffd4-111">For example, the implementation for a live process would be different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4ffd4-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ffd4-112">Requirements</span></span>  
 <span data-ttu-id="4ffd4-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4ffd4-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ffd4-114">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="4ffd4-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="4ffd4-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4ffd4-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="4ffd4-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="4ffd4-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="4ffd4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ffd4-117">See also</span></span>

- [<span data-ttu-id="4ffd4-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4ffd4-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
