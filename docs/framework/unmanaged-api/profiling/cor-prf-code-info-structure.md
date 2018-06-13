---
title: COR_PRF_CODE_INFO, structure
ms.date: 03/30/2017
api_name:
- COR_PRF_CODE_INFO
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_CODE_INFO
helpviewer_keywords:
- COR_PRF_CODE_INFO structure [.NET Framework profiling]
ms.assetid: cf30e27c-1f7e-43a2-ba1e-01e4137301db
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 852e6cbd666441b92afb583b15b72d50d26eff8c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449782"
---
# <a name="corprfcodeinfo-structure"></a><span data-ttu-id="584a8-102">COR_PRF_CODE_INFO, structure</span><span class="sxs-lookup"><span data-stu-id="584a8-102">COR_PRF_CODE_INFO Structure</span></span>
<span data-ttu-id="584a8-103">Représente un bloc contigu de code natif stocké en mémoire.</span><span class="sxs-lookup"><span data-stu-id="584a8-103">Represents one contiguous block of native code stored in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="584a8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="584a8-104">Syntax</span></span>  
  
```  
typedef struct _COR_PRF_CODE_INFO {  
    UINT_PTR startAddress;  
    SIZE_T size;  
} COR_PRF_CODE_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="584a8-105">Membres</span><span class="sxs-lookup"><span data-stu-id="584a8-105">Members</span></span>  
  
|<span data-ttu-id="584a8-106">Membre</span><span class="sxs-lookup"><span data-stu-id="584a8-106">Member</span></span>|<span data-ttu-id="584a8-107">Description</span><span class="sxs-lookup"><span data-stu-id="584a8-107">Description</span></span>|  
|------------|-----------------|  
|`startAddress`|<span data-ttu-id="584a8-108">Adresse de départ du bloc contigu de code.</span><span class="sxs-lookup"><span data-stu-id="584a8-108">The starting address of the contiguous block of code.</span></span>|  
|`size`|<span data-ttu-id="584a8-109">La taille du bloc.</span><span class="sxs-lookup"><span data-stu-id="584a8-109">The size of the block.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="584a8-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="584a8-110">Requirements</span></span>  
 <span data-ttu-id="584a8-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="584a8-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="584a8-112">**En-tête :** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="584a8-112">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="584a8-113">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="584a8-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="584a8-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="584a8-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="584a8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="584a8-115">See Also</span></span>  
 [<span data-ttu-id="584a8-116">Structures de profilage</span><span class="sxs-lookup"><span data-stu-id="584a8-116">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)
