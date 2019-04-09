---
title: _CorImageUnloading, fonction
ms.date: 03/30/2017
api_name:
- _CorImageUnloading
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorImageUnloading
helpviewer_keywords:
- _CorImageUnloading function [.NET Framework hosting]
ms.assetid: b4367214-6dac-4280-aa11-fd487ff30bc4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1cb5f9decbcdfb71f67a5132dc59773f1de8b0a9
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59086427"
---
# <a name="corimageunloading-function"></a><span data-ttu-id="6850d-102">_CorImageUnloading, fonction</span><span class="sxs-lookup"><span data-stu-id="6850d-102">_CorImageUnloading Function</span></span>
<span data-ttu-id="6850d-103">Notifie le chargeur lorsque les images de modules managés sont déchargées.</span><span class="sxs-lookup"><span data-stu-id="6850d-103">Notifies the loader when the managed module images are unloaded.</span></span>  
  
 <span data-ttu-id="6850d-104">Cette fonction n’est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="6850d-104">This function is not implemented.</span></span> <span data-ttu-id="6850d-105">Si elle est appelée, elle retourne E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6850d-105">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6850d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6850d-106">Syntax</span></span>  
  
```  
STDAPI (VOID) _CorImageUnloading(   
   [in] PVOID* ImageBase  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6850d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6850d-107">Parameters</span></span>  
 `ImageBase`  
 <span data-ttu-id="6850d-108">[in] Pointeur vers l’emplacement de départ de l’image à décharger.</span><span class="sxs-lookup"><span data-stu-id="6850d-108">[in] A pointer to the starting location of the image to unload.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6850d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6850d-109">Requirements</span></span>  
 <span data-ttu-id="6850d-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6850d-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6850d-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="6850d-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="6850d-112">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6850d-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="6850d-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="6850d-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="6850d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6850d-114">See also</span></span>

- [<span data-ttu-id="6850d-115">Fonctions statiques globales des métadonnées</span><span class="sxs-lookup"><span data-stu-id="6850d-115">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
