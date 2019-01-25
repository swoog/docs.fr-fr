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
ms.openlocfilehash: 9f307ad5689602b030c609a51f6834bdbb0ec4f8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54717713"
---
# <a name="ivalidator-interface"></a><span data-ttu-id="0c860-102">IValidator, interface</span><span class="sxs-lookup"><span data-stu-id="0c860-102">IValidator Interface</span></span>
<span data-ttu-id="0c860-103">Fournit des méthodes pour la validation des images (PE) exécutables portables et de signalement des erreurs de validation.</span><span class="sxs-lookup"><span data-stu-id="0c860-103">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0c860-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c860-104">Methods</span></span>  
  
|<span data-ttu-id="0c860-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="0c860-105">Method</span></span>|<span data-ttu-id="0c860-106">Description</span><span class="sxs-lookup"><span data-stu-id="0c860-106">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="0c860-107">Valider</span><span class="sxs-lookup"><span data-stu-id="0c860-107">Validate</span></span>|<span data-ttu-id="0c860-108">Valide le fichier de langage intermédiaire (MSIL) PE ou Microsoft spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c860-108">Validates the specified PE or Microsoft intermediate language (MSIL) file.</span></span>|  
|<span data-ttu-id="0c860-109">FormatEventInfo</span><span class="sxs-lookup"><span data-stu-id="0c860-109">FormatEventInfo</span></span>|<span data-ttu-id="0c860-110">Obtient le message d’erreur correspondant à l’erreur de validation spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c860-110">Gets the error message corresponding to the specified validation error.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0c860-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0c860-111">Requirements</span></span>  
 <span data-ttu-id="0c860-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0c860-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0c860-113">**En-tête :** IValidator.idl, IValidator.h</span><span class="sxs-lookup"><span data-stu-id="0c860-113">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="0c860-114">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0c860-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0c860-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0c860-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c860-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c860-116">See also</span></span>
- [<span data-ttu-id="0c860-117">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="0c860-117">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
- [<span data-ttu-id="0c860-118">CorRuntimeHost, coclasse</span><span class="sxs-lookup"><span data-stu-id="0c860-118">CorRuntimeHost Coclass</span></span>](../../../../docs/framework/unmanaged-api/hosting/corruntimehost-coclass.md)
