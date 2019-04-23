---
title: IDENTITY_ATTRIBUTE, structure
ms.date: 03/30/2017
api_name:
- IDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDENTITY_ATTRIBUTE
helpviewer_keywords:
- IDENTITY_ATTRIBUTE structure [.NET Framework fusion]
ms.assetid: 1ee7c434-9681-4fa8-badd-652cb1a9742b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: cb970d31fb5158adc7dbcbb7cc0175cc91c83c8c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59107339"
---
# <a name="identityattribute-structure"></a><span data-ttu-id="f67e0-102">IDENTITY_ATTRIBUTE, structure</span><span class="sxs-lookup"><span data-stu-id="f67e0-102">IDENTITY_ATTRIBUTE Structure</span></span>
<span data-ttu-id="f67e0-103">Contient des informations d’attribut de métadonnées sur une [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) instance.</span><span class="sxs-lookup"><span data-stu-id="f67e0-103">Contains metadata attribute information about an [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f67e0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f67e0-104">Syntax</span></span>  
  
```  
typedef struct _IDENTITY_ATTRIBUTE {  
    LPCWSTR  pszNamespace;  
    LPCWSTR  pszName;  
    LPCWSTR  pszValue;  
} IDENTITY_ATTRIBUTE;  
```  
  
## <a name="members"></a><span data-ttu-id="f67e0-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f67e0-105">Members</span></span>  
  
|<span data-ttu-id="f67e0-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f67e0-106">Member</span></span>|<span data-ttu-id="f67e0-107">Description</span><span class="sxs-lookup"><span data-stu-id="f67e0-107">Description</span></span>|  
|------------|-----------------|  
|`pszNamespace`|<span data-ttu-id="f67e0-108">Un pointeur vers une chaîne de caractères se terminant par null qui contient l’espace de noms de l’attribut est dans.</span><span class="sxs-lookup"><span data-stu-id="f67e0-108">A pointer to a null-terminated character string that contains the namespace the attribute is in.</span></span>|  
|`pszName`|<span data-ttu-id="f67e0-109">Un pointeur vers une chaîne de caractères se terminant par null qui contient le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="f67e0-109">A pointer to a null-terminated character string that contains the name of the attribute.</span></span>|  
|`pszValue`|<span data-ttu-id="f67e0-110">Un pointeur vers une chaîne de caractères se terminant par null qui contient la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="f67e0-110">A pointer to a null-terminated character string that contains the value of the attribute.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f67e0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f67e0-111">Remarks</span></span>  
 <span data-ttu-id="f67e0-112">Le `IDENTITY_ATTRIBUTE` structure contient trois pointeurs vers des chaînes de caractères se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="f67e0-112">The `IDENTITY_ATTRIBUTE` structure contains three pointers to null-terminated character strings.</span></span> <span data-ttu-id="f67e0-113">Ces trois chaînes décrivent un attribut.</span><span class="sxs-lookup"><span data-stu-id="f67e0-113">These three strings describe one attribute.</span></span>  
  
 <span data-ttu-id="f67e0-114">Une instance d’un `IDENTITY_ATTRIBUTE` structure est associée à une instance d’un [IDENTITY_ATTRIBUTE_BLOB](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="f67e0-114">An instance of an `IDENTITY_ATTRIBUTE` structure is associated with an instance of an [IDENTITY_ATTRIBUTE_BLOB](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md) structure.</span></span> <span data-ttu-id="f67e0-115">Le `IDENTITY_ATTRIBUTE` structure contient les chaînes réelles et correspondants `IDENTITY_ATTRIBUTE_BLOB` structure répertorie les offsets pour les trois chaînes répertoriées dans le `IDENTITY_ATTRIBUTE` structure.</span><span class="sxs-lookup"><span data-stu-id="f67e0-115">The `IDENTITY_ATTRIBUTE` structure contains the actual strings, and the corresponding `IDENTITY_ATTRIBUTE_BLOB` structure lists the offsets to the three strings listed in the `IDENTITY_ATTRIBUTE` structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f67e0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f67e0-116">Requirements</span></span>  
 <span data-ttu-id="f67e0-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f67e0-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f67e0-118">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="f67e0-118">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="f67e0-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f67e0-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f67e0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f67e0-120">See also</span></span>

- [<span data-ttu-id="f67e0-121">IDefinitionIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="f67e0-121">IDefinitionIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md)
- [<span data-ttu-id="f67e0-122">IDENTITY_ATTRIBUTE_BLOB, structure</span><span class="sxs-lookup"><span data-stu-id="f67e0-122">IDENTITY_ATTRIBUTE_BLOB Structure</span></span>](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md)
- [<span data-ttu-id="f67e0-123">Structures de fusion</span><span class="sxs-lookup"><span data-stu-id="f67e0-123">Fusion Structures</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-structures.md)
