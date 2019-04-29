---
title: ICLRDataTarget::ReadVirtual, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.ReadVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::ReadVirtual
helpviewer_keywords:
- ReadVirtual method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::ReadVirtual method [.NET Framework debugging]
ms.assetid: da3769eb-1828-4aa1-b9ed-db4842136a43
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 38e2ec063d46ce9c890927391107888032e31378
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698094"
---
# <a name="iclrdatatargetreadvirtual-method"></a><span data-ttu-id="e6624-102">ICLRDataTarget::ReadVirtual, méthode</span><span class="sxs-lookup"><span data-stu-id="e6624-102">ICLRDataTarget::ReadVirtual Method</span></span>
<span data-ttu-id="e6624-103">Lit les données à partir de l’adresse de mémoire virtuelle spécifiée dans la mémoire tampon spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e6624-103">Reads data from the specified virtual memory address into the specified buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6624-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6624-104">Syntax</span></span>  
  
```  
HRESULT ReadVirtual (  
    [in] CLRDATA_ADDRESS    address,  
    [out, size_is(bytesRequested), length_is(*bytesRead)]   
        BYTE                *buffer,  
    [in] ULONG32            bytesRequested,  
    [out] ULONG32           *bytesRead  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6624-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6624-105">Parameters</span></span>  
 `address`  
 <span data-ttu-id="e6624-106">[in] CLRDATA_ADDRESS qui stocke l’adresse de mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="e6624-106">[in] A CLRDATA_ADDRESS that stores the virtual memory address.</span></span>  
  
 `buffer`  
 <span data-ttu-id="e6624-107">[out] Un pointeur vers une mémoire tampon qui reçoit les données.</span><span class="sxs-lookup"><span data-stu-id="e6624-107">[out] A pointer to a buffer that receives the data.</span></span>  
  
 `bytesRequested`  
 <span data-ttu-id="e6624-108">[in] La longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e6624-108">[in] The length of the buffer.</span></span>  
  
 `bytesRead`  
 <span data-ttu-id="e6624-109">[out] Pointeur vers le nombre d’octets retournés.</span><span class="sxs-lookup"><span data-stu-id="e6624-109">[out] A pointer to the number of bytes returned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6624-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6624-110">Requirements</span></span>  
 <span data-ttu-id="e6624-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e6624-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6624-112">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="e6624-112">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="e6624-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e6624-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e6624-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6624-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6624-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6624-115">See also</span></span>

- [<span data-ttu-id="e6624-116">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="e6624-116">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
