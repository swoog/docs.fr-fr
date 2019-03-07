---
title: GetHistoryFileDirectory, fonction
ms.date: 03/30/2017
api_name:
- GetHistoryFileDirectory
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- GetHistoryFileDirectory
helpviewer_keywords:
- GetHistoryFileDirectory function [.NET Framework fusion]
ms.assetid: 93232222-926e-42ac-b85d-8a6d33977672
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 21742881c5aef7384be318297aa3432411c3d57c
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57479279"
---
# <a name="gethistoryfiledirectory-function"></a><span data-ttu-id="59f54-102">GetHistoryFileDirectory, fonction</span><span class="sxs-lookup"><span data-stu-id="59f54-102">GetHistoryFileDirectory Function</span></span>
<span data-ttu-id="59f54-103">Récupère le chemin d’accès du répertoire de l’historique de l’application.</span><span class="sxs-lookup"><span data-stu-id="59f54-103">Retrieves the path of the application history directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="59f54-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59f54-104">Syntax</span></span>  
  
```  
HRESULT GetHistoryFileDirectory (  
    [in]      LPWSTR      wzDir,  
    [in,out]  LPCWSTR  *pdwsize,  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="59f54-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59f54-105">Parameters</span></span>  
 `wzDir`  
 <span data-ttu-id="59f54-106">[out] Une mémoire tampon pour contenir le chemin d’accès au répertoire de l’historique de l’application.</span><span class="sxs-lookup"><span data-stu-id="59f54-106">[out] A buffer to hold the path to the application history directory.</span></span>  
  
 `pdwSize`  
 <span data-ttu-id="59f54-107">[in, out] La longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="59f54-107">[in, out] The length of the buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="59f54-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="59f54-108">Return Value</span></span>  
 <span data-ttu-id="59f54-109">Cette méthode retourne des codes d’erreur COM standards, tel que défini dans le fichier WinError.h, en plus des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="59f54-109">This method returns standard COM error codes, as defined in the WinError.h file in addition to the following values.</span></span>  
  
|<span data-ttu-id="59f54-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="59f54-110">Return code</span></span>|<span data-ttu-id="59f54-111">Description</span><span class="sxs-lookup"><span data-stu-id="59f54-111">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="59f54-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="59f54-112">S_OK</span></span>|<span data-ttu-id="59f54-113">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="59f54-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="59f54-114">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="59f54-114">E_INVALIDARG</span></span>|<span data-ttu-id="59f54-115">`wzDir` ou `pdwSize` est null, ou la version de chaîne est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="59f54-115">`wzDir` or `pdwSize` is null, or the version string is incorrect.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="59f54-116">Notes</span><span class="sxs-lookup"><span data-stu-id="59f54-116">Remarks</span></span>  
 <span data-ttu-id="59f54-117">Opération réussie, le `pdwSize` argument est défini sur la longueur de la chaîne de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="59f54-117">On successful completion, the `pdwSize` argument is set to the length of the path string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="59f54-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="59f54-118">Requirements</span></span>  
 <span data-ttu-id="59f54-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="59f54-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="59f54-120">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="59f54-120">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="59f54-121">**Bibliothèque :** Le fichier fusion.dll et Mscorwks.dll.</span><span class="sxs-lookup"><span data-stu-id="59f54-121">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="59f54-122">Utilisez le fichier Fusion.dll plutôt que Mscorwks.dll pour vous assurer que vous ciblez la version correcte du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="59f54-122">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="59f54-123">**Versions du .NET Framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="59f54-123">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59f54-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59f54-124">See also</span></span>
- [<span data-ttu-id="59f54-125">CreateHistoryReader, fonction</span><span class="sxs-lookup"><span data-stu-id="59f54-125">CreateHistoryReader Function</span></span>](../../../../docs/framework/unmanaged-api/fusion/createhistoryreader-function.md)
- [<span data-ttu-id="59f54-126">NukeDownloadedCache, fonction</span><span class="sxs-lookup"><span data-stu-id="59f54-126">NukeDownloadedCache Function</span></span>](../../../../docs/framework/unmanaged-api/fusion/nukedownloadedcache-function.md)
- [<span data-ttu-id="59f54-127">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="59f54-127">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
