---
title: ICorProfilerInfo::GetObjectSize, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetObjectSize
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetObjectSize
helpviewer_keywords:
- GetObjectSize method [.NET Framework profiling]
- ICorProfilerInfo::GetObjectSize method [.NET Framework profiling]
ms.assetid: 9f02e763-73f7-42cb-a41c-f78499d9482c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d366a0093ca82d2e5b3c40729777a1b6c0766bda
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049542"
---
# <a name="icorprofilerinfogetobjectsize-method"></a><span data-ttu-id="57f25-102">ICorProfilerInfo::GetObjectSize, méthode</span><span class="sxs-lookup"><span data-stu-id="57f25-102">ICorProfilerInfo::GetObjectSize Method</span></span>
<span data-ttu-id="57f25-103">Obtient la taille d’un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="57f25-103">Gets the size of a specified object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57f25-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57f25-104">Syntax</span></span>  
  
```  
HRESULT GetObjectSize(  
    [in]  ObjectID objectId,  
    [out] ULONG  *pcSize);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57f25-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57f25-105">Parameters</span></span>  
 `objectId`  
 <span data-ttu-id="57f25-106">[in] L’ID de l’objet.</span><span class="sxs-lookup"><span data-stu-id="57f25-106">[in] The ID of the object.</span></span>  
  
 `pcSize`  
 <span data-ttu-id="57f25-107">[out] Pointeur vers la taille de l’objet, en octets.</span><span class="sxs-lookup"><span data-stu-id="57f25-107">[out] A pointer to the object's size, in bytes.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="57f25-108">Notes</span><span class="sxs-lookup"><span data-stu-id="57f25-108">Remarks</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="57f25-109">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="57f25-109">This method is obsolete.</span></span> <span data-ttu-id="57f25-110">Renvoie la COR_E_OVERFLOW objets supérieur à 4 Go sur les plateformes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="57f25-110">It returns COR_E_OVERFLOW for objects greater than 4GB on 64-bit platforms.</span></span> <span data-ttu-id="57f25-111">Utilisez le [ICorProfilerInfo4::GetObjectSize2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-getobjectsize2-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="57f25-111">Use the  [ICorProfilerInfo4::GetObjectSize2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-getobjectsize2-method.md) method instead.</span></span>  
  
 <span data-ttu-id="57f25-112">Différents objets des mêmes types ont souvent la même taille.</span><span class="sxs-lookup"><span data-stu-id="57f25-112">Different objects of the same types often have the same size.</span></span> <span data-ttu-id="57f25-113">Toutefois, certains types, tels que des tableaux ou des chaînes, peuvent avoir une taille différente pour chaque objet.</span><span class="sxs-lookup"><span data-stu-id="57f25-113">However, some types, such as arrays or strings, may have a different size for each object.</span></span>  
  
 <span data-ttu-id="57f25-114">La taille retournée par la `GetObjectSize` méthode n’inclut pas de marge intérieure alignement susceptibles d’apparaître une fois que l’objet est sur le tas de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="57f25-114">The size returned by the `GetObjectSize` method does not include any alignment padding that may appear after the object is on the garbage collection heap.</span></span> <span data-ttu-id="57f25-115">Si vous utilisez le `GetObjectSize` méthode pour passer d’un objet à l’objet sur le tas de garbage collection, ajoutez alignement remplissage manuellement, en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="57f25-115">If you use the `GetObjectSize` method to advance from object to object on the garbage collection heap, add alignment padding manually, as necessary.</span></span>  
  
- <span data-ttu-id="57f25-116">Sur Windows 32 bits, COR_PRF_GC_GEN_0, COR_PRF_GC_GEN_1 et COR_PRF_GC_GEN_2 utilisent alignement de 4 octets, et COR_PRF_GC_LARGE_OBJECT_HEAP utilise l’alignement de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="57f25-116">On 32-bit Windows, COR_PRF_GC_GEN_0, COR_PRF_GC_GEN_1, and COR_PRF_GC_GEN_2 use 4-byte alignment, and COR_PRF_GC_LARGE_OBJECT_HEAP uses 8-byte alignment.</span></span>  
  
- <span data-ttu-id="57f25-117">Sur Windows 64 bits, l’alignement est toujours de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="57f25-117">On 64-bit Windows, the alignment is always 8 bytes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57f25-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57f25-118">Requirements</span></span>  
 <span data-ttu-id="57f25-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="57f25-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57f25-120">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="57f25-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="57f25-121">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="57f25-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="57f25-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57f25-122">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57f25-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57f25-123">See also</span></span>

- [<span data-ttu-id="57f25-124">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="57f25-124">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
