---
title: ICorProfilerInfo3::GetRuntimeInformation, méthode
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetRuntimeInformation Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetRuntimeInformation
helpviewer_keywords:
- GetRuntimeInformation method [.NET Framework profiling]
- ICorProfilerInfo3::GetRuntimeInformation method [.NET Framework profiling]
ms.assetid: 4400fb8c-0407-4791-8557-f011fd2aee51
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a13e3e525c7f019e7dc49111b88ac374345830af
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59164929"
---
# <a name="icorprofilerinfo3getruntimeinformation-method"></a><span data-ttu-id="af3f8-102">ICorProfilerInfo3::GetRuntimeInformation, méthode</span><span class="sxs-lookup"><span data-stu-id="af3f8-102">ICorProfilerInfo3::GetRuntimeInformation Method</span></span>
<span data-ttu-id="af3f8-103">Fournit des informations de version sur le common language runtime (CLR) qui est en cours de profilage.</span><span class="sxs-lookup"><span data-stu-id="af3f8-103">Provides version information about the common language runtime (CLR) that is being profiled.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="af3f8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af3f8-104">Syntax</span></span>  
  
```  
HRESULT GetRuntimeInformation(  
       [out] USHORT *pClrInstanceId,  
       [out] COR_PRF_RUNTIME_TYPE *pRuntimeType,  
       [out] USHORT *pMajorVersion,  
       [out] USHORT *pMinorVersion,  
       [out] USHORT *pBuildNumber,  
       [out] USHORT *pQFEVersion,  
       [in]  ULONG  cchVersionString,  
       [out] ULONG  *pcchVersionString,  
       [out, size_is(cchVersionString), length_is(*pcchVersionString)]  
                   WCHAR  szVersionString[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="af3f8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af3f8-105">Parameters</span></span>  
 `pClrInstanceId`  
 <span data-ttu-id="af3f8-106">[out] ID représentatif d’une instance CLR en cours d’exécution dans un processus.</span><span class="sxs-lookup"><span data-stu-id="af3f8-106">[out] The representative ID of a running CLR instance in a process.</span></span> <span data-ttu-id="af3f8-107">Ceci est le même que le `ClrInstanceID` que le suivi d’événements pour l’événement de démarrage de Windows (ETW) signale.</span><span class="sxs-lookup"><span data-stu-id="af3f8-107">This is the same as the `ClrInstanceID` that the event tracing for Windows (ETW) startup event reports.</span></span>  
  
 `pRuntimeType`  
 <span data-ttu-id="af3f8-108">[out] Le type de runtime.</span><span class="sxs-lookup"><span data-stu-id="af3f8-108">[out] The runtime type.</span></span> <span data-ttu-id="af3f8-109">Ce paramètre retourne `COR_PRF_DESKTOP_CLR` pour la version de bureau du CLR, ou `COR_PRF_CORE_CLR` pour la version principale du CLR utilisée dans Silverlight.</span><span class="sxs-lookup"><span data-stu-id="af3f8-109">This parameter returns `COR_PRF_DESKTOP_CLR` for the desktop version of the CLR, or `COR_PRF_CORE_CLR` for the core version of the CLR used in Silverlight.</span></span>  
  
 `pMajorVersion`  
 <span data-ttu-id="af3f8-110">[out] Numéro de version principale du CLR.</span><span class="sxs-lookup"><span data-stu-id="af3f8-110">[out] The major version number of the CLR.</span></span>  
  
 `pMinorVersion`  
 <span data-ttu-id="af3f8-111">[out] Numéro de version mineure du CLR.</span><span class="sxs-lookup"><span data-stu-id="af3f8-111">[out] The minor version number of the CLR.</span></span>  
  
 `pBuildVersion`  
 <span data-ttu-id="af3f8-112">[out] Le numéro de build du CLR.</span><span class="sxs-lookup"><span data-stu-id="af3f8-112">[out] The build version number of the CLR.</span></span>  
  
 `pQFEVersion`  
 <span data-ttu-id="af3f8-113">[out] Le numéro de version du CLR qui est associé à une mise à jour logicielle.</span><span class="sxs-lookup"><span data-stu-id="af3f8-113">[out] The version number of the CLR that is associated with a software update.</span></span>  
  
 `cchVersionString`  
 <span data-ttu-id="af3f8-114">[in] La longueur, en caractères, de la mémoire tampon qui `szVersionString` pointe vers.</span><span class="sxs-lookup"><span data-stu-id="af3f8-114">[in] The length, in characters, of the buffer that `szVersionString` points to.</span></span>  
  
 `pcchVersionString`  
 <span data-ttu-id="af3f8-115">[out] La longueur, en caractères, de `szVersionString`.</span><span class="sxs-lookup"><span data-stu-id="af3f8-115">[out] The length, in characters, of `szVersionString`.</span></span>  
  
 `szVersionString`  
 <span data-ttu-id="af3f8-116">[out] La chaîne de version CLR.</span><span class="sxs-lookup"><span data-stu-id="af3f8-116">[out] The CLR version string.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="af3f8-117">Notes</span><span class="sxs-lookup"><span data-stu-id="af3f8-117">Remarks</span></span>  
 <span data-ttu-id="af3f8-118">Vous pouvez passer null pour n’importe quel paramètre.</span><span class="sxs-lookup"><span data-stu-id="af3f8-118">You may pass null for any parameter.</span></span> <span data-ttu-id="af3f8-119">Toutefois, `pcchVersionString` ne peut pas être null, sauf si `szVersionString` a également la valeur null.</span><span class="sxs-lookup"><span data-stu-id="af3f8-119">However, `pcchVersionString` cannot be null unless `szVersionString` is also null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="af3f8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af3f8-120">Requirements</span></span>  
 <span data-ttu-id="af3f8-121">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="af3f8-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="af3f8-122">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="af3f8-122">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="af3f8-123">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="af3f8-123">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="af3f8-124">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="af3f8-124">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="af3f8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af3f8-125">See also</span></span>

- [<span data-ttu-id="af3f8-126">ICorProfilerInfo3, interface</span><span class="sxs-lookup"><span data-stu-id="af3f8-126">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)
- [<span data-ttu-id="af3f8-127">Interfaces de profilage</span><span class="sxs-lookup"><span data-stu-id="af3f8-127">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
- [<span data-ttu-id="af3f8-128">Profilage</span><span class="sxs-lookup"><span data-stu-id="af3f8-128">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)
