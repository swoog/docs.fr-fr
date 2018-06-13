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
ms.openlocfilehash: 9e79a69bf71aee035fb1f9a0178879d7c19e62b9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448919"
---
# <a name="ivalidator-interface"></a><span data-ttu-id="6f42e-102">IValidator, interface</span><span class="sxs-lookup"><span data-stu-id="6f42e-102">IValidator Interface</span></span>
<span data-ttu-id="6f42e-103">Fournit des méthodes pour la validation des images (PE) exécutables portables et de rapports d’erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="6f42e-103">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6f42e-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6f42e-104">Methods</span></span>  
  
|<span data-ttu-id="6f42e-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="6f42e-105">Method</span></span>|<span data-ttu-id="6f42e-106">Description</span><span class="sxs-lookup"><span data-stu-id="6f42e-106">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="6f42e-107">Valider</span><span class="sxs-lookup"><span data-stu-id="6f42e-107">Validate</span></span>|<span data-ttu-id="6f42e-108">Valide le fichier PE ou Microsoft intermediate language (MSIL) en spécifié.</span><span class="sxs-lookup"><span data-stu-id="6f42e-108">Validates the specified PE or Microsoft intermediate language (MSIL) file.</span></span>|  
|<span data-ttu-id="6f42e-109">FormatEventInfo</span><span class="sxs-lookup"><span data-stu-id="6f42e-109">FormatEventInfo</span></span>|<span data-ttu-id="6f42e-110">Obtient le message d’erreur correspondant à l’erreur de validation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f42e-110">Gets the error message corresponding to the specified validation error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="6f42e-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="6f42e-111">Requirements</span></span>  
 <span data-ttu-id="6f42e-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6f42e-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6f42e-113">**En-tête :** IValidator.idl, IValidator.h</span><span class="sxs-lookup"><span data-stu-id="6f42e-113">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="6f42e-114">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6f42e-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="6f42e-115">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6f42e-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6f42e-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f42e-116">See Also</span></span>  
 [<span data-ttu-id="6f42e-117">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="6f42e-117">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="6f42e-118">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="6f42e-118">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
