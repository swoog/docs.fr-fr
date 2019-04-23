---
title: CorEventAttr, énumération
ms.date: 03/30/2017
api_name:
- CorEventAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorEventAttr
helpviewer_keywords:
- CorEventAttr enumeration [.NET Framework metadata]
ms.assetid: dc2b3281-3820-487e-930d-350b66dc6417
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a1a50c15071ea1e696e508c779309225c7e7bfa2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59097819"
---
# <a name="coreventattr-enumeration"></a><span data-ttu-id="19b8a-102">CorEventAttr, énumération</span><span class="sxs-lookup"><span data-stu-id="19b8a-102">CorEventAttr Enumeration</span></span>
<span data-ttu-id="19b8a-103">Contient des valeurs qui décrivent les métadonnées d'un événement.</span><span class="sxs-lookup"><span data-stu-id="19b8a-103">Contains values that describe the metadata of an event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="19b8a-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19b8a-104">Syntax</span></span>  
  
```  
typedef enum CorEventAttr {  
  
    evSpecialName           =   0x0200,  
  
    evReservedMask          =   0x0400,  
    evRTSpecialName         =   0x0400,  
  
} CorEventAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="19b8a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="19b8a-105">Members</span></span>  
  
|<span data-ttu-id="19b8a-106">Membre</span><span class="sxs-lookup"><span data-stu-id="19b8a-106">Member</span></span>|<span data-ttu-id="19b8a-107">Description</span><span class="sxs-lookup"><span data-stu-id="19b8a-107">Description</span></span>|  
|------------|-----------------|  
|`evSpecialName`|<span data-ttu-id="19b8a-108">Spécifie que l’événement est spécial, et que son nom décrit comment.</span><span class="sxs-lookup"><span data-stu-id="19b8a-108">Specifies that the event is special, and that its name describes how.</span></span>|  
|`evReservedMask`|<span data-ttu-id="19b8a-109">Réservé à un usage interne par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="19b8a-109">Reserved for internal use by the common language runtime.</span></span>|  
|`evRTSpecialName`|<span data-ttu-id="19b8a-110">Spécifie que le common language runtime doit vérifier l’encodage du nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="19b8a-110">Specifies that the common language runtime should check the encoding of the event name.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="19b8a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19b8a-111">Requirements</span></span>  
 <span data-ttu-id="19b8a-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="19b8a-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="19b8a-113">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="19b8a-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="19b8a-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="19b8a-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19b8a-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19b8a-115">See also</span></span>

- [<span data-ttu-id="19b8a-116">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="19b8a-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
