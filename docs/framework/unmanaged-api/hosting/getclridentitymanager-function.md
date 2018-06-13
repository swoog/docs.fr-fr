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
ms.openlocfilehash: 6a0672196ebaea5c91139851b89a7476ff6363b0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430793"
---
# <a name="getclridentitymanager-function"></a><span data-ttu-id="e9e92-102">GetCLRIdentityManager, fonction</span><span class="sxs-lookup"><span data-stu-id="e9e92-102">GetCLRIdentityManager Function</span></span>
<span data-ttu-id="e9e92-103">Obtient un pointeur vers une interface qui permet le common language runtime (CLR) pour gérer les identités.</span><span class="sxs-lookup"><span data-stu-id="e9e92-103">Gets a pointer to an interface that allows the common language runtime (CLR) to manage identities.</span></span>  
  
 <span data-ttu-id="e9e92-104">Cette fonction est déconseillée dans le [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="e9e92-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9e92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9e92-105">Syntax</span></span>  
  
```  
STDAPI GetCLRIdentityManager(  
    [in]  REFIID      riid,  
    [out] IUnknown  **ppManager  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e9e92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9e92-106">Parameters</span></span>  
 `riid`  
 <span data-ttu-id="e9e92-107">[in] A `REFIID` (un identificateur d’interface) qui spécifie l’interface à obtenir.</span><span class="sxs-lookup"><span data-stu-id="e9e92-107">[in] A `REFIID` (an interface identifier) that specifies which interface to get.</span></span> <span data-ttu-id="e9e92-108">Cette valeur doit être IID_ICLRAssemblyIdentityManager ou IID_ICLRHostBindingPolicyManager.</span><span class="sxs-lookup"><span data-stu-id="e9e92-108">This value must be either IID_ICLRAssemblyIdentityManager or IID_ICLRHostBindingPolicyManager.</span></span>  
  
 `ppManager`  
 <span data-ttu-id="e9e92-109">[out] Un pointeur vers l’adresse un [ICLRAssemblyIdentityManager](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md) ou [ICLRHostBindingPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="e9e92-109">[out] A pointer to the address of either an [ICLRAssemblyIdentityManager](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md) or an [ICLRHostBindingPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrhostbindingpolicymanager-interface.md) object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e9e92-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e9e92-110">Remarks</span></span>  
 <span data-ttu-id="e9e92-111">Appelez le [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) fonction permettant d’obtenir un pointeur vers le `GetCLRIdentityManager` (fonction).</span><span class="sxs-lookup"><span data-stu-id="e9e92-111">Call the [GetRealProcAddress](../../../../docs/framework/unmanaged-api/hosting/getrealprocaddress-function.md) function to get a pointer to the `GetCLRIdentityManager` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e9e92-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e9e92-112">Requirements</span></span>  
 <span data-ttu-id="e9e92-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e9e92-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e9e92-114">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="e9e92-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e9e92-115">**Bibliothèque :** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="e9e92-115">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="e9e92-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e9e92-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9e92-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9e92-117">See Also</span></span>  
 [<span data-ttu-id="e9e92-118">Fonctions d’hébergement CLR dépréciées</span><span class="sxs-lookup"><span data-stu-id="e9e92-118">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
