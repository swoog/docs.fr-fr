---
title: ICorRuntimeHost::MapFile, méthode
ms.date: 03/30/2017
api_name:
- ICorRuntimeHost.MapFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorRuntimeHost::MapFile
helpviewer_keywords:
- ICorRuntimeHost::MapFile method [.NET Framework hosting]
- MapFile method [.NET Framework hosting]
ms.assetid: 45ae0502-0a31-4342-b7e3-f36e1cf738f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 956de98fca1caec0ac1b94afc7251f9741246f94
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57494777"
---
# <a name="icorruntimehostmapfile-method"></a><span data-ttu-id="bf24b-102">ICorRuntimeHost::MapFile, méthode</span><span class="sxs-lookup"><span data-stu-id="bf24b-102">ICorRuntimeHost::MapFile Method</span></span>
<span data-ttu-id="bf24b-103">Mappe le fichier spécifié dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="bf24b-103">Maps the specified file into memory.</span></span> <span data-ttu-id="bf24b-104">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="bf24b-104">This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bf24b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf24b-105">Syntax</span></span>  
  
```  
HRESULT MapFile(  
    [in]  HANDLE    hFile,  
    [out] HMODULE*  hMapAddress  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bf24b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf24b-106">Parameters</span></span>  
 `hFile`  
 <span data-ttu-id="bf24b-107">[in] Le handle du fichier à mapper.</span><span class="sxs-lookup"><span data-stu-id="bf24b-107">[in] The handle of the file to be mapped.</span></span>  
  
 `hMapAddress`  
 <span data-ttu-id="bf24b-108">[out] L’adresse mémoire de départ à partir duquel commencer le fichier de mappage.</span><span class="sxs-lookup"><span data-stu-id="bf24b-108">[out] The starting memory address at which to begin mapping the file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bf24b-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bf24b-109">Requirements</span></span>  
 <span data-ttu-id="bf24b-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bf24b-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bf24b-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bf24b-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bf24b-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bf24b-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bf24b-113">**Version du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="bf24b-113">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf24b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf24b-114">See also</span></span>
- [<span data-ttu-id="bf24b-115">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="bf24b-115">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
