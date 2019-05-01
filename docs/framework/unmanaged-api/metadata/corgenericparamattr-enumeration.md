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
ms.openlocfilehash: 0aa9b84c9e16811f799a3cd2ad096508db3f7d34
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045786"
---
# <a name="corgenericparamattr-enumeration"></a><span data-ttu-id="0ea15-102">CorGenericParamAttr, énumération</span><span class="sxs-lookup"><span data-stu-id="0ea15-102">CorGenericParamAttr Enumeration</span></span>
<span data-ttu-id="0ea15-103">Contient des valeurs qui décrivent le <xref:System.Type> paramètres pour les types génériques, comme utilisés lors d’appels à [IMetaDataEmit2::DefineGenericParam](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definegenericparam-method.md).</span><span class="sxs-lookup"><span data-stu-id="0ea15-103">Contains values that describe the <xref:System.Type> parameters for generic types, as used in calls to [IMetaDataEmit2::DefineGenericParam](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definegenericparam-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0ea15-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ea15-104">Syntax</span></span>  
  
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
  
## <a name="members"></a><span data-ttu-id="0ea15-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0ea15-105">Members</span></span>  
  
|<span data-ttu-id="0ea15-106">Membre</span><span class="sxs-lookup"><span data-stu-id="0ea15-106">Member</span></span>|<span data-ttu-id="0ea15-107">Description</span><span class="sxs-lookup"><span data-stu-id="0ea15-107">Description</span></span>|  
|------------|-----------------|  
|`gpVarianceMask`|<span data-ttu-id="0ea15-108">Variance de paramètre s’applique uniquement aux paramètres génériques pour les interfaces et délégués.</span><span class="sxs-lookup"><span data-stu-id="0ea15-108">Parameter variance applies only to generic parameters for interfaces and delegates.</span></span>|  
|`gpNonVariant`|<span data-ttu-id="0ea15-109">Indique l’absence de variance.</span><span class="sxs-lookup"><span data-stu-id="0ea15-109">Indicates the absence of variance.</span></span>|  
|`gpCovariant`|<span data-ttu-id="0ea15-110">Indique la covariance.</span><span class="sxs-lookup"><span data-stu-id="0ea15-110">Indicates covariance.</span></span>|  
|`gpContravariant`|<span data-ttu-id="0ea15-111">Indique la contravariance.</span><span class="sxs-lookup"><span data-stu-id="0ea15-111">Indicates contravariance.</span></span>|  
|`gpSpecialConstraintMask`|<span data-ttu-id="0ea15-112">Les contraintes spéciales peuvent s’appliquer à tout <xref:System.Type> paramètre.</span><span class="sxs-lookup"><span data-stu-id="0ea15-112">Special constraints can apply to any <xref:System.Type> parameter.</span></span>|  
|`gpNoSpecialConstraint`|<span data-ttu-id="0ea15-113">Indique qu’aucune contrainte s’applique à la <xref:System.Type> paramètre.</span><span class="sxs-lookup"><span data-stu-id="0ea15-113">Indicates that no constraint applies to the <xref:System.Type> parameter.</span></span>|  
|`gpReferenceTypeConstraint`|<span data-ttu-id="0ea15-114">Indique que le <xref:System.Type> paramètre doit être un type référence.</span><span class="sxs-lookup"><span data-stu-id="0ea15-114">Indicates that the <xref:System.Type> parameter must be a reference type.</span></span>|  
|`gpNotNullableValueTypeConstraint`|<span data-ttu-id="0ea15-115">Indique que le <xref:System.Type> paramètre doit être un type valeur qui ne peut pas être une valeur null.</span><span class="sxs-lookup"><span data-stu-id="0ea15-115">Indicates that the <xref:System.Type> parameter must be a value type that cannot be a null value.</span></span>|  
|`gpDefaultConstructorConstraint`|<span data-ttu-id="0ea15-116">Indique que le <xref:System.Type> paramètre doit avoir un constructeur public par défaut qui n’accepte aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0ea15-116">Indicates that the <xref:System.Type> parameter must have a default public constructor that takes no parameters.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0ea15-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ea15-117">Requirements</span></span>  
 <span data-ttu-id="0ea15-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0ea15-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0ea15-119">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="0ea15-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="0ea15-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0ea15-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ea15-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ea15-121">See also</span></span>

- [<span data-ttu-id="0ea15-122">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="0ea15-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
