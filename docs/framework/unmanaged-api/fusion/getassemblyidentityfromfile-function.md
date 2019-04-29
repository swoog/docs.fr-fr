---
title: GetAssemblyIdentityFromFile, fonction
ms.date: 03/30/2017
api_name:
- GetAssemblyIdentityFromFile
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- COM
f1_keywords:
- GetAssemblyIdentityFromFile
helpviewer_keywords:
- GetAssemblyIdentityFromFile function [.NET Framework fusion]
ms.assetid: 2c32da53-76c7-4048-84d0-d05207333004
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4f5dd25ec2a6a1b0b5d6266c3d8e728bd128a9ed
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697756"
---
# <a name="getassemblyidentityfromfile-function"></a><span data-ttu-id="9df0d-102">GetAssemblyIdentityFromFile, fonction</span><span class="sxs-lookup"><span data-stu-id="9df0d-102">GetAssemblyIdentityFromFile Function</span></span>
<span data-ttu-id="9df0d-103">Obtient un pointeur vers un `IUnknown` objet avec la valeur `IID` dans l’assembly dans le chemin de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="9df0d-103">Gets a pointer to an `IUnknown` object with the specified `IID` in the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9df0d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9df0d-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyIdentityFromFile (  
    [in]  LPCWSTR   pwzFilePath,  
    [in]  REFIID    riid,  
    [out] IUnknown  **ppIdentity  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="9df0d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9df0d-105">Parameters</span></span>  
 `pwzFilePath`  
 <span data-ttu-id="9df0d-106">[in] Un chemin d’accès valide à l’assembly demandé.</span><span class="sxs-lookup"><span data-stu-id="9df0d-106">[in] A valid path to the requested assembly.</span></span>  
  
 `riid`  
 <span data-ttu-id="9df0d-107">[in] Le `IID` de l’interface à retourner.</span><span class="sxs-lookup"><span data-stu-id="9df0d-107">[in] The `IID` of the interface to return.</span></span>  
  
 `ppIdentity`  
 <span data-ttu-id="9df0d-108">[out] Le pointeur d’interface retourné.</span><span class="sxs-lookup"><span data-stu-id="9df0d-108">[out] The returned interface pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9df0d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9df0d-109">Requirements</span></span>  
 <span data-ttu-id="9df0d-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9df0d-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9df0d-111">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="9df0d-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="9df0d-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9df0d-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9df0d-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9df0d-113">See also</span></span>

- [<span data-ttu-id="9df0d-114">IUnknown</span><span class="sxs-lookup"><span data-stu-id="9df0d-114">IUnknown</span></span>](/cpp/atl/iunknown)
- [<span data-ttu-id="9df0d-115">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="9df0d-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
