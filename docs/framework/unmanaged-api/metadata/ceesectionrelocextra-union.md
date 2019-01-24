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
ms.openlocfilehash: 9d6a5673c2aaf287131274b0c590f00a69c64fed
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54517147"
---
# <a name="ceesectionrelocextra-union"></a><span data-ttu-id="b0503-102">CeeSectionRelocExtra, union</span><span class="sxs-lookup"><span data-stu-id="b0503-102">CeeSectionRelocExtra Union</span></span>
<span data-ttu-id="b0503-103">Représente un offset d’adresse qui est utilisé par le [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface pour déplacer une section.</span><span class="sxs-lookup"><span data-stu-id="b0503-103">Represents an address offset that is used by the [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface to relocate a section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0503-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0503-104">Syntax</span></span>  
  
```  
typedef union  {  
    USHORT highAdj;  
} CeeSectionRelocExtra;  
```  
  
## <a name="members"></a><span data-ttu-id="b0503-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b0503-105">Members</span></span>  
  
|<span data-ttu-id="b0503-106">Membre</span><span class="sxs-lookup"><span data-stu-id="b0503-106">Member</span></span>|<span data-ttu-id="b0503-107">Description</span><span class="sxs-lookup"><span data-stu-id="b0503-107">Description</span></span>|  
|------------|-----------------|  
|`highAdj`|<span data-ttu-id="b0503-108">L’ajustement de la limite supérieure de la section.</span><span class="sxs-lookup"><span data-stu-id="b0503-108">The upper address adjustment for the section.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b0503-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b0503-109">Requirements</span></span>  
 <span data-ttu-id="b0503-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b0503-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0503-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b0503-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b0503-112">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b0503-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b0503-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b0503-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0503-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0503-114">See also</span></span>
- [<span data-ttu-id="b0503-115">Unions de métadonnées</span><span class="sxs-lookup"><span data-stu-id="b0503-115">Metadata Unions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-unions.md)
