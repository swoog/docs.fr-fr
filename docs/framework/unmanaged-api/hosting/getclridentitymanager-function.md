---
title: GetCLRIdentityManager, fonction
ms.date: 03/30/2017
api_name:
- GetCLRIdentityManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- GetCLRIdentityManager
helpviewer_keywords:
- GetCLRIdentityManager function [.NET Framework hosting]
ms.assetid: 66eeca30-adb4-45f4-aff5-347564c95724
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 84f71266d84cc98c2a5deb4aa8639e36808315a3
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59130180"
---
# <a name="getclridentitymanager-function"></a><span data-ttu-id="04ff5-102">GetCLRIdentityManager, fonction</span><span class="sxs-lookup"><span data-stu-id="04ff5-102">GetCLRIdentityManager Function</span></span>
<span data-ttu-id="04ff5-103">Obtient un pointeur vers une interface qui autorise le common language runtime (CLR) pour gérer les identités.</span><span class="sxs-lookup"><span data-stu-id="04ff5-103">Gets a pointer to an interface that allows the common language runtime (CLR) to manage identities.</span></span>  
  
 <span data-ttu-id="04ff5-104">Cette fonction a été déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="04ff5-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04ff5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04ff5-105">Syntax</span></span>  
  
```  
STDAPI GetCLRIdentityManager(  
    [in]  REFIID      riid,  
    [out] IUnknown  **ppManager  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="04ff5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04ff5-106">Parameters</span></span>  
 `riid`  
 <span data-ttu-id="04ff5-107">[in] Un `REFIID` (un identificateur d’interface) qui spécifie quelle interface à obtenir.</span><span class="sxs-lookup"><span data-stu-id="04ff5-107">[in] A `REFIID` (an interface identifier) that specifies which interface to get.</span></span> <span data-ttu-id="04ff5-108">Cette valeur doit être IID_ICLRAssemblyIdentityManager ou IID_ICLRHostBindingPolicyManager.</span><span class="sxs-lookup"><span data-stu-id="04ff5-108">This value must be either IID_ICLRAssemblyIdentityManager or IID_ICLRHostBindingPolicyManager.</span></span>  
  
 `ppManager`  
 <span data-ttu-id="04ff5-109">[out] Un pointeur vers l’adresse un [ICLRAssemblyIdentityManager](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md) ou un [ICLRHostBindingPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="04ff5-109">[out] A pointer to the address of either an [ICLRAssemblyIdentityManager](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md) or an [ICLRHostBindingPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md) object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="04ff5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="04ff5-110">Remarks</span></span>  
 <span data-ttu-id="04ff5-111">Appelez le [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) fonction pour obtenir un pointeur vers le `GetCLRIdentityManager` (fonction).</span><span class="sxs-lookup"><span data-stu-id="04ff5-111">Call the [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) function to get a pointer to the `GetCLRIdentityManager` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04ff5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04ff5-112">Requirements</span></span>  
 <span data-ttu-id="04ff5-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="04ff5-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04ff5-114">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="04ff5-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="04ff5-115">**Bibliothèque :** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="04ff5-115">**Library:** MSCorWks.dll</span></span>  
  
 **<span data-ttu-id="04ff5-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="04ff5-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="04ff5-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04ff5-117">See also</span></span>

- [<span data-ttu-id="04ff5-118">Fonction d'hébergement du CLR déconseillées</span><span class="sxs-lookup"><span data-stu-id="04ff5-118">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
