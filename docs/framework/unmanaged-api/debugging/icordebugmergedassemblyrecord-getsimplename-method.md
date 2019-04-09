---
title: ICorDebugMergedAssemblyRecord::GetSimpleName, méthode
ms.date: 03/30/2017
ms.assetid: bc3410f6-ebca-4bca-9b45-fc38c74fa9cb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: df142ea8f02d5cefc5c63a2d376afb331b4379ce
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59197982"
---
# <a name="icordebugmergedassemblyrecordgetsimplename-method"></a><span data-ttu-id="7622c-102">ICorDebugMergedAssemblyRecord::GetSimpleName, méthode</span><span class="sxs-lookup"><span data-stu-id="7622c-102">ICorDebugMergedAssemblyRecord::GetSimpleName Method</span></span>
<span data-ttu-id="7622c-103">Obtient le nom simple de l'assembly.</span><span class="sxs-lookup"><span data-stu-id="7622c-103">Gets the simple name of the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7622c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7622c-104">Syntax</span></span>  
  
```  
HRESULT GetSimpleName(  
   [in] ULONG32 cchName,   
   [out] ULONG32 *pcchName,   
   [out, size_is(cchName), length_is(*pcchName)] WCHAR szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="7622c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7622c-105">Parameters</span></span>  
 `cchName`  
 <span data-ttu-id="7622c-106">[in] Nombre de caractères dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="7622c-106">[in] The number of characters in the `szName` buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="7622c-107">[out] Pointeur vers le nombre de caractères réellement écrits dans la mémoire tampon `szName`.</span><span class="sxs-lookup"><span data-stu-id="7622c-107">[out] A pointer to the number of characters actually written to the `szName` buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="7622c-108">Pointeur vers un tableau de caractères.</span><span class="sxs-lookup"><span data-stu-id="7622c-108">A pointer to a character array.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7622c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7622c-109">Remarks</span></span>  
 <span data-ttu-id="7622c-110">Cette méthode récupère le nom simple d'un assembly (par exemple, « System.Collections »), sans extension de fichier, version, culture ni jeton de clé publique.</span><span class="sxs-lookup"><span data-stu-id="7622c-110">This method retrieves the simple name of an assembly (such as "System.Collections"), without a file extension, version, culture, or public key token.</span></span> <span data-ttu-id="7622c-111">Elle correspond à la propriété <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="7622c-111">It corresponds to the <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> property in managed code.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7622c-112">Cette méthode est uniquement disponible avec .NET Native.</span><span class="sxs-lookup"><span data-stu-id="7622c-112">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7622c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7622c-113">Requirements</span></span>  
 <span data-ttu-id="7622c-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7622c-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7622c-115">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7622c-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7622c-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7622c-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="7622c-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="7622c-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="7622c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7622c-118">See also</span></span>

- [<span data-ttu-id="7622c-119">ICorDebugMergedAssemblyRecord, interface</span><span class="sxs-lookup"><span data-stu-id="7622c-119">ICorDebugMergedAssemblyRecord Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="7622c-120">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="7622c-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
