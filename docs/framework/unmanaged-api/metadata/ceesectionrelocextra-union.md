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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62043288"
---
# <a name="ceesectionrelocextra-union"></a><span data-ttu-id="a8c61-102">CeeSectionRelocExtra, union</span><span class="sxs-lookup"><span data-stu-id="a8c61-102">CeeSectionRelocExtra Union</span></span>
<span data-ttu-id="a8c61-103">Représente un offset d’adresse qui est utilisé par le [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface pour déplacer une section.</span><span class="sxs-lookup"><span data-stu-id="a8c61-103">Represents an address offset that is used by the [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface to relocate a section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8c61-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8c61-104">Syntax</span></span>  
  
```  
typedef union  {  
    USHORT highAdj;  
} CeeSectionRelocExtra;  
```  
  
## <a name="members"></a><span data-ttu-id="a8c61-105">Membres</span><span class="sxs-lookup"><span data-stu-id="a8c61-105">Members</span></span>  
  
|<span data-ttu-id="a8c61-106">Membre</span><span class="sxs-lookup"><span data-stu-id="a8c61-106">Member</span></span>|<span data-ttu-id="a8c61-107">Description</span><span class="sxs-lookup"><span data-stu-id="a8c61-107">Description</span></span>|  
|------------|-----------------|  
|`highAdj`|<span data-ttu-id="a8c61-108">L’ajustement de la limite supérieure de la section.</span><span class="sxs-lookup"><span data-stu-id="a8c61-108">The upper address adjustment for the section.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a8c61-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8c61-109">Requirements</span></span>  
 <span data-ttu-id="a8c61-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a8c61-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8c61-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="a8c61-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="a8c61-112">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a8c61-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="a8c61-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a8c61-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8c61-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8c61-114">See also</span></span>

- [<span data-ttu-id="a8c61-115">Unions de métadonnées</span><span class="sxs-lookup"><span data-stu-id="a8c61-115">Metadata Unions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-unions.md)
