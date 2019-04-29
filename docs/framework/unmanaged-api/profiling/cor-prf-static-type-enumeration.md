---
title: COR_PRF_STATIC_TYPE, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_STATIC_TYPE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_STATIC_TYPE
helpviewer_keywords:
- COR_PRF_STATIC_TYPE enumeration [.NET Framework profiling]
ms.assetid: 441d7809-5b65-41a5-ba64-2910a8008315
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 310915ce84819a2a5a2d5e1f22356b61c16e7ec7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61599011"
---
# <a name="corprfstatictype-enumeration"></a><span data-ttu-id="b7952-102">COR_PRF_STATIC_TYPE, énumération</span><span class="sxs-lookup"><span data-stu-id="b7952-102">COR_PRF_STATIC_TYPE Enumeration</span></span>
<span data-ttu-id="b7952-103">Indique si un champ est statique et si oui, la qualité statique qui s'y applique.</span><span class="sxs-lookup"><span data-stu-id="b7952-103">Indicates whether a field is static and, if so, the static quality that applies to the field.</span></span> <span data-ttu-id="b7952-104">Ces valeurs peuvent être combinées à l’aide de l’opération OR au niveau du bit pour indiquer que le champ a plusieurs qualités statiques différentes.</span><span class="sxs-lookup"><span data-stu-id="b7952-104">These values can be combined using the bitwise OR operation to indicate that the field has multiple, different static qualities.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7952-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7952-105">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_FIELD_NOT_A_STATIC = 0x0,  
    COR_PRF_FIELD_APP_DOMAIN_STATIC = 0x1,  
    COR_PRF_FIELD_THREAD_STATIC = 0x2,  
    COR_PRF_FIELD_CONTEXT_STATIC = 0x4,  
    COR_PRF_FIELD_RVA_STATIC = 0x8  
} COR_PRF_STATIC_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="b7952-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b7952-106">Members</span></span>  
  
|<span data-ttu-id="b7952-107">Membre</span><span class="sxs-lookup"><span data-stu-id="b7952-107">Member</span></span>|<span data-ttu-id="b7952-108">Description</span><span class="sxs-lookup"><span data-stu-id="b7952-108">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FIELD_NOT_A_STATIC`|<span data-ttu-id="b7952-109">Le champ n’est pas statique.</span><span class="sxs-lookup"><span data-stu-id="b7952-109">The field is not static.</span></span>|  
|`COR_PRF_FIELD_APP_DOMAIN_STATIC`|<span data-ttu-id="b7952-110">Le champ est statique de domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="b7952-110">The field is application domain-static.</span></span>|  
|`COR_PRF_FIELD_THREAD_STATIC`|<span data-ttu-id="b7952-111">Le champ est thread-static.</span><span class="sxs-lookup"><span data-stu-id="b7952-111">The field is thread-static.</span></span>|  
|`COR_PRF_FIELD_CONTEXT_STATIC`|<span data-ttu-id="b7952-112">Le champ est statique de contexte.</span><span class="sxs-lookup"><span data-stu-id="b7952-112">The field is context-static.</span></span>|  
|`COR_PRF_FIELD_RVA_STATIC`|<span data-ttu-id="b7952-113">Le champ est l’adresse virtuelle relative (RVA)-statique.</span><span class="sxs-lookup"><span data-stu-id="b7952-113">The field is relative virtual address (RVA)-static.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b7952-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7952-114">Requirements</span></span>  
 <span data-ttu-id="b7952-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b7952-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7952-116">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b7952-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b7952-117">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7952-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7952-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7952-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7952-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7952-119">See also</span></span>

- [<span data-ttu-id="b7952-120">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="b7952-120">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
