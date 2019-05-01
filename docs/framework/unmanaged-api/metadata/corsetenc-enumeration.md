---
title: CorSetENC, énumération
ms.date: 03/30/2017
api_name:
- CorSetENC
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorSetENC
helpviewer_keywords:
- CorSetENC enumeration [.NET Framework metadata]
ms.assetid: fe4150e8-071d-43fb-8e06-c3c616dbeed2
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1fd903cb4a9ce664b7a1c958a3fef0c639d6845d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045316"
---
# <a name="corsetenc-enumeration"></a><span data-ttu-id="8b365-102">CorSetENC, énumération</span><span class="sxs-lookup"><span data-stu-id="8b365-102">CorSetENC Enumeration</span></span>
<span data-ttu-id="8b365-103">Contient des valeurs utilisées pour influencer le comportement pendant la génération de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="8b365-103">Contains values used to influence behavior during the generation of metadata.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b365-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b365-104">Syntax</span></span>  
  
```  
typedef enum CorSetENC {  
  
    MDSetENCOn                  = 0x00000001,  
    MDSetENCOff                 = 0x00000002,  
  
    MDUpdateENC                 = 0x00000001,  
    MDUpdateFull                = 0x00000002,  
    MDUpdateExtension           = 0x00000003,  
    MDUpdateIncremental         = 0x00000004,  
    MDUpdateDelta               = 0x00000005,  
    MDUpdateMask                = 0x00000007  
  
} CorSetENC;  
```  
  
## <a name="members"></a><span data-ttu-id="8b365-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8b365-105">Members</span></span>  
  
|<span data-ttu-id="8b365-106">Membre</span><span class="sxs-lookup"><span data-stu-id="8b365-106">Member</span></span>|<span data-ttu-id="8b365-107">Description</span><span class="sxs-lookup"><span data-stu-id="8b365-107">Description</span></span>|  
|------------|-----------------|  
|`MDSetENCOn`|<span data-ttu-id="8b365-108">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="8b365-108">Obsolete.</span></span>|  
|`MDSetENCOff`|<span data-ttu-id="8b365-109">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="8b365-109">Obsolete.</span></span>|  
|`MDUpdateENC`|<span data-ttu-id="8b365-110">Indique que tandis que les métadonnées peuvent être mis à jour, jetons ne peut pas être déplacés.</span><span class="sxs-lookup"><span data-stu-id="8b365-110">Indicates that whereas metadata can be updated, tokens cannot be moved.</span></span>|  
|`MDUpdateFull`|<span data-ttu-id="8b365-111">Indique que les jetons peuvent être déplacées au cours des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="8b365-111">Indicates that tokens can be moved during updates.</span></span>|  
|`MDUpdateExtension`|<span data-ttu-id="8b365-112">Indique que les mises à jour peuvent comporter que des ajouts.</span><span class="sxs-lookup"><span data-stu-id="8b365-112">Indicates that updates can consist only of additions.</span></span> <span data-ttu-id="8b365-113">Les jetons ne peuvent pas être déplacées.</span><span class="sxs-lookup"><span data-stu-id="8b365-113">Tokens cannot be moved.</span></span>|  
|`MDUpdateIncremental`|<span data-ttu-id="8b365-114">Indique que la compilation est incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="8b365-114">Indicates that compilation is incremental.</span></span>|  
|`MDUpdateDelta`|<span data-ttu-id="8b365-115">Indique que seules les métadonnées modifiées doivent être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="8b365-115">Indicates that only changed metadata should be saved.</span></span>|  
|`MDUpdateMask`|<span data-ttu-id="8b365-116">Inclut `MDUpdateENC`, `MDUpdateFull` et `MDUpdateIncremental`.</span><span class="sxs-lookup"><span data-stu-id="8b365-116">Includes `MDUpdateENC`, `MDUpdateFull` and `MDUpdateIncremental`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="8b365-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b365-117">Requirements</span></span>  
 <span data-ttu-id="8b365-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8b365-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b365-119">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="8b365-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="8b365-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8b365-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b365-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b365-121">See also</span></span>

- [<span data-ttu-id="8b365-122">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="8b365-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
