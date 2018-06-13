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
ms.openlocfilehash: 1b0871636f816d62c1f65c74d22014d74fb1fb97
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433277"
---
# <a name="iclrruntimeinfosetdefaultstartupflags-method"></a><span data-ttu-id="56570-102">ICLRRuntimeInfo::SetDefaultStartupFlags, méthode</span><span class="sxs-lookup"><span data-stu-id="56570-102">ICLRRuntimeInfo::SetDefaultStartupFlags Method</span></span>
<span data-ttu-id="56570-103">Définit les indicateurs de démarrage et le fichier de configuration d’hôte qui permet de démarrer le runtime.</span><span class="sxs-lookup"><span data-stu-id="56570-103">Sets the startup flags and the host configuration file that will be used to start the runtime.</span></span> <span data-ttu-id="56570-104">Cette méthode remplace l’utilisation de la `startupFlags` paramètre dans le [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) et [CorBindToRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md) fonctions.</span><span class="sxs-lookup"><span data-stu-id="56570-104">This method supersedes the use of the `startupFlags` parameter in the [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) and [CorBindToRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md) functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="56570-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56570-105">Syntax</span></span>  
  
```  
HRESULT SetDefaultStartupFlags(  
           [in]  DWORD dwStartupFlags,  
           [in]  LPCWSTR pwzHostConfigFile);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="56570-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56570-106">Parameters</span></span>  
 `dwStartupFlags`  
 <span data-ttu-id="56570-107">[in] Les indicateurs de démarrage hôtes à définir.</span><span class="sxs-lookup"><span data-stu-id="56570-107">[in] The host startup flags to set.</span></span> <span data-ttu-id="56570-108">Utilisez les mêmes indicateurs comme avec la [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) et [CorBindToRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md) fonctions.</span><span class="sxs-lookup"><span data-stu-id="56570-108">Use the same flags as with the [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) and [CorBindToRuntimeHost](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimehost-function.md) functions.</span></span>  
  
 `pwzHostConfigFile`  
 <span data-ttu-id="56570-109">[in] Le chemin du répertoire du fichier de configuration hôte à définir.</span><span class="sxs-lookup"><span data-stu-id="56570-109">[in] The directory path of the host configuration file to set.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="56570-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="56570-110">Return Value</span></span>  
 <span data-ttu-id="56570-111">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="56570-111">This method returns the following specific HRESULT as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="56570-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="56570-112">HRESULT</span></span>|<span data-ttu-id="56570-113">Description</span><span class="sxs-lookup"><span data-stu-id="56570-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="56570-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="56570-114">S_OK</span></span>|<span data-ttu-id="56570-115">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="56570-115">The method completed successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="56570-116">Notes</span><span class="sxs-lookup"><span data-stu-id="56570-116">Remarks</span></span>  
 <span data-ttu-id="56570-117">Un hôte multithread doit synchroniser des appels à cette méthode.</span><span class="sxs-lookup"><span data-stu-id="56570-117">A multithreaded host should synchronize calls to this method.</span></span> <span data-ttu-id="56570-118">Sinon, le thread A peut appeler le `SetStartupFlags` méthode une fois que le thread B a terminé un appel à `SetStartupFlags` et avant que le thread B démarre l’exécution.</span><span class="sxs-lookup"><span data-stu-id="56570-118">Otherwise, thread A might call the `SetStartupFlags` method after thread B completes a call to `SetStartupFlags` and before thread B starts the runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="56570-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="56570-119">Requirements</span></span>  
 <span data-ttu-id="56570-120">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="56570-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="56570-121">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="56570-121">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="56570-122">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="56570-122">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="56570-123">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="56570-123">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56570-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56570-124">See Also</span></span>  
 [<span data-ttu-id="56570-125">ICLRRuntimeInfo, interface</span><span class="sxs-lookup"><span data-stu-id="56570-125">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="56570-126">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="56570-126">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="56570-127">Hébergement</span><span class="sxs-lookup"><span data-stu-id="56570-127">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
