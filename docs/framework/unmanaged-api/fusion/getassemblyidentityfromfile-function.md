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
ms.openlocfilehash: 5ea151417a1cb53104ec29fff1e76e21f82ec9bb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431641"
---
# <a name="getassemblyidentityfromfile-function"></a><span data-ttu-id="50e0b-102">GetAssemblyIdentityFromFile, fonction</span><span class="sxs-lookup"><span data-stu-id="50e0b-102">GetAssemblyIdentityFromFile Function</span></span>
<span data-ttu-id="50e0b-103">Obtient un pointeur vers un `IUnknown` objet `IID` dans l’assembly sur le chemin d’accès de fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="50e0b-103">Gets a pointer to an `IUnknown` object with the specified `IID` in the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50e0b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50e0b-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyIdentityFromFile (  
    [in]  LPCWSTR   pwzFilePath,  
    [in]  REFIID    riid,  
    [out] IUnknown  **ppIdentity  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="50e0b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50e0b-105">Parameters</span></span>  
 `pwzFilePath`  
 <span data-ttu-id="50e0b-106">[in] Un chemin d’accès valide à l’assembly demandé.</span><span class="sxs-lookup"><span data-stu-id="50e0b-106">[in] A valid path to the requested assembly.</span></span>  
  
 `riid`  
 <span data-ttu-id="50e0b-107">[in] Le `IID` de l’interface à retourner.</span><span class="sxs-lookup"><span data-stu-id="50e0b-107">[in] The `IID` of the interface to return.</span></span>  
  
 `ppIdentity`  
 <span data-ttu-id="50e0b-108">[out] Pointeur d’interface retourné.</span><span class="sxs-lookup"><span data-stu-id="50e0b-108">[out] The returned interface pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="50e0b-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="50e0b-109">Requirements</span></span>  
 <span data-ttu-id="50e0b-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="50e0b-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50e0b-111">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="50e0b-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="50e0b-112">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="50e0b-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50e0b-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50e0b-113">See Also</span></span>  
 <span data-ttu-id="50e0b-114"><<!--zzxref:IUnknown --> `IUnknown`></span><span class="sxs-lookup"><span data-stu-id="50e0b-114"><<!--zzxref:IUnknown --> `IUnknown`></span></span>  
 [<span data-ttu-id="50e0b-115">Fonctions statiques globales de fusion</span><span class="sxs-lookup"><span data-stu-id="50e0b-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
