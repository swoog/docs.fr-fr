---
title: CorExitProcess, fonction
ms.date: 03/30/2017
api_name:
- CorExitProcess
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- CorExitProcess
helpviewer_keywords:
- CorExitProcess function [.NET Framework hosting]
ms.assetid: a5cab4c6-990e-47f3-8798-cf422b791015
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3e7f3208d7ac84645fa4c7ad7e0b71f6a0d3d3d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429327"
---
# <a name="corexitprocess-function"></a><span data-ttu-id="9814b-102">CorExitProcess, fonction</span><span class="sxs-lookup"><span data-stu-id="9814b-102">CorExitProcess Function</span></span>
<span data-ttu-id="9814b-103">Arrête le processus non managé en cours.</span><span class="sxs-lookup"><span data-stu-id="9814b-103">Shuts down the current unmanaged process.</span></span>  
  
 <span data-ttu-id="9814b-104">Cette fonction est déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="9814b-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span> <span data-ttu-id="9814b-105">Utilisez le [ICLRMetaHost::ExitProcess](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-exitprocess-method.md) méthode à la place.</span><span class="sxs-lookup"><span data-stu-id="9814b-105">Use the [ICLRMetaHost::ExitProcess](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-exitprocess-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9814b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9814b-106">Syntax</span></span>  
  
```  
void STDMETHODCALLTYPE CorExitProcess (   
  int  exitCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9814b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9814b-107">Parameters</span></span>  
 `exitCode`  
 <span data-ttu-id="9814b-108">Entier qui spécifie le code de sortie.</span><span class="sxs-lookup"><span data-stu-id="9814b-108">An integer that specifies the process exit code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9814b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9814b-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9814b-110">Compter les [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], `CorExitProcess` quitte chaque exécution commencée dans le processus, et pas seulement le runtime auquel les API héritées ont été liés.</span><span class="sxs-lookup"><span data-stu-id="9814b-110">Beginning with the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], `CorExitProcess` exits every started runtime in the process, not just the runtime to which the legacy APIs have been bound.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9814b-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9814b-111">Requirements</span></span>  
 <span data-ttu-id="9814b-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9814b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9814b-113">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9814b-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9814b-114">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9814b-114">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9814b-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9814b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9814b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9814b-116">See Also</span></span>  
 [<span data-ttu-id="9814b-117">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="9814b-117">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
