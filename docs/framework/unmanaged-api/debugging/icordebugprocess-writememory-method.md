---
title: ICorDebugProcess::WriteMemory, méthode
ms.date: 03/30/2017
api_name:
- ICorDebugProcess.WriteMemory
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::WriteMemory
helpviewer_keywords:
- ICorDebugProcess::WriteMemory method [.NET Framework debugging]
- WriteMemory method [.NET Framework debugging]
ms.assetid: d5c07d86-045d-4391-893b-0bcd2959f90e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6da4c282c7f969a406a657d1e30dd6120a32b4e3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420906"
---
# <a name="icordebugprocesswritememory-method"></a><span data-ttu-id="ee98c-102">ICorDebugProcess::WriteMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="ee98c-102">ICorDebugProcess::WriteMemory Method</span></span>
<span data-ttu-id="ee98c-103">Écrit des données dans une zone de mémoire dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="ee98c-103">Writes data to an area of memory in this process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee98c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee98c-104">Syntax</span></span>  
  
```  
HRESULT WriteMemory(  
    [in]  CORDB_ADDRESS address,  
    [in]  DWORD size,  
    [in, size_is(size)] BYTE buffer[],  
    [out] SIZE_T *written);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ee98c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee98c-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="ee98c-106">[in] A `CORDB_ADDRESS` valeur qui est l’adresse de base de la zone de mémoire vers lequel les données est écrites.</span><span class="sxs-lookup"><span data-stu-id="ee98c-106">[in] A `CORDB_ADDRESS` value that is the base address of the memory area to which data is written.</span></span> <span data-ttu-id="ee98c-107">Avant le transfert de données se produit, le système vérifie que la zone de mémoire de la taille spécifiée, en commençant à l’adresse de base est accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="ee98c-107">Before data transfer occurs, the system verifies that the memory area of the specified size, beginning at the base address, is accessible for writing.</span></span> <span data-ttu-id="ee98c-108">Si elle n’est pas accessible, la méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="ee98c-108">If it is not accessible, the method fails.</span></span>  
  
 `size`  
 <span data-ttu-id="ee98c-109">[in] Le nombre d’octets à écrire dans la zone de mémoire.</span><span class="sxs-lookup"><span data-stu-id="ee98c-109">[in] The number of bytes to be written to the memory area.</span></span>  
  
 `buffer`  
 <span data-ttu-id="ee98c-110">[in] Une mémoire tampon qui contient les données à écrire.</span><span class="sxs-lookup"><span data-stu-id="ee98c-110">[in] A buffer that contains data to be written.</span></span>  
  
 `written`  
 <span data-ttu-id="ee98c-111">[out] Pointeur vers une variable qui reçoit le nombre d’octets écrits dans la zone de mémoire dans ce processus.</span><span class="sxs-lookup"><span data-stu-id="ee98c-111">[out] A pointer to a variable that receives the number of bytes written to the memory area in this process.</span></span> <span data-ttu-id="ee98c-112">Si `written` est NULL, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ee98c-112">If `written` is NULL, this parameter is ignored.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ee98c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ee98c-113">Remarks</span></span>  
 <span data-ttu-id="ee98c-114">Données sont automatiquement écrite derrière les points d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="ee98c-114">Data is automatically written behind any breakpoints.</span></span> <span data-ttu-id="ee98c-115">Dans le .NET Framework version 2.0, les débogueurs natifs doivent utilisez pas cette méthode pour injecter des points d’arrêt dans le flux d’instructions.</span><span class="sxs-lookup"><span data-stu-id="ee98c-115">In the .NET Framework version 2.0, native debuggers should not use this method to inject breakpoints into the instruction stream.</span></span> <span data-ttu-id="ee98c-116">Utilisez [ICorDebugProcess2::SetUnmanagedBreakpoint](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setunmanagedbreakpoint-method.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="ee98c-116">Use [ICorDebugProcess2::SetUnmanagedBreakpoint](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess2-setunmanagedbreakpoint-method.md) instead.</span></span>  
  
 <span data-ttu-id="ee98c-117">Le `WriteMemory` méthode doit être utilisée uniquement en dehors du code managé.</span><span class="sxs-lookup"><span data-stu-id="ee98c-117">The `WriteMemory` method should be used only outside of managed code.</span></span> <span data-ttu-id="ee98c-118">Cette méthode peut endommager le runtime pour une utilisation incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ee98c-118">This method can corrupt the runtime if used improperly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ee98c-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ee98c-119">Requirements</span></span>  
 <span data-ttu-id="ee98c-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ee98c-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee98c-121">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ee98c-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ee98c-122">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ee98c-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ee98c-123">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee98c-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
