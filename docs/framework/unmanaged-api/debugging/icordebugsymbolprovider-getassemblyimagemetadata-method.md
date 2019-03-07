---
title: ICorDebugSymbolProvider::GetAssemblyImageMetadata, méthode
ms.date: 03/30/2017
ms.assetid: c3c9de67-b865-4ecf-b887-1f1d0719a0c0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2cb255330937b00a987ee0d07f0332d04fe1746d
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57489980"
---
# <a name="icordebugsymbolprovidergetassemblyimagemetadata-method"></a><span data-ttu-id="ef9c0-102">ICorDebugSymbolProvider::GetAssemblyImageMetadata, méthode</span><span class="sxs-lookup"><span data-stu-id="ef9c0-102">ICorDebugSymbolProvider::GetAssemblyImageMetadata Method</span></span>
<span data-ttu-id="ef9c0-103">Retourne les métadonnées d'un assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="ef9c0-103">Returns the metadata from a merged assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef9c0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef9c0-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyImageMetadata(  
   [out] ICorDebugMemoryBuffer** ppMemoryBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ef9c0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef9c0-105">Parameters</span></span>  
 `ppMemoryBuffer`  
 <span data-ttu-id="ef9c0-106">[out] Un pointeur vers l’adresse d’un [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) objet qui contient des informations sur la taille et l’adresse des métadonnées de l’assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="ef9c0-106">[out] A pointer to the address of an [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) object that contains information about the size and address of the merged assembly's metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ef9c0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="ef9c0-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ef9c0-108">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="ef9c0-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ef9c0-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ef9c0-109">Requirements</span></span>  
 <span data-ttu-id="ef9c0-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ef9c0-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef9c0-111">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ef9c0-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ef9c0-112">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ef9c0-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ef9c0-113">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef9c0-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef9c0-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef9c0-114">See also</span></span>
- [<span data-ttu-id="ef9c0-115">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="ef9c0-115">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="ef9c0-116">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="ef9c0-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
