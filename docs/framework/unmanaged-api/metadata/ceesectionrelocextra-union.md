---
title: CeeSectionRelocExtra, union
ms.date: 03/30/2017
api_name:
- CeeSectionRelocExtra Union
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CeeSectionRelocExtra
helpviewer_keywords:
- CeeSectionRelocExtra union [.NET Framework metadata]
ms.assetid: d9568cf6-7f98-4cd6-ab36-0a2bd509afcc
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 8a78a4b82d0b2064c90c938a8614b0c7594f7856
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59182271"
---
# <a name="ceesectionrelocextra-union"></a><span data-ttu-id="fb06f-102">CeeSectionRelocExtra, union</span><span class="sxs-lookup"><span data-stu-id="fb06f-102">CeeSectionRelocExtra Union</span></span>
<span data-ttu-id="fb06f-103">Représente un offset d’adresse qui est utilisé par le [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface pour déplacer une section.</span><span class="sxs-lookup"><span data-stu-id="fb06f-103">Represents an address offset that is used by the [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface to relocate a section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fb06f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb06f-104">Syntax</span></span>  
  
```  
typedef union  {  
    USHORT highAdj;  
} CeeSectionRelocExtra;  
```  
  
## <a name="members"></a><span data-ttu-id="fb06f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="fb06f-105">Members</span></span>  
  
|<span data-ttu-id="fb06f-106">Membre</span><span class="sxs-lookup"><span data-stu-id="fb06f-106">Member</span></span>|<span data-ttu-id="fb06f-107">Description</span><span class="sxs-lookup"><span data-stu-id="fb06f-107">Description</span></span>|  
|------------|-----------------|  
|`highAdj`|<span data-ttu-id="fb06f-108">L’ajustement de la limite supérieure de la section.</span><span class="sxs-lookup"><span data-stu-id="fb06f-108">The upper address adjustment for the section.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fb06f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb06f-109">Requirements</span></span>  
 <span data-ttu-id="fb06f-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fb06f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fb06f-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="fb06f-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fb06f-112">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fb06f-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 **<span data-ttu-id="fb06f-113">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="fb06f-113">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="fb06f-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb06f-114">See also</span></span>

- [<span data-ttu-id="fb06f-115">Unions de métadonnées</span><span class="sxs-lookup"><span data-stu-id="fb06f-115">Metadata Unions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-unions.md)
