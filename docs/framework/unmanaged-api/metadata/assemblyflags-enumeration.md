---
title: AssemblyFlags, énumération
ms.date: 03/30/2017
api_name:
- AssemblyFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyFlags
helpviewer_keywords:
- AssemblyFlags enumeration [.NET Framework metadata]
ms.assetid: 40f9bd9e-16ec-447e-81b0-168c875e9866
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 9796dd234611fd6bbdf2b949b8a0ed66527aaba9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521255"
---
# <a name="assemblyflags-enumeration"></a><span data-ttu-id="3eedc-102">AssemblyFlags, énumération</span><span class="sxs-lookup"><span data-stu-id="3eedc-102">AssemblyFlags Enumeration</span></span>
<span data-ttu-id="3eedc-103">Contient des valeurs qui décrivent les fonctionnalités d’exécution d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="3eedc-103">Contains values that describe run-time features of an assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3eedc-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3eedc-104">Syntax</span></span>  
  
```  
typedef enum {  
    afImplicitExportedTypes = 0x0001,  
    afImplicitResources = 0x0002,  
    afNonSideBySideAppDomain = 0x0010,  
    afNonSideBySideProcess = 0x0020,  
    afNonSideBySideMachine = 0x0030  
} AssemblyFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="3eedc-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3eedc-105">Members</span></span>  
  
|<span data-ttu-id="3eedc-106">Membre</span><span class="sxs-lookup"><span data-stu-id="3eedc-106">Member</span></span>|<span data-ttu-id="3eedc-107">Description</span><span class="sxs-lookup"><span data-stu-id="3eedc-107">Description</span></span>|  
|------------|-----------------|  
|`afImplicitExportedTypes`|<span data-ttu-id="3eedc-108">Spécifie que les définitions de types exportés sont implicites dans les fichiers qui composent l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3eedc-108">Specifies that exported type definitions are implicit within the files that comprise the assembly.</span></span> <span data-ttu-id="3eedc-109">Dans les versions 1.0 et 1.1 du .NET Framework, cette valeur est toujours supposée être définie.</span><span class="sxs-lookup"><span data-stu-id="3eedc-109">In the .NET Framework versions 1.0 and 1.1, this value is always assumed to be set.</span></span>|  
|`afImplicitResources`|<span data-ttu-id="3eedc-110">Spécifie que les définitions de ressources sont implicites dans les fichiers qui composent l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3eedc-110">Specifies that resource definitions are implicit within the files that comprise the assembly.</span></span> <span data-ttu-id="3eedc-111">Dans le .NET Framework 1.0 et 1.1, cette valeur est toujours supposée être définie.</span><span class="sxs-lookup"><span data-stu-id="3eedc-111">In the .NET Framework 1.0 and 1.1, this value is always assumed to be set.</span></span>|  
|`afNonSideBySideAppDomain`|<span data-ttu-id="3eedc-112">Spécifie que l’assembly ne peut pas s’exécuter avec d’autres versions si elles sont exécutées sur le même domaine d’application.</span><span class="sxs-lookup"><span data-stu-id="3eedc-112">Specifies that the assembly cannot execute with other versions if they are running in the same application domain.</span></span>|  
|`afNonSideBySideProcess`|<span data-ttu-id="3eedc-113">Spécifie que l’assembly ne peut pas s’exécuter avec d’autres versions si elles sont exécutées dans le même processus.</span><span class="sxs-lookup"><span data-stu-id="3eedc-113">Specifies that the assembly cannot execute with other versions if they are running in the same process.</span></span>|  
|`afNonSideBySideMachine`|<span data-ttu-id="3eedc-114">Spécifie que l’assembly ne peut pas s’exécuter avec d’autres versions si elles sont exécutées sur le même ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3eedc-114">Specifies that the assembly cannot execute with other versions if they are running on the same computer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3eedc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="3eedc-115">Remarks</span></span>  
 <span data-ttu-id="3eedc-116">Les valeurs comprises entre 0 x 0010 et 0 x 0070 inclus, sont utilisés pour décrire les fonctionnalités de compatibilité de la côte à côte de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="3eedc-116">The values between 0x0010 and 0x0070, inclusive, are used to describe side-by-side compatibility features of the referenced assembly.</span></span> <span data-ttu-id="3eedc-117">Si aucune de ces valeurs sont définies, l’assembly est supposé être compatible avec côte à côte.</span><span class="sxs-lookup"><span data-stu-id="3eedc-117">If none of these values are set, the assembly is assumed to be side-by-side compatible.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3eedc-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3eedc-118">Requirements</span></span>  
 <span data-ttu-id="3eedc-119">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3eedc-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3eedc-120">**En-tête :** MsCorEE.h</span><span class="sxs-lookup"><span data-stu-id="3eedc-120">**Header:** MsCorEE.h</span></span>  
  
 <span data-ttu-id="3eedc-121">**Bibliothèque :** Inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3eedc-121">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="3eedc-122">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3eedc-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3eedc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eedc-123">See also</span></span>
- [<span data-ttu-id="3eedc-124">Énumérations de métadonnées</span><span class="sxs-lookup"><span data-stu-id="3eedc-124">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
- [<span data-ttu-id="3eedc-125">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="3eedc-125">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
