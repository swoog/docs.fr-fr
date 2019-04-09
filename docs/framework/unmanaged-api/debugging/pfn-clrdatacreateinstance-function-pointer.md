---
title: PFN_CLRDataCreateInstance (pointeur fonction)
ms.date: 03/30/2017
api_name:
- PFN_CLRDataCreateInstance
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- PFN_CLRDataCreateInstance
helpviewer_keywords:
- PFN_CLRDataCreateInstance function pointer [.NET Framework debugging]
ms.assetid: 5c66ac57-d751-4de5-af9f-26ceb949af8b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ff2ddb1e98f3455c6915acf8149f528176228425
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59177981"
---
# <a name="pfnclrdatacreateinstance-function-pointer"></a><span data-ttu-id="dd4f3-102">PFN_CLRDataCreateInstance (pointeur fonction)</span><span class="sxs-lookup"><span data-stu-id="dd4f3-102">PFN_CLRDataCreateInstance Function Pointer</span></span>
<span data-ttu-id="dd4f3-103">Pointe vers une fonction qui crée un objet d’interface pour l’élément cible spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-103">Points to a function that creates an interface object for the specified target item.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dd4f3-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd4f3-104">Syntax</span></span>  
  
```  
typedef HRESULT (STDAPICALLTYPE* PFN_CLRDataCreateInstance) (  
    [in]  REFIID           iid,  
    [in]  ICLRDataTarget  *target,  
    [out] void           **iface  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="dd4f3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd4f3-105">Parameters</span></span>  
 `iid`  
 <span data-ttu-id="dd4f3-106">[in] L’identificateur de l’interface à instancier.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-106">[in] The identifier of the interface to be instantiated.</span></span>  
  
 `target`  
 <span data-ttu-id="dd4f3-107">[in] Un pointeur vers un implémenté par l’utilisateur [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) objet qui représente l’élément cible pour lequel créer l’objet d’interface.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-107">[in] A pointer to a user-implemented [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) object that represents the target item for which to create the interface object.</span></span>  
  
 `iface`  
 <span data-ttu-id="dd4f3-108">[out] Pointeur vers l’adresse de l’objet de l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-108">[out] A pointer to the address of the returned interface object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dd4f3-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dd4f3-109">Remarks</span></span>  
 <span data-ttu-id="dd4f3-110">Le `ICLRDataTarget` objet est implémenté par le writer de l’application de débogage.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-110">The `ICLRDataTarget` object is implemented by the writer of the debugging application.</span></span> <span data-ttu-id="dd4f3-111">L’implémentation varie selon le type d’élément cible qui est représenté.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-111">The implementation depends on the type of target item being represented.</span></span> <span data-ttu-id="dd4f3-112">L’élément cible peut être un processus, vidage de mémoire, ordinateur distant et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="dd4f3-112">The target item may be a process, memory dump, remote machine, and so on.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dd4f3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd4f3-113">Requirements</span></span>  
 <span data-ttu-id="dd4f3-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dd4f3-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dd4f3-115">**En-tête :** ClrData.idl</span><span class="sxs-lookup"><span data-stu-id="dd4f3-115">**Header:** ClrData.idl</span></span>  
  
 <span data-ttu-id="dd4f3-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dd4f3-116">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="dd4f3-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="dd4f3-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="dd4f3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd4f3-118">See also</span></span>

- [<span data-ttu-id="dd4f3-119">Fonctions statiques globales du débogage</span><span class="sxs-lookup"><span data-stu-id="dd4f3-119">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
