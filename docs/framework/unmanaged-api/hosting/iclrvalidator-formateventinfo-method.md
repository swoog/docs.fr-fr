---
title: ICLRValidator::FormatEventInfo, méthode
ms.date: 03/30/2017
api_name:
- ICLRValidator.FormatEventInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRValidator::FormatEventInfo
helpviewer_keywords:
- FormatEventInfo method, ICLRValidator interface [.NET Framework hosting]
- ICLRValidator::FormatEventInfo method [.NET Framework hosting]
ms.assetid: 808e1f1d-52f4-47c4-83cc-dcf47d075219
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9117a82dff48dcda8d96f0feb7b8c4a001fa17f1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59205873"
---
# <a name="iclrvalidatorformateventinfo-method"></a><span data-ttu-id="d441f-102">ICLRValidator::FormatEventInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="d441f-102">ICLRValidator::FormatEventInfo Method</span></span>
<span data-ttu-id="d441f-103">Obtient un message détaillé sur l’erreur de validation spécifié.</span><span class="sxs-lookup"><span data-stu-id="d441f-103">Gets a detailed message about the specified validation error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d441f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d441f-104">Syntax</span></span>  
  
```  
HRESULT FormatEventInfo (  
    [in] HRESULT            hVECode,  
    [in] VEContext          Context,  
    [in, out] LPWSTR        msg,  
    [in] unsigned long      ulMaxLength,  
    [in] SAFEARRAY(VARIANT) psa  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d441f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d441f-105">Parameters</span></span>  
 `hVECode`  
 <span data-ttu-id="d441f-106">[in] La valeur HRESULT qui a été passée au gestionnaire d’erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="d441f-106">[in] The HRESULT value that was passed to the validation error handler.</span></span>  
  
 `Context`  
 <span data-ttu-id="d441f-107">[in] Un `VEContext` instance qui contient des informations de contexte sur les erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="d441f-107">[in] A `VEContext` instance that contains context information about the validation errors.</span></span>  
  
 `msg`  
 <span data-ttu-id="d441f-108">[in, out] Le message d’erreur convivial.</span><span class="sxs-lookup"><span data-stu-id="d441f-108">[in, out] The friendly error message.</span></span>  
  
 `ulMaxLength`  
 <span data-ttu-id="d441f-109">[in] La longueur maximale du message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d441f-109">[in] The maximum length of the error message.</span></span>  
  
 `psa`  
 <span data-ttu-id="d441f-110">[in] Un tableau sécurisé de paramètres supplémentaires à utiliser dans le message.</span><span class="sxs-lookup"><span data-stu-id="d441f-110">[in] A safe array of additional parameters to be used in the message.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d441f-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d441f-111">Return Value</span></span>  
  
|<span data-ttu-id="d441f-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d441f-112">HRESULT</span></span>|<span data-ttu-id="d441f-113">Description</span><span class="sxs-lookup"><span data-stu-id="d441f-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d441f-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="d441f-114">S_OK</span></span>|<span data-ttu-id="d441f-115">`FormatEventInfo` retourné avec succès.</span><span class="sxs-lookup"><span data-stu-id="d441f-115">`FormatEventInfo` returned successfully.</span></span>|  
|<span data-ttu-id="d441f-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d441f-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d441f-117">Le common language runtime (CLR) n’a pas été chargé dans un processus ou le CLR est dans un état dans lequel il ne peut pas exécuter le code managé ou traiter l’appel avec succès.</span><span class="sxs-lookup"><span data-stu-id="d441f-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d441f-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d441f-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d441f-119">L’appel a expiré.</span><span class="sxs-lookup"><span data-stu-id="d441f-119">The call timed out.</span></span>|  
|<span data-ttu-id="d441f-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d441f-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d441f-121">L’appelant ne possède pas le verrou.</span><span class="sxs-lookup"><span data-stu-id="d441f-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d441f-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d441f-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d441f-123">Un événement a été annulé alors qu’un thread bloqué ou Fibre l’attendait.</span><span class="sxs-lookup"><span data-stu-id="d441f-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d441f-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d441f-124">E_FAIL</span></span>|<span data-ttu-id="d441f-125">Une défaillance catastrophique inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d441f-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d441f-126">Lorsqu’une méthode retourne E_FAIL, le CLR n’est plus utilisable au sein du processus.</span><span class="sxs-lookup"><span data-stu-id="d441f-126">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d441f-127">Les appels suivants aux méthodes d’hébergement retournent HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="d441f-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d441f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d441f-128">Requirements</span></span>  
 <span data-ttu-id="d441f-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d441f-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d441f-130">**En-tête :** IValidator.idl, IValidator.h</span><span class="sxs-lookup"><span data-stu-id="d441f-130">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="d441f-131">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d441f-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d441f-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d441f-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d441f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d441f-133">See also</span></span>

- [<span data-ttu-id="d441f-134">ICLRErrorReportingManager, interface</span><span class="sxs-lookup"><span data-stu-id="d441f-134">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)
- [<span data-ttu-id="d441f-135">ICLRValidator, interface</span><span class="sxs-lookup"><span data-stu-id="d441f-135">ICLRValidator Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrvalidator-interface.md)
