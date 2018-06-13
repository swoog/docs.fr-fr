---
title: CorPEKind, énumération
ms.date: 03/30/2017
api_name:
- CorPEKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorPEKind
helpviewer_keywords:
- CorPEKind enumeration [.NET Framework metadata]
ms.assetid: 22dc6dea-b1b9-4982-a730-a022d586b117
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b5869eb16bd768d58a6f27a83f2d8d51914a8aed
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443113"
---
# <a name="corpekind-enumeration"></a><span data-ttu-id="c7622-102">CorPEKind, énumération</span><span class="sxs-lookup"><span data-stu-id="c7622-102">CorPEKind Enumeration</span></span>
<span data-ttu-id="c7622-103">Contient des valeurs qui décrivent un fichier exécutable portable (PE), tel que retourné par un appel à [IMetaDataImport2::GetPEKind](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getpekind-method.md).</span><span class="sxs-lookup"><span data-stu-id="c7622-103">Contains values that describe a portable executable (PE) file, as returned from a call to [IMetaDataImport2::GetPEKind](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-getpekind-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7622-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7622-104">Syntax</span></span>  
  
```  
typedef enum CorPEKind {  
  
    peNot           = 0x00000000,  
    peILonly        = 0x00000001,  
    pe32BitRequired = 0x00000002,  
    pe32Plus        = 0x00000004,  
    pe32Unmanaged   = 0x00000008,  
    pe32BitPreferred= 0x00000010  
  
} CorPEKind;  
```  
  
## <a name="members"></a><span data-ttu-id="c7622-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c7622-105">Members</span></span>  
  
|<span data-ttu-id="c7622-106">Membre</span><span class="sxs-lookup"><span data-stu-id="c7622-106">Member</span></span>|<span data-ttu-id="c7622-107">Description</span><span class="sxs-lookup"><span data-stu-id="c7622-107">Description</span></span>|  
|------------|-----------------|  
|`peNot`|<span data-ttu-id="c7622-108">Indique qu’il ne s’agit pas d’un fichier PE.</span><span class="sxs-lookup"><span data-stu-id="c7622-108">Indicates that this is not a PE file.</span></span>|  
|`peILOnly`|<span data-ttu-id="c7622-109">Indique que ce fichier exécutable portable contient uniquement du code managé.</span><span class="sxs-lookup"><span data-stu-id="c7622-109">Indicates that this PE file contains only managed code.</span></span>|  
|`pe32BitRequired`|<span data-ttu-id="c7622-110">Indique que ce fichier exécutable portable fait des appels Win32.</span><span class="sxs-lookup"><span data-stu-id="c7622-110">Indicates that this PE file makes Win32 calls.</span></span>|  
|`pe32Plus`|<span data-ttu-id="c7622-111">Indique que ce fichier exécutable portable s’exécute sur une plateforme 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c7622-111">Indicates that this PE file runs on a 64-bit platform.</span></span>|  
|`pe32Unmanaged`|<span data-ttu-id="c7622-112">Indique que ce fichier exécutable portable est du code natif.</span><span class="sxs-lookup"><span data-stu-id="c7622-112">Indicates that this PE file is native code.</span></span>|  
|<span data-ttu-id="c7622-113">pe32BitPreferred</span><span class="sxs-lookup"><span data-stu-id="c7622-113">pe32BitPreferred</span></span>|<span data-ttu-id="c7622-114">Indique que ce fichier PE est indépendant de la plateforme et s’il préfère qu’être chargé dans un environnement 32 bits.</span><span class="sxs-lookup"><span data-stu-id="c7622-114">Indicates that this PE file is platform-neutral and prefers to be loaded in a 32-bit environment.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c7622-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c7622-115">Remarks</span></span>  
 <span data-ttu-id="c7622-116">Ces valeurs peuvent être utilisées dans des combinaisons au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="c7622-116">These values can be used in bitwise combinations.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7622-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c7622-117">Requirements</span></span>  
 <span data-ttu-id="c7622-118">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c7622-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7622-119">**En-tête :** CorHdr.h</span><span class="sxs-lookup"><span data-stu-id="c7622-119">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="c7622-120">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7622-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7622-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7622-121">See Also</span></span>  
 [<span data-ttu-id="c7622-122">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="c7622-122">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
