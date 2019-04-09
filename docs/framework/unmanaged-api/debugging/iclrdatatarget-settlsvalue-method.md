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
ms.openlocfilehash: 4c0be35772b10d89f90da5b33f47aa781034b13a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59152930"
---
# <a name="iclrdatatargetsettlsvalue-method"></a><span data-ttu-id="1805d-102">ICLRDataTarget::SetTLSValue, méthode</span><span class="sxs-lookup"><span data-stu-id="1805d-102">ICLRDataTarget::SetTLSValue Method</span></span>
<span data-ttu-id="1805d-103">Définit une valeur dans le stockage local des threads (TLS) du thread spécifié dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="1805d-103">Sets a value in the thread local storage (TLS) of the specified thread in the target process.</span></span> <span data-ttu-id="1805d-104">Cette méthode est appelée par les services d’accès de données common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="1805d-104">This method is called by the common language runtime (CLR) data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1805d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1805d-105">Syntax</span></span>  
  
```  
HRESULT SetTLSValue (  
    [in] ULONG32            threadID,  
    [in] ULONG32            index,  
    [in] CLRDATA_ADDRESS    value  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1805d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1805d-106">Parameters</span></span>  
 `threadID`  
 <span data-ttu-id="1805d-107">[in] L’identificateur de système d’exploitation d’un thread dans le processus cible.</span><span class="sxs-lookup"><span data-stu-id="1805d-107">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `index`  
 <span data-ttu-id="1805d-108">[in] Index de l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="1805d-108">[in] The index of the location.</span></span> <span data-ttu-id="1805d-109">Cette valeur doit être un index valide dans le magasin local du thread spécifié.</span><span class="sxs-lookup"><span data-stu-id="1805d-109">This value must be a valid index in the local store of the specified thread.</span></span>  
  
 `value`  
 <span data-ttu-id="1805d-110">[in] Un `CLRDATA_ADDRESS` valeur qui spécifie la valeur à placer dans l’emplacement TLS donné.</span><span class="sxs-lookup"><span data-stu-id="1805d-110">[in] A `CLRDATA_ADDRESS` value that specifies the value to place in the given TLS location.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1805d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1805d-111">Remarks</span></span>  
 <span data-ttu-id="1805d-112">Cette méthode est implémentée par le writer de l'application de débogage.</span><span class="sxs-lookup"><span data-stu-id="1805d-112">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1805d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1805d-113">Requirements</span></span>  
 <span data-ttu-id="1805d-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1805d-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1805d-115">**En-tête :** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="1805d-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="1805d-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1805d-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="1805d-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="1805d-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1805d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1805d-118">See also</span></span>

- [<span data-ttu-id="1805d-119">ICLRDataTarget, interface</span><span class="sxs-lookup"><span data-stu-id="1805d-119">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
