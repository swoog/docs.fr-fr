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
ms.openlocfilehash: b31df454c49ddccc74a7e877c09efa4f45b69d9e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491792"
---
# <a name="assemblyrefflags-enumeration"></a><span data-ttu-id="38003-102">AssemblyRefFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="38003-102">AssemblyRefFlags Enumeration</span></span>
<span data-ttu-id="38003-103">Contient des valeurs qui décrivent les fonctionnalités d’une référence d’assembly.</span><span class="sxs-lookup"><span data-stu-id="38003-103">Contains values that describe features of an assembly reference.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38003-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38003-104">Syntax</span></span>  
  
```  
typedef enum {  
    arfFullOriginator = 0x0001  
} AssemblyRefFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="38003-105">Membres</span><span class="sxs-lookup"><span data-stu-id="38003-105">Members</span></span>  
  
|<span data-ttu-id="38003-106">Membre</span><span class="sxs-lookup"><span data-stu-id="38003-106">Member</span></span>|<span data-ttu-id="38003-107">Description</span><span class="sxs-lookup"><span data-stu-id="38003-107">Description</span></span>|  
|------------|-----------------|  
|`arfFullOriginator`|<span data-ttu-id="38003-108">Spécifie que la référence d’assembly contient des informations complètes et non hachées, sur le serveur de publication de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="38003-108">Specifies that the assembly reference contains full, unhashed information about the publisher of the assembly.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="38003-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="38003-109">Requirements</span></span>  
 <span data-ttu-id="38003-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="38003-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="38003-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="38003-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="38003-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="38003-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38003-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38003-113">See also</span></span>
- [<span data-ttu-id="38003-114">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="38003-114">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
- [<span data-ttu-id="38003-115">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="38003-115">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
- [<span data-ttu-id="38003-116">DefineAssemblyRef, méthode</span><span class="sxs-lookup"><span data-stu-id="38003-116">DefineAssemblyRef Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-defineassemblyref-method.md)
