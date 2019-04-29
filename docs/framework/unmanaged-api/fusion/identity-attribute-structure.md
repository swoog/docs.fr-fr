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
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61698042"
---
# <a name="identityattribute-structure"></a><span data-ttu-id="8b459-102">IDENTITY_ATTRIBUTE, structure</span><span class="sxs-lookup"><span data-stu-id="8b459-102">IDENTITY_ATTRIBUTE Structure</span></span>
<span data-ttu-id="8b459-103">Contient des informations d’attribut de métadonnées sur une [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) instance.</span><span class="sxs-lookup"><span data-stu-id="8b459-103">Contains metadata attribute information about an [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8b459-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b459-104">Syntax</span></span>  
  
```  
typedef struct _IDENTITY_ATTRIBUTE {  
    LPCWSTR  pszNamespace;  
    LPCWSTR  pszName;  
    LPCWSTR  pszValue;  
} IDENTITY_ATTRIBUTE;  
```  
  
## <a name="members"></a><span data-ttu-id="8b459-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8b459-105">Members</span></span>  
  
|<span data-ttu-id="8b459-106">Membre</span><span class="sxs-lookup"><span data-stu-id="8b459-106">Member</span></span>|<span data-ttu-id="8b459-107">Description</span><span class="sxs-lookup"><span data-stu-id="8b459-107">Description</span></span>|  
|------------|-----------------|  
|`pszNamespace`|<span data-ttu-id="8b459-108">Un pointeur vers une chaîne de caractères se terminant par null qui contient l’espace de noms de l’attribut est dans.</span><span class="sxs-lookup"><span data-stu-id="8b459-108">A pointer to a null-terminated character string that contains the namespace the attribute is in.</span></span>|  
|`pszName`|<span data-ttu-id="8b459-109">Un pointeur vers une chaîne de caractères se terminant par null qui contient le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="8b459-109">A pointer to a null-terminated character string that contains the name of the attribute.</span></span>|  
|`pszValue`|<span data-ttu-id="8b459-110">Un pointeur vers une chaîne de caractères se terminant par null qui contient la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="8b459-110">A pointer to a null-terminated character string that contains the value of the attribute.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8b459-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8b459-111">Remarks</span></span>  
 <span data-ttu-id="8b459-112">Le `IDENTITY_ATTRIBUTE` structure contient trois pointeurs vers des chaînes de caractères se terminant par null.</span><span class="sxs-lookup"><span data-stu-id="8b459-112">The `IDENTITY_ATTRIBUTE` structure contains three pointers to null-terminated character strings.</span></span> <span data-ttu-id="8b459-113">Ces trois chaînes décrivent un attribut.</span><span class="sxs-lookup"><span data-stu-id="8b459-113">These three strings describe one attribute.</span></span>  
  
 <span data-ttu-id="8b459-114">Une instance d’un `IDENTITY_ATTRIBUTE` structure est associée à une instance d’un [IDENTITY_ATTRIBUTE_BLOB](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md) structure.</span><span class="sxs-lookup"><span data-stu-id="8b459-114">An instance of an `IDENTITY_ATTRIBUTE` structure is associated with an instance of an [IDENTITY_ATTRIBUTE_BLOB](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md) structure.</span></span> <span data-ttu-id="8b459-115">Le `IDENTITY_ATTRIBUTE` structure contient les chaînes réelles et correspondants `IDENTITY_ATTRIBUTE_BLOB` structure répertorie les offsets pour les trois chaînes répertoriées dans le `IDENTITY_ATTRIBUTE` structure.</span><span class="sxs-lookup"><span data-stu-id="8b459-115">The `IDENTITY_ATTRIBUTE` structure contains the actual strings, and the corresponding `IDENTITY_ATTRIBUTE_BLOB` structure lists the offsets to the three strings listed in the `IDENTITY_ATTRIBUTE` structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8b459-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b459-116">Requirements</span></span>  
 <span data-ttu-id="8b459-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8b459-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8b459-118">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="8b459-118">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="8b459-119">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8b459-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b459-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b459-120">See also</span></span>

- [<span data-ttu-id="8b459-121">IDefinitionIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="8b459-121">IDefinitionIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md)
- [<span data-ttu-id="8b459-122">IDENTITY_ATTRIBUTE_BLOB, structure</span><span class="sxs-lookup"><span data-stu-id="8b459-122">IDENTITY_ATTRIBUTE_BLOB Structure</span></span>](../../../../docs/framework/unmanaged-api/fusion/identity-attribute-blob-structure.md)
- [<span data-ttu-id="8b459-123">Structures de fusion</span><span class="sxs-lookup"><span data-stu-id="8b459-123">Fusion Structures</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-structures.md)
