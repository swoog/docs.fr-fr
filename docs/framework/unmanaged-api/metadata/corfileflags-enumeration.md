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
ms.openlocfilehash: 7ecc2f62a6bb8119b7fe06a82aea827a58d04ecb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33441666"
---
# <a name="corfileflags-enumeration"></a><span data-ttu-id="d999c-102">CorFileFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="d999c-102">CorFileFlags Enumeration</span></span>
<span data-ttu-id="d999c-103">Contient des valeurs qui décrivent le type de fichier défini dans un appel à [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="d999c-103">Contains values that describe the type of file defined in a call to [IMetaDataAssemblyEmit::DefineFile](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d999c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d999c-104">Syntax</span></span>  
  
```  
typedef enum CorFileFlags {  
  
    ffContainsMetaData      =   0x0000,  
    ffContainsNoMetaData    =   0x0001  
  
} CorFileFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="d999c-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d999c-105">Members</span></span>  
  
|<span data-ttu-id="d999c-106">Membre</span><span class="sxs-lookup"><span data-stu-id="d999c-106">Member</span></span>|<span data-ttu-id="d999c-107">Description</span><span class="sxs-lookup"><span data-stu-id="d999c-107">Description</span></span>|  
|------------|-----------------|  
|`ffContainsMetaData`|<span data-ttu-id="d999c-108">Indique que le fichier n’est pas un fichier de ressources.</span><span class="sxs-lookup"><span data-stu-id="d999c-108">Indicates that the file is not a resource file.</span></span>|  
|`ffContainsNoMetaData`|<span data-ttu-id="d999c-109">Indique que le fichier, et éventuellement un fichier de ressources ne contient pas de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="d999c-109">Indicates that the file, possibly a resource file, does not contain metadata.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d999c-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d999c-110">Requirements</span></span>  
 <span data-ttu-id="d999c-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d999c-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d999c-112">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="d999c-112">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="d999c-113">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d999c-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d999c-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d999c-114">See Also</span></span>  
 [<span data-ttu-id="d999c-115">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="d999c-115">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
