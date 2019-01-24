---
title: CLRDataCreateInstance, fonction
ms.date: 03/30/2017
api_name:
- CLRDataCreateInstance
api_location:
- mscordbi.dll
- mscordacwks.dll
api_type:
- COM
f1_keywords:
- CLRDataCreateInstance
helpviewer_keywords:
- CLRDataCreateInstance function [.NET Framework debugging]
ms.assetid: 440bad90-5a88-45e7-9157-4596801d8d19
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c22d9bf286a2241b0c1c5512e29532a01032cb3d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54648869"
---
# <a name="clrdatacreateinstance-function"></a><span data-ttu-id="47aba-102">CLRDataCreateInstance, fonction</span><span class="sxs-lookup"><span data-stu-id="47aba-102">CLRDataCreateInstance Function</span></span>
<span data-ttu-id="47aba-103">Crée un objet d’interface pour l’élément cible spécifié.</span><span class="sxs-lookup"><span data-stu-id="47aba-103">Creates an interface object for the specified target item.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47aba-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47aba-104">Syntax</span></span>  
  
```  
HRESULT CLRDataCreateInstance (  
    [in]  REFIID           iid,   
    [in]  ICLRDataTarget  *target,   
    [out] void           **iface  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="47aba-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47aba-105">Parameters</span></span>  
 `iid`  
 <span data-ttu-id="47aba-106">[in] L’identificateur de l’interface à instancier.</span><span class="sxs-lookup"><span data-stu-id="47aba-106">[in] The identifier of the interface to be instantiated.</span></span>  
  
 `target`  
 <span data-ttu-id="47aba-107">[in] Un pointeur vers un implémenté par l’utilisateur [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) objet qui représente l’élément cible pour lequel créer l’objet d’interface.</span><span class="sxs-lookup"><span data-stu-id="47aba-107">[in] A pointer to a user-implemented [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) object that represents the target item for which to create the interface object.</span></span>  
  
 `iface`  
 <span data-ttu-id="47aba-108">[out] Pointeur vers l’adresse de l’objet de l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="47aba-108">[out] A pointer to the address of the returned interface object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="47aba-109">Notes</span><span class="sxs-lookup"><span data-stu-id="47aba-109">Remarks</span></span>  
 <span data-ttu-id="47aba-110">Le `ICLRDataTarget` objet est implémenté par le writer de l’application de débogage.</span><span class="sxs-lookup"><span data-stu-id="47aba-110">The `ICLRDataTarget` object is implemented by the writer of the debugging application.</span></span> <span data-ttu-id="47aba-111">L’implémentation varie selon le type d’élément cible qui est représenté.</span><span class="sxs-lookup"><span data-stu-id="47aba-111">The implementation depends on the type of target item being represented.</span></span> <span data-ttu-id="47aba-112">L’élément cible peut être un processus, vidage de mémoire, ordinateur distant et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="47aba-112">The target item may be a process, memory dump, remote machine, and so on.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="47aba-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="47aba-113">Requirements</span></span>  
 <span data-ttu-id="47aba-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="47aba-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="47aba-115">**En-tête :** ClrData.idl</span><span class="sxs-lookup"><span data-stu-id="47aba-115">**Header:** ClrData.idl</span></span>  
  
 <span data-ttu-id="47aba-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="47aba-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="47aba-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="47aba-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47aba-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47aba-118">See also</span></span>
- [<span data-ttu-id="47aba-119">Fonctions statiques globales de débogage</span><span class="sxs-lookup"><span data-stu-id="47aba-119">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
