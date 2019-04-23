---
title: ICorDebugProcess7::SetWriteableMetadataUpdateMode, méthode
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugProcess7.SetWriteableMetadataUpdateMode
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 8589bba7-7304-45ba-9e31-7bf43dfd5c19
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 94e2f1c13c91c50daa5730898adf0aedf00f6579
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59092615"
---
# <a name="icordebugprocess7setwriteablemetadataupdatemode-method"></a><span data-ttu-id="282e6-102">ICorDebugProcess7::SetWriteableMetadataUpdateMode, méthode</span><span class="sxs-lookup"><span data-stu-id="282e6-102">ICorDebugProcess7::SetWriteableMetadataUpdateMode Method</span></span>
<span data-ttu-id="282e6-103">[Pris en charge dans .NET Framework 4.5.2 et ultérieur]</span><span class="sxs-lookup"><span data-stu-id="282e6-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="282e6-104">Configure la façon dont le débogueur gère les mises à jour en mémoire des métadonnées dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="282e6-104">Configures how the debugger handles in-memory updates to metadata within the target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="282e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="282e6-105">Syntax</span></span>  
  
```cpp
HRESULT SetWriteableMetadataUpdateMode(  
   WriteableMetadataUpdateMode flags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="282e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="282e6-106">Parameters</span></span>  
 `flags`  
 <span data-ttu-id="282e6-107">Un [WriteableMetadataUpdateMode](../../../../docs/framework/unmanaged-api/debugging/writeablemetadataupdatemode-enumeration.md) valeur d’énumération qui spécifie si les mises à jour en mémoire des métadonnées dans le processus cible sont visibles (`WriteableMetadataUpdateMode::AlwaysShowUpdates`) ou non visibles (`WriteableMetadataUpdateMode::LegacyCompatPolicy`) pour le débogueur.</span><span class="sxs-lookup"><span data-stu-id="282e6-107">A [WriteableMetadataUpdateMode](../../../../docs/framework/unmanaged-api/debugging/writeablemetadataupdatemode-enumeration.md) enumeration value that specifies whether in-memory updates to metadata in the target process are visible (`WriteableMetadataUpdateMode::AlwaysShowUpdates`) or not visible (`WriteableMetadataUpdateMode::LegacyCompatPolicy`) to the debugger.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="282e6-108">Notes</span><span class="sxs-lookup"><span data-stu-id="282e6-108">Remarks</span></span>  
 <span data-ttu-id="282e6-109">Les mises à jour apportées aux métadonnées du processus cible peuvent provenir de Modifier et continuer, d'un profileur ou de <xref:System.Reflection.Emit?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="282e6-109">Updates to the metadata of the target process can come from Edit and Continue, a profiler, or <xref:System.Reflection.Emit?displayProperty=nameWithType>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="282e6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="282e6-110">Requirements</span></span>  
 <span data-ttu-id="282e6-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="282e6-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="282e6-112">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="282e6-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="282e6-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="282e6-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="282e6-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="282e6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="282e6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="282e6-115">See also</span></span>

- [<span data-ttu-id="282e6-116">ICorDebugProcess7, interface</span><span class="sxs-lookup"><span data-stu-id="282e6-116">ICorDebugProcess7 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess7-interface.md)
- [<span data-ttu-id="282e6-117">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="282e6-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
