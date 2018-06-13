---
title: CorCallingConvention, énumération
ms.date: 03/30/2017
api_name:
- CorCallingConvention
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCallingConvention
helpviewer_keywords:
- CorCallingConvention enumeration [.NET Framework metadata]
ms.assetid: 69156fbf-7219-43bf-b4b8-b13f1a2fcb86
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 468ad1acf55c4d1b4fc2b53730f16ee8630cf19b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444013"
---
# <a name="corcallingconvention-enumeration"></a><span data-ttu-id="627ff-102">CorCallingConvention, énumération</span><span class="sxs-lookup"><span data-stu-id="627ff-102">CorCallingConvention Enumeration</span></span>
<span data-ttu-id="627ff-103">Contient des valeurs qui décrivent les types de conventions d’appel effectuées dans le code managé.</span><span class="sxs-lookup"><span data-stu-id="627ff-103">Contains values that describe the types of calling conventions that are made in managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="627ff-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="627ff-104">Syntax</span></span>  
  
```  
typedef enum CorCallingConvention  
{  
    IMAGE_CEE_CS_CALLCONV_DEFAULT       = 0x0,  
  
    IMAGE_CEE_CS_CALLCONV_VARARG        = 0x5,  
    IMAGE_CEE_CS_CALLCONV_FIELD         = 0x6,  
    IMAGE_CEE_CS_CALLCONV_LOCAL_SIG     = 0x7,  
    IMAGE_CEE_CS_CALLCONV_PROPERTY      = 0x8,  
    IMAGE_CEE_CS_CALLCONV_UNMGD         = 0x9,  
    IMAGE_CEE_CS_CALLCONV_GENERICINST   = 0xa,  
    IMAGE_CEE_CS_CALLCONV_NATIVEVARARG  = 0xb,  
    IMAGE_CEE_CS_CALLCONV_MAX           = 0xc,  
  
    IMAGE_CEE_CS_CALLCONV_MASK          = 0x0f,  
    IMAGE_CEE_CS_CALLCONV_HASTHIS       = 0x20,  
    IMAGE_CEE_CS_CALLCONV_EXPLICITTHIS  = 0x40,  
    IMAGE_CEE_CS_CALLCONV_GENERIC       = 0x10  
  
} CorCallingConvention;  
```  
  
## <a name="members"></a><span data-ttu-id="627ff-105">Membres</span><span class="sxs-lookup"><span data-stu-id="627ff-105">Members</span></span>  
  
|<span data-ttu-id="627ff-106">Membre</span><span class="sxs-lookup"><span data-stu-id="627ff-106">Member</span></span>|<span data-ttu-id="627ff-107">Description</span><span class="sxs-lookup"><span data-stu-id="627ff-107">Description</span></span>|  
|------------|-----------------|  
|`IMAGE_CEE_CS_CALLCONV_DEFAULT`|<span data-ttu-id="627ff-108">Indique la convention d’appel par défaut.</span><span class="sxs-lookup"><span data-stu-id="627ff-108">Indicates a default calling convention.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_VARARG`|<span data-ttu-id="627ff-109">Indique que la méthode accepte un nombre variable de paramètres.</span><span class="sxs-lookup"><span data-stu-id="627ff-109">Indicates that the method takes a variable number of parameters.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_FIELD`|<span data-ttu-id="627ff-110">Indique que l’appel est dans un champ.</span><span class="sxs-lookup"><span data-stu-id="627ff-110">Indicates that the call is to a field.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_LOCAL_SIG`|<span data-ttu-id="627ff-111">Indique que l’appel concerne une méthode locale.</span><span class="sxs-lookup"><span data-stu-id="627ff-111">Indicates that the call is to a local method.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_PROPERTY`|<span data-ttu-id="627ff-112">Indique que l’appel est à une propriété.</span><span class="sxs-lookup"><span data-stu-id="627ff-112">Indicates that the call is to a property.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_UNMGD`|<span data-ttu-id="627ff-113">Indique que l’appel n’est pas géré.</span><span class="sxs-lookup"><span data-stu-id="627ff-113">Indicates that the call is unmanaged.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_GENERICINST`|<span data-ttu-id="627ff-114">Indique une instanciation de méthode générique.</span><span class="sxs-lookup"><span data-stu-id="627ff-114">Indicates a generic method instantiation.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_NATIVEVARARG`|<span data-ttu-id="627ff-115">Indique qu’un appel PInvoke de 64 bits à une méthode qui accepte un nombre variable de paramètres.</span><span class="sxs-lookup"><span data-stu-id="627ff-115">Indicates a 64-bit PInvoke call to a method that takes a variable number of parameters.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_MAX`|<span data-ttu-id="627ff-116">Décrit une valeur de 4 bits non valide.</span><span class="sxs-lookup"><span data-stu-id="627ff-116">Describes an invalid 4-bit value.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_MASK`|<span data-ttu-id="627ff-117">Indique que la convention d’appel est décrite par les quatre bits inférieurs.</span><span class="sxs-lookup"><span data-stu-id="627ff-117">Indicates that the calling convention is described by the bottom four bits.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_HASTHIS`|<span data-ttu-id="627ff-118">Indique que le bit supérieur décrit un `this` paramètre.</span><span class="sxs-lookup"><span data-stu-id="627ff-118">Indicates that the top bit describes a `this` parameter.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_EXPLICITTHIS`|<span data-ttu-id="627ff-119">Indique qu’un `this` paramètre est explicitement décrit dans la signature.</span><span class="sxs-lookup"><span data-stu-id="627ff-119">Indicates that a `this` parameter is explicitly described in the signature.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_GENERIC`|<span data-ttu-id="627ff-120">Indique une signature de méthode générique avec un nombre explicite d’arguments de type.</span><span class="sxs-lookup"><span data-stu-id="627ff-120">Indicates a generic method signature with an explicit number of type arguments.</span></span> <span data-ttu-id="627ff-121">Il précède un nombre de paramètres ordinaires.</span><span class="sxs-lookup"><span data-stu-id="627ff-121">This precedes an ordinary parameter count.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="627ff-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="627ff-122">Requirements</span></span>  
 <span data-ttu-id="627ff-123">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="627ff-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="627ff-124">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="627ff-124">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="627ff-125">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="627ff-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="627ff-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="627ff-126">See Also</span></span>  
 [<span data-ttu-id="627ff-127">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="627ff-127">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
