---
title: NukeDownloadedCache, fonction
ms.date: 03/30/2017
api_name:
- NukeDownloadedCache
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- NukeDownloadedCache
helpviewer_keywords:
- NukeDownloadedCache function [.NET Framework fusion]
ms.assetid: fac2b1c6-6fa3-4818-805b-b63972024c86
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4e549e13c0d51e4aa708a674a2224168ab66f8ad
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59178163"
---
# <a name="nukedownloadedcache-function"></a><span data-ttu-id="997f1-102">NukeDownloadedCache, fonction</span><span class="sxs-lookup"><span data-stu-id="997f1-102">NukeDownloadedCache Function</span></span>
<span data-ttu-id="997f1-103">Supprime le cache de téléchargement du common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="997f1-103">Deletes the common language runtime (CLR) download cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="997f1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="997f1-104">Syntax</span></span>  
  
```  
HRESULT NukeDownloadedCache();  
```  
  
## <a name="return-value"></a><span data-ttu-id="997f1-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="997f1-105">Return Value</span></span>  
 <span data-ttu-id="997f1-106">Cette méthode retourne des codes d’erreur COM standards, tel que défini dans WinError.h.</span><span class="sxs-lookup"><span data-stu-id="997f1-106">This method returns standard COM error codes, as defined in WinError.h.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="997f1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="997f1-107">Remarks</span></span>  
 <span data-ttu-id="997f1-108">Le cache de téléchargement CLR est la zone où les assemblys avec nom fort qui sont téléchargés à partir d’une URL sont stockés pour une réutilisation éventuelle.</span><span class="sxs-lookup"><span data-stu-id="997f1-108">The CLR download cache is the area where strong-named assemblies that are downloaded from a URL are stored for possible reuse.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="997f1-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="997f1-109">Requirements</span></span>  
 <span data-ttu-id="997f1-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="997f1-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="997f1-111">**En-tête :** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="997f1-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="997f1-112">**Bibliothèque :** Le fichier fusion.dll et Mscorwks.dll.</span><span class="sxs-lookup"><span data-stu-id="997f1-112">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="997f1-113">Utilisez le fichier Fusion.dll plutôt que Mscorwks.dll pour vous assurer que vous ciblez la version correcte du .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="997f1-113">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 **<span data-ttu-id="997f1-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="997f1-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="997f1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="997f1-115">See also</span></span>

- [<span data-ttu-id="997f1-116">CreateHistoryReader, fonction</span><span class="sxs-lookup"><span data-stu-id="997f1-116">CreateHistoryReader Function</span></span>](../../../../docs/framework/unmanaged-api/fusion/createhistoryreader-function.md)
- [<span data-ttu-id="997f1-117">GetHistoryFileDirectory, fonction</span><span class="sxs-lookup"><span data-stu-id="997f1-117">GetHistoryFileDirectory Function</span></span>](../../../../docs/framework/unmanaged-api/fusion/gethistoryfiledirectory-function.md)
- [<span data-ttu-id="997f1-118">Fonctions statiques globales de la fusion</span><span class="sxs-lookup"><span data-stu-id="997f1-118">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
