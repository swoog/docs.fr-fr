---
title: EClrUnhandledException, énumération
ms.date: 03/30/2017
api_name:
- EClrUnhandledException
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EClrUnhandledException
helpviewer_keywords:
- EClrUnhandledException enumeration [.NET Framework hosting]
ms.assetid: d231044e-2b53-4836-93f9-8117ff0e5c3a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 65910745aa6291f93fd42d8f99a0e84dc1e38fdd
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54686684"
---
# <a name="eclrunhandledexception-enumeration"></a><span data-ttu-id="0ff1f-102">EClrUnhandledException, énumération</span><span class="sxs-lookup"><span data-stu-id="0ff1f-102">EClrUnhandledException Enumeration</span></span>
<span data-ttu-id="0ff1f-103">Décrit les options disponibles pour la gestion des exceptions qui ne sont pas gérées dans le code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-103">Describes the available options for managing exceptions that are unhandled in user code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ff1f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ff1f-104">Syntax</span></span>  
  
```  
typedef enum {  
    eRuntimeDeterminedPolicy,  
    eHostDeterminedPolicy  
} EClrUnhandledException;  
```  
  
## <a name="members"></a><span data-ttu-id="0ff1f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0ff1f-105">Members</span></span>  
  
|<span data-ttu-id="0ff1f-106">Membre</span><span class="sxs-lookup"><span data-stu-id="0ff1f-106">Member</span></span>|<span data-ttu-id="0ff1f-107">Description</span><span class="sxs-lookup"><span data-stu-id="0ff1f-107">Description</span></span>|  
|------------|-----------------|  
|`eRuntimeDeterminedPolicy`|<span data-ttu-id="0ff1f-108">Spécifie que le comportement par défaut se produit.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-108">Specifies that the default behavior occurs.</span></span> <span data-ttu-id="0ff1f-109">Le processus est détruit.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-109">The process is torn down.</span></span>|  
|`eHostDeterminedPolicy`|<span data-ttu-id="0ff1f-110">Spécifie que le common language runtime (CLR) ignore les exceptions non gérées et permet à l’hôte de déterminer toute action supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-110">Specifies that the common language runtime (CLR) ignores unhandled exceptions and lets the host determine any further action.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0ff1f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0ff1f-111">Remarks</span></span>  
 <span data-ttu-id="0ff1f-112">Pour spécifier que le CLR se comportent comme les versions antérieures, utilisez le `eHostDeterminedPolicy` membre.</span><span class="sxs-lookup"><span data-stu-id="0ff1f-112">To specify that the CLR behave like earlier versions, use the `eHostDeterminedPolicy` member.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0ff1f-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0ff1f-113">Requirements</span></span>  
 <span data-ttu-id="0ff1f-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0ff1f-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ff1f-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="0ff1f-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0ff1f-116">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0ff1f-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0ff1f-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0ff1f-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ff1f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ff1f-118">See also</span></span>
- [<span data-ttu-id="0ff1f-119">EClrFailure, énumération</span><span class="sxs-lookup"><span data-stu-id="0ff1f-119">EClrFailure Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [<span data-ttu-id="0ff1f-120">EClrOperation, énumération</span><span class="sxs-lookup"><span data-stu-id="0ff1f-120">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)
- [<span data-ttu-id="0ff1f-121">ICLRPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="0ff1f-121">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
- [<span data-ttu-id="0ff1f-122">SetUnhandledExceptionPolicy, méthode</span><span class="sxs-lookup"><span data-stu-id="0ff1f-122">SetUnhandledExceptionPolicy Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setunhandledexceptionpolicy-method.md)
- [<span data-ttu-id="0ff1f-123">IHostPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="0ff1f-123">IHostPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)
- [<span data-ttu-id="0ff1f-124">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="0ff1f-124">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
