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
ms.openlocfilehash: fd7a67237d89864915f8b4f1f7361d1f113d1e5d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404731"
---
# <a name="iclrmetadatalocator-interface"></a><span data-ttu-id="45e57-102">ICLRMetadataLocator, interface</span><span class="sxs-lookup"><span data-stu-id="45e57-102">ICLRMetadataLocator Interface</span></span>
<span data-ttu-id="45e57-103">Utilisé par la couche de services d’accès aux données pour localiser les métadonnées des assemblys dans un processus cible.</span><span class="sxs-lookup"><span data-stu-id="45e57-103">Used by the data access services layer to locate metadata of assemblies in a target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="45e57-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45e57-104">Methods</span></span>  
  
|<span data-ttu-id="45e57-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="45e57-105">Method</span></span>|<span data-ttu-id="45e57-106">Description</span><span class="sxs-lookup"><span data-stu-id="45e57-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="45e57-107">GetMetadata, méthode</span><span class="sxs-lookup"><span data-stu-id="45e57-107">GetMetadata Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrmetadatalocator-getmetadata-method.md)|<span data-ttu-id="45e57-108">Récupère les métadonnées d’une image du processus cible.</span><span class="sxs-lookup"><span data-stu-id="45e57-108">Retrieves the metadata of an image from the target process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="45e57-109">Notes</span><span class="sxs-lookup"><span data-stu-id="45e57-109">Remarks</span></span>  
 <span data-ttu-id="45e57-110">Le client API (c'est-à-dire le débogueur) doit implémenter cette interface comme il convient pour le processus cible particulier.</span><span class="sxs-lookup"><span data-stu-id="45e57-110">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="45e57-111">Par exemple, l’implémentation pour un processus actif serait différente de celui d’un vidage de mémoire.</span><span class="sxs-lookup"><span data-stu-id="45e57-111">For example, the implementation for a live process would be different from that of a memory dump.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="45e57-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="45e57-112">Requirements</span></span>  
 <span data-ttu-id="45e57-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="45e57-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="45e57-114">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="45e57-114">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="45e57-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="45e57-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="45e57-116">**.**</span><span class="sxs-lookup"><span data-stu-id="45e57-116">**.**</span></span> <span data-ttu-id="45e57-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="45e57-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="45e57-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45e57-118">See Also</span></span>  
 [<span data-ttu-id="45e57-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="45e57-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
