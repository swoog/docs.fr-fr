---
title: ICorDebugMergedAssemblyRecord::GetVersion, méthode
ms.date: 03/30/2017
ms.assetid: c6858b06-ae26-4312-b325-ea6025016675
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 36cf8647b3caafeaae2db3c2fd53471496e922fa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61666947"
---
# <a name="icordebugmergedassemblyrecordgetversion-method"></a><span data-ttu-id="0a3eb-102">ICorDebugMergedAssemblyRecord::GetVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="0a3eb-102">ICorDebugMergedAssemblyRecord::GetVersion Method</span></span>
<span data-ttu-id="0a3eb-103">Obtient les informations de version de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="0a3eb-103">Gets the assembly's version information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a3eb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a3eb-104">Syntax</span></span>  
  
```  
HRESULT GetVersion(  
   [out] USHORT *pMajor,   
   [out] USHORT *pMinor,   
   [out] USHORT *pBuild,   
   [out] USHORT *pRevision  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0a3eb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a3eb-105">Parameters</span></span>  
 `pMajor`  
 <span data-ttu-id="0a3eb-106">[out] Pointeur vers le numéro de version principale.</span><span class="sxs-lookup"><span data-stu-id="0a3eb-106">[out] A pointer to the major version number.</span></span>  
  
 `pMinor`  
 <span data-ttu-id="0a3eb-107">[out] Pointeur vers le numéro de version secondaire.</span><span class="sxs-lookup"><span data-stu-id="0a3eb-107">[out] A pointer to the minor version number.</span></span>  
  
 `pBuild`  
 <span data-ttu-id="0a3eb-108">[out] Pointeur vers le numéro de build.</span><span class="sxs-lookup"><span data-stu-id="0a3eb-108">[out] A pointer to the build number.</span></span>  
  
 `pRevision`  
 <span data-ttu-id="0a3eb-109">[out] Pointeur vers le numéro de révision.</span><span class="sxs-lookup"><span data-stu-id="0a3eb-109">[out] A pointer to the revision number.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0a3eb-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0a3eb-110">Remarks</span></span>  
 <span data-ttu-id="0a3eb-111">Pour plus d'informations sur les numéros de version d'assembly, consultez la rubrique de la classe <xref:System.Version>.</span><span class="sxs-lookup"><span data-stu-id="0a3eb-111">For information on assembly version numbers, see the <xref:System.Version> class topic.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0a3eb-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="0a3eb-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a3eb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a3eb-113">Requirements</span></span>  
 <span data-ttu-id="0a3eb-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a3eb-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a3eb-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0a3eb-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0a3eb-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0a3eb-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0a3eb-117">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0a3eb-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a3eb-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a3eb-118">See also</span></span>

- [<span data-ttu-id="0a3eb-119">ICorDebugMergedAssemblyRecord, interface</span><span class="sxs-lookup"><span data-stu-id="0a3eb-119">ICorDebugMergedAssemblyRecord Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="0a3eb-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="0a3eb-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
