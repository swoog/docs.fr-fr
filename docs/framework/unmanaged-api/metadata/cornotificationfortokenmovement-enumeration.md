---
title: CorNotificationForTokenMovement, énumération
ms.date: 03/30/2017
api_name:
- CorNotificationForTokenMovement
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorNotificationForTokenMovement
helpviewer_keywords:
- CorNotificationForTokenMovement enumeration [.NET Framework metadata]
ms.assetid: 1edd1670-976a-4fc8-bef7-7c41e60ad989
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 15c5e8b34f2748868611bd7dc47ef73c491b1338
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59189428"
---
# <a name="cornotificationfortokenmovement-enumeration"></a><span data-ttu-id="edf15-102">CorNotificationForTokenMovement, énumération</span><span class="sxs-lookup"><span data-stu-id="edf15-102">CorNotificationForTokenMovement Enumeration</span></span>
<span data-ttu-id="edf15-103">Spécifie les notifications qui seront envoyées au client d’API de métadonnées lorsqu’un remappage de jeton se produit.</span><span class="sxs-lookup"><span data-stu-id="edf15-103">Specifies the notifications that will be sent to the metadata API client when a token remap occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="edf15-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edf15-104">Syntax</span></span>  
  
```  
typedef enum CorNotificationForTokenMovement {  
  
    MDNotifyDefault             = 0x0000000f,  
    MDNotifyAll                 = 0xffffffff,  
    MDNotifyNone                = 0x00000000,  
    MDNotifyMethodDef           = 0x00000001,  
    MDNotifyMemberRef           = 0x00000002,  
    MDNotifyFieldDef            = 0x00000004,  
    MDNotifyTypeRef             = 0x00000008,  
  
    MDNotifyTypeDef             = 0x00000010,  
    MDNotifyParamDef            = 0x00000020,  
    MDNotifyInterfaceImpl       = 0x00000040,  
    MDNotifyProperty            = 0x00000080,  
    MDNotifyEvent               = 0x00000100,  
    MDNotifySignature           = 0x00000200,  
    MDNotifyTypeSpec            = 0x00000400,  
    MDNotifyCustomAttribute     = 0x00000800,  
    MDNotifySecurityValue       = 0x00001000,  
    MDNotifyPermission          = 0x00002000,  
    MDNotifyModuleRef           = 0x00004000,  
  
    MDNotifyNameSpace           = 0x00008000,  
  
    MDNotifyAssemblyRef         = 0x01000000,  
    MDNotifyFile                = 0x02000000,  
    MDNotifyExportedType        = 0x04000000,  
    MDNotifyResource            = 0x08000000  
  
} CorNotificationForTokenMovement;  
```  
  
## <a name="members"></a><span data-ttu-id="edf15-105">Membres</span><span class="sxs-lookup"><span data-stu-id="edf15-105">Members</span></span>  
  
|<span data-ttu-id="edf15-106">Membre</span><span class="sxs-lookup"><span data-stu-id="edf15-106">Member</span></span>|<span data-ttu-id="edf15-107">Description</span><span class="sxs-lookup"><span data-stu-id="edf15-107">Description</span></span>|  
|------------|-----------------|  
|`MDNotifyDefault`|<span data-ttu-id="edf15-108">Notifier quand `mdTypeRef`, `mdMethodDef`, `mdMemberRef`, ou `mdFieldDef` déplacement de jetons.</span><span class="sxs-lookup"><span data-stu-id="edf15-108">Notify when `mdTypeRef`, `mdMethodDef`, `mdMemberRef`, or `mdFieldDef` tokens move.</span></span>|  
|`MDNotifyAll`|<span data-ttu-id="edf15-109">Notifier lorsque n’importe quel jeton se déplace.</span><span class="sxs-lookup"><span data-stu-id="edf15-109">Notify when any token moves.</span></span>|  
|`MDNotifyNone`|<span data-ttu-id="edf15-110">Ne pas avertir lorsque le déplacement des jetons.</span><span class="sxs-lookup"><span data-stu-id="edf15-110">Do not notify when tokens move.</span></span>|  
|`MDNotifyMethodDef`|<span data-ttu-id="edf15-111">Notifier quand un `mdMethodDef` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-111">Notify when an `mdMethodDef` token moves.</span></span>|  
|`MDNotifyMemberRef`|<span data-ttu-id="edf15-112">Notifier quand un `mdMemberRef` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-112">Notify when an `mdMemberRef` token moves.</span></span>|  
|`MDNotifyFieldDef`|<span data-ttu-id="edf15-113">Notifier quand un `mdFieldDef` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-113">Notify when an `mdFieldDef` token moves.</span></span>|  
|`MDNotifyTypeRef`|<span data-ttu-id="edf15-114">Notifier quand un `mdTypeRef` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-114">Notify when an `mdTypeRef` token moves.</span></span>|  
|`MDNotifyTypeDef`|<span data-ttu-id="edf15-115">Notifier quand un `mdTypeDef` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-115">Notify when an `mdTypeDef` token moves.</span></span>|  
|`MDNotifyParamDef`|<span data-ttu-id="edf15-116">Notifier quand un `mdParamDef` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-116">Notify when an `mdParamDef` token moves.</span></span>|  
|`MDNotifyInterfaceImpl`|<span data-ttu-id="edf15-117">Notifier quand un `mdInterfaceImpl` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-117">Notify when an `mdInterfaceImpl` token moves.</span></span>|  
|`MDNotifyProperty`|<span data-ttu-id="edf15-118">Notifier quand un `mdProperty` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-118">Notify when an `mdProperty` token moves.</span></span>|  
|`MDNotifyEvent`|<span data-ttu-id="edf15-119">Notifier quand un `mdEvent` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-119">Notify when an `mdEvent` token moves.</span></span>|  
|`MDNotifySignature`|<span data-ttu-id="edf15-120">Notifier quand un `mdSignature` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-120">Notify when an `mdSignature` token moves.</span></span>|  
|`MDNotifyTypeSpec`|<span data-ttu-id="edf15-121">Notifier quand un `mdTypeSpec` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-121">Notify when an `mdTypeSpec` token moves.</span></span>|  
|`MDNotifyCustomAttribute`|<span data-ttu-id="edf15-122">Notifier quand un `mdCustomAttribute` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-122">Notify when an `mdCustomAttribute` token moves.</span></span>|  
|`MDNotifySecurityValue`|<span data-ttu-id="edf15-123">Notifier quand un `mdSecurityValue` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-123">Notify when an `mdSecurityValue` token moves.</span></span>|  
|`MDNotifyPermission`|<span data-ttu-id="edf15-124">Notifier quand un `mdPermission` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-124">Notify when an `mdPermission` token moves.</span></span>|  
|`MDNotifyModuleRef`|<span data-ttu-id="edf15-125">Notifier quand un `mdModuleRef` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-125">Notify when an `mdModuleRef` token moves.</span></span>|  
|`MDNotifyNameSpace`|<span data-ttu-id="edf15-126">Notifier quand un `mdNameSpace` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-126">Notify when an `mdNameSpace` token moves.</span></span>|  
|`MDNotifyAssemblyRef`|<span data-ttu-id="edf15-127">Notifier quand un `mdAssemblyRef` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-127">Notify when an `mdAssemblyRef` token moves.</span></span>|  
|`MDNotifyFile`|<span data-ttu-id="edf15-128">Notifier quand un `mdFile` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-128">Notify when an `mdFile` token moves.</span></span>|  
|`MDNotifyExportedType`|<span data-ttu-id="edf15-129">Notifier quand un `mdExportedType` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-129">Notify when an `mdExportedType` token moves.</span></span>|  
|`MDNotifyResource`|<span data-ttu-id="edf15-130">Notifier quand un `mdManifestResource` se déplace du jeton.</span><span class="sxs-lookup"><span data-stu-id="edf15-130">Notify when an `mdManifestResource` token moves.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="edf15-131">Notes</span><span class="sxs-lookup"><span data-stu-id="edf15-131">Remarks</span></span>  
 <span data-ttu-id="edf15-132">Un jeton peut être re-mappé (autrement dit, déplacé) pendant une fusion des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="edf15-132">A token may be re-mapped (that is, moved) during a metadata merge.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="edf15-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edf15-133">Requirements</span></span>  
 <span data-ttu-id="edf15-134">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="edf15-134">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="edf15-135">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="edf15-135">**Header:** CorHdr.h</span></span>  
  
 **<span data-ttu-id="edf15-136">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="edf15-136">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="edf15-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edf15-137">See also</span></span>

- [<span data-ttu-id="edf15-138">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="edf15-138">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
