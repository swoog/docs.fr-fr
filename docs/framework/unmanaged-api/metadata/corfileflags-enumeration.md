---
title: CorFileFlags, énumération
ms.date: 03/30/2017
api_name:
- CorFileFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorFileFlags
helpviewer_keywords:
- CorFileFlags enumeration [.NET Framework metadata]
ms.assetid: d16703fd-518f-412e-92cb-74433d11032e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8a614ad1bd9738c993775667ccd261a089e8b57a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624258"
---
# <a name="corfileflags-enumeration"></a><span data-ttu-id="1e7bf-102">CorFileFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="1e7bf-102">CorFileFlags Enumeration</span></span>
<span data-ttu-id="1e7bf-103">Contient des valeurs qui décrivent le type de fichier défini dans un appel à [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="1e7bf-103">Contains values that describe the type of file defined in a call to [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1e7bf-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e7bf-104">Syntax</span></span>  
  
```  
typedef enum CorFileFlags {  
  
    ffContainsMetaData      =   0x0000,  
    ffContainsNoMetaData    =   0x0001  
  
} CorFileFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="1e7bf-105">Membres</span><span class="sxs-lookup"><span data-stu-id="1e7bf-105">Members</span></span>  
  
|<span data-ttu-id="1e7bf-106">Membre</span><span class="sxs-lookup"><span data-stu-id="1e7bf-106">Member</span></span>|<span data-ttu-id="1e7bf-107">Description</span><span class="sxs-lookup"><span data-stu-id="1e7bf-107">Description</span></span>|  
|------------|-----------------|  
|`ffContainsMetaData`|<span data-ttu-id="1e7bf-108">Indique que le fichier n’est pas un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="1e7bf-108">Indicates that the file is not a resource file.</span></span>|  
|`ffContainsNoMetaData`|<span data-ttu-id="1e7bf-109">Indique que le fichier, éventuellement un fichier de ressources, ne contient pas de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="1e7bf-109">Indicates that the file, possibly a resource file, does not contain metadata.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1e7bf-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e7bf-110">Requirements</span></span>  
 <span data-ttu-id="1e7bf-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1e7bf-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1e7bf-112">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="1e7bf-112">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="1e7bf-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1e7bf-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1e7bf-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e7bf-114">See also</span></span>
- [<span data-ttu-id="1e7bf-115">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="1e7bf-115">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
