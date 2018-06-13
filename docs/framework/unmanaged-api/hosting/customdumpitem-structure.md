---
title: CustomDumpItem, structure
ms.date: 03/30/2017
api_name:
- CustomDumpItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CustomDumpItem
helpviewer_keywords:
- CustomDumpItem structure [.NET Framework hosting]
ms.assetid: fd9085ff-7beb-4c38-97f0-037cd8ba4f65
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f742d219d603488bbade091f7a8192785d3e84f6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33433094"
---
# <a name="customdumpitem-structure"></a><span data-ttu-id="64445-102">CustomDumpItem, structure</span><span class="sxs-lookup"><span data-stu-id="64445-102">CustomDumpItem Structure</span></span>
<span data-ttu-id="64445-103">Décrit un élément à ajouter à un dump personnalisé dans le rapport d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="64445-103">Describes an item to be added to a custom dump in error reporting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="64445-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64445-104">Syntax</span></span>  
  
```  
struct {  
    ECustomDumpItemKind itemKind;   
    union {  
        UINT_PTR pReserved;  
    }  
} CustomDumpItem;  
```  
  
## <a name="members"></a><span data-ttu-id="64445-105">Membres</span><span class="sxs-lookup"><span data-stu-id="64445-105">Members</span></span>  
  
|<span data-ttu-id="64445-106">Membre</span><span class="sxs-lookup"><span data-stu-id="64445-106">Member</span></span>|<span data-ttu-id="64445-107">Description</span><span class="sxs-lookup"><span data-stu-id="64445-107">Description</span></span>|  
|------------|-----------------|  
|`itemKind`|<span data-ttu-id="64445-108">Un [ECustomDumpItemKind](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md) valeur qui indique le type d’élément à ajouter.</span><span class="sxs-lookup"><span data-stu-id="64445-108">An [ECustomDumpItemKind](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md) value that indicates the kind of item to be added.</span></span>|  
|`pReserved`|<span data-ttu-id="64445-109">Actuellement non utilisé.</span><span class="sxs-lookup"><span data-stu-id="64445-109">Not currently used.</span></span> <span data-ttu-id="64445-110">Les éléments ajoutés à l’union doivent être non supérieure à la taille du pointeur.</span><span class="sxs-lookup"><span data-stu-id="64445-110">Any items added to the union must be no larger than pointer size.</span></span> <span data-ttu-id="64445-111">Si un `struct` est nécessaire, vous devez allouer séparément et pointer sur elle.</span><span class="sxs-lookup"><span data-stu-id="64445-111">If a `struct` is required, you must allocate it separately and point to it.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="64445-112">Notes</span><span class="sxs-lookup"><span data-stu-id="64445-112">Remarks</span></span>  
 <span data-ttu-id="64445-113">[ICLRErrorReportingManager::BeginCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) prend un paramètre de type `CustomDumpItem`.</span><span class="sxs-lookup"><span data-stu-id="64445-113">[ICLRErrorReportingManager::BeginCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) takes a parameter of type `CustomDumpItem`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="64445-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="64445-114">Requirements</span></span>  
 <span data-ttu-id="64445-115">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="64445-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="64445-116">**En-tête :** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="64445-116">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="64445-117">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="64445-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="64445-118">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="64445-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="64445-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64445-119">See Also</span></span>  
 [<span data-ttu-id="64445-120">Structures d’hébergement</span><span class="sxs-lookup"><span data-stu-id="64445-120">Hosting Structures</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
