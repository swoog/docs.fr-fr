---
title: INotifyConnection2::UnregisterNotifySource, méthode
ms.date: 03/30/2017
api_name:
- INotifyConnection2.UnregisterNotifySource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifyConnection2::UnregisterNotifySource
helpviewer_keywords:
- INotifyConnection2::UnregisterNotifySource method [.NET Framework debugging]
- UnregisterNotifySource method [.NET Framework debugging]
ms.assetid: 2fc6c715-646f-41fd-9c12-c59b40575269
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 742be1467d2f1e6eb7d8567ddf85f8e65ea4b8d9
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61794327"
---
# <a name="inotifyconnection2unregisternotifysource-method"></a><span data-ttu-id="896cb-102">INotifyConnection2::UnregisterNotifySource, méthode</span><span class="sxs-lookup"><span data-stu-id="896cb-102">INotifyConnection2::UnregisterNotifySource Method</span></span>
<span data-ttu-id="896cb-103">Supprime un objet de source de notification spécifié à partir de la connexion.</span><span class="sxs-lookup"><span data-stu-id="896cb-103">Removes a specified notification source object from the connection.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="896cb-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="896cb-104">Syntax</span></span>  
  
```  
HRESULT UnregisterNotifySource  
(  
    [in]  INotifySource2*  in_pNotifySource  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="896cb-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="896cb-105">Parameters</span></span>  
 `in_pNotifySource`  
 <span data-ttu-id="896cb-106">[in] Objet de notification doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="896cb-106">[in] Notification object to be unregistered.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="896cb-107">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="896cb-107">Return Value</span></span>  
 <span data-ttu-id="896cb-108">S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="896cb-108">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="896cb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="896cb-109">Requirements</span></span>  
 <span data-ttu-id="896cb-110">**En-tête :** ProtocolNotify2.idl</span><span class="sxs-lookup"><span data-stu-id="896cb-110">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="896cb-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="896cb-111">See also</span></span>

- [<span data-ttu-id="896cb-112">INotifyConnection2, interface</span><span class="sxs-lookup"><span data-stu-id="896cb-112">INotifyConnection2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-interface.md)
- [<span data-ttu-id="896cb-113">INotifySource2, interface</span><span class="sxs-lookup"><span data-stu-id="896cb-113">INotifySource2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysource2-interface.md)
- [<span data-ttu-id="896cb-114">INotifySink2, interface</span><span class="sxs-lookup"><span data-stu-id="896cb-114">INotifySink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifysink2-interface.md)
- [<span data-ttu-id="896cb-115">RegisterNotifySource, méthode</span><span class="sxs-lookup"><span data-stu-id="896cb-115">RegisterNotifySource Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/inotifyconnection2-registernotifysource-method.md)
