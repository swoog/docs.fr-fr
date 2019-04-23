---
title: GetRequestedRuntimeVersion, fonction
ms.date: 03/30/2017
api_name:
- GetRequestedRuntimeVersion
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetRequestedRuntimeVersion
helpviewer_keywords:
- GetRequestedRuntimeVersion function [.NET Framework hosting]
ms.assetid: 82f596a4-483d-4509-b0c5-a84c53c3da1b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1ee737f4c6d34e77996f5ba08ce4d84132a99238
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59207329"
---
# <a name="getrequestedruntimeversion-function"></a><span data-ttu-id="62d42-102">GetRequestedRuntimeVersion, fonction</span><span class="sxs-lookup"><span data-stu-id="62d42-102">GetRequestedRuntimeVersion Function</span></span>
<span data-ttu-id="62d42-103">Obtient le numéro de version du common language runtime (CLR) demandé par l’application spécifiée.</span><span class="sxs-lookup"><span data-stu-id="62d42-103">Gets the version number of the common language runtime (CLR) requested by the specified application.</span></span> <span data-ttu-id="62d42-104">Si cette version n’est pas installée, obtient la version la plus récente est installée avant la version demandée.</span><span class="sxs-lookup"><span data-stu-id="62d42-104">If that version is not installed, gets the most recent version that is installed before the requested version.</span></span>  
  
 <span data-ttu-id="62d42-105">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="62d42-105">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62d42-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62d42-106">Syntax</span></span>  
  
```  
HRESULT GetRequestedRuntimeVersion (  
    [in]  LPWSTR  pExe,   
    [out] LPWSTR  pVersion,   
    [in]  DWORD   cchBuffer,   
    [out] DWORD  *pdwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="62d42-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62d42-107">Parameters</span></span>  
 `pExe`  
 <span data-ttu-id="62d42-108">[in] Le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="62d42-108">[in] The name of the application.</span></span>  
  
 `pVersion`  
 <span data-ttu-id="62d42-109">[out] Une mémoire tampon qui contient la chaîne de numéro de version en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="62d42-109">[out] A buffer that contains the version number string upon successful completion.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="62d42-110">[in] La longueur de la mémoire tampon de version.</span><span class="sxs-lookup"><span data-stu-id="62d42-110">[in] The length of the version buffer.</span></span>  
  
 `pdwLength`  
 <span data-ttu-id="62d42-111">[out] Pointeur vers la longueur de la chaîne de numéro de version.</span><span class="sxs-lookup"><span data-stu-id="62d42-111">[out] A pointer to the length of the version number string.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="62d42-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="62d42-112">Return Value</span></span>  
 <span data-ttu-id="62d42-113">Cette méthode retourne des codes d’erreur de composant COM (Object Model) standard, tel que défini dans WinError.h, en plus des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="62d42-113">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="62d42-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="62d42-114">Return code</span></span>|<span data-ttu-id="62d42-115">Description</span><span class="sxs-lookup"><span data-stu-id="62d42-115">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="62d42-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="62d42-116">S_OK</span></span>|<span data-ttu-id="62d42-117">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="62d42-117">The method completed successfully.</span></span>|  
|<span data-ttu-id="62d42-118">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="62d42-118">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="62d42-119">Le tampon de version n’est pas suffisamment grand pour stocker la chaîne de version.</span><span class="sxs-lookup"><span data-stu-id="62d42-119">The version buffer is not large enough to store the version string.</span></span>|  
|<span data-ttu-id="62d42-120">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="62d42-120">E_POINTER</span></span>|<span data-ttu-id="62d42-121">`pdwLength` a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="62d42-121">`pdwLength` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="62d42-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62d42-122">Requirements</span></span>  
 <span data-ttu-id="62d42-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="62d42-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62d42-124">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="62d42-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="62d42-125">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="62d42-125">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="62d42-126">**Versions du .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="62d42-126">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62d42-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62d42-127">See also</span></span>

- [<span data-ttu-id="62d42-128">GetRequestedRuntimeInfo, fonction</span><span class="sxs-lookup"><span data-stu-id="62d42-128">GetRequestedRuntimeInfo Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getrequestedruntimeinfo-function.md)
- [<span data-ttu-id="62d42-129">GetVersionFromProcess, fonction</span><span class="sxs-lookup"><span data-stu-id="62d42-129">GetVersionFromProcess Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/getversionfromprocess-function.md)
- [<span data-ttu-id="62d42-130">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="62d42-130">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
