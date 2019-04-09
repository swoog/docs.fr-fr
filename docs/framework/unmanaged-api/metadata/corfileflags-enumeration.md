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
ms.openlocfilehash: 076d5de3e9d1925e3a030fee4a06a89862105897
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59159612"
---
# <a name="corfileflags-enumeration"></a><span data-ttu-id="1c67e-102">CorFileFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="1c67e-102">CorFileFlags Enumeration</span></span>
<span data-ttu-id="1c67e-103">Contient des valeurs qui décrivent le type de fichier défini dans un appel à [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="1c67e-103">Contains values that describe the type of file defined in a call to [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1c67e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c67e-104">Syntax</span></span>  
  
```  
typedef enum CorFileFlags {  
  
    ffContainsMetaData      =   0x0000,  
    ffContainsNoMetaData    =   0x0001  
  
} CorFileFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="1c67e-105">Membres</span><span class="sxs-lookup"><span data-stu-id="1c67e-105">Members</span></span>  
  
|<span data-ttu-id="1c67e-106">Membre</span><span class="sxs-lookup"><span data-stu-id="1c67e-106">Member</span></span>|<span data-ttu-id="1c67e-107">Description</span><span class="sxs-lookup"><span data-stu-id="1c67e-107">Description</span></span>|  
|------------|-----------------|  
|`ffContainsMetaData`|<span data-ttu-id="1c67e-108">Indique que le fichier n’est pas un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="1c67e-108">Indicates that the file is not a resource file.</span></span>|  
|`ffContainsNoMetaData`|<span data-ttu-id="1c67e-109">Indique que le fichier, éventuellement un fichier de ressources, ne contient pas de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="1c67e-109">Indicates that the file, possibly a resource file, does not contain metadata.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1c67e-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c67e-110">Requirements</span></span>  
 <span data-ttu-id="1c67e-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1c67e-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1c67e-112">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="1c67e-112">**Header:** CorHdr.h</span></span>  
  
 **<span data-ttu-id="1c67e-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="1c67e-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="1c67e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c67e-114">See also</span></span>

- [<span data-ttu-id="1c67e-115">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="1c67e-115">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
