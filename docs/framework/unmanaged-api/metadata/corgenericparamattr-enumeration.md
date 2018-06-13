---
title: CorGenericParamAttr, énumération
ms.date: 03/30/2017
api_name:
- CorGenericParamAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorGenericParamAttr
helpviewer_keywords:
- CorGenericParamAttr enumeration [.NET Framework metadata]
ms.assetid: 36c76266-71d8-48dc-bd89-54943fa659c1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9d56be8c6f224010da22803894524299c0d376ba
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443534"
---
# <a name="corgenericparamattr-enumeration"></a><span data-ttu-id="164c4-102">CorGenericParamAttr, énumération</span><span class="sxs-lookup"><span data-stu-id="164c4-102">CorGenericParamAttr Enumeration</span></span>
<span data-ttu-id="164c4-103">Contient des valeurs qui décrivent le <xref:System.Type> paramètres pour les types génériques, comme utilisés lors d’appels à [IMetaDataEmit2::DefineGenericParam](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definegenericparam-method.md).</span><span class="sxs-lookup"><span data-stu-id="164c4-103">Contains values that describe the <xref:System.Type> parameters for generic types, as used in calls to [IMetaDataEmit2::DefineGenericParam](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definegenericparam-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="164c4-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="164c4-104">Syntax</span></span>  
  
```  
typedef enum CorGenericParamAttr {  
  
    gpVarianceMask                     =   0x0003,  
    gpNonVariant                       =   0x0000,   
    gpCovariant                        =   0x0001,  
    gpContravariant                    =   0x0002,  
  
    gpSpecialConstraintMask            =   0x001C,  
    gpNoSpecialConstraint              =   0x0000,  
    gpReferenceTypeConstraint          =   0x0004,   
    gpNotNullableValueTypeConstraint   =   0x0008,  
    gpDefaultConstructorConstraint     =   0x0010  
  
} CorGenericParamAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="164c4-105">Membres</span><span class="sxs-lookup"><span data-stu-id="164c4-105">Members</span></span>  
  
|<span data-ttu-id="164c4-106">Membre</span><span class="sxs-lookup"><span data-stu-id="164c4-106">Member</span></span>|<span data-ttu-id="164c4-107">Description</span><span class="sxs-lookup"><span data-stu-id="164c4-107">Description</span></span>|  
|------------|-----------------|  
|`gpVarianceMask`|<span data-ttu-id="164c4-108">Variance du paramètre s’applique uniquement aux paramètres génériques pour les interfaces et délégués.</span><span class="sxs-lookup"><span data-stu-id="164c4-108">Parameter variance applies only to generic parameters for interfaces and delegates.</span></span>|  
|`gpNonVariant`|<span data-ttu-id="164c4-109">Indique l’absence de variation.</span><span class="sxs-lookup"><span data-stu-id="164c4-109">Indicates the absence of variance.</span></span>|  
|`gpCovariant`|<span data-ttu-id="164c4-110">Indique la covariance.</span><span class="sxs-lookup"><span data-stu-id="164c4-110">Indicates covariance.</span></span>|  
|`gpContravariant`|<span data-ttu-id="164c4-111">Indique la contravariance.</span><span class="sxs-lookup"><span data-stu-id="164c4-111">Indicates contravariance.</span></span>|  
|`gpSpecialConstraintMask`|<span data-ttu-id="164c4-112">Les contraintes spéciales peuvent s’appliquer à tout <xref:System.Type> paramètre.</span><span class="sxs-lookup"><span data-stu-id="164c4-112">Special constraints can apply to any <xref:System.Type> parameter.</span></span>|  
|`gpNoSpecialConstraint`|<span data-ttu-id="164c4-113">Indique qu’aucune contrainte s’applique à la <xref:System.Type> paramètre.</span><span class="sxs-lookup"><span data-stu-id="164c4-113">Indicates that no constraint applies to the <xref:System.Type> parameter.</span></span>|  
|`gpReferenceTypeConstraint`|<span data-ttu-id="164c4-114">Indique que le <xref:System.Type> paramètre doit être un type référence.</span><span class="sxs-lookup"><span data-stu-id="164c4-114">Indicates that the <xref:System.Type> parameter must be a reference type.</span></span>|  
|`gpNotNullableValueTypeConstraint`|<span data-ttu-id="164c4-115">Indique que le <xref:System.Type> paramètre doit être un type valeur qui ne peut pas être une valeur null.</span><span class="sxs-lookup"><span data-stu-id="164c4-115">Indicates that the <xref:System.Type> parameter must be a value type that cannot be a null value.</span></span>|  
|`gpDefaultConstructorConstraint`|<span data-ttu-id="164c4-116">Indique que le <xref:System.Type> paramètre doit avoir un constructeur public par défaut qui ne prend aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="164c4-116">Indicates that the <xref:System.Type> parameter must have a default public constructor that takes no parameters.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="164c4-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="164c4-117">Requirements</span></span>  
 <span data-ttu-id="164c4-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="164c4-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="164c4-119">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="164c4-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="164c4-120">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="164c4-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="164c4-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="164c4-121">See Also</span></span>  
 [<span data-ttu-id="164c4-122">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="164c4-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
