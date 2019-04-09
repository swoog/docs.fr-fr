---
title: Icordebugsymbolprovider::getinstancefieldsymbols, méthode
ms.date: 03/30/2017
ms.assetid: a29b9233-ee67-4b53-b8bc-c00b281e7edb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9ea9afdd2c032e99d7feee6b2935161c70c56787
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59187692"
---
# <a name="icordebugsymbolprovidergetinstancefieldsymbols-method"></a><span data-ttu-id="54a6a-102">Icordebugsymbolprovider::getinstancefieldsymbols, méthode</span><span class="sxs-lookup"><span data-stu-id="54a6a-102">ICorDebugSymbolProvider::GetInstanceFieldSymbols Method</span></span>
<span data-ttu-id="54a6a-103">Obtient les symboles de champ d'instance qui correspondent à une signature typespec.</span><span class="sxs-lookup"><span data-stu-id="54a6a-103">Gets the instance field symbols that correspond to a typespec signature.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="54a6a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54a6a-104">Syntax</span></span>  
  
```  
HRESULT GetInstanceFieldSymbols(  
   [in] ULONG32 cbSignature,  
   [in, size_is(cbSignature)]  BYTE typeSig[],  
   [in] ULONG32 cRequestedSymbols,  
   [out] ULONG32 *pcFetchedSymbols,  
   [out, size_is(cRequestedSymbols), length_is(*pcFetchedSymbols)] ICorDebugInstanceFieldSymbol *pSymbols[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="54a6a-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54a6a-105">Parameters</span></span>  
 `cbSignature`  
 <span data-ttu-id="54a6a-106">[in] Nombre d'octets dans le tableau `typeSig`.</span><span class="sxs-lookup"><span data-stu-id="54a6a-106">[in] The number of bytes in the `typeSig` array.</span></span>  
  
 `typeSig`  
 <span data-ttu-id="54a6a-107">[in] Tableau d'octets contenant la signature `typespec`.</span><span class="sxs-lookup"><span data-stu-id="54a6a-107">[in] A byte array that contains the `typespec` signature.</span></span>  
  
 `cRequestedSymbols`  
 <span data-ttu-id="54a6a-108">[in] Nombre de symboles demandés.</span><span class="sxs-lookup"><span data-stu-id="54a6a-108">[in] The number of symbols requested.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="54a6a-109">[out] Pointeur vers le nombre de symboles récupérés par la méthode.</span><span class="sxs-lookup"><span data-stu-id="54a6a-109">[out] A pointer to the number of symbols retrieved by the method.</span></span>  
  
 `pSymbols`  
 <span data-ttu-id="54a6a-110">[out] Un pointeur vers un [ICorDebugStaticFieldSymbol](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md) tableau qui contient les symboles de champ d’instance demandée.</span><span class="sxs-lookup"><span data-stu-id="54a6a-110">[out] A pointer to an [ICorDebugStaticFieldSymbol](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md) array that contains the requested instance field symbols.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="54a6a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="54a6a-111">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="54a6a-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="54a6a-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="54a6a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54a6a-113">Requirements</span></span>  
 <span data-ttu-id="54a6a-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="54a6a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="54a6a-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="54a6a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="54a6a-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="54a6a-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="54a6a-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="54a6a-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="54a6a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54a6a-118">See also</span></span>

- [<span data-ttu-id="54a6a-119">GetStaticFieldSymbols, méthode</span><span class="sxs-lookup"><span data-stu-id="54a6a-119">GetStaticFieldSymbols Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-getstaticfieldsymbols-method.md)
- [<span data-ttu-id="54a6a-120">ICorDebugSymbolProvider, interface</span><span class="sxs-lookup"><span data-stu-id="54a6a-120">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)
- [<span data-ttu-id="54a6a-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="54a6a-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
