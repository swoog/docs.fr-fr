---
title: IValidator, interface
ms.date: 03/30/2017
api_name:
- IValidator
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IValidator
helpviewer_keywords:
- IValidator interface [.NET Framework hosting]
ms.assetid: b297e3b0-20f9-478f-b707-5e2eecb2b5b2
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2f516bf1f19e4d4a77e2d6af834a1c3d4e34c327
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59121912"
---
# <a name="ivalidator-interface"></a><span data-ttu-id="356c3-102">IValidator, interface</span><span class="sxs-lookup"><span data-stu-id="356c3-102">IValidator Interface</span></span>
<span data-ttu-id="356c3-103">Fournit des méthodes pour la validation des images (PE) exécutables portables et de signalement des erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="356c3-103">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="356c3-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="356c3-104">Methods</span></span>  
  
|<span data-ttu-id="356c3-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="356c3-105">Method</span></span>|<span data-ttu-id="356c3-106">Description</span><span class="sxs-lookup"><span data-stu-id="356c3-106">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="356c3-107">Valider</span><span class="sxs-lookup"><span data-stu-id="356c3-107">Validate</span></span>|<span data-ttu-id="356c3-108">Valide le fichier de langage intermédiaire (MSIL) PE ou Microsoft spécifié.</span><span class="sxs-lookup"><span data-stu-id="356c3-108">Validates the specified PE or Microsoft intermediate language (MSIL) file.</span></span>|  
|<span data-ttu-id="356c3-109">FormatEventInfo</span><span class="sxs-lookup"><span data-stu-id="356c3-109">FormatEventInfo</span></span>|<span data-ttu-id="356c3-110">Obtient le message d’erreur correspondant à l’erreur de validation spécifié.</span><span class="sxs-lookup"><span data-stu-id="356c3-110">Gets the error message corresponding to the specified validation error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="356c3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="356c3-111">Requirements</span></span>  
 <span data-ttu-id="356c3-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="356c3-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="356c3-113">**En-tête :** IValidator.idl, IValidator.h</span><span class="sxs-lookup"><span data-stu-id="356c3-113">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="356c3-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="356c3-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="356c3-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="356c3-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="356c3-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="356c3-116">See also</span></span>

- [<span data-ttu-id="356c3-117">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="356c3-117">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="356c3-118">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="356c3-118">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
