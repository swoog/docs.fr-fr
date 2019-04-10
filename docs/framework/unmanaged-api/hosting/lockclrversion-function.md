---
title: LockClrVersion, fonction
ms.date: 03/30/2017
api_name:
- LockClrVersion
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- LockClrVersion
helpviewer_keywords:
- LockClrVersion function [.NET Framework hosting]
ms.assetid: 1318ee37-c43b-40eb-bbe8-88fc46453d74
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 91bb1a9416e577dbb5cc96e8be87033c53232811
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59336692"
---
# <a name="lockclrversion-function"></a><span data-ttu-id="ca10d-102">LockClrVersion, fonction</span><span class="sxs-lookup"><span data-stu-id="ca10d-102">LockClrVersion Function</span></span>
<span data-ttu-id="ca10d-103">Permet à l’hôte déterminer quelle version du common language runtime (CLR) sera utilisée au sein du processus avant d’initialiser le CLR explicitement.</span><span class="sxs-lookup"><span data-stu-id="ca10d-103">Allows the host to determine which version of the common language runtime (CLR) will be used within the process before explicitly initializing the CLR.</span></span>  
  
 <span data-ttu-id="ca10d-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="ca10d-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca10d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca10d-105">Syntax</span></span>  
  
```  
HRESULT LockClrVersion (  
    [in] FLockClrVersionCallback   hostCallback,  
    [in] FLockClrVersionCallback  *pBeginHostSetup,  
    [in] FLockClrVersionCallback  *pEndHostSetup  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ca10d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca10d-106">Parameters</span></span>  
 `hostCallback`  
 <span data-ttu-id="ca10d-107">[in] La fonction doit être appelée par le CLR lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="ca10d-107">[in] The function to be called by the CLR upon initialization.</span></span>  
  
 `pBeginHostSetup`  
 <span data-ttu-id="ca10d-108">[in] La fonction doit être appelée par l’hôte pour informer le CLR que l’initialisation démarre.</span><span class="sxs-lookup"><span data-stu-id="ca10d-108">[in] The function to be called by the host to inform the CLR that initialization is starting.</span></span>  
  
 `pEndHostSetup`  
 <span data-ttu-id="ca10d-109">[in] La fonction doit être appelée par l’hôte pour informer le CLR que l’initialisation est terminée.</span><span class="sxs-lookup"><span data-stu-id="ca10d-109">[in] The function to be called by the host to inform the CLR that initialization is complete.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ca10d-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ca10d-110">Return Value</span></span>  
 <span data-ttu-id="ca10d-111">Cette méthode retourne des codes d’erreur COM standards, tel que défini dans WinError.h, en plus des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ca10d-111">This method returns standard COM error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="ca10d-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ca10d-112">Return code</span></span>|<span data-ttu-id="ca10d-113">Description</span><span class="sxs-lookup"><span data-stu-id="ca10d-113">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="ca10d-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca10d-114">S_OK</span></span>|<span data-ttu-id="ca10d-115">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="ca10d-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="ca10d-116">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ca10d-116">E_INVALIDARG</span></span>|<span data-ttu-id="ca10d-117">Un ou plusieurs des arguments sont null.</span><span class="sxs-lookup"><span data-stu-id="ca10d-117">One or more of the arguments is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ca10d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ca10d-118">Remarks</span></span>  
 <span data-ttu-id="ca10d-119">L’hôte appelle `LockClrVersion` avant d’initialiser le CLR.</span><span class="sxs-lookup"><span data-stu-id="ca10d-119">The host calls `LockClrVersion` before initializing the CLR.</span></span> `LockClrVersion` <span data-ttu-id="ca10d-120">accepte trois paramètres, qui sont tous des rappels de type [FLockClrVersionCallback](../../../../docs/framework/unmanaged-api/hosting/flockclrversioncallback-function-pointer.md).</span><span class="sxs-lookup"><span data-stu-id="ca10d-120">takes three parameters, all of which are callbacks of type [FLockClrVersionCallback](../../../../docs/framework/unmanaged-api/hosting/flockclrversioncallback-function-pointer.md).</span></span> <span data-ttu-id="ca10d-121">Ce type est défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="ca10d-121">This type is defined as follows.</span></span>  
  
```  
typedef HRESULT ( __stdcall *FLockClrVersionCallback ) ();  
```  
  
 <span data-ttu-id="ca10d-122">Les étapes suivantes se produisent lors de l’initialisation du runtime :</span><span class="sxs-lookup"><span data-stu-id="ca10d-122">The following steps occur upon initialization of the runtime:</span></span>  
  
1. <span data-ttu-id="ca10d-123">L’hôte appelle [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) ou l’une des autres fonctions d’initialisation de runtime.</span><span class="sxs-lookup"><span data-stu-id="ca10d-123">The host calls [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) or one of the other runtime initialization functions.</span></span> <span data-ttu-id="ca10d-124">L’hôte peut également initialiser le runtime à l’aide d’activation d’un objet COM.</span><span class="sxs-lookup"><span data-stu-id="ca10d-124">Alternatively, the host could initialize the runtime using COM object activation.</span></span>  
  
2. <span data-ttu-id="ca10d-125">Le runtime appelle la fonction spécifiée par le `hostCallback` paramètre.</span><span class="sxs-lookup"><span data-stu-id="ca10d-125">The runtime calls the function specified by the `hostCallback` parameter.</span></span>  
  
3. <span data-ttu-id="ca10d-126">La fonction spécifiée par `hostCallback` effectue ensuite la séquence d’appels suivante :</span><span class="sxs-lookup"><span data-stu-id="ca10d-126">The function specified by `hostCallback` then makes the following sequence of calls:</span></span>  
  
    -   <span data-ttu-id="ca10d-127">La fonction spécifiée par le `pBeginHostSetup` paramètre.</span><span class="sxs-lookup"><span data-stu-id="ca10d-127">The function specified by the `pBeginHostSetup` parameter.</span></span>  
  
    -   `CorBindToRuntimeEx` <span data-ttu-id="ca10d-128">(ou une autre fonction de l’initialisation du runtime).</span><span class="sxs-lookup"><span data-stu-id="ca10d-128">(or another runtime initialization function).</span></span>  
  
    -   <span data-ttu-id="ca10d-129">[ICLRRuntimeHost::SetHostControl](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-sethostcontrol-method.md).</span><span class="sxs-lookup"><span data-stu-id="ca10d-129">[ICLRRuntimeHost::SetHostControl](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-sethostcontrol-method.md).</span></span>  
  
    -   <span data-ttu-id="ca10d-130">[ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md).</span><span class="sxs-lookup"><span data-stu-id="ca10d-130">[ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md).</span></span>  
  
    -   <span data-ttu-id="ca10d-131">La fonction spécifiée par le `pEndHostSetup` paramètre.</span><span class="sxs-lookup"><span data-stu-id="ca10d-131">The function specified by the `pEndHostSetup` parameter.</span></span>  
  
 <span data-ttu-id="ca10d-132">Tous les appels de `pBeginHostSetup` à `pEndHostSetup` doit se produire sur un thread unique ou une fibre, avec la même pile logique.</span><span class="sxs-lookup"><span data-stu-id="ca10d-132">All the calls from `pBeginHostSetup` to `pEndHostSetup` must occur on a single thread or fiber, with the same logical stack.</span></span> <span data-ttu-id="ca10d-133">Ce thread peut être différent du thread sur lequel `hostCallback` est appelée.</span><span class="sxs-lookup"><span data-stu-id="ca10d-133">This thread can be different from the thread upon which `hostCallback` is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca10d-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca10d-134">Requirements</span></span>  
 <span data-ttu-id="ca10d-135">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ca10d-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca10d-136">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="ca10d-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ca10d-137">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ca10d-137">**Library:** MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="ca10d-138">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ca10d-138">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ca10d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca10d-139">See also</span></span>

- [<span data-ttu-id="ca10d-140">Fonction d'hébergement du CLR déconseillées</span><span class="sxs-lookup"><span data-stu-id="ca10d-140">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
