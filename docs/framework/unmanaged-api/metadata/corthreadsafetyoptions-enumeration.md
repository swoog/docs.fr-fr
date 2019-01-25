---
title: CorThreadSafetyOptions, énumération
ms.date: 03/30/2017
api_name:
- CorThreadSafetyOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorThreadSafetyOptions
helpviewer_keywords:
- CorThreadSafetyOptions enumeration [.NET Framework metadata]
ms.assetid: dae07d9b-df51-488c-b17e-52d6e48217bd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b460c2c4b0d38ec46ee9d7341de9b320a2ecaa7e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54594640"
---
# <a name="corthreadsafetyoptions-enumeration"></a><span data-ttu-id="d8d4b-102">CorThreadSafetyOptions, énumération</span><span class="sxs-lookup"><span data-stu-id="d8d4b-102">CorThreadSafetyOptions Enumeration</span></span>
<span data-ttu-id="d8d4b-103">Spécifie des indicateurs permettant de sélectionner des options pour la sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="d8d4b-103">Specifies flags to select options for thread safety.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d8d4b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8d4b-104">Syntax</span></span>  
  
```  
typedef enum CorThreadSafetyOptions {  
    MDThreadSafetyDefault       = 0x00000000,  
    MDThreadSafetyOff           = 0x00000000,  
    MDThreadSafetyOn            = 0x00000001,  
} CorThreadSafetyOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="d8d4b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="d8d4b-105">Members</span></span>  
  
|<span data-ttu-id="d8d4b-106">Membre</span><span class="sxs-lookup"><span data-stu-id="d8d4b-106">Member</span></span>|<span data-ttu-id="d8d4b-107">Description</span><span class="sxs-lookup"><span data-stu-id="d8d4b-107">Description</span></span>|  
|------------|-----------------|  
|`MDThreadSatetyDefault`|<span data-ttu-id="d8d4b-108">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d8d4b-108">Default value.</span></span> <span data-ttu-id="d8d4b-109">Comme pour `MDThreadSatetyOff`.</span><span class="sxs-lookup"><span data-stu-id="d8d4b-109">Same as `MDThreadSatetyOff`.</span></span>|  
|`MDThreadSatetyOff`|<span data-ttu-id="d8d4b-110">Indique qu’un verrou de lecture/écriture ne peut pas être défini.</span><span class="sxs-lookup"><span data-stu-id="d8d4b-110">Indicates that a reader/writer lock cannot be set.</span></span>|  
|`MDThreadSatetyOn`|<span data-ttu-id="d8d4b-111">Indique qu’un verrou en lecture/écriture peut être défini.</span><span class="sxs-lookup"><span data-stu-id="d8d4b-111">Indicates that a reader/writer lock can be set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d8d4b-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d8d4b-112">Requirements</span></span>  
 <span data-ttu-id="d8d4b-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d8d4b-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8d4b-114">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="d8d4b-114">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="d8d4b-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8d4b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8d4b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8d4b-116">See also</span></span>
- [<span data-ttu-id="d8d4b-117">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="d8d4b-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
