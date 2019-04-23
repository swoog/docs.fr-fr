---
title: COR_PRF_RUNTIME_TYPE, énumération
ms.date: 03/30/2017
api_name:
- COR_PRF_RUNTIME_TYPE Enumeration
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_RUNTIME_TYPE
helpviewer_keywords:
- COR_PRF_RUNTIME_TYPE enumeration [.NET Framework profiling]
ms.assetid: 35449514-333f-4918-9c60-7aa198d655d2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e57c622780f0bc92061fd2928ea861f904d9eb37
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59122107"
---
# <a name="corprfruntimetype-enumeration"></a><span data-ttu-id="12700-102">COR_PRF_RUNTIME_TYPE, énumération</span><span class="sxs-lookup"><span data-stu-id="12700-102">COR_PRF_RUNTIME_TYPE Enumeration</span></span>
<span data-ttu-id="12700-103">Contient des valeurs qui indiquent la version du common language runtime (CLR) : bureau ou CoreCLR, qui est utilisé dans Silverlight.</span><span class="sxs-lookup"><span data-stu-id="12700-103">Contains values that indicate the version of the common language runtime (CLR): desktop or CoreCLR, which is used in Silverlight.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12700-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12700-104">Syntax</span></span>  
  
```  
typedef enum  
{  
    COR_PRF_DESKTOP_CLR = 0x1,  
    COR_PRF_CORE_CLR    = 0x2,  
} COR_PRF_RUNTIME_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="12700-105">Membres</span><span class="sxs-lookup"><span data-stu-id="12700-105">Members</span></span>  
  
|<span data-ttu-id="12700-106">Membre</span><span class="sxs-lookup"><span data-stu-id="12700-106">Member</span></span>|<span data-ttu-id="12700-107">Description</span><span class="sxs-lookup"><span data-stu-id="12700-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_DESKTOP_CLR`|<span data-ttu-id="12700-108">La version du CLR de bureau.</span><span class="sxs-lookup"><span data-stu-id="12700-108">The desktop version of the CLR.</span></span>|  
|`COR_PRF_CORE_CLR`|<span data-ttu-id="12700-109">La version principale du CLR, utilisée dans Silverlight.</span><span class="sxs-lookup"><span data-stu-id="12700-109">The core version of the CLR, used in Silverlight.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="12700-110">Notes</span><span class="sxs-lookup"><span data-stu-id="12700-110">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="12700-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12700-111">Requirements</span></span>  
 <span data-ttu-id="12700-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="12700-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="12700-113">**En-tête :** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="12700-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="12700-114">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="12700-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="12700-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="12700-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12700-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12700-116">See also</span></span>

- [<span data-ttu-id="12700-117">Énumérations de profilage</span><span class="sxs-lookup"><span data-stu-id="12700-117">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
