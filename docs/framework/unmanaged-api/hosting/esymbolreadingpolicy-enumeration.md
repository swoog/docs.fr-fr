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
ms.openlocfilehash: 28f6bdbc3e382f82b7fdd632b9fc8c4d422629c8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429731"
---
# <a name="esymbolreadingpolicy-enumeration"></a><span data-ttu-id="f03a6-102">ESymbolReadingPolicy, énumération</span><span class="sxs-lookup"><span data-stu-id="f03a6-102">ESymbolReadingPolicy Enumeration</span></span>
<span data-ttu-id="f03a6-103">Contient des valeurs qui définissent la stratégie pour la lecture des fichiers de programme (PDB) de la base de données.</span><span class="sxs-lookup"><span data-stu-id="f03a6-103">Contains values that set the policy for reading program database (PDB) files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f03a6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f03a6-104">Syntax</span></span>  
  
```  
typedef enum {  
    eSymbolReadingNever,  
    eSymbolReadingAlways,  
    eSymbolReadingFullTrustOnly  
} ESymbolReadingPolicy;  
```  
  
## <a name="members"></a><span data-ttu-id="f03a6-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f03a6-105">Members</span></span>  
  
|<span data-ttu-id="f03a6-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f03a6-106">Member</span></span>|<span data-ttu-id="f03a6-107">Description</span><span class="sxs-lookup"><span data-stu-id="f03a6-107">Description</span></span>|  
|------------|-----------------|  
|`eSymbolReadingAlways`|<span data-ttu-id="f03a6-108">Spécifie que le débogueur doit toujours lire des fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="f03a6-108">Specifies that the debugger should always read PDB files.</span></span>|  
|`eSymbolReadingFullTrustOnly`|<span data-ttu-id="f03a6-109">Spécifie que le débogueur doit lire uniquement les fichiers PDB qui sont associés à des assemblys de confiance totale.</span><span class="sxs-lookup"><span data-stu-id="f03a6-109">Specifies that the debugger should read only PDB files that are associated with full-trust assemblies.</span></span>|  
|`eSymbolReadingNever`|<span data-ttu-id="f03a6-110">Spécifie que le débogueur ne doit jamais lire les fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="f03a6-110">Specifies that the debugger should never read PDB files.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f03a6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f03a6-111">Remarks</span></span>  
 <span data-ttu-id="f03a6-112">Le `ESymbolReadingPolicy` énumération est utilisée avec la [ICLRDebugManager::SetSymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f03a6-112">The `ESymbolReadingPolicy` enumeration is used with the [ICLRDebugManager::SetSymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f03a6-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f03a6-113">Requirements</span></span>  
 <span data-ttu-id="f03a6-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f03a6-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f03a6-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="f03a6-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f03a6-116">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f03a6-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f03a6-117">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f03a6-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f03a6-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f03a6-118">See Also</span></span>  
 [<span data-ttu-id="f03a6-119">Énumérations d’hébergement</span><span class="sxs-lookup"><span data-stu-id="f03a6-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
