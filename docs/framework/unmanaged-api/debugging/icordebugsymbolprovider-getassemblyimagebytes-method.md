---
title: ICorDebugSymbolProvider::GetAssemblyImageBytes, méthode
ms.date: 03/30/2017
ms.assetid: 3db215aa-e180-4f70-8d23-6d5a0ffbc8e5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7975ca3da16be10285e618752981249602371c43
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418589"
---
# <a name="icordebugsymbolprovidergetassemblyimagebytes-method"></a><span data-ttu-id="4d9ce-102">ICorDebugSymbolProvider::GetAssemblyImageBytes, méthode</span><span class="sxs-lookup"><span data-stu-id="4d9ce-102">ICorDebugSymbolProvider::GetAssemblyImageBytes Method</span></span>
<span data-ttu-id="4d9ce-103">Lit les données d’un assembly fusionné pour une adresse virtuelle relative (RVA) donnée dans l’assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="4d9ce-103">Reads data from a merged assembly given a relative virtual address (RVA) in the merged assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4d9ce-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d9ce-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyImageBytes(  
   [in] CORDB_ADDRESS rva,   
   [in] ULONG32 length,   
   [out] ICorDebugMemoryBuffer** ppMemoryBuffer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4d9ce-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d9ce-105">Parameters</span></span>  
 `rva`  
 <span data-ttu-id="4d9ce-106">[in] Adresse virtuelle relative (RVA) dans un assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="4d9ce-106">[in] A relative virtual address (RVA) in a merged assembly.</span></span>  
  
 `length`  
 <span data-ttu-id="4d9ce-107">Nombre d’octets à lire à partir de l’assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="4d9ce-107">The number of bytes to read from the merged assembly.</span></span>  
  
 `ppMemoryBuffer`  
 <span data-ttu-id="4d9ce-108">Un pointeur vers l’adresse d’un [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) objet qui contient des informations sur la mémoire tampon avec des métadonnées de l’assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="4d9ce-108">A pointer to the address of an [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) object that contains information about the memory buffer with merged assembly metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4d9ce-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4d9ce-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4d9ce-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="4d9ce-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4d9ce-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4d9ce-111">Requirements</span></span>  
 <span data-ttu-id="4d9ce-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4d9ce-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4d9ce-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4d9ce-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4d9ce-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4d9ce-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4d9ce-115">**Versions du .NET framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4d9ce-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d9ce-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d9ce-116">See Also</span></span>  
 [<span data-ttu-id="4d9ce-117">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="4d9ce-117">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [<span data-ttu-id="4d9ce-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="4d9ce-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
