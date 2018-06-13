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
ms.openlocfilehash: bba40acf7bfd20897ece4de285fe7a9175be83e0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431761"
---
# <a name="gethistoryfiledirectory-function"></a><span data-ttu-id="ad97c-102">GetHistoryFileDirectory, fonction</span><span class="sxs-lookup"><span data-stu-id="ad97c-102">GetHistoryFileDirectory Function</span></span>
<span data-ttu-id="ad97c-103">Récupère le chemin d’accès du répertoire de l’historique de l’application.</span><span class="sxs-lookup"><span data-stu-id="ad97c-103">Retrieves the path of the application history directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad97c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad97c-104">Syntax</span></span>  
  
```  
HRESULT GetHistoryFileDirectory (  
    [in]      LPWSTR      wzDir,  
    [in,out]  LPCWSTR  *pdwsize,  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ad97c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad97c-105">Parameters</span></span>  
 `wzDir`  
 <span data-ttu-id="ad97c-106">[out] Une mémoire tampon pour stocker le chemin d’accès au répertoire de l’historique de l’application.</span><span class="sxs-lookup"><span data-stu-id="ad97c-106">[out] A buffer to hold the path to the application history directory.</span></span>  
  
 `pdwSize`  
 <span data-ttu-id="ad97c-107">[dans, out] La longueur de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ad97c-107">[in, out] The length of the buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ad97c-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ad97c-108">Return Value</span></span>  
 <span data-ttu-id="ad97c-109">Cette méthode retourne des codes d’erreur COM standard, tel que défini dans le fichier WinError.h, en plus des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ad97c-109">This method returns standard COM error codes, as defined in the WinError.h file in addition to the following values.</span></span>  
  
|<span data-ttu-id="ad97c-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ad97c-110">Return code</span></span>|<span data-ttu-id="ad97c-111">Description</span><span class="sxs-lookup"><span data-stu-id="ad97c-111">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="ad97c-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad97c-112">S_OK</span></span>|<span data-ttu-id="ad97c-113">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="ad97c-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="ad97c-114">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ad97c-114">E_INVALIDARG</span></span>|<span data-ttu-id="ad97c-115">`wzDir` ou `pdwSize` est null, ou la version de chaîne est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ad97c-115">`wzDir` or `pdwSize` is null, or the version string is incorrect.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ad97c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ad97c-116">Remarks</span></span>  
 <span data-ttu-id="ad97c-117">Opération réussie, le `pdwSize` argument est défini à la longueur de la chaîne de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="ad97c-117">On successful completion, the `pdwSize` argument is set to the length of the path string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad97c-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ad97c-118">Requirements</span></span>  
 <span data-ttu-id="ad97c-119">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ad97c-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad97c-120">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="ad97c-120">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="ad97c-121">**Bibliothèque :** Fusion.dll et Mscorwks.dll.</span><span class="sxs-lookup"><span data-stu-id="ad97c-121">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="ad97c-122">Utilisez le fichier Fusion.dll plutôt que Mscorwks.dll pour garantir que vous ciblez la version appropriée du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ad97c-122">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="ad97c-123">**Versions du .NET framework :** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ad97c-123">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad97c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad97c-124">See Also</span></span>  
 [<span data-ttu-id="ad97c-125">CreateHistoryReader, fonction</span><span class="sxs-lookup"><span data-stu-id="ad97c-125">CreateHistoryReader Function</span></span>](../../../../docs/framework/unmanaged-api/fusion/createhistoryreader-function.md)  
 [<span data-ttu-id="ad97c-126">NukeDownloadedCache, fonction</span><span class="sxs-lookup"><span data-stu-id="ad97c-126">NukeDownloadedCache Function</span></span>](../../../../docs/framework/unmanaged-api/fusion/nukedownloadedcache-function.md)  
 [<span data-ttu-id="ad97c-127">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="ad97c-127">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
