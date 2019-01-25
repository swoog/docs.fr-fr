---
title: BucketParameters, structure
ms.date: 03/30/2017
api_name:
- BucketParameters
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- BucketParameters
helpviewer_keywords:
- BucketParameters structure [.NET Framework hosting]
ms.assetid: 9432487e-f276-45d6-9a13-9a68024dbd46
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cf52f74c38b479664ad7e015180b26e0a53c235e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54508299"
---
# <a name="bucketparameters-structure"></a><span data-ttu-id="fbb13-102">BucketParameters, structure</span><span class="sxs-lookup"><span data-stu-id="fbb13-102">BucketParameters Structure</span></span>
<span data-ttu-id="fbb13-103">Stocke le nom de type d’un événement et les paramètres de l’exception actuelle est associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="fbb13-103">Stores the type name of an event and the parameters for the current exception that is associated with the event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fbb13-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbb13-104">Syntax</span></span>  
  
```  
typedef struct _BucketParameters {  
    BOOL  fInited;                    
    WCHAR pszEventTypeName[255];      
    WCHAR pszParams[10][255];         
} BucketParameters;  
```  
  
## <a name="members"></a><span data-ttu-id="fbb13-105">Membres</span><span class="sxs-lookup"><span data-stu-id="fbb13-105">Members</span></span>  
  
|<span data-ttu-id="fbb13-106">Membre</span><span class="sxs-lookup"><span data-stu-id="fbb13-106">Member</span></span>|<span data-ttu-id="fbb13-107">Description</span><span class="sxs-lookup"><span data-stu-id="fbb13-107">Description</span></span>|  
|------------|-----------------|  
|`fInited`|<span data-ttu-id="fbb13-108">`true`, si le reste de cette structure est valide ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="fbb13-108">`true`, if the rest of this structure is valid; otherwise, `false`.</span></span>|  
|`pszEventTypeName`|<span data-ttu-id="fbb13-109">Nom du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="fbb13-109">Name of the event type.</span></span>|  
|`pszParams`|<span data-ttu-id="fbb13-110">Tableau de chaînes, dont chacun spécifie un paramètre pour l’exception actuelle associée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="fbb13-110">An array of strings, each of which specifies a parameter for the current exception associated with the event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fbb13-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fbb13-111">Requirements</span></span>  
 <span data-ttu-id="fbb13-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fbb13-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fbb13-113">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="fbb13-113">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="fbb13-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fbb13-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fbb13-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbb13-115">See also</span></span>
- [<span data-ttu-id="fbb13-116">Structures d’hébergement</span><span class="sxs-lookup"><span data-stu-id="fbb13-116">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
