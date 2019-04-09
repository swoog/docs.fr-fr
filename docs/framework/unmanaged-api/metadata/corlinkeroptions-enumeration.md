---
title: CorLinkerOptions, énumération
ms.date: 03/30/2017
api_name:
- CorLinkerOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorLinkerOptions
helpviewer_keywords:
- CorLinkerOptions enumeration [.NET Framework metadata]
ms.assetid: a656aad6-cc7e-4994-8251-004a6a45e18f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dc0554ed89d21607978d059b26c4ad69e59a2d4c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59166632"
---
# <a name="corlinkeroptions-enumeration"></a><span data-ttu-id="ec4ff-102">CorLinkerOptions, énumération</span><span class="sxs-lookup"><span data-stu-id="ec4ff-102">CorLinkerOptions Enumeration</span></span>
<span data-ttu-id="ec4ff-103">Spécifie des indicateurs permettant de sélectionner des options pour l'éditeur de liens de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ec4ff-103">Specifies flags to select options for the metadata linker.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ec4ff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec4ff-104">Syntax</span></span>  
  
```  
typedef enum CorLinkerOptions {  
    MDAssembly          = 0x00000000,  
    MDNetModule         = 0x00000001,  
} CorLinkerOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="ec4ff-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ec4ff-105">Members</span></span>  
  
|<span data-ttu-id="ec4ff-106">Membre</span><span class="sxs-lookup"><span data-stu-id="ec4ff-106">Member</span></span>|<span data-ttu-id="ec4ff-107">Description</span><span class="sxs-lookup"><span data-stu-id="ec4ff-107">Description</span></span>|  
|------------|-----------------|  
|`MDAssembly`|<span data-ttu-id="ec4ff-108">Les types privés et les fonctions globales ne sont pas conservées.</span><span class="sxs-lookup"><span data-stu-id="ec4ff-108">The private types and global functions are not preserved.</span></span>|  
|`MDNetModule`|<span data-ttu-id="ec4ff-109">Les types privés et les fonctions globales sont conservées.</span><span class="sxs-lookup"><span data-stu-id="ec4ff-109">The private types and global functions are preserved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ec4ff-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec4ff-110">Requirements</span></span>  
 <span data-ttu-id="ec4ff-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ec4ff-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ec4ff-112">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="ec4ff-112">**Header:** CorHdr.h</span></span>  
  
 **<span data-ttu-id="ec4ff-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ec4ff-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ec4ff-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec4ff-114">See also</span></span>

- [<span data-ttu-id="ec4ff-115">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="ec4ff-115">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
