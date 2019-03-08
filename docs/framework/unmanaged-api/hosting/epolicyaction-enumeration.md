---
title: EPolicyAction, énumération
ms.date: 03/30/2017
api_name:
- EPolicyAction
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EPolicyAction
helpviewer_keywords:
- EPolicyAction enumeration [.NET Framework hosting]
ms.assetid: 72dd76ba-239e-45ac-9ded-318fb07d6c6d
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: aa8589b3f27ba97d32e77dbfecb190edc69dbc18
ms.sourcegitcommit: 58fc0e6564a37fa1b9b1b140a637e864c4cf696e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2019
ms.locfileid: "57677329"
---
# <a name="epolicyaction-enumeration"></a><span data-ttu-id="85dcb-102">EPolicyAction, énumération</span><span class="sxs-lookup"><span data-stu-id="85dcb-102">EPolicyAction Enumeration</span></span>
<span data-ttu-id="85dcb-103">Décrit les actions de stratégie que l’hôte peut définir pour les opérations décrites par [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) et les échecs décrits par [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="85dcb-103">Describes the policy actions the host can set for operations described by [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) and failures described by [EClrFailure](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="85dcb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85dcb-104">Syntax</span></span>  
  
```  
typedef enum {  
    eNoAction,  
    eThrowException,  
    eAbortThread,  
    eRudeAbortThread,  
    eUnloadAppDomain,  
    eRudeUnloadAppDomain,  
    eExitProcess,  
    eFastExitProcess,  
    eRudeExitProcess,  
    eDisableRuntime  
} EPolicyAction;  
```  
  
## <a name="members"></a><span data-ttu-id="85dcb-105">Membres</span><span class="sxs-lookup"><span data-stu-id="85dcb-105">Members</span></span>  
  
|<span data-ttu-id="85dcb-106">Membre</span><span class="sxs-lookup"><span data-stu-id="85dcb-106">Member</span></span>|<span data-ttu-id="85dcb-107">Description</span><span class="sxs-lookup"><span data-stu-id="85dcb-107">Description</span></span>|  
|------------|-----------------|  
|`eAbortThread`|<span data-ttu-id="85dcb-108">Spécifie que le common language runtime (CLR) doit abandonner le thread normalement.</span><span class="sxs-lookup"><span data-stu-id="85dcb-108">Specifies that the common language runtime (CLR) should abort the thread gracefully.</span></span> <span data-ttu-id="85dcb-109">Un abandon correct implique des tentatives d’exécution de tous les `finally` bloque les `catch` blocs liés aux abandons de thread et les finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="85dcb-109">A graceful abort includes attempts to run all `finally` blocks, any `catch` blocks related to thread aborts, and finalizers.</span></span>|  
|`eDisableRuntime`|<span data-ttu-id="85dcb-110">Spécifie que le CLR doit entrer dans un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="85dcb-110">Specifies that the CLR should enter a disabled state.</span></span> <span data-ttu-id="85dcb-111">Aucun autre code managé peut être exécuté dans le processus affecté et les threads sont bloqués de pénétrer dans le CLR.</span><span class="sxs-lookup"><span data-stu-id="85dcb-111">No further managed code can be executed in the affected process, and threads are blocked from entering the CLR.</span></span>|  
|`eExitProcess`|<span data-ttu-id="85dcb-112">Spécifie que le CLR doit tenter une sortie normale du processus, notamment l’exécution des finaliseurs et effectuer des opérations de journalisation et de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="85dcb-112">Specifies that the CLR should attempt a graceful exit of the process, including running finalizers and performing cleanup and logging operations.</span></span>|  
|`eFastExitProcess`|<span data-ttu-id="85dcb-113">Spécifie que le CLR doit quitter le processus immédiatement, sans exécuter les finaliseurs ou effectuer des opérations de nettoyage et la journalisation.</span><span class="sxs-lookup"><span data-stu-id="85dcb-113">Specifies that the CLR should exit the process immediately, without running finalizers or performing cleanup and logging operations.</span></span> <span data-ttu-id="85dcb-114">Toutefois, la notification est envoyée au débogueur.</span><span class="sxs-lookup"><span data-stu-id="85dcb-114">However, notification is sent to the debugger.</span></span>|  
|`eNoAction`|<span data-ttu-id="85dcb-115">Spécifie qu’aucune action à entreprendre.</span><span class="sxs-lookup"><span data-stu-id="85dcb-115">Specifies that no action should be taken.</span></span>|  
|`eRudeAbortThread`|<span data-ttu-id="85dcb-116">Spécifie que le CLR doit effectuer un abandon de thread brutal.</span><span class="sxs-lookup"><span data-stu-id="85dcb-116">Specifies that the CLR should perform a rude thread abort.</span></span> <span data-ttu-id="85dcb-117">Seuls les `catch` et `finally` blocs marqués avec <xref:System.EnterpriseServices.MustRunInClientContextAttribute> sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="85dcb-117">Only those `catch` and `finally` blocks marked with <xref:System.EnterpriseServices.MustRunInClientContextAttribute> are executed.</span></span>|  
|`eRudeExitProcess`|<span data-ttu-id="85dcb-118">Spécifie que le CLR doit quitter le processus sans exécuter des finaliseurs ou la journalisation des opérations.</span><span class="sxs-lookup"><span data-stu-id="85dcb-118">Specifies that the CLR should exit the process without running finalizers or logging operations.</span></span>|  
|`eRudeUnloadAppDomain`|<span data-ttu-id="85dcb-119">Spécifie que le CLR doit effectuer un déchargement brutal du <xref:System.AppDomain>.</span><span class="sxs-lookup"><span data-stu-id="85dcb-119">Specifies that the CLR should perform a rude unload of the <xref:System.AppDomain>.</span></span> <span data-ttu-id="85dcb-120">Seuls les finaliseurs marqués avec <xref:System.EnterpriseServices.MustRunInClientContextAttribute> sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="85dcb-120">Only finalizers marked with <xref:System.EnterpriseServices.MustRunInClientContextAttribute> are executed.</span></span> <span data-ttu-id="85dcb-121">De même, tous les threads avec cette <xref:System.AppDomain> dans leur pile reçoivent un `ThreadAbortException`, mais uniquement ceux `catch` et `finally` blocs marqués avec <xref:System.EnterpriseServices.MustRunInClientContextAttribute> sont exécutées.</span><span class="sxs-lookup"><span data-stu-id="85dcb-121">Similarly, all threads with this <xref:System.AppDomain> in their stack receive a `ThreadAbortException`, but only those `catch` and `finally` blocks marked with <xref:System.EnterpriseServices.MustRunInClientContextAttribute> are executed.</span></span>|  
|`eThrowException`|<span data-ttu-id="85dcb-122">Spécifie qu’une exception appropriée à la condition, par exemple une mémoire insuffisante, un dépassement de tampon, etc., doit être levée.</span><span class="sxs-lookup"><span data-stu-id="85dcb-122">Specifies that an exception appropriate to the condition, such as out-of-memory, buffer overflow, and so forth, should be thrown.</span></span>|  
|`eUnloadAppDomain`|<span data-ttu-id="85dcb-123">Spécifie que le <xref:System.AppDomain> doit être déchargée.</span><span class="sxs-lookup"><span data-stu-id="85dcb-123">Specifies that the <xref:System.AppDomain> should be unloaded.</span></span> <span data-ttu-id="85dcb-124">Le CLR tente d’exécuter des finaliseurs.</span><span class="sxs-lookup"><span data-stu-id="85dcb-124">The CLR attempts to run finalizers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="85dcb-125">Notes</span><span class="sxs-lookup"><span data-stu-id="85dcb-125">Remarks</span></span>  
 <span data-ttu-id="85dcb-126">L’hôte définit les actions de stratégie en appelant des méthodes de la [ICLRPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="85dcb-126">The host sets policy actions by calling methods of the [ICLRPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md) interface.</span></span> <span data-ttu-id="85dcb-127">Pour plus d’informations sur les abandons brutaux et sans perte de données, consultez le [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) énumération.</span><span class="sxs-lookup"><span data-stu-id="85dcb-127">For information about rude and graceful aborts, see the [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="85dcb-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="85dcb-128">Requirements</span></span>  
 <span data-ttu-id="85dcb-129">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="85dcb-129">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="85dcb-130">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="85dcb-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="85dcb-131">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="85dcb-131">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="85dcb-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="85dcb-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="85dcb-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85dcb-133">See also</span></span>
- [<span data-ttu-id="85dcb-134">EClrFailure, énumération</span><span class="sxs-lookup"><span data-stu-id="85dcb-134">EClrFailure Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrfailure-enumeration.md)
- [<span data-ttu-id="85dcb-135">ICLRPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="85dcb-135">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)
- [<span data-ttu-id="85dcb-136">IHostPolicyManager, interface</span><span class="sxs-lookup"><span data-stu-id="85dcb-136">IHostPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)
- [<span data-ttu-id="85dcb-137">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="85dcb-137">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
