---
title: CorTokenType, énumération
ms.date: 03/30/2017
api_name:
- CorTokenType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorTokenType
helpviewer_keywords:
- CorTokenType enumeration [.NET Framework metadata]
ms.assetid: 93c9a369-225f-4eff-9b78-3fbee4902cf1
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 1b33b50e53c454f2b62253d12943ea044240d8cc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62045199"
---
# <a name="cortokentype-enumeration"></a><span data-ttu-id="ff1fe-102">CorTokenType, énumération</span><span class="sxs-lookup"><span data-stu-id="ff1fe-102">CorTokenType Enumeration</span></span>
<span data-ttu-id="ff1fe-103">Indique le type d’un jeton de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-103">Indicates the type of a metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff1fe-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff1fe-104">Syntax</span></span>  
  
```  
typedef enum CorTokenType {  
  
    mdtModule                       = 0x00000000,  
    mdtTypeRef                      = 0x01000000,  
    mdtTypeDef                      = 0x02000000,  
    mdtFieldDef                     = 0x04000000,  
    mdtMethodDef                    = 0x06000000,  
    mdtParamDef                     = 0x08000000,  
    mdtInterfaceImpl                = 0x09000000,  
    mdtMemberRef                    = 0x0a000000,  
    mdtCustomAttribute              = 0x0c000000,  
    mdtPermission                   = 0x0e000000,  
    mdtSignature                    = 0x11000000,  
    mdtEvent                        = 0x14000000,  
    mdtProperty                     = 0x17000000,  
    mdtModuleRef                    = 0x1a000000,  
    mdtTypeSpec                     = 0x1b000000,  
    mdtAssembly                     = 0x20000000,  
    mdtAssemblyRef                  = 0x23000000,  
    mdtFile                         = 0x26000000,  
    mdtExportedType                 = 0x27000000,  
    mdtManifestResource             = 0x28000000,  
    mdtGenericParam                 = 0x2a000000,  
    mdtMethodSpec                   = 0x2b000000,  
    mdtGenericParamConstraint       = 0x2c000000,  
    mdtString                       = 0x70000000,  
    mdtName                         = 0x71000000,  
    mdtBaseType                     = 0x72000000  
  
} CorTokenType;  
```  
  
## <a name="members"></a><span data-ttu-id="ff1fe-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ff1fe-105">Members</span></span>  
  
|<span data-ttu-id="ff1fe-106">Membre</span><span class="sxs-lookup"><span data-stu-id="ff1fe-106">Member</span></span>|<span data-ttu-id="ff1fe-107">Description</span><span class="sxs-lookup"><span data-stu-id="ff1fe-107">Description</span></span>|  
|------------|-----------------|  
|`mdtModule`|<span data-ttu-id="ff1fe-108">Un `mdModule` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-108">An `mdModule` token.</span></span>|  
|`mdtTypeRef`|<span data-ttu-id="ff1fe-109">Un `mdTypeRef` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-109">An `mdTypeRef` token.</span></span>|  
|`mdtTypeDef`|<span data-ttu-id="ff1fe-110">Un `mdTypeDef` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-110">An `mdTypeDef` token.</span></span>|  
|`mdtFieldDef`|<span data-ttu-id="ff1fe-111">Un `mdFieldDef` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-111">An `mdFieldDef` token.</span></span>|  
|`mdtMethodDef`|<span data-ttu-id="ff1fe-112">Un `mdMethodDef` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-112">An `mdMethodDef` token.</span></span>|  
|`mdtParamDef`|<span data-ttu-id="ff1fe-113">Un `mdParamDef` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-113">An `mdParamDef` token.</span></span>|  
|`mdtInterfaceImpl`|<span data-ttu-id="ff1fe-114">Un `mdInterfaceImpl` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-114">An `mdInterfaceImpl` token.</span></span>|  
|`mdtMemberRef`|<span data-ttu-id="ff1fe-115">Un `mdMemberRef` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-115">An `mdMemberRef` token.</span></span>|  
|`mdtCustomAttribute`|<span data-ttu-id="ff1fe-116">Un `mdCustomAttribute` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-116">An `mdCustomAttribute` token.</span></span>|  
|`mdtPermission`|<span data-ttu-id="ff1fe-117">Un `mdPermission` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-117">An `mdPermission` token.</span></span>|  
|`mdtSignature`|<span data-ttu-id="ff1fe-118">Un `mdSignature` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-118">An `mdSignature` token.</span></span>|  
|`mdtEvent`|<span data-ttu-id="ff1fe-119">Un `mdEvent` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-119">An `mdEvent` token.</span></span>|  
|`mdtProperty`|<span data-ttu-id="ff1fe-120">Un `mdProperty` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-120">An `mdProperty` token.</span></span>|  
|`mdtModuleRef`|<span data-ttu-id="ff1fe-121">Un `mdModuleRef` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-121">An `mdModuleRef` token.</span></span>|  
|`mdtTypeSpec`|<span data-ttu-id="ff1fe-122">Un `mdTypeSpec` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-122">An `mdTypeSpec` token.</span></span>|  
|`mdtAssembly`|<span data-ttu-id="ff1fe-123">Un `mdAssembly` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-123">An `mdAssembly` token.</span></span>|  
|`mdtAssemblyRef`|<span data-ttu-id="ff1fe-124">Un `mdAssemblyRef` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-124">An `mdAssemblyRef` token.</span></span>|  
|`mdtFile`|<span data-ttu-id="ff1fe-125">Un `mdFile` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-125">An `mdFile` token.</span></span>|  
|`mdtExportedType`|<span data-ttu-id="ff1fe-126">Un `mdExportedType` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-126">An `mdExportedType` token.</span></span>|  
|`mdtManifestResource`|<span data-ttu-id="ff1fe-127">Un `mdManifestResource` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-127">An `mdManifestResource` token.</span></span>|  
|`mdtGenericParam`|<span data-ttu-id="ff1fe-128">Un `mdGenericParam` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-128">An `mdGenericParam` token.</span></span>|  
|`mdtMethodSpec`|<span data-ttu-id="ff1fe-129">Un `mdMethodSpec` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-129">An `mdMethodSpec` token.</span></span>|  
|`mdtGenericParamConstraint`|<span data-ttu-id="ff1fe-130">Un `mdGenericParamConstraint` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-130">An `mdGenericParamConstraint` token.</span></span>|  
|`mdtString`|<span data-ttu-id="ff1fe-131">Un `mdString` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-131">An `mdString` token.</span></span>|  
|`mdtName`|<span data-ttu-id="ff1fe-132">Un `mdName` jeton.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-132">An `mdName` token.</span></span>|  
|`mdtBaseType`|<span data-ttu-id="ff1fe-133">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-133">Not used.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="ff1fe-134">Notes</span><span class="sxs-lookup"><span data-stu-id="ff1fe-134">Remarks</span></span>  
 <span data-ttu-id="ff1fe-135">Chaque valeur est égale à la valeur de l’octet dans le jeton de métadonnées correspondant.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-135">Each value is equal to the value of the top byte in the corresponding metadata token.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ff1fe-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff1fe-136">Requirements</span></span>  
 <span data-ttu-id="ff1fe-137">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ff1fe-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ff1fe-138">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="ff1fe-138">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="ff1fe-139">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ff1fe-139">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff1fe-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff1fe-140">See also</span></span>

- [<span data-ttu-id="ff1fe-141">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="ff1fe-141">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
