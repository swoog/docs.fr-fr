---
title: ICorDebugSymbolProvider::GetAssemblyImageBytes, méthode
ms.date: 03/30/2017
ms.assetid: 3db215aa-e180-4f70-8d23-6d5a0ffbc8e5
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 103e724c37ae356729dd5bba3ff66c0f443f6eaa
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61953523"
---
# <a name="icordebugsymbolprovidergetassemblyimagebytes-method"></a><span data-ttu-id="a9bd5-102">ICorDebugSymbolProvider::GetAssemblyImageBytes, méthode</span><span class="sxs-lookup"><span data-stu-id="a9bd5-102">ICorDebugSymbolProvider::GetAssemblyImageBytes Method</span></span>
<span data-ttu-id="a9bd5-103">Lit les données d’un assembly fusionné pour une adresse virtuelle relative (RVA) donnée dans l’assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-103">Reads data from a merged assembly given a relative virtual address (RVA) in the merged assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a9bd5-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9bd5-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyImageBytes(  
   [in] CORDB_ADDRESS rva,   
   [in] ULONG32 length,   
   [out] ICorDebugMemoryBuffer** ppMemoryBuffer  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a9bd5-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9bd5-105">Parameters</span></span>  
 `rva`  
 <span data-ttu-id="a9bd5-106">[in] Adresse virtuelle relative (RVA) dans un assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-106">[in] A relative virtual address (RVA) in a merged assembly.</span></span>  
  
 `length`  
 <span data-ttu-id="a9bd5-107">Nombre d'octets à lire à partir de l'assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-107">The number of bytes to read from the merged assembly.</span></span>  
  
 `ppMemoryBuffer`  
 <span data-ttu-id="a9bd5-108">Un pointeur vers l’adresse d’un [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) objet qui contient des informations sur la mémoire tampon avec des métadonnées de l’assembly fusionné.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-108">A pointer to the address of an [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) object that contains information about the memory buffer with merged assembly metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a9bd5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a9bd5-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="a9bd5-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="a9bd5-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a9bd5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9bd5-111">Requirements</span></span>  
 <span data-ttu-id="a9bd5-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a9bd5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a9bd5-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a9bd5-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a9bd5-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a9bd5-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a9bd5-115">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a9bd5-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9bd5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9bd5-116">See also</span></span>

- [<span data-ttu-id="a9bd5-117">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="a9bd5-117">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="a9bd5-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="a9bd5-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
