---
title: INotifySource2::SetNotifyFilter, méthode
ms.date: 03/30/2017
api_name:
- INotifySource2.SetNotifyFilter
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySource2::SetNotifyFilter
helpviewer_keywords:
- INotifySource2::SetNotifyFilter method [.NET Framework debugging]
- SetNotifyFilter method [.NET Framework debugging]
ms.assetid: 6351fc92-b126-4af6-9bf3-0a8ce92845fc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 37e4abeebce155a4c332e864b4dfb6cf5a1141ec
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59151747"
---
# <a name="inotifysource2setnotifyfilter-method"></a><span data-ttu-id="cae27-102">INotifySource2::SetNotifyFilter, méthode</span><span class="sxs-lookup"><span data-stu-id="cae27-102">INotifySource2::SetNotifyFilter Method</span></span>
<span data-ttu-id="cae27-103">Assigne un filtre de notification pour une utilisation avec cette source.</span><span class="sxs-lookup"><span data-stu-id="cae27-103">Assigns a notification filter for use with this source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cae27-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cae27-104">Syntax</span></span>  
  
```  
HRESULT SetNotifyFilter  
(  
    [in]  NOTIFY_FILTER   in_NotifyFilter,  
    [in]  USER_THREAD*    in_pUserThreadFilter  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cae27-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cae27-105">Parameters</span></span>  
 `in_NotifyFilter`  
 <span data-ttu-id="cae27-106">[in] Une combinaison au niveau du bit de la [NOTIFY_FILTER](../../../../docs/framework/unmanaged-api/diagnostics/notify-filter-enumeration.md) valeurs d’énumération qui identifient des rappels pour l’API de débogage.</span><span class="sxs-lookup"><span data-stu-id="cae27-106">[in] A bitwise combination of the [NOTIFY_FILTER](../../../../docs/framework/unmanaged-api/diagnostics/notify-filter-enumeration.md) enumeration values that identify callbacks for the debugger API.</span></span>  
  
 `in_pUserThreadFilter`  
 <span data-ttu-id="cae27-107">[in] Un pointeur vers un [USER_THREAD](../../../../docs/framework/unmanaged-api/diagnostics/user-thread-structure.md) structure qui identifie des threads pour l’API de débogage.</span><span class="sxs-lookup"><span data-stu-id="cae27-107">[in] A pointer to a [USER_THREAD](../../../../docs/framework/unmanaged-api/diagnostics/user-thread-structure.md) structure that identifies threads for the debugger API.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cae27-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cae27-108">Return Value</span></span>  
 <span data-ttu-id="cae27-109">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="cae27-109">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cae27-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cae27-110">Requirements</span></span>  
 <span data-ttu-id="cae27-111">**En-tête :** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="cae27-111">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cae27-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cae27-112">See also</span></span>

- [<span data-ttu-id="cae27-113">INotifySource2, interface</span><span class="sxs-lookup"><span data-stu-id="cae27-113">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)
- [<span data-ttu-id="cae27-114">INotifyConnection2, interface</span><span class="sxs-lookup"><span data-stu-id="cae27-114">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
- [<span data-ttu-id="cae27-115">INotifySink2, interface</span><span class="sxs-lookup"><span data-stu-id="cae27-115">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)
