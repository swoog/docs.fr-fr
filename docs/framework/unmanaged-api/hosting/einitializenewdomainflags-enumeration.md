---
title: EInitializeNewDomainFlags, énumération
ms.date: 03/30/2017
api_name:
- EInitializeNewDomainFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EInitializeNewDomainFlags
helpviewer_keywords:
- EInitializeNewDomainFlags enumeration [.NET Framework hosting]
ms.assetid: 3a120ab2-f5ef-4c9b-8595-d3ed7247c342
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 04b0d9989d66888c33de0359e4c93529fcfbf8d1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61628624"
---
# <a name="einitializenewdomainflags-enumeration"></a><span data-ttu-id="3a249-102">EInitializeNewDomainFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="3a249-102">EInitializeNewDomainFlags Enumeration</span></span>
<span data-ttu-id="3a249-103">Permet à l’hôte de fournir au runtime avec des informations sur l’initialisation d’un domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="3a249-103">Enables the host to provide the runtime with information about the initialization of an application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a249-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a249-104">Syntax</span></span>  
  
```  
typedef enum {  
    eInitializeNewDomainFlags_None              = 0x0000,  
    eInitializeNewDomainFlags_NoSecurityChanges = 0x0002  
} EInitializeNewDomainFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="3a249-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3a249-105">Members</span></span>  
  
|<span data-ttu-id="3a249-106">Membre</span><span class="sxs-lookup"><span data-stu-id="3a249-106">Member</span></span>|<span data-ttu-id="3a249-107">Description</span><span class="sxs-lookup"><span data-stu-id="3a249-107">Description</span></span>|  
|------------|-----------------|  
|`eInitializeNewDomainFlags_None`|<span data-ttu-id="3a249-108">Aucun indicateur.</span><span class="sxs-lookup"><span data-stu-id="3a249-108">No flags.</span></span>|  
|`eInitializeNewDomainFlags_NoSecurityChanges`|<span data-ttu-id="3a249-109">Informe le common language runtime (CLR) que l’hôte n’apportera pas de modifications à l’état de sécurité du domaine d’application dans le <xref:System.AppDomainManager.InitializeNewDomain%2A> (méthode).</span><span class="sxs-lookup"><span data-stu-id="3a249-109">Informs the common language runtime (CLR) that the host will not make changes to the security state of the application domain in the <xref:System.AppDomainManager.InitializeNewDomain%2A> method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3a249-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3a249-110">Remarks</span></span>  
 <span data-ttu-id="3a249-111">Le [ICLRDomainManager::SetAppDomainManagerType](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setappdomainmanagertype-method.md) méthode prend un paramètre de type `EInitializeNewDomainFlags`.</span><span class="sxs-lookup"><span data-stu-id="3a249-111">The [ICLRDomainManager::SetAppDomainManagerType](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setappdomainmanagertype-method.md) method takes a parameter of type `EInitializeNewDomainFlags`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a249-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a249-112">Requirements</span></span>  
 <span data-ttu-id="3a249-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3a249-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a249-114">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3a249-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3a249-115">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3a249-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3a249-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a249-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a249-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a249-117">See also</span></span>

- [<span data-ttu-id="3a249-118">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="3a249-118">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
- [<span data-ttu-id="3a249-119">SetAppDomainManagerType, méthode</span><span class="sxs-lookup"><span data-stu-id="3a249-119">SetAppDomainManagerType Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdomainmanager-setappdomainmanagertype-method.md)
