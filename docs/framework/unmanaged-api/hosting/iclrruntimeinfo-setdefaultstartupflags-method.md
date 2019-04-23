---
title: ICLRRuntimeInfo::SetDefaultStartupFlags, méthode
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.SetDefaultStartupFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::SetDefaultStartupFlags
helpviewer_keywords:
- ICLRRuntimeInfo::SetDefaultStartupFlags method [.NET Framework hosting]
- SetDefaultStartupFlags method [.NET Framework hosting]
ms.assetid: 98ae174f-bff0-48f1-9e05-6cb63b451824
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3174cf3b4f4f4ac4b2c8e69030357eb1e46cf3c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59197826"
---
# <a name="iclrruntimeinfosetdefaultstartupflags-method"></a><span data-ttu-id="61501-102">ICLRRuntimeInfo::SetDefaultStartupFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="61501-102">ICLRRuntimeInfo::SetDefaultStartupFlags Method</span></span>
<span data-ttu-id="61501-103">Définit les indicateurs de démarrage et le fichier de configuration d’hôte qui sera utilisé pour démarrer le runtime.</span><span class="sxs-lookup"><span data-stu-id="61501-103">Sets the startup flags and the host configuration file that will be used to start the runtime.</span></span> <span data-ttu-id="61501-104">Cette méthode remplace l’utilisation de la `startupFlags` paramètre dans le [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) et [CorBindToRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md) fonctions.</span><span class="sxs-lookup"><span data-stu-id="61501-104">This method supersedes the use of the `startupFlags` parameter in the [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) and [CorBindToRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md) functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61501-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61501-105">Syntax</span></span>  
  
```  
HRESULT SetDefaultStartupFlags(  
           [in]  DWORD dwStartupFlags,  
           [in]  LPCWSTR pwzHostConfigFile);  
```  
  
## <a name="parameters"></a><span data-ttu-id="61501-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61501-106">Parameters</span></span>  
 `dwStartupFlags`  
 <span data-ttu-id="61501-107">[in] Les indicateurs de démarrage hôte à définir.</span><span class="sxs-lookup"><span data-stu-id="61501-107">[in] The host startup flags to set.</span></span> <span data-ttu-id="61501-108">Utilisez les mêmes indicateurs comme avec la [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) et [CorBindToRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md) fonctions.</span><span class="sxs-lookup"><span data-stu-id="61501-108">Use the same flags as with the [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) and [CorBindToRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md) functions.</span></span>  
  
 `pwzHostConfigFile`  
 <span data-ttu-id="61501-109">[in] Le chemin du répertoire du fichier de configuration d’hôte à définir.</span><span class="sxs-lookup"><span data-stu-id="61501-109">[in] The directory path of the host configuration file to set.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="61501-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="61501-110">Return Value</span></span>  
 <span data-ttu-id="61501-111">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="61501-111">This method returns the following specific HRESULT as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="61501-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="61501-112">HRESULT</span></span>|<span data-ttu-id="61501-113">Description</span><span class="sxs-lookup"><span data-stu-id="61501-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="61501-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="61501-114">S_OK</span></span>|<span data-ttu-id="61501-115">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="61501-115">The method completed successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="61501-116">Notes</span><span class="sxs-lookup"><span data-stu-id="61501-116">Remarks</span></span>  
 <span data-ttu-id="61501-117">Un hôte multithread doit synchroniser des appels à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="61501-117">A multithreaded host should synchronize calls to this method.</span></span> <span data-ttu-id="61501-118">Sinon, le thread A peut appeler le `SetStartupFlags` méthode une fois que le thread B a terminé un appel à `SetStartupFlags` et avant que thread B démarre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="61501-118">Otherwise, thread A might call the `SetStartupFlags` method after thread B completes a call to `SetStartupFlags` and before thread B starts the runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="61501-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61501-119">Requirements</span></span>  
 <span data-ttu-id="61501-120">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="61501-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61501-121">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="61501-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="61501-122">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="61501-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="61501-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61501-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61501-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61501-124">See also</span></span>

- [<span data-ttu-id="61501-125">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="61501-125">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)
- [<span data-ttu-id="61501-126">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="61501-126">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="61501-127">Hébergement</span><span class="sxs-lookup"><span data-stu-id="61501-127">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
