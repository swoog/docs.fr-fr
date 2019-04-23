---
title: CorArgType, énumération
ms.date: 03/30/2017
api_name:
- CorArgType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorArgType
helpviewer_keywords:
- CorArgType enumeration [.NET Framework metadata]
ms.assetid: 3c1cb268-57a0-4664-91c7-f6908ff29e32
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: af9ca932a4c4a12a2c89571f40162a4ecbd5c33d
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59144493"
---
# <a name="corargtype-enumeration"></a><span data-ttu-id="c4f3c-102">CorArgType, énumération</span><span class="sxs-lookup"><span data-stu-id="c4f3c-102">CorArgType Enumeration</span></span>
<span data-ttu-id="c4f3c-103">Contient des valeurs qui décrivent le type natif d'un handle de runtime.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-103">Contains values that describe the native type of a runtime handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4f3c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4f3c-104">Syntax</span></span>  
  
```  
typedef enum CorArgType {  
  
    IMAGE_CEE_CS_END        = 0x0,  
    IMAGE_CEE_CS_VOID       = 0x1,  
    IMAGE_CEE_CS_I4         = 0x2,  
    IMAGE_CEE_CS_I8         = 0x3,  
    IMAGE_CEE_CS_R4         = 0x4,  
    IMAGE_CEE_CS_R8         = 0x5,  
    IMAGE_CEE_CS_PTR        = 0x6,  
    IMAGE_CEE_CS_OBJECT     = 0x7,  
    IMAGE_CEE_CS_STRUCT4    = 0x8,  
    IMAGE_CEE_CS_STRUCT32   = 0x9,  
    IMAGE_CEE_CS_BYVALUE    = 0xA  
  
} CorArgType;  
```  
  
## <a name="requirements"></a><span data-ttu-id="c4f3c-105">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4f3c-105">Requirements</span></span>  
 <span data-ttu-id="c4f3c-106">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c4f3c-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4f3c-107">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="c4f3c-107">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="c4f3c-108">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4f3c-108">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4f3c-109">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4f3c-109">See also</span></span>

- [<span data-ttu-id="c4f3c-110">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="c4f3c-110">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
