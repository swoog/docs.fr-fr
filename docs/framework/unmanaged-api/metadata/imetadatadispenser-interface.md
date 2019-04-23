---
title: IMetaDataDispenser, interface
ms.date: 03/30/2017
api_name:
- IMetaDataDispenser
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenser
helpviewer_keywords:
- IMetaDataDispenser interface [.NET Framework metadata]
ms.assetid: 989840b3-9822-4ce5-a6c5-b375d3340a7a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dda284fc86f0a82472c59d6bab08fd4a87364723
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59225974"
---
# <a name="imetadatadispenser-interface"></a><span data-ttu-id="d22e6-102">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="d22e6-102">IMetaDataDispenser Interface</span></span>
<span data-ttu-id="d22e6-103">Fournit des méthodes pour créer une nouvelle étendue de métadonnées, ou ouvrez-en une existante.</span><span class="sxs-lookup"><span data-stu-id="d22e6-103">Provides methods to create a new metadata scope, or open an existing one.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d22e6-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d22e6-104">Methods</span></span>  
  
|<span data-ttu-id="d22e6-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d22e6-105">Method</span></span>|<span data-ttu-id="d22e6-106">Description</span><span class="sxs-lookup"><span data-stu-id="d22e6-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d22e6-107">DefineScope, méthode</span><span class="sxs-lookup"><span data-stu-id="d22e6-107">DefineScope Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-definescope-method.md)|<span data-ttu-id="d22e6-108">Crée une nouvelle zone en mémoire dans lequel vous pouvez créer des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d22e6-108">Creates a new area in memory where you can create new metadata.</span></span>|  
|[<span data-ttu-id="d22e6-109">OpenScope, méthode</span><span class="sxs-lookup"><span data-stu-id="d22e6-109">OpenScope Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md)|<span data-ttu-id="d22e6-110">Ouvre un fichier sur disque existant et mappe ses métadonnées dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d22e6-110">Opens an existing, on-disk file and maps its metadata into memory.</span></span>|  
|[<span data-ttu-id="d22e6-111">OpenScopeOnMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="d22e6-111">OpenScopeOnMemory Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscopeonmemory-method.md)|<span data-ttu-id="d22e6-112">Ouvre une zone de mémoire qui contient les métadonnées existantes.</span><span class="sxs-lookup"><span data-stu-id="d22e6-112">Opens an area of memory that contains existing metadata.</span></span> <span data-ttu-id="d22e6-113">Autrement dit, cette méthode ouvre une zone de mémoire dans lequel les données existantes sont traitées en tant que métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d22e6-113">That is, this method opens a specified area of memory in which the existing data is treated as metadata.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d22e6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d22e6-114">Requirements</span></span>  
 <span data-ttu-id="d22e6-115">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d22e6-115">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d22e6-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d22e6-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d22e6-117">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d22e6-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d22e6-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d22e6-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d22e6-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d22e6-119">See also</span></span>

- [<span data-ttu-id="d22e6-120">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="d22e6-120">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [<span data-ttu-id="d22e6-121">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="d22e6-121">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
