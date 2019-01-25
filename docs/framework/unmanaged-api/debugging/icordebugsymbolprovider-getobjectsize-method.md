---
title: ICorDebugSymbolProvider::GetObjectSize, méthode
ms.date: 03/30/2017
ms.assetid: 3c564396-ac64-4ef3-b4f6-df96f1d46fc7
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 99714a50d0b3966476cea2f7ed02f04a2ebf6cea
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54512409"
---
# <a name="icordebugsymbolprovidergetobjectsize-method"></a><span data-ttu-id="aaf41-102">ICorDebugSymbolProvider::GetObjectSize, méthode</span><span class="sxs-lookup"><span data-stu-id="aaf41-102">ICorDebugSymbolProvider::GetObjectSize Method</span></span>
<span data-ttu-id="aaf41-103">Retourne la taille d'un objet en fonction de sa signature typespec.</span><span class="sxs-lookup"><span data-stu-id="aaf41-103">Returns the object size for an object based on its typespec signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aaf41-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaf41-104">Syntax</span></span>  
  
```  
HRESULT GetObjectSize(  
   [in] ULONG32 cbSignature,  
   [in, size_is(cbSignature)]  BYTE typeSig[],  
   [out] ULONG32 *pObjectSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aaf41-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aaf41-105">Parameters</span></span>  
 `cbSignature`  
 <span data-ttu-id="aaf41-106">[in] Nombre d'octets dans la signature typespec.</span><span class="sxs-lookup"><span data-stu-id="aaf41-106">[in] The number of bytes in the typespec signature.</span></span>  
  
 <span data-ttu-id="aaf41-107">typeSig</span><span class="sxs-lookup"><span data-stu-id="aaf41-107">typeSig</span></span>  
 <span data-ttu-id="aaf41-108">[in] Signature typespec.</span><span class="sxs-lookup"><span data-stu-id="aaf41-108">[in] The typespec signature.</span></span>  
  
 `pObjectSize`  
 <span data-ttu-id="aaf41-109">[out] Pointeur vers la taille de l'objet.</span><span class="sxs-lookup"><span data-stu-id="aaf41-109">[out] A pointer to the size of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="aaf41-110">Notes</span><span class="sxs-lookup"><span data-stu-id="aaf41-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="aaf41-111">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="aaf41-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aaf41-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aaf41-112">Requirements</span></span>  
 <span data-ttu-id="aaf41-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aaf41-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aaf41-114">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="aaf41-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="aaf41-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aaf41-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aaf41-116">**Versions du .NET Framework :** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aaf41-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="aaf41-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaf41-117">See also</span></span>
- [<span data-ttu-id="aaf41-118">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="aaf41-118">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="aaf41-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="aaf41-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
