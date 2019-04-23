---
title: ICLRTaskManager::GetCurrentTaskType, méthode
ms.date: 03/30/2017
api_name:
- ICLRTaskManager.GetCurrentTaskType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRTaskManager::GetCurrentTaskType
helpviewer_keywords:
- GetCurrentTaskType method [.NET Framework hosting]
- ICLRTaskManager::GetCurrentTaskType method [.NET Framework hosting]
ms.assetid: 6b0d9259-dbe2-45bb-b34d-990f60c73424
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2963e2a31fd62470e3ed6933edb38119d286071b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59071972"
---
# <a name="iclrtaskmanagergetcurrenttasktype-method"></a><span data-ttu-id="75474-102">ICLRTaskManager::GetCurrentTaskType, méthode</span><span class="sxs-lookup"><span data-stu-id="75474-102">ICLRTaskManager::GetCurrentTaskType Method</span></span>
<span data-ttu-id="75474-103">Obtient le type de la tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="75474-103">Gets the type of the task that is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75474-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75474-104">Syntax</span></span>  
  
```  
HRESULT GetCurrentTaskType(  
    [out] ETaskType *pTaskType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="75474-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75474-105">Parameters</span></span>  
 `pTaskType`  
 <span data-ttu-id="75474-106">[out] Un pointeur vers une valeur de la [ETaskType](../../../../docs/framework/unmanaged-api/hosting/etasktype-enumeration.md) énumération qui indique le type de tâche en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="75474-106">[out] A pointer to a value of the [ETaskType](../../../../docs/framework/unmanaged-api/hosting/etasktype-enumeration.md) enumeration that indicates the type of task that is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="75474-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75474-107">Requirements</span></span>  
 <span data-ttu-id="75474-108">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="75474-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="75474-109">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="75474-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="75474-110">**Bibliothèque :** Inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="75474-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="75474-111">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="75474-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75474-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75474-112">See also</span></span>

- [<span data-ttu-id="75474-113">ICLRTaskManager, interface</span><span class="sxs-lookup"><span data-stu-id="75474-113">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)
