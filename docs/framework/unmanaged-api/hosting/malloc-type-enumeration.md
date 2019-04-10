---
title: MALLOC_TYPE (énumération)
ms.date: 03/30/2017
api_name:
- MALLOC_TYPE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- MALLOC_TYPE
helpviewer_keywords:
- MALLOC_TYPE Enumeration
ms.assetid: c02476f9-23a2-4af7-9282-aa9c42c7429b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 695f69c8d9c3a295a705971743733339cf8aab13
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59211944"
---
# <a name="malloctype-enumeration"></a><span data-ttu-id="87068-102">MALLOC_TYPE (énumération)</span><span class="sxs-lookup"><span data-stu-id="87068-102">MALLOC_TYPE Enumeration</span></span>
<span data-ttu-id="87068-103">Contient des valeurs qui spécifient les caractéristiques de la mémoire est allouée.</span><span class="sxs-lookup"><span data-stu-id="87068-103">Contains values that specify the characteristics of the memory that is being allocated.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="87068-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87068-104">Syntax</span></span>  
  
```  
typedef enum {  
    MALLOC_THREADSAFE = 0x1,  
    MALLOC_EXECUTABLE = 0x2,  
} MALLOC_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="87068-105">Membres</span><span class="sxs-lookup"><span data-stu-id="87068-105">Members</span></span>  
  
|<span data-ttu-id="87068-106">Membre</span><span class="sxs-lookup"><span data-stu-id="87068-106">Member</span></span>|<span data-ttu-id="87068-107">Description</span><span class="sxs-lookup"><span data-stu-id="87068-107">Description</span></span>|  
|------------|-----------------|  
|`MALLOC_EXECUTABLE`|<span data-ttu-id="87068-108">La mémoire allouée peut contenir un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="87068-108">The allocated memory can contain an executable file.</span></span>|  
|`MALLOC_THREADSAFE`|<span data-ttu-id="87068-109">La mémoire allouée est thread-safe.</span><span class="sxs-lookup"><span data-stu-id="87068-109">The allocated memory is thread-safe.</span></span> <span data-ttu-id="87068-110">Autrement dit, la mémoire est accessible par plusieurs threads sans synchronisation.</span><span class="sxs-lookup"><span data-stu-id="87068-110">That is, the memory can be accessed by multiple threads without any synchronization.</span></span><br /><br /> <span data-ttu-id="87068-111">Si cet indicateur n’est pas défini, les appels sur l’objet doivent être sérialisés.</span><span class="sxs-lookup"><span data-stu-id="87068-111">If this flag is not set, calls on the object must be serialized.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="87068-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87068-112">Requirements</span></span>  
 <span data-ttu-id="87068-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="87068-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="87068-114">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="87068-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="87068-115">**Bibliothèque :** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="87068-115">**Library:** MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="87068-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="87068-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="87068-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87068-117">See also</span></span>

- [<span data-ttu-id="87068-118">Énumérations d'hébergement</span><span class="sxs-lookup"><span data-stu-id="87068-118">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
