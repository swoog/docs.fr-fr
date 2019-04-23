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
ms.openlocfilehash: 5998ce684726b2386d8f1e05eb7eaeccf455747c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59110454"
---
# <a name="bucketparameters-structure"></a><span data-ttu-id="341a0-102">BucketParameters, structure</span><span class="sxs-lookup"><span data-stu-id="341a0-102">BucketParameters Structure</span></span>
<span data-ttu-id="341a0-103">Stocke le nom de type d’un événement et les paramètres de l’exception actuelle est associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="341a0-103">Stores the type name of an event and the parameters for the current exception that is associated with the event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="341a0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="341a0-104">Syntax</span></span>  
  
```  
typedef struct _BucketParameters {  
    BOOL  fInited;                    
    WCHAR pszEventTypeName[255];      
    WCHAR pszParams[10][255];         
} BucketParameters;  
```  
  
## <a name="members"></a><span data-ttu-id="341a0-105">Membres</span><span class="sxs-lookup"><span data-stu-id="341a0-105">Members</span></span>  
  
|<span data-ttu-id="341a0-106">Membre</span><span class="sxs-lookup"><span data-stu-id="341a0-106">Member</span></span>|<span data-ttu-id="341a0-107">Description</span><span class="sxs-lookup"><span data-stu-id="341a0-107">Description</span></span>|  
|------------|-----------------|  
|`fInited`|<span data-ttu-id="341a0-108">`true`, si le reste de cette structure est valide ; Sinon, `false`.</span><span class="sxs-lookup"><span data-stu-id="341a0-108">`true`, if the rest of this structure is valid; otherwise, `false`.</span></span>|  
|`pszEventTypeName`|<span data-ttu-id="341a0-109">Nom du type d’événement.</span><span class="sxs-lookup"><span data-stu-id="341a0-109">Name of the event type.</span></span>|  
|`pszParams`|<span data-ttu-id="341a0-110">Tableau de chaînes, dont chacun spécifie un paramètre pour l’exception actuelle associée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="341a0-110">An array of strings, each of which specifies a parameter for the current exception associated with the event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="341a0-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="341a0-111">Requirements</span></span>  
 <span data-ttu-id="341a0-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="341a0-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="341a0-113">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="341a0-113">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="341a0-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="341a0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="341a0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="341a0-115">See also</span></span>

- [<span data-ttu-id="341a0-116">Structures d’hébergement</span><span class="sxs-lookup"><span data-stu-id="341a0-116">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
