---
title: NOTIFY_FILTER, énumération
ms.date: 03/30/2017
api_name:
- NOTIFY_FILTER
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- NOTIFY_FILTER
helpviewer_keywords:
- NOTIFY_FILTER enumeration [.NET Framework debugging]
ms.assetid: 4789d08f-8683-45d3-ac30-73d48c61e470
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 98c3e1ed3da209cbded5d76d938d2420fce606be
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431014"
---
# <a name="notifyfilter-enumeration"></a><span data-ttu-id="55e56-102">NOTIFY_FILTER, énumération</span><span class="sxs-lookup"><span data-stu-id="55e56-102">NOTIFY_FILTER Enumeration</span></span>
<span data-ttu-id="55e56-103">Identifie des rappels pour les fonctions de débogueur.</span><span class="sxs-lookup"><span data-stu-id="55e56-103">Identifies callbacks for debugger functions.</span></span> <span data-ttu-id="55e56-104">Pour plus d’informations, consultez la [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="55e56-104">For more information, see the [INotifySource2::SetNotifyFilter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-setnotifyfilter-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="55e56-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55e56-105">Syntax</span></span>  
  
```  
enum tagNOTIFY_FILTER  
{  
    NOTIFY_FILTER_ONSYNCCALLOUT    = 0x1,  
    NOTIFY_FILTER_ONSYNCCALLENTER  = 0x2,  
    NOTIFY_FILTER_ONSYNCCALLEXIT   = 0x4,  
    NOTIFY_FILTER_ONSYNCCALLRETURN = 0x8,  
    NOTIFY_FILTER_ALLSYNC = NOTIFY_FILTER_ONSYNCCALLOUT | NOTIFY_FILTER_ONSYNCCALLENTER | NOTIFY_FILTER_ONSYNCCALLEXIT | NOTIFY_FILTER_ONSYNCCALLRETURN,  
    NOTIFY_FILTER_ALL              = 0xffffffff,  
    NOTIFY_FILTER_NONE             = 0  
};  
```  
  
## <a name="members"></a><span data-ttu-id="55e56-106">Membres</span><span class="sxs-lookup"><span data-stu-id="55e56-106">Members</span></span>  
  
|<span data-ttu-id="55e56-107">Membre</span><span class="sxs-lookup"><span data-stu-id="55e56-107">Member</span></span>|<span data-ttu-id="55e56-108">Description</span><span class="sxs-lookup"><span data-stu-id="55e56-108">Description</span></span>|  
|------------|-----------------|  
|`NOTIFY_FILTER_ONSYNCCALLOUT`|<span data-ttu-id="55e56-109">Indique que le [INotifySink2::OnSyncCallOut](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallout-method.md) méthode doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="55e56-109">Indicates that the [INotifySink2::OnSyncCallOut](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallout-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLENTER`|<span data-ttu-id="55e56-110">Indique que le [INotifySink2::OnSyncCallEnter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallenter-method.md) méthode doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="55e56-110">Indicates that the [INotifySink2::OnSyncCallEnter](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallenter-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLEXIT`|<span data-ttu-id="55e56-111">Indique que le [INotifySink2::OnSyncCallExit](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallexit-method.md) méthode doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="55e56-111">Indicates that the [INotifySink2::OnSyncCallExit](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallexit-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ONSYNCCALLRETURN`|<span data-ttu-id="55e56-112">Indique que le [INotifySink2::OnSyncCallReturn](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallreturn-method.md) méthode doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="55e56-112">Indicates that the [INotifySink2::OnSyncCallReturn](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-onsynccallreturn-method.md) method should be invoked.</span></span>|  
|`NOTIFY_FILTER_ALLSYNC`|<span data-ttu-id="55e56-113">Indique que tous les [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md) méthode doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="55e56-113">Indicates that all of the [INotifySink2](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md) methods should be invoked.</span></span>|  
|`NOTIFY_FILTER_ALL`|<span data-ttu-id="55e56-114">Active toutes les notifications existantes et futures.</span><span class="sxs-lookup"><span data-stu-id="55e56-114">Activates all existing and future notifications.</span></span>|  
|`NOTIFY_FILTER_NONE`|<span data-ttu-id="55e56-115">Indique qu’aucune méthode de notification doit être appelée.</span><span class="sxs-lookup"><span data-stu-id="55e56-115">Indicates that no notification methods should be invoked.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="55e56-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="55e56-116">Requirements</span></span>  
 <span data-ttu-id="55e56-117">**En-tête :** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="55e56-117">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55e56-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55e56-118">See Also</span></span>  
 [<span data-ttu-id="55e56-119">Énumérations du magasin de symboles de diagnostics</span><span class="sxs-lookup"><span data-stu-id="55e56-119">Diagnostics Symbol Store Enumerations</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/diagnostics-symbol-store-enumerations.md)
