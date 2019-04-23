---
title: ESymbolReadingPolicy, énumération
ms.date: 03/30/2017
api_name:
- ESymbolReadingPolicy
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ESymbolReadingPolicy
helpviewer_keywords:
- ESymbolReadingPolicy enumeration [.NET Framework hosting]
ms.assetid: 4dc6c80d-b694-480b-a378-d5b18420ce17
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9ba29952fe4a6edfc6e9e80ec02f82de65ef0064
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59208421"
---
# <a name="esymbolreadingpolicy-enumeration"></a><span data-ttu-id="22727-102">ESymbolReadingPolicy, énumération</span><span class="sxs-lookup"><span data-stu-id="22727-102">ESymbolReadingPolicy Enumeration</span></span>
<span data-ttu-id="22727-103">Contient des valeurs qui définissent la stratégie pour la lecture des fichiers de programme (PDB) de la base de données.</span><span class="sxs-lookup"><span data-stu-id="22727-103">Contains values that set the policy for reading program database (PDB) files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22727-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22727-104">Syntax</span></span>  
  
```  
typedef enum {  
    eSymbolReadingNever,  
    eSymbolReadingAlways,  
    eSymbolReadingFullTrustOnly  
} ESymbolReadingPolicy;  
```  
  
## <a name="members"></a><span data-ttu-id="22727-105">Membres</span><span class="sxs-lookup"><span data-stu-id="22727-105">Members</span></span>  
  
|<span data-ttu-id="22727-106">Membre</span><span class="sxs-lookup"><span data-stu-id="22727-106">Member</span></span>|<span data-ttu-id="22727-107">Description</span><span class="sxs-lookup"><span data-stu-id="22727-107">Description</span></span>|  
|------------|-----------------|  
|`eSymbolReadingAlways`|<span data-ttu-id="22727-108">Spécifie que le débogueur doit toujours lire des fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="22727-108">Specifies that the debugger should always read PDB files.</span></span>|  
|`eSymbolReadingFullTrustOnly`|<span data-ttu-id="22727-109">Spécifie que le débogueur doit lire uniquement les fichiers PDB qui sont associés à des assemblys de confiance totale.</span><span class="sxs-lookup"><span data-stu-id="22727-109">Specifies that the debugger should read only PDB files that are associated with full-trust assemblies.</span></span>|  
|`eSymbolReadingNever`|<span data-ttu-id="22727-110">Spécifie que le débogueur doit lire jamais les fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="22727-110">Specifies that the debugger should never read PDB files.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="22727-111">Notes</span><span class="sxs-lookup"><span data-stu-id="22727-111">Remarks</span></span>  
 <span data-ttu-id="22727-112">Le `ESymbolReadingPolicy` énumération est utilisée avec la [ICLRDebugManager::SetSymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="22727-112">The `ESymbolReadingPolicy` enumeration is used with the [ICLRDebugManager::SetSymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22727-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22727-113">Requirements</span></span>  
 <span data-ttu-id="22727-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="22727-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22727-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="22727-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="22727-116">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="22727-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="22727-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22727-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22727-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22727-118">See also</span></span>

- [<span data-ttu-id="22727-119">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="22727-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
