---
title: Interface de ICorProfilerInfo7
ms.date: 03/30/2017
ms.assetid: cf37c462-73c5-412a-a7f8-bb26ca746313
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 79a722cd3318def36c20a49c1567c6f0d4989d39
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455404"
---
# <a name="icorprofilerinfo7-interface"></a><span data-ttu-id="8d6eb-102">Interface de ICorProfilerInfo7</span><span class="sxs-lookup"><span data-stu-id="8d6eb-102">ICorProfilerInfo7 Interface</span></span>
<span data-ttu-id="8d6eb-103">[Prise en charge dans [!INCLUDE[net_v461](../../../../includes/net-v461-md.md)] et versions ultérieures]</span><span class="sxs-lookup"><span data-stu-id="8d6eb-103">[Supported in the [!INCLUDE[net_v461](../../../../includes/net-v461-md.md)] and later versions]</span></span>  
  
 <span data-ttu-id="8d6eb-104">Une sous-classe de [ICorProfilerInfo6](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md) qui fournit une méthode à appliquer qui vient d’être défini des métadonnées à un module et qui fournit l’accès à un flux de symbole de mémoire.</span><span class="sxs-lookup"><span data-stu-id="8d6eb-104">A subclass of [ICorProfilerInfo6](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo6-interface.md) that provides a method to apply newly defined metadata to a module and that provides access to an in-memory symbol stream.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="8d6eb-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8d6eb-105">Methods</span></span>  
  
|<span data-ttu-id="8d6eb-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="8d6eb-106">Method</span></span>|<span data-ttu-id="8d6eb-107">Description</span><span class="sxs-lookup"><span data-stu-id="8d6eb-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8d6eb-108">ApplyMetaData, méthode</span><span class="sxs-lookup"><span data-stu-id="8d6eb-108">ApplyMetaData Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-applymetadata-method.md)|<span data-ttu-id="8d6eb-109">Applique les métadonnées qui vient d’être définie par le `IMetadataEmit::Define*` méthodes à un module spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d6eb-109">Applies the metadata newly defined by the `IMetadataEmit::Define*` methods to a specified module.</span></span>|  
|[<span data-ttu-id="8d6eb-110">GetInMemorySymbolsLength, méthode</span><span class="sxs-lookup"><span data-stu-id="8d6eb-110">GetInMemorySymbolsLength Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-getinmemorysymbolslength-method.md)|<span data-ttu-id="8d6eb-111">Retourne la longueur d’un flux de symbole de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="8d6eb-111">Returns the length of an in-memory symbol stream.</span></span>|  
|[<span data-ttu-id="8d6eb-112">ReadInMemorySymbols</span><span class="sxs-lookup"><span data-stu-id="8d6eb-112">ReadInMemorySymbols</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo7-readinmemorysymbols.md)|<span data-ttu-id="8d6eb-113">Lit les octets à partir d’un flux de symbole de mémoire.</span><span class="sxs-lookup"><span data-stu-id="8d6eb-113">Reads bytes from an in-memory symbol stream.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8d6eb-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8d6eb-114">Requirements</span></span>  
 <span data-ttu-id="8d6eb-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8d6eb-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d6eb-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8d6eb-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8d6eb-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8d6eb-117">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d6eb-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d6eb-118">See Also</span></span>  
 [<span data-ttu-id="8d6eb-119">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="8d6eb-119">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
