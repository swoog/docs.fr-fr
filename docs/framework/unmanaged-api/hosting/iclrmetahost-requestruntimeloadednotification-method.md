---
title: ICLRMetaHost::RequestRuntimeLoadedNotification, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.RequestRuntimeLoadedNotification
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::RequestRuntimeLoadedNotification
helpviewer_keywords:
- RequestRuntimeLoadedNotification method [.NET Framework hosting]
- ICLRMetaHost::RequestRuntimeLoadedNotification method [.NET Framework hosting]
ms.assetid: 0d5ccc4d-0193-41f5-af54-45d7b70d5321
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 61fce3e06b5245872f7061716e8d995dd5f5043c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61984644"
---
# <a name="iclrmetahostrequestruntimeloadednotification-method"></a><span data-ttu-id="bb2aa-102">ICLRMetaHost::RequestRuntimeLoadedNotification, méthode</span><span class="sxs-lookup"><span data-stu-id="bb2aa-102">ICLRMetaHost::RequestRuntimeLoadedNotification Method</span></span>
<span data-ttu-id="bb2aa-103">Fournit une fonction de rappel qui est garantie être appelée lorsqu’une version du common language runtime (CLR) est chargée en premier, mais pas encore démarrée.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-103">Provides a callback function that is guaranteed to be called when a common language runtime (CLR) version is first loaded, but not yet started.</span></span> <span data-ttu-id="bb2aa-104">Cette méthode remplace la [LockClrVersion](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="bb2aa-104">This method supersedes the [LockClrVersion](../../../../docs/framework/unmanaged-api/hosting/lockclrversion-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb2aa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb2aa-105">Syntax</span></span>  
  
```  
HRESULT RequestRuntimeLoadedNotification (  
    [in] RuntimeLoadedCallbackFnPtr pCallbackFunction);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb2aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb2aa-106">Parameters</span></span>  
 `pCallbackFunction`  
 <span data-ttu-id="bb2aa-107">[in] La fonction de rappel qui est appelée lorsqu’un nouveau runtime a été chargé.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-107">[in] The callback function that is invoked when a new runtime has been loaded.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bb2aa-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bb2aa-108">Return Value</span></span>  
 <span data-ttu-id="bb2aa-109">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="bb2aa-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bb2aa-110">HRESULT</span></span>|<span data-ttu-id="bb2aa-111">Description</span><span class="sxs-lookup"><span data-stu-id="bb2aa-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bb2aa-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb2aa-112">S_OK</span></span>|<span data-ttu-id="bb2aa-113">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="bb2aa-114">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="bb2aa-114">E_POINTER</span></span>|<span data-ttu-id="bb2aa-115">`pCallbackFunction` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-115">`pCallbackFunction` is null.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bb2aa-116">Notes</span><span class="sxs-lookup"><span data-stu-id="bb2aa-116">Remarks</span></span>  
 <span data-ttu-id="bb2aa-117">Le rappel fonctionne de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="bb2aa-117">The callback works in the following way:</span></span>  
  
- <span data-ttu-id="bb2aa-118">Le rappel est appelé uniquement lorsqu’un runtime est chargé pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-118">The callback is invoked only when a runtime is loaded for the first time.</span></span>  
  
- <span data-ttu-id="bb2aa-119">Le rappel n’est pas appelé pour les chargements réentrants du même runtime.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-119">The callback is not invoked for reentrant loads of the same runtime.</span></span>  
  
- <span data-ttu-id="bb2aa-120">Pour les chargements de runtime non réentrants, les appels à la fonction de rappel sont sérialisés.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-120">For non-reentrant runtime loads, calls to the callback function are serialized.</span></span>  
  
 <span data-ttu-id="bb2aa-121">La fonction de rappel a le prototype suivant :</span><span class="sxs-lookup"><span data-stu-id="bb2aa-121">The callback function has the following prototype:</span></span>  
  
```  
typedef void (__stdcall *RuntimeLoadedCallbackFnPtr)(  
                     ICLRRuntimeInfo *pRuntimeInfo,  
                     CallbackThreadSetFnPtr pfnCallbackThreadSet,  
                     CallbackThreadUnsetFnPtr pfnCallbackThreadUnset);  
```  
  
 <span data-ttu-id="bb2aa-122">Les prototypes de fonction de rappel sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb2aa-122">The callback function prototypes are as follows:</span></span>  
  
- <span data-ttu-id="bb2aa-123">`pfnCallbackThreadSet`:</span><span class="sxs-lookup"><span data-stu-id="bb2aa-123">`pfnCallbackThreadSet`:</span></span>  
  
    ```  
    typedef HRESULT (__stdcall *CallbackThreadSetFnPtr)();  
    ```  
  
- <span data-ttu-id="bb2aa-124">`pfnCallbackThreadUnset`:</span><span class="sxs-lookup"><span data-stu-id="bb2aa-124">`pfnCallbackThreadUnset`:</span></span>  
  
    ```  
    typedef HRESULT (__stdcall *CallbackThreadUnsetFnPtr)();  
    ```  
  
 <span data-ttu-id="bb2aa-125">Si l’hôte a l’intention de charger ou de provoquer un autre runtime à charger de manière réentrante, la `pfnCallbackThreadSet` et `pfnCallbackThreadUnset` les paramètres qui sont fournies dans le rappel de fonction doit être utilisée de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="bb2aa-125">If the host intends to load or cause another runtime to be loaded in a reentrant manner, the `pfnCallbackThreadSet` and `pfnCallbackThreadUnset` parameters that are provided in the callback function must be used in the following way:</span></span>  
  
- <span data-ttu-id="bb2aa-126">`pfnCallbackThreadSet` doit être appelée par le thread qui peut entraîner une charge de l’exécution avant la tentative de type de charge.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-126">`pfnCallbackThreadSet` must be called by the thread that might cause a runtime load before such a load is attempted.</span></span>  
  
- <span data-ttu-id="bb2aa-127">`pfnCallbackThreadUnset` doit être appelée lorsque le thread ne provoquera plus tel un chargement de runtime (et avant le retour du rappel initial).</span><span class="sxs-lookup"><span data-stu-id="bb2aa-127">`pfnCallbackThreadUnset` must be called when the thread will no longer cause such a runtime load (and before returning from the initial callback).</span></span>  
  
- <span data-ttu-id="bb2aa-128">`pfnCallbackThreadSet` et `pfnCallbackThreadUnset` sont tous deux non réentrante.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-128">`pfnCallbackThreadSet` and `pfnCallbackThreadUnset` are both non-reentrant.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bb2aa-129">Héberger des applications ne doivent pas appeler `pfnCallbackThreadSet` et `pfnCallbackThreadUnset` sort du cadre de la `pCallbackFunction` paramètre.</span><span class="sxs-lookup"><span data-stu-id="bb2aa-129">Host applications must not call `pfnCallbackThreadSet` and `pfnCallbackThreadUnset` outside the scope of the `pCallbackFunction` parameter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb2aa-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb2aa-130">Requirements</span></span>  
 <span data-ttu-id="bb2aa-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bb2aa-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb2aa-132">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="bb2aa-132">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="bb2aa-133">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bb2aa-133">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bb2aa-134">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb2aa-134">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb2aa-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb2aa-135">See also</span></span>

- [<span data-ttu-id="bb2aa-136">ICLRMetaHost, interface</span><span class="sxs-lookup"><span data-stu-id="bb2aa-136">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)
- [<span data-ttu-id="bb2aa-137">Hébergement</span><span class="sxs-lookup"><span data-stu-id="bb2aa-137">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
