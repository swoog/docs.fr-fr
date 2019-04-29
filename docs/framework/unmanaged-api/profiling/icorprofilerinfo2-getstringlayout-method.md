---
title: ICorProfilerInfo2::GetStringLayout, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetStringLayout
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetStringLayout
helpviewer_keywords:
- GetStringLayout method [.NET Framework profiling]
- ICorProfilerInfo2::GetStringLayout method [.NET Framework profiling]
ms.assetid: 43189651-a535-4803-a1d1-f1c427ace2ca
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cc94c63edb602d87a7c08a9051eb2ef760834477
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791653"
---
# <a name="icorprofilerinfo2getstringlayout-method"></a><span data-ttu-id="d5a77-102">ICorProfilerInfo2::GetStringLayout, méthode</span><span class="sxs-lookup"><span data-stu-id="d5a77-102">ICorProfilerInfo2::GetStringLayout Method</span></span>
<span data-ttu-id="d5a77-103">Obtient des informations sur la disposition d'un objet string.</span><span class="sxs-lookup"><span data-stu-id="d5a77-103">Gets information about the layout of a string object.</span></span> <span data-ttu-id="d5a77-104">Cette méthode est déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)]et est remplacée par la [ICorProfilerInfo3::GetStringLayout2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getstringlayout2-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="d5a77-104">This method is deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], and is superseded by the [ICorProfilerInfo3::GetStringLayout2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-getstringlayout2-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5a77-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5a77-105">Syntax</span></span>  
  
```  
HRESULT GetStringLayout(  
    [out] ULONG *pBufferLengthOffset,  
    [out] ULONG *pStringLengthOffset,  
    [out] ULONG *pBufferOffset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d5a77-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5a77-106">Parameters</span></span>  
 `pBufferLengthOffset`  
 <span data-ttu-id="d5a77-107">[out] Un pointeur vers l’offset de l’emplacement, relatif à la `ObjectID` pointeur, qui stocke la longueur de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d5a77-107">[out] A pointer to the offset of the location, relative to the `ObjectID` pointer, that stores the length of the string.</span></span> <span data-ttu-id="d5a77-108">La longueur est stockée comme un `DWORD`.</span><span class="sxs-lookup"><span data-stu-id="d5a77-108">The length is stored as a `DWORD`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d5a77-109">Ce paramètre retourne la longueur de la chaîne elle-même, pas la longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d5a77-109">This parameter returns the length of the string itself, not the length of the buffer.</span></span> <span data-ttu-id="d5a77-110">La longueur de la mémoire tampon n’est plus disponible.</span><span class="sxs-lookup"><span data-stu-id="d5a77-110">The length of the buffer is no longer available.</span></span>  
  
 `PStringLengthOffset`  
 <span data-ttu-id="d5a77-111">[out] Un pointeur vers l’offset de l’emplacement, relatif à la `ObjectID` pointeur, qui stocke la longueur de la chaîne elle-même.</span><span class="sxs-lookup"><span data-stu-id="d5a77-111">[out] A pointer to the offset of the location, relative to the `ObjectID` pointer, that stores the length of the string itself.</span></span> <span data-ttu-id="d5a77-112">La longueur est stockée comme un `DWORD`.</span><span class="sxs-lookup"><span data-stu-id="d5a77-112">The length is stored as a `DWORD`.</span></span>  
  
 `pBufferOffset`  
 <span data-ttu-id="d5a77-113">[out] Un pointeur vers l’offset de la mémoire tampon, relative à la `ObjectID` pointeur, qui stocke la chaîne de caractères larges.</span><span class="sxs-lookup"><span data-stu-id="d5a77-113">[out] A pointer to the offset of the buffer, relative to the `ObjectID` pointer, that stores the string of wide characters.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d5a77-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d5a77-114">Remarks</span></span>  
 <span data-ttu-id="d5a77-115">Le `GetStringLayout` méthode obtient les offsets, relatif à la `ObjectID` pointeur, des emplacements dans lesquels sont stockés les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d5a77-115">The `GetStringLayout` method gets the offsets, relative to the `ObjectID` pointer, of the locations in which the following are stored:</span></span>  
  
- <span data-ttu-id="d5a77-116">La longueur de la mémoire tampon de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d5a77-116">The length of the string's buffer.</span></span>  
  
- <span data-ttu-id="d5a77-117">La longueur de la chaîne elle-même.</span><span class="sxs-lookup"><span data-stu-id="d5a77-117">The length of the string itself.</span></span>  
  
- <span data-ttu-id="d5a77-118">La mémoire tampon qui contient la chaîne réelle de caractères larges.</span><span class="sxs-lookup"><span data-stu-id="d5a77-118">The buffer that contains the actual string of wide characters.</span></span>  
  
 <span data-ttu-id="d5a77-119">Chaînes peuvent être se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="d5a77-119">Strings may be null-terminated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d5a77-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5a77-120">Requirements</span></span>  
 <span data-ttu-id="d5a77-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d5a77-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d5a77-122">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="d5a77-122">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="d5a77-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d5a77-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d5a77-124">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d5a77-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d5a77-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5a77-125">See also</span></span>

- [<span data-ttu-id="d5a77-126">ICorProfilerInfo, interface</span><span class="sxs-lookup"><span data-stu-id="d5a77-126">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [<span data-ttu-id="d5a77-127">ICorProfilerInfo2, interface</span><span class="sxs-lookup"><span data-stu-id="d5a77-127">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
