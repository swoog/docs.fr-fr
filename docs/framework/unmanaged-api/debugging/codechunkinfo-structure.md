---
title: CodeChunkInfo, structure
ms.date: 03/30/2017
api_name:
- CodeChunkInfo
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CodeChunkInfo
helpviewer_keywords:
- CodeChunkInfo structure [.NET Framework debugging]
ms.assetid: 0f482454-8517-48de-ba7a-d7aedab13bb5
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 58c9d4c66af0bb9f4e66d17b18ac78ef8271bc31
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59072660"
---
# <a name="codechunkinfo-structure"></a><span data-ttu-id="9b4c1-102">CodeChunkInfo, structure</span><span class="sxs-lookup"><span data-stu-id="9b4c1-102">CodeChunkInfo Structure</span></span>

<span data-ttu-id="9b4c1-103">Représente un bloc de code unique en mémoire.</span><span class="sxs-lookup"><span data-stu-id="9b4c1-103">Represents a single chunk of code in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b4c1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b4c1-104">Syntax</span></span>  
  
```  
typedef struct _CodeChunkInfo {  
    CORDB_ADDRESS startAddr;  
    ULONG32       length;  
} CodeChunkInfo;  
```  
  
## <a name="members"></a><span data-ttu-id="9b4c1-105">Membres</span><span class="sxs-lookup"><span data-stu-id="9b4c1-105">Members</span></span>  
  
|<span data-ttu-id="9b4c1-106">Membre</span><span class="sxs-lookup"><span data-stu-id="9b4c1-106">Member</span></span>|<span data-ttu-id="9b4c1-107">Description</span><span class="sxs-lookup"><span data-stu-id="9b4c1-107">Description</span></span>|  
|------------|-----------------|  
|`startAddr`|<span data-ttu-id="9b4c1-108">Un `CORDB_ADDRESS` valeur qui spécifie l’adresse de départ du segment.</span><span class="sxs-lookup"><span data-stu-id="9b4c1-108">A `CORDB_ADDRESS` value that specifies the starting address of the chunk.</span></span>|  
|`length`|<span data-ttu-id="9b4c1-109">La taille, en octets, du bloc.</span><span class="sxs-lookup"><span data-stu-id="9b4c1-109">The size, in bytes, of the chunk.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9b4c1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9b4c1-110">Remarks</span></span>  
 <span data-ttu-id="9b4c1-111">Le bloc de code unique est une région de code natif qui fait partie d’un objet de code comme une fonction.</span><span class="sxs-lookup"><span data-stu-id="9b4c1-111">The single chunk of code is a region of native code that is part of a code object such as a function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b4c1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b4c1-112">Requirements</span></span>  
 <span data-ttu-id="9b4c1-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9b4c1-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9b4c1-114">**En-tête :** CorDebug.idl</span><span class="sxs-lookup"><span data-stu-id="9b4c1-114">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="9b4c1-115">**Bibliothèque :** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9b4c1-115">**Library:** CorGuids.lib</span></span>  
  
 **<span data-ttu-id="9b4c1-116">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="9b4c1-116">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9b4c1-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b4c1-117">See also</span></span>

- [<span data-ttu-id="9b4c1-118">GetCodeChunks, méthode</span><span class="sxs-lookup"><span data-stu-id="9b4c1-118">GetCodeChunks Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugcode2-getcodechunks-method.md)
- [<span data-ttu-id="9b4c1-119">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="9b4c1-119">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)
- [<span data-ttu-id="9b4c1-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="9b4c1-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
