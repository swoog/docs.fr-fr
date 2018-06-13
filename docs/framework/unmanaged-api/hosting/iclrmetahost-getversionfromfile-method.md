---
title: ICLRMetaHost::GetVersionFromFile, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.GetVersionFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::GetVersionFromFile
helpviewer_keywords:
- ICLRMetaHost::GetVersionFromFile method [.NET Framework hosting]
- GetVersionFromFile method [.NET Framework hosting]
ms.assetid: 55bb3eb4-f665-42fc-973c-465567570e82
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 538e596c3a705020150f52c9e55605a49434ce8f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33434049"
---
# <a name="iclrmetahostgetversionfromfile-method"></a><span data-ttu-id="b4471-102">ICLRMetaHost::GetVersionFromFile, méthode</span><span class="sxs-lookup"><span data-stu-id="b4471-102">ICLRMetaHost::GetVersionFromFile Method</span></span>
<span data-ttu-id="b4471-103">Obtient d’origine .NET Framework version de compilation d’un assembly (stockée dans les métadonnées), étant donnée son chemin d’accès de fichier.</span><span class="sxs-lookup"><span data-stu-id="b4471-103">Gets an assembly's original .NET Framework compilation version (stored in the metadata), given its file path.</span></span> <span data-ttu-id="b4471-104">Cette méthode remplace la [GetFileVersion](../../../../docs/framework/unmanaged-api/hosting/getfileversion-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="b4471-104">This method supersedes the [GetFileVersion](../../../../docs/framework/unmanaged-api/hosting/getfileversion-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4471-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4471-105">Syntax</span></span>  
  
```  
HRESULT GetVersionFromFile (  
    [in] LPCWSTR pwzFilePath,  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBuffer);  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b4471-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4471-106">Parameters</span></span>  
 `pwzFilePath`  
 <span data-ttu-id="b4471-107">[in] Le chemin d’accès de fichier d’assembly complet.</span><span class="sxs-lookup"><span data-stu-id="b4471-107">[in] The complete assembly file path.</span></span>  
  
 `pwzbuffer`  
 <span data-ttu-id="b4471-108">[out] La version de compilation .NET Framework stockée dans les métadonnées, au format « v*A*. *B*[. *X*] ».</span><span class="sxs-lookup"><span data-stu-id="b4471-108">[out] The .NET Framework compilation version stored in the metadata, in the format "v*A*.*B*[.*X*]".</span></span> <span data-ttu-id="b4471-109">*A*, *B*, et *X* sont des nombres décimaux qui correspondent à la version principale, la version secondaire et le numéro de build.</span><span class="sxs-lookup"><span data-stu-id="b4471-109">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span> <span data-ttu-id="b4471-110">La longueur de cette chaîne est limitée à MAX_PATH.</span><span class="sxs-lookup"><span data-stu-id="b4471-110">The length of this string is limited to MAX_PATH.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b4471-111">Cette sortie correspond au nom de répertoire pour la version de .NET Framework, tel qu’il apparaît sous C:\Windows\Microsoft.NET\Framework.</span><span class="sxs-lookup"><span data-stu-id="b4471-111">This output matches the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework.</span></span>  
  
 <span data-ttu-id="b4471-112">Exemples de valeurs sont « v1.0.3705 », « v1.1.4322 », « v2.0.50727 » et « v4.0. *X*», où *X* varie selon le numéro de build installé.</span><span class="sxs-lookup"><span data-stu-id="b4471-112">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*X*", where *X* depends on the build number installed.</span></span> <span data-ttu-id="b4471-113">Notez que le préfixe « v » est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b4471-113">Note that the "v" prefix is required.</span></span>  
  
 `pcchBuffer`  
 <span data-ttu-id="b4471-114">[dans, out] La taille de `pwzbuffer` pour éviter les dépassements de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b4471-114">[in, out] The size of `pwzbuffer` to avoid buffer overruns.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b4471-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b4471-115">Return Value</span></span>  
 <span data-ttu-id="b4471-116">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="b4471-116">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="b4471-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b4471-117">HRESULT</span></span>|<span data-ttu-id="b4471-118">Description</span><span class="sxs-lookup"><span data-stu-id="b4471-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b4471-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4471-119">S_OK</span></span>|<span data-ttu-id="b4471-120">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="b4471-120">The method completed successfully.</span></span>|  
|<span data-ttu-id="b4471-121">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="b4471-121">E_POINTER</span></span>|<span data-ttu-id="b4471-122">`pwzbuffer` ou `pcchBuffer` est null.</span><span class="sxs-lookup"><span data-stu-id="b4471-122">`pwzbuffer` or `pcchBuffer` is null.</span></span>|  
|<span data-ttu-id="b4471-123">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span><span class="sxs-lookup"><span data-stu-id="b4471-123">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span></span>|<span data-ttu-id="b4471-124">La mémoire tampon est trop petite.</span><span class="sxs-lookup"><span data-stu-id="b4471-124">The buffer is too small.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b4471-125">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b4471-125">Requirements</span></span>  
 <span data-ttu-id="b4471-126">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b4471-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b4471-127">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="b4471-127">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="b4471-128">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b4471-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="b4471-129">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b4471-129">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4471-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4471-130">See Also</span></span>  
 [<span data-ttu-id="b4471-131">ICLRMetaHost, interface</span><span class="sxs-lookup"><span data-stu-id="b4471-131">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)  
 [<span data-ttu-id="b4471-132">Hébergement</span><span class="sxs-lookup"><span data-stu-id="b4471-132">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
