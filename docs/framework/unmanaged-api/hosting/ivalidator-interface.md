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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61765347"
---
# <a name="ivalidator-interface"></a><span data-ttu-id="f455f-102">IValidator, interface</span><span class="sxs-lookup"><span data-stu-id="f455f-102">IValidator Interface</span></span>
<span data-ttu-id="f455f-103">Fournit des méthodes pour la validation des images (PE) exécutables portables et de signalement des erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="f455f-103">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f455f-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f455f-104">Methods</span></span>  
  
|<span data-ttu-id="f455f-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f455f-105">Method</span></span>|<span data-ttu-id="f455f-106">Description</span><span class="sxs-lookup"><span data-stu-id="f455f-106">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="f455f-107">Valider</span><span class="sxs-lookup"><span data-stu-id="f455f-107">Validate</span></span>|<span data-ttu-id="f455f-108">Valide le fichier de langage intermédiaire (MSIL) PE ou Microsoft spécifié.</span><span class="sxs-lookup"><span data-stu-id="f455f-108">Validates the specified PE or Microsoft intermediate language (MSIL) file.</span></span>|  
|<span data-ttu-id="f455f-109">FormatEventInfo</span><span class="sxs-lookup"><span data-stu-id="f455f-109">FormatEventInfo</span></span>|<span data-ttu-id="f455f-110">Obtient le message d’erreur correspondant à l’erreur de validation spécifié.</span><span class="sxs-lookup"><span data-stu-id="f455f-110">Gets the error message corresponding to the specified validation error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f455f-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f455f-111">Requirements</span></span>  
 <span data-ttu-id="f455f-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f455f-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f455f-113">**En-tête :** IValidator.idl, IValidator.h</span><span class="sxs-lookup"><span data-stu-id="f455f-113">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="f455f-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f455f-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f455f-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f455f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f455f-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f455f-116">See also</span></span>

- [<span data-ttu-id="f455f-117">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="f455f-117">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="f455f-118">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="f455f-118">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
