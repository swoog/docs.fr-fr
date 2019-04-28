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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61904759"
---
# <a name="imetadatadispenser-interface"></a><span data-ttu-id="947dc-102">IMetaDataDispenser, interface</span><span class="sxs-lookup"><span data-stu-id="947dc-102">IMetaDataDispenser Interface</span></span>
<span data-ttu-id="947dc-103">Fournit des méthodes pour créer une nouvelle étendue de métadonnées, ou ouvrez-en une existante.</span><span class="sxs-lookup"><span data-stu-id="947dc-103">Provides methods to create a new metadata scope, or open an existing one.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="947dc-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="947dc-104">Methods</span></span>  
  
|<span data-ttu-id="947dc-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="947dc-105">Method</span></span>|<span data-ttu-id="947dc-106">Description</span><span class="sxs-lookup"><span data-stu-id="947dc-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="947dc-107">DefineScope, méthode</span><span class="sxs-lookup"><span data-stu-id="947dc-107">DefineScope Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-definescope-method.md)|<span data-ttu-id="947dc-108">Crée une nouvelle zone en mémoire dans lequel vous pouvez créer des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="947dc-108">Creates a new area in memory where you can create new metadata.</span></span>|  
|[<span data-ttu-id="947dc-109">OpenScope, méthode</span><span class="sxs-lookup"><span data-stu-id="947dc-109">OpenScope Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md)|<span data-ttu-id="947dc-110">Ouvre un fichier sur disque existant et mappe ses métadonnées dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="947dc-110">Opens an existing, on-disk file and maps its metadata into memory.</span></span>|  
|[<span data-ttu-id="947dc-111">OpenScopeOnMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="947dc-111">OpenScopeOnMemory Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscopeonmemory-method.md)|<span data-ttu-id="947dc-112">Ouvre une zone de mémoire qui contient les métadonnées existantes.</span><span class="sxs-lookup"><span data-stu-id="947dc-112">Opens an area of memory that contains existing metadata.</span></span> <span data-ttu-id="947dc-113">Autrement dit, cette méthode ouvre une zone de mémoire dans lequel les données existantes sont traitées en tant que métadonnées spécifiée.</span><span class="sxs-lookup"><span data-stu-id="947dc-113">That is, this method opens a specified area of memory in which the existing data is treated as metadata.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="947dc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="947dc-114">Requirements</span></span>  
 <span data-ttu-id="947dc-115">**Plateforme :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="947dc-115">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="947dc-116">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="947dc-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="947dc-117">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="947dc-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="947dc-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="947dc-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="947dc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="947dc-119">See also</span></span>

- [<span data-ttu-id="947dc-120">IMetaDataDispenserEx, interface</span><span class="sxs-lookup"><span data-stu-id="947dc-120">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [<span data-ttu-id="947dc-121">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="947dc-121">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
