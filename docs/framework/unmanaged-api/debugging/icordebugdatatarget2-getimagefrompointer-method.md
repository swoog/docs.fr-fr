---
title: ICorDebugDataTarget2::GetImageFromPointer, méthode
ms.date: 03/30/2017
ms.assetid: 939cabe1-b647-4090-b662-eeec23c6c58d
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5dab9183075f563f52a4fc982eda5cb172556554
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59154373"
---
# <a name="icordebugdatatarget2getimagefrompointer-method"></a><span data-ttu-id="3cf42-102">ICorDebugDataTarget2::GetImageFromPointer, méthode</span><span class="sxs-lookup"><span data-stu-id="3cf42-102">ICorDebugDataTarget2::GetImageFromPointer Method</span></span>
<span data-ttu-id="3cf42-103">Retourne l'adresse de base et la taille d'un module à partir d'une adresse présente dans ce module.</span><span class="sxs-lookup"><span data-stu-id="3cf42-103">Returns the module base address and size from an address in that module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3cf42-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cf42-104">Syntax</span></span>  
  
```  
HRESULT GetImageFromPointer(  
   [in] CORDB_ADDRESS addr,   
   [out] CORDB_ADDRESS *pImageBase,   
   [out] ULONG32 *pSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3cf42-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cf42-105">Parameters</span></span>  
 `addr`  
 <span data-ttu-id="3cf42-106">Un [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente une adresse dans un module.</span><span class="sxs-lookup"><span data-stu-id="3cf42-106">A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) value that represents an address in a module.</span></span>  
  
 `pImageBase`  
 <span data-ttu-id="3cf42-107">[out] Un [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) valeur qui représente l’adresse de base du module.</span><span class="sxs-lookup"><span data-stu-id="3cf42-107">[out] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) value that represents the module's base address.</span></span>  
  
 `pSize`  
 <span data-ttu-id="3cf42-108">Pointeur vers la taille du module.</span><span class="sxs-lookup"><span data-stu-id="3cf42-108">A pointer to the module size.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3cf42-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3cf42-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3cf42-110">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="3cf42-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3cf42-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cf42-111">Requirements</span></span>  
 <span data-ttu-id="3cf42-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3cf42-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3cf42-113">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3cf42-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3cf42-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3cf42-114">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="3cf42-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3cf42-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3cf42-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cf42-116">See also</span></span>

- [<span data-ttu-id="3cf42-117">ICorDebugDataTarget2, interface</span><span class="sxs-lookup"><span data-stu-id="3cf42-117">ICorDebugDataTarget2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget2-interface.md)
- [<span data-ttu-id="3cf42-118">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3cf42-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
