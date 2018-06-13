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
ms.openlocfilehash: 3407fcac420b8129dd39eabf84aec84b58651944
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33442831"
---
# <a name="corthreadsafetyoptions-enumeration"></a><span data-ttu-id="f76d9-102">CorThreadSafetyOptions, énumération</span><span class="sxs-lookup"><span data-stu-id="f76d9-102">CorThreadSafetyOptions Enumeration</span></span>
<span data-ttu-id="f76d9-103">Spécifie des indicateurs permettant de sélectionner des options pour la sécurité des threads.</span><span class="sxs-lookup"><span data-stu-id="f76d9-103">Specifies flags to select options for thread safety.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f76d9-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f76d9-104">Syntax</span></span>  
  
```  
typedef enum CorThreadSafetyOptions {  
    MDThreadSafetyDefault       = 0x00000000,  
    MDThreadSafetyOff           = 0x00000000,  
    MDThreadSafetyOn            = 0x00000001,  
} CorThreadSafetyOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="f76d9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f76d9-105">Members</span></span>  
  
|<span data-ttu-id="f76d9-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f76d9-106">Member</span></span>|<span data-ttu-id="f76d9-107">Description</span><span class="sxs-lookup"><span data-stu-id="f76d9-107">Description</span></span>|  
|------------|-----------------|  
|`MDThreadSatetyDefault`|<span data-ttu-id="f76d9-108">Valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f76d9-108">Default value.</span></span> <span data-ttu-id="f76d9-109">Comme pour `MDThreadSatetyOff`.</span><span class="sxs-lookup"><span data-stu-id="f76d9-109">Same as `MDThreadSatetyOff`.</span></span>|  
|`MDThreadSatetyOff`|<span data-ttu-id="f76d9-110">Indique qu’un verrou de lecteur/writer ne peut pas être défini.</span><span class="sxs-lookup"><span data-stu-id="f76d9-110">Indicates that a reader/writer lock cannot be set.</span></span>|  
|`MDThreadSatetyOn`|<span data-ttu-id="f76d9-111">Indique qu’un verrou de lecteur/writer peut être défini.</span><span class="sxs-lookup"><span data-stu-id="f76d9-111">Indicates that a reader/writer lock can be set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f76d9-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f76d9-112">Requirements</span></span>  
 <span data-ttu-id="f76d9-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f76d9-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f76d9-114">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="f76d9-114">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="f76d9-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f76d9-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f76d9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f76d9-116">See Also</span></span>  
 [<span data-ttu-id="f76d9-117">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="f76d9-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
