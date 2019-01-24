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
ms.openlocfilehash: 814073b766d5d562b414a566ae3f92abd664ce35
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54707841"
---
# <a name="icorruntimehostmapfile-method"></a><span data-ttu-id="a3ebc-102">ICorRuntimeHost::MapFile, méthode</span><span class="sxs-lookup"><span data-stu-id="a3ebc-102">ICorRuntimeHost::MapFile Method</span></span>
<span data-ttu-id="a3ebc-103">Mappe le fichier spécifié dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-103">Maps the specified file into memory.</span></span> <span data-ttu-id="a3ebc-104">Cette méthode est obsolète.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-104">This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3ebc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3ebc-105">Syntax</span></span>  
  
```  
HRESULT MapFile(  
    [in]  HANDLE    hFile,  
    [out] HMODULE*  hMapAddress  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a3ebc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3ebc-106">Parameters</span></span>  
 `hFile`  
 <span data-ttu-id="a3ebc-107">[in] Le handle du fichier à mapper.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-107">[in] The handle of the file to be mapped.</span></span>  
  
 `hMapAddress`  
 <span data-ttu-id="a3ebc-108">[out] L’adresse mémoire de départ à partir duquel commencer le fichier de mappage.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-108">[out] The starting memory address at which to begin mapping the file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a3ebc-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a3ebc-109">Requirements</span></span>  
 <span data-ttu-id="a3ebc-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a3ebc-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3ebc-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="a3ebc-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="a3ebc-112">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a3ebc-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a3ebc-113">**Version du .NET framework :** 1.0, 1.1</span><span class="sxs-lookup"><span data-stu-id="a3ebc-113">**.NET Framework Version:** 1.0, 1.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3ebc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3ebc-114">See also</span></span>
- [<span data-ttu-id="a3ebc-115">ICorRuntimeHost, interface</span><span class="sxs-lookup"><span data-stu-id="a3ebc-115">ICorRuntimeHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
