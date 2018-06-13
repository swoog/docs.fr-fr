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
ms.openlocfilehash: d9d4965751db1a70871270317a644b0acb1302f7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405978"
---
# <a name="clrdatacreateinstance-function"></a><span data-ttu-id="9d0cc-102">CLRDataCreateInstance, fonction</span><span class="sxs-lookup"><span data-stu-id="9d0cc-102">CLRDataCreateInstance Function</span></span>
<span data-ttu-id="9d0cc-103">Crée un objet d’interface pour l’élément cible spécifié.</span><span class="sxs-lookup"><span data-stu-id="9d0cc-103">Creates an interface object for the specified target item.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d0cc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d0cc-104">Syntax</span></span>  
  
```  
HRESULT CLRDataCreateInstance (  
    [in]  REFIID           iid,   
    [in]  ICLRDataTarget  *target,   
    [out] void           **iface  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9d0cc-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d0cc-105">Parameters</span></span>  
 `iid`  
 <span data-ttu-id="9d0cc-106">[in] Identificateur de l’interface pour être instancié.</span><span class="sxs-lookup"><span data-stu-id="9d0cc-106">[in] The identifier of the interface to be instantiated.</span></span>  
  
 `target`  
 <span data-ttu-id="9d0cc-107">[in] Un pointeur vers un implémenté par l’utilisateur [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) objet qui représente l’élément cible pour lequel créer l’objet d’interface.</span><span class="sxs-lookup"><span data-stu-id="9d0cc-107">[in] A pointer to a user-implemented [ICLRDataTarget](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md) object that represents the target item for which to create the interface object.</span></span>  
  
 `iface`  
 <span data-ttu-id="9d0cc-108">[out] Pointeur vers l’adresse de l’objet d’interface retourné.</span><span class="sxs-lookup"><span data-stu-id="9d0cc-108">[out] A pointer to the address of the returned interface object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9d0cc-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9d0cc-109">Remarks</span></span>  
 <span data-ttu-id="9d0cc-110">Le `ICLRDataTarget` objet est implémenté par le writer de l’application de débogage.</span><span class="sxs-lookup"><span data-stu-id="9d0cc-110">The `ICLRDataTarget` object is implemented by the writer of the debugging application.</span></span> <span data-ttu-id="9d0cc-111">L’implémentation varie selon le type de l’élément cible qui est représenté.</span><span class="sxs-lookup"><span data-stu-id="9d0cc-111">The implementation depends on the type of target item being represented.</span></span> <span data-ttu-id="9d0cc-112">L’élément cible peut être un processus, vidage de la mémoire, ordinateur distant et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9d0cc-112">The target item may be a process, memory dump, remote machine, and so on.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d0cc-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9d0cc-113">Requirements</span></span>  
 <span data-ttu-id="9d0cc-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9d0cc-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d0cc-115">**En-tête :** ClrData.idl</span><span class="sxs-lookup"><span data-stu-id="9d0cc-115">**Header:** ClrData.idl</span></span>  
  
 <span data-ttu-id="9d0cc-116">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9d0cc-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9d0cc-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d0cc-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d0cc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d0cc-118">See Also</span></span>  
 [<span data-ttu-id="9d0cc-119">Fonctions statiques globales de débogage</span><span class="sxs-lookup"><span data-stu-id="9d0cc-119">Debugging Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-global-static-functions.md)
