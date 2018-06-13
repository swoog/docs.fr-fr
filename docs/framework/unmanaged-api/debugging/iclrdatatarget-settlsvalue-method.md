---
title: ICLRDataTarget::SetTLSValue, méthode
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.SetTLSValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::SetTLSValue
helpviewer_keywords:
- ICLRDataTarget::SetTLSValue method [.NET Framework debugging]
- SetTLSValue method [.NET Framework debugging]
ms.assetid: 4a2d6a24-749a-47ad-9f01-4517203d3f35
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 18733c2d643a75f9bb11159ba4acdbc8ab064c55
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33404102"
---
# <a name="iclrdatatargetsettlsvalue-method"></a><span data-ttu-id="3c135-102">ICLRDataTarget::SetTLSValue, méthode</span><span class="sxs-lookup"><span data-stu-id="3c135-102">ICLRDataTarget::SetTLSValue Method</span></span>
<span data-ttu-id="3c135-103">Définit une valeur dans le stockage local des threads (TLS) du thread spécifié dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="3c135-103">Sets a value in the thread local storage (TLS) of the specified thread in the target process.</span></span> <span data-ttu-id="3c135-104">Cette méthode est appelée par les services d’accès données common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="3c135-104">This method is called by the common language runtime (CLR) data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c135-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c135-105">Syntax</span></span>  
  
```  
HRESULT SetTLSValue (  
    [in] ULONG32            threadID,  
    [in] ULONG32            index,  
    [in] CLRDATA_ADDRESS    value  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3c135-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c135-106">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="3c135-107">[in] L’identificateur de système d’exploitation d’un thread dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="3c135-107">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `index`  
 <span data-ttu-id="3c135-108">[in] Index de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="3c135-108">[in] The index of the location.</span></span> <span data-ttu-id="3c135-109">Cette valeur doit être un index valide dans le magasin local du thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="3c135-109">This value must be a valid index in the local store of the specified thread.</span></span>  
  
 `value`  
 <span data-ttu-id="3c135-110">[in] A `CLRDATA_ADDRESS` valeur qui spécifie la valeur à placer dans l’emplacement de TLS donné.</span><span class="sxs-lookup"><span data-stu-id="3c135-110">[in] A `CLRDATA_ADDRESS` value that specifies the value to place in the given TLS location.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3c135-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3c135-111">Remarks</span></span>  
 <span data-ttu-id="3c135-112">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="3c135-112">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c135-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3c135-113">Requirements</span></span>  
 <span data-ttu-id="3c135-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3c135-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c135-115">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="3c135-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="3c135-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c135-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c135-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c135-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c135-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c135-118">See Also</span></span>  
 [<span data-ttu-id="3c135-119">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="3c135-119">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
