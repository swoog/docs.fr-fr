---
title: ICLRDebuggingLibraryProvider::ProvideLibrary, méthode
ms.date: 03/30/2017
api_name:
- ICLRDebuggingLibraryProvider.ProvideLibrary Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebuggingLibraryProvider::ProvideLibrary
helpviewer_keywords:
- ProvideLibrary method [.NET Framework debugging]
- ICLRDebuggingLibraryProvider::ProvideLibrary method [.NET Framework debugging]
ms.assetid: 86f06245-9517-49be-8d8c-ca5deaf34c02
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5f5d44b6497e971e6d1ed030c043b91b88c070b6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59218509"
---
# <a name="iclrdebugginglibraryproviderprovidelibrary-method"></a><span data-ttu-id="3e5a1-102">ICLRDebuggingLibraryProvider::ProvideLibrary, méthode</span><span class="sxs-lookup"><span data-stu-id="3e5a1-102">ICLRDebuggingLibraryProvider::ProvideLibrary Method</span></span>
<span data-ttu-id="3e5a1-103">Obtient un fournisseur de bibliothèque interface de rappel qui permet de common language runtime (CLR) des bibliothèques de débogage spécifiques à la version être à la demande et le chargement.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-103">Gets a library provider callback interface that allows common language runtime (CLR) version-specific debugging libraries to be located and loaded on demand.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e5a1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e5a1-104">Syntax</span></span>  
  
```  
HRESULT ProvideLibrary(  
     [in] const WCHAR* pwszFileName,  
     [in] DWORD dwTimestamp,  
     [in] DWORD dwSizeOfImage,  
     [out] HMODULE* hModule);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3e5a1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e5a1-105">Parameters</span></span>  
 `pwszFilename`  
 <span data-ttu-id="3e5a1-106">[in] Nom du module demandé.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-106">[in] The name of the module being requested.</span></span>  
  
 `dwTimestamp`  
 <span data-ttu-id="3e5a1-107">[in] L’horodatage stockée dans l’en-tête du fichier COFF de fichiers PE.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-107">[in] The date time stamp stored in the COFF file header of PE files.</span></span>  
  
 `pLibraryProvider`  
 <span data-ttu-id="3e5a1-108">[in] Le `SizeOfImage` champ stocké dans l’en-tête de fichier facultatif COFF de fichiers PE.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-108">[in] The `SizeOfImage` field stored in the COFF optional file header of PE files.</span></span>  
  
 `hModule`  
 <span data-ttu-id="3e5a1-109">[out] Le handle du module demandé.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-109">[out] The handle to the requested module.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3e5a1-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3e5a1-110">Return Value</span></span>  
 <span data-ttu-id="3e5a1-111">Cette méthode retourne les HRESULT spécifiques suivants ainsi que les erreurs HRESULT indiquant l'échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-111">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="3e5a1-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="3e5a1-112">HRESULT</span></span>|<span data-ttu-id="3e5a1-113">Description</span><span class="sxs-lookup"><span data-stu-id="3e5a1-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="3e5a1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e5a1-114">S_OK</span></span>|<span data-ttu-id="3e5a1-115">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-115">The method completed successfully.</span></span>|  
  
## <a name="exceptions"></a><span data-ttu-id="3e5a1-116">Exceptions</span><span class="sxs-lookup"><span data-stu-id="3e5a1-116">Exceptions</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3e5a1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3e5a1-117">Remarks</span></span>  
 `ProvideLibrary` <span data-ttu-id="3e5a1-118">permet au débogueur de fournir des modules qui sont nécessaires pour le débogage de fichiers CLR spécifiques tels que mscordbi.dll et mscordacwks.dll.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-118">allows the debugger to provide modules that are needed for debugging specific CLR files such as mscordbi.dll and mscordacwks.dll.</span></span> <span data-ttu-id="3e5a1-119">Les handles de module doivent rester valides tant qu’un appel à la [ICLRDebugging::CanUnloadNow](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-canunloadnow-method.md) méthode indique qu’ils peuvent être libérés, à quel point il est responsable de l’appelant pour libérer les handles.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-119">The module handles have to remain valid until a call to the [ICLRDebugging::CanUnloadNow](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-canunloadnow-method.md) method indicates that they may be freed, at which point it is the caller’s responsibility to free the handles.</span></span>  
  
 <span data-ttu-id="3e5a1-120">Le débogueur peut utiliser tous les moyens pour rechercher ou obtenir le module de débogage.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-120">The debugger may use any available means to locate or procure the debugging module.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="3e5a1-121">Cette fonctionnalité permet à l’appelant de l’API de fournir des modules qui contiennent du code exécutable et potentiellement malveillant.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-121">This feature allows the API caller to provide modules that contain executable, and possibly malicious, code.</span></span> <span data-ttu-id="3e5a1-122">Par mesure de sécurité, l’appelant ne doit pas utiliser `ProvideLibrary` distribuer n’importe quel code qu’il n’est pas prêt à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-122">As a security precaution, the caller should not use `ProvideLibrary` to distribute any code that it is not willing to execute itself.</span></span>  
>   
>  <span data-ttu-id="3e5a1-123">Si un problème de sécurité sérieux est découvert dans une bibliothèque déjà libérée, tels que mscordbi.dll ou mscordacwks.dll, le shim peut être corrigé pour reconnaître les mauvaises versions des fichiers.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-123">If a serious security issue is discovered in an already released library, such as mscordbi.dll or mscordacwks.dll, the shim can be patched to recognize the bad versions of the files.</span></span> <span data-ttu-id="3e5a1-124">Le shim peut ensuite émettre des demandes pour les versions corrigées des fichiers et rejeter les mauvaises versions si elles sont fournies en réponse à toute demande.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-124">The shim can then issue requests for the patched versions of the files and reject the bad versions if they are provided in response to any request.</span></span> <span data-ttu-id="3e5a1-125">Cela peut se produire uniquement si l’utilisateur a corrigé vers une nouvelle version du shim.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-125">This can occur only if the user has patched to a new version of the shim.</span></span> <span data-ttu-id="3e5a1-126">Versions non corrigées restent vulnérables.</span><span class="sxs-lookup"><span data-stu-id="3e5a1-126">Unpatched versions will remain vulnerable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3e5a1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e5a1-127">Requirements</span></span>  
 <span data-ttu-id="3e5a1-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3e5a1-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3e5a1-129">**En-tête :** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3e5a1-129">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3e5a1-130">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3e5a1-130">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="3e5a1-131">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="3e5a1-131">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="3e5a1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e5a1-132">See also</span></span>

- [<span data-ttu-id="3e5a1-133">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="3e5a1-133">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
- [<span data-ttu-id="3e5a1-134">Débogage</span><span class="sxs-lookup"><span data-stu-id="3e5a1-134">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
