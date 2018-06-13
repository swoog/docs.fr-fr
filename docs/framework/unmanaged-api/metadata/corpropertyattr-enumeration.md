---
title: CorPropertyAttr, énumération
ms.date: 03/30/2017
api_name:
- CorPropertyAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorPropertyAttr
helpviewer_keywords:
- CorPropertyAttr enumeration [.NET Framework metadata]
ms.assetid: 58ac8202-854d-4efd-acfb-d2da8b446e12
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 263981708af2e40bd3690a3cd344156488eed0dd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33442677"
---
# <a name="corpropertyattr-enumeration"></a><span data-ttu-id="61304-102">CorPropertyAttr, énumération</span><span class="sxs-lookup"><span data-stu-id="61304-102">CorPropertyAttr Enumeration</span></span>
<span data-ttu-id="61304-103">Contient des valeurs qui décrivent les métadonnées d'une propriété.</span><span class="sxs-lookup"><span data-stu-id="61304-103">Contains values that describe the metadata of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61304-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61304-104">Syntax</span></span>  
  
```  
typedef enum CorPropertyAttr {  
  
    prSpecialName           =   0x0200,   
    prReservedMask          =   0xf400,  
    prRTSpecialName         =   0x0400,  
    prHasDefault            =   0x1000,  
    prUnused                =   0xe9ff  
  
} CorPropertyAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="61304-105">Membres</span><span class="sxs-lookup"><span data-stu-id="61304-105">Members</span></span>  
  
|<span data-ttu-id="61304-106">Membre</span><span class="sxs-lookup"><span data-stu-id="61304-106">Member</span></span>|<span data-ttu-id="61304-107">Description</span><span class="sxs-lookup"><span data-stu-id="61304-107">Description</span></span>|  
|------------|-----------------|  
|`prSpecialName`|<span data-ttu-id="61304-108">Spécifie que la propriété est spéciale et que son nom décrit comment.</span><span class="sxs-lookup"><span data-stu-id="61304-108">Specifies that the property is special, and that its name describes how.</span></span>|  
|`prReservedMask`|<span data-ttu-id="61304-109">Réservé à un usage interne par le common language runtime.</span><span class="sxs-lookup"><span data-stu-id="61304-109">Reserved for internal use by the common language runtime.</span></span>|  
|`prRTSpecialName`|<span data-ttu-id="61304-110">Spécifie que les métadonnées du common language runtime API internes doivent vérifier l’encodage du nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="61304-110">Specifies that the common language runtime metadata internal APIs should check the encoding of the property name.</span></span>|  
|`prHasDefault`|<span data-ttu-id="61304-111">Spécifie que la propriété a une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="61304-111">Specifies that the property has a default value.</span></span>|  
|`prUnused`|<span data-ttu-id="61304-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="61304-112">Unused.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="61304-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="61304-113">Requirements</span></span>  
 <span data-ttu-id="61304-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="61304-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="61304-115">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="61304-115">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="61304-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="61304-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61304-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61304-117">See Also</span></span>  
 [<span data-ttu-id="61304-118">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="61304-118">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
