---
title: AssemblyRefFlags, énumération
ms.date: 03/30/2017
api_name:
- AssemblyRefFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyRefFlags
helpviewer_keywords:
- AssemblyRefFlags enumeration [.NET Framework metadata]
ms.assetid: decd4f46-f3b2-466f-9501-e74f2b86b846
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bc98b2421d23ffd6dfb716a8cc782b46a9d59ce0
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59128893"
---
# <a name="assemblyrefflags-enumeration"></a><span data-ttu-id="79450-102">AssemblyRefFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="79450-102">AssemblyRefFlags Enumeration</span></span>
<span data-ttu-id="79450-103">Contient des valeurs qui décrivent les fonctionnalités d’une référence d’assembly.</span><span class="sxs-lookup"><span data-stu-id="79450-103">Contains values that describe features of an assembly reference.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79450-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79450-104">Syntax</span></span>  
  
```  
typedef enum {  
    arfFullOriginator = 0x0001  
} AssemblyRefFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="79450-105">Membres</span><span class="sxs-lookup"><span data-stu-id="79450-105">Members</span></span>  
  
|<span data-ttu-id="79450-106">Membre</span><span class="sxs-lookup"><span data-stu-id="79450-106">Member</span></span>|<span data-ttu-id="79450-107">Description</span><span class="sxs-lookup"><span data-stu-id="79450-107">Description</span></span>|  
|------------|-----------------|  
|`arfFullOriginator`|<span data-ttu-id="79450-108">Spécifie que la référence d’assembly contient des informations complètes et non hachées, sur le serveur de publication de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="79450-108">Specifies that the assembly reference contains full, unhashed information about the publisher of the assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="79450-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79450-109">Requirements</span></span>  
 <span data-ttu-id="79450-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="79450-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79450-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="79450-111">**Header:** Cor.h</span></span>  
  
 **<span data-ttu-id="79450-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="79450-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="79450-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79450-113">See also</span></span>

- [<span data-ttu-id="79450-114">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="79450-114">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
- [<span data-ttu-id="79450-115">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="79450-115">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
- [<span data-ttu-id="79450-116">DefineAssemblyRef, méthode</span><span class="sxs-lookup"><span data-stu-id="79450-116">DefineAssemblyRef Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md)
