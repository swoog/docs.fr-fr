---
title: ClrCreateManagedInstance, fonction
ms.date: 03/30/2017
api_name:
- ClrCreateManagedInstance
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- ClrCreateManagedInstance
helpviewer_keywords:
- ClrCreateManagedInstance function [.NET Framework hosting]
ms.assetid: 58ba42c0-4857-43bf-a039-73a4dc6544c2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a375ea586bacc2d3dafe53d493a7467730fae889
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432319"
---
# <a name="clrcreatemanagedinstance-function"></a><span data-ttu-id="098da-102">ClrCreateManagedInstance, fonction</span><span class="sxs-lookup"><span data-stu-id="098da-102">ClrCreateManagedInstance Function</span></span>
<span data-ttu-id="098da-103">Crée une instance du type managé spécifié.</span><span class="sxs-lookup"><span data-stu-id="098da-103">Creates an instance of the specified managed type.</span></span>  
  
 <span data-ttu-id="098da-104">Cette fonction est déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="098da-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span> <span data-ttu-id="098da-105">Utilisez l’activation COM pour créer une instance du type managé ou utilisez l’hébergement (consultez [CLR Interfaces d’hébergement ajoutées dans le .NET Framework 4 et 4.5](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)).</span><span class="sxs-lookup"><span data-stu-id="098da-105">Use COM activation to create an instance of the managed type, or use hosting (see [CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5](../../../../docs/framework/unmanaged-api/hosting/clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="098da-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="098da-106">Syntax</span></span>  
  
```  
STDAPI ClrCreateManagedInstance (  
    [in]  LPCWSTR  pTypeName,   
    [in]  REFIID   riid,   
    [out] void     **ppObject  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="098da-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="098da-107">Parameters</span></span>  
 `pTypeName`  
 <span data-ttu-id="098da-108">[in] Pointeur vers le nom de type de l’instance demandé.</span><span class="sxs-lookup"><span data-stu-id="098da-108">[in] A pointer to the name of the instance type being requested.</span></span>  
  
 `riid`  
 <span data-ttu-id="098da-109">[in] Le `IID` type de l’instance demandé.</span><span class="sxs-lookup"><span data-stu-id="098da-109">[in] The `IID` of the instance type being requested.</span></span>  
  
 `ppObject`  
 <span data-ttu-id="098da-110">[out] Pointeur vers un pointeur vers une instance du type managé qui a été demandée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="098da-110">[out] A pointer to a pointer to an instance of the managed type that was requested by the caller.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="098da-111">Notes</span><span class="sxs-lookup"><span data-stu-id="098da-111">Remarks</span></span>  
 <span data-ttu-id="098da-112">Le common language runtime doit déjà être chargé dans un processus.</span><span class="sxs-lookup"><span data-stu-id="098da-112">The common language runtime should already be loaded into a process.</span></span> <span data-ttu-id="098da-113">Par exemple, il peut être chargé à l’aide d’un appel à la [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) fonctionner avant du `ClrCreateManagedInstance` est appelée.</span><span class="sxs-lookup"><span data-stu-id="098da-113">For example, it can be loaded by using a call to the [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) function before the `ClrCreateManagedInstance` function is called.</span></span> <span data-ttu-id="098da-114">Si le runtime n’est pas chargé, `ClrCreateManagedInstance` tente d’abord charger la version v1.0.3705 du runtime.</span><span class="sxs-lookup"><span data-stu-id="098da-114">If the runtime is not loaded, `ClrCreateManagedInstance` first tries to load v1.0.3705 of the runtime.</span></span> <span data-ttu-id="098da-115">En cas d’échec, il tente de charger la dernière version du runtime.</span><span class="sxs-lookup"><span data-stu-id="098da-115">If that fails, it attempts to load the latest version of the runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="098da-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="098da-116">Requirements</span></span>  
 <span data-ttu-id="098da-117">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="098da-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="098da-118">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="098da-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="098da-119">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="098da-119">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="098da-120">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="098da-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="098da-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="098da-121">See Also</span></span>  
 [<span data-ttu-id="098da-122">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="098da-122">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)  
 [<span data-ttu-id="098da-123">Hébergement</span><span class="sxs-lookup"><span data-stu-id="098da-123">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
