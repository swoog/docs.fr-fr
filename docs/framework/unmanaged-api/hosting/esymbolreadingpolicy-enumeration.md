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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59208421"
---
# <a name="esymbolreadingpolicy-enumeration"></a><span data-ttu-id="2dbc8-102">ESymbolReadingPolicy, énumération</span><span class="sxs-lookup"><span data-stu-id="2dbc8-102">ESymbolReadingPolicy Enumeration</span></span>
<span data-ttu-id="2dbc8-103">Contient des valeurs qui définissent la stratégie pour la lecture des fichiers de programme (PDB) de la base de données.</span><span class="sxs-lookup"><span data-stu-id="2dbc8-103">Contains values that set the policy for reading program database (PDB) files.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2dbc8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2dbc8-104">Syntax</span></span>  
  
```  
typedef enum {  
    eSymbolReadingNever,  
    eSymbolReadingAlways,  
    eSymbolReadingFullTrustOnly  
} ESymbolReadingPolicy;  
```  
  
## <a name="members"></a><span data-ttu-id="2dbc8-105">Membres</span><span class="sxs-lookup"><span data-stu-id="2dbc8-105">Members</span></span>  
  
|<span data-ttu-id="2dbc8-106">Membre</span><span class="sxs-lookup"><span data-stu-id="2dbc8-106">Member</span></span>|<span data-ttu-id="2dbc8-107">Description</span><span class="sxs-lookup"><span data-stu-id="2dbc8-107">Description</span></span>|  
|------------|-----------------|  
|`eSymbolReadingAlways`|<span data-ttu-id="2dbc8-108">Spécifie que le débogueur doit toujours lire des fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="2dbc8-108">Specifies that the debugger should always read PDB files.</span></span>|  
|`eSymbolReadingFullTrustOnly`|<span data-ttu-id="2dbc8-109">Spécifie que le débogueur doit lire uniquement les fichiers PDB qui sont associés à des assemblys de confiance totale.</span><span class="sxs-lookup"><span data-stu-id="2dbc8-109">Specifies that the debugger should read only PDB files that are associated with full-trust assemblies.</span></span>|  
|`eSymbolReadingNever`|<span data-ttu-id="2dbc8-110">Spécifie que le débogueur doit lire jamais les fichiers PDB.</span><span class="sxs-lookup"><span data-stu-id="2dbc8-110">Specifies that the debugger should never read PDB files.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2dbc8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2dbc8-111">Remarks</span></span>  
 <span data-ttu-id="2dbc8-112">Le `ESymbolReadingPolicy` énumération est utilisée avec la [ICLRDebugManager::SetSymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="2dbc8-112">The `ESymbolReadingPolicy` enumeration is used with the [ICLRDebugManager::SetSymbolReadingPolicy](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setsymbolreadingpolicy-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2dbc8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dbc8-113">Requirements</span></span>  
 <span data-ttu-id="2dbc8-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2dbc8-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2dbc8-115">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="2dbc8-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="2dbc8-116">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2dbc8-116">**Library:** MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="2dbc8-117">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="2dbc8-117">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="2dbc8-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dbc8-118">See also</span></span>

- [<span data-ttu-id="2dbc8-119">Énumérations d'hébergement</span><span class="sxs-lookup"><span data-stu-id="2dbc8-119">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
