---
title: ICLRMetaHost::ExitProcess, méthode
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.ExitProcess
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::ExitProcess
helpviewer_keywords:
- ICLRMetaHost::ExitProcess method [.NET Framework hosting]
- ExitProcess method, ICLRMetaHost interface [.NET Framework hosting]
ms.assetid: b4df98cc-4e4e-407b-b8f4-e0076afef3a4
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fc71762fb4a660cf84814cdd46d09696a161f3c9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431595"
---
# <a name="iclrmetahostexitprocess-method"></a><span data-ttu-id="d3558-102">ICLRMetaHost::ExitProcess, méthode</span><span class="sxs-lookup"><span data-stu-id="d3558-102">ICLRMetaHost::ExitProcess Method</span></span>
<span data-ttu-id="d3558-103">Tente de charger tous les runtimes s’arrête, puis se termine le processus.</span><span class="sxs-lookup"><span data-stu-id="d3558-103">Attempts to shut down all loaded runtimes gracefully and then terminates the process.</span></span> <span data-ttu-id="d3558-104">Remplace le [CorExitProcess](../../../../docs/framework/unmanaged-api/hosting/corexitprocess-function.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="d3558-104">Supersedes the [CorExitProcess](../../../../docs/framework/unmanaged-api/hosting/corexitprocess-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3558-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3558-105">Syntax</span></span>  
  
```  
HRESULT ExitProcess (  
    [in] INT32 iExitCode);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d3558-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3558-106">Parameters</span></span>  
 `iExitCode`  
 <span data-ttu-id="d3558-107">[in] Le code de sortie pour le processus.</span><span class="sxs-lookup"><span data-stu-id="d3558-107">[in] The exit code for the process.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d3558-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d3558-108">Return Value</span></span>  
 <span data-ttu-id="d3558-109">Cette méthode ne retourne jamais, donc sa valeur de retour n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="d3558-109">This method never returns, so its return value is undefined.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d3558-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d3558-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3558-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d3558-111">Requirements</span></span>  
 <span data-ttu-id="d3558-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d3558-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3558-113">**En-tête :** MetaHost.h</span><span class="sxs-lookup"><span data-stu-id="d3558-113">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="d3558-114">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d3558-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d3558-115">**Versions du .NET framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3558-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3558-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3558-116">See Also</span></span>  
 [<span data-ttu-id="d3558-117">ICLRMetaHost, interface</span><span class="sxs-lookup"><span data-stu-id="d3558-117">ICLRMetaHost Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md)  
 [<span data-ttu-id="d3558-118">Hébergement</span><span class="sxs-lookup"><span data-stu-id="d3558-118">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
