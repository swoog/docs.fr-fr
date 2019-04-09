---
title: ICLRRuntimeInfo::GetInterface, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetInterface
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetInterface
helpviewer_keywords:
- GetInterface method [.NET Framework hosting]
- ICLRRuntimeInfo::GetInterface method [.NET Framework hosting]
ms.assetid: cc7b0e5b-48c3-4509-8ebb-611ddb1f7ec2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2f229e421cc69f2ff45110233c4c6c36d7a1fc4c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59152748"
---
# <a name="iclrruntimeinfogetinterface-method"></a><span data-ttu-id="967a9-102">ICLRRuntimeInfo::GetInterface, méthode</span><span class="sxs-lookup"><span data-stu-id="967a9-102">ICLRRuntimeInfo::GetInterface Method</span></span>
<span data-ttu-id="967a9-103">Charge le CLR dans le processus actuel et retourne des pointeurs d’interface, runtime comme [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md), [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md), et [IMetaDataDispenserEx](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md).</span><span class="sxs-lookup"><span data-stu-id="967a9-103">Loads the CLR into the current process and returns runtime interface pointers, such as [ICLRRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-interface.md), [ICLRStrongName](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md), and [IMetaDataDispenserEx](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md).</span></span>  
  
 <span data-ttu-id="967a9-104">Cette méthode remplace toutes les `CorBindTo`\* des fonctions dans le [déconseillé fonctions d’hébergement CLR](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) section.</span><span class="sxs-lookup"><span data-stu-id="967a9-104">This method supersedes all the `CorBindTo`\* functions in the [Deprecated CLR Hosting Functions](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md) section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="967a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="967a9-105">Syntax</span></span>  
  
```  
HRESULT GetInterface(  
[in]  REFCLSID rclsid,  
[in]  REFIID   riid,  
[out, iid_is(riid), retval] LPVOID *ppUnk);  
```  
  
## <a name="parameters"></a><span data-ttu-id="967a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="967a9-106">Parameters</span></span>  
 `rclsid`  
 <span data-ttu-id="967a9-107">[in] L’interface CLSID pour la coclasse.</span><span class="sxs-lookup"><span data-stu-id="967a9-107">[in] The CLSID interface for the coclass.</span></span>  
  
 `riid`  
 <span data-ttu-id="967a9-108">[in] IID de demandé `rclsid` interface.</span><span class="sxs-lookup"><span data-stu-id="967a9-108">[in] The IID of the requested `rclsid` interface.</span></span>  
  
 `ppUnk`  
 <span data-ttu-id="967a9-109">[out] Pointeur vers l’interface interrogée.</span><span class="sxs-lookup"><span data-stu-id="967a9-109">[out] A pointer to the queried interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="967a9-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="967a9-110">Return Value</span></span>  
 <span data-ttu-id="967a9-111">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="967a9-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="967a9-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="967a9-112">HRESULT</span></span>|<span data-ttu-id="967a9-113">Description</span><span class="sxs-lookup"><span data-stu-id="967a9-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="967a9-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="967a9-114">S_OK</span></span>|<span data-ttu-id="967a9-115">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="967a9-115">The method completed successfully.</span></span>|  
|<span data-ttu-id="967a9-116">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="967a9-116">E_POINTER</span></span>|`ppUnk` <span data-ttu-id="967a9-117">a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="967a9-117">is null.</span></span>|  
|<span data-ttu-id="967a9-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="967a9-118">E_OUTOFMEMORY</span></span>|<span data-ttu-id="967a9-119">Pas assez de mémoire est disponible pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="967a9-119">Not enough memory is available to handle the request.</span></span>|  
|<span data-ttu-id="967a9-120">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span><span class="sxs-lookup"><span data-stu-id="967a9-120">CLR_E_SHIM_LEGACYRUNTIMEALREADYBOUND</span></span>|<span data-ttu-id="967a9-121">Un runtime différent était déjà lié à la stratégie d’activation 2 de version CLR héritée.</span><span class="sxs-lookup"><span data-stu-id="967a9-121">A different runtime was already bound to the legacy CLR version 2 activation policy.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="967a9-122">Notes</span><span class="sxs-lookup"><span data-stu-id="967a9-122">Remarks</span></span>  
 <span data-ttu-id="967a9-123">Cette méthode provoque le CLR être chargé, mais non initialisé.</span><span class="sxs-lookup"><span data-stu-id="967a9-123">This method causes the CLR to be loaded but not initialized.</span></span>  
  
 <span data-ttu-id="967a9-124">Le tableau suivant montre les combinaisons prises en charge pour `rclsid` et `riid`.</span><span class="sxs-lookup"><span data-stu-id="967a9-124">The following table shows the supported combinations for `rclsid` and `riid`.</span></span>  
  
|`rclsid`|`riid`|  
|--------------|------------|  
|<span data-ttu-id="967a9-125">CLSID_CorMetaDataDispenser</span><span class="sxs-lookup"><span data-stu-id="967a9-125">CLSID_CorMetaDataDispenser</span></span>|<span data-ttu-id="967a9-126">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span><span class="sxs-lookup"><span data-stu-id="967a9-126">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span></span>|  
|<span data-ttu-id="967a9-127">CLSID_CorMetaDataDispenserRuntime</span><span class="sxs-lookup"><span data-stu-id="967a9-127">CLSID_CorMetaDataDispenserRuntime</span></span>|<span data-ttu-id="967a9-128">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span><span class="sxs-lookup"><span data-stu-id="967a9-128">IID_IMetaDataDispenser, IID_IMetaDataDispenserEx</span></span>|  
|<span data-ttu-id="967a9-129">CLSID_CorRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="967a9-129">CLSID_CorRuntimeHost</span></span>|<span data-ttu-id="967a9-130">IID_ICorRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="967a9-130">IID_ICorRuntimeHost</span></span>|  
|<span data-ttu-id="967a9-131">CLSID_CLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="967a9-131">CLSID_CLRRuntimeHost</span></span>|<span data-ttu-id="967a9-132">IID_ICLRRuntimeHost</span><span class="sxs-lookup"><span data-stu-id="967a9-132">IID_ICLRRuntimeHost</span></span>|  
|<span data-ttu-id="967a9-133">CLSID_TypeNameFactory</span><span class="sxs-lookup"><span data-stu-id="967a9-133">CLSID_TypeNameFactory</span></span>|<span data-ttu-id="967a9-134">IID_ITypeNameFactory</span><span class="sxs-lookup"><span data-stu-id="967a9-134">IID_ITypeNameFactory</span></span>|  
|<span data-ttu-id="967a9-135">CLSID_CLRDebuggingLegacy</span><span class="sxs-lookup"><span data-stu-id="967a9-135">CLSID_CLRDebuggingLegacy</span></span>|<span data-ttu-id="967a9-136">IID_ICorDebug</span><span class="sxs-lookup"><span data-stu-id="967a9-136">IID_ICorDebug</span></span>|  
|||  
|<span data-ttu-id="967a9-137">CLSID_CLRStrongName</span><span class="sxs-lookup"><span data-stu-id="967a9-137">CLSID_CLRStrongName</span></span>|<span data-ttu-id="967a9-138">IID_ICLRStrongName</span><span class="sxs-lookup"><span data-stu-id="967a9-138">IID_ICLRStrongName</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="967a9-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="967a9-139">Requirements</span></span>  
 <span data-ttu-id="967a9-140">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="967a9-140">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="967a9-141">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="967a9-141">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="967a9-142">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="967a9-142">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="967a9-143">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="967a9-143">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="967a9-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="967a9-144">See also</span></span>

- [<span data-ttu-id="967a9-145">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="967a9-145">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="967a9-146">Interfaces d'hébergement</span><span class="sxs-lookup"><span data-stu-id="967a9-146">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="967a9-147">Hébergement</span><span class="sxs-lookup"><span data-stu-id="967a9-147">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
