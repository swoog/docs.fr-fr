---
title: ASSEMBLYMETADATA, structure
ms.date: 03/30/2017
api_name:
- ASSEMBLYMETADATA
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ASSEMBLYMETADATA
helpviewer_keywords:
- ASSEMBLYMETADATA structure [.NET Framework metadata]
ms.assetid: 1af98e57-9145-4d35-bb78-77d1da7c91a5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 83f6190872ecf4435688f3b7c82a61f5f15d9f62
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443324"
---
# <a name="assemblymetadata-structure"></a><span data-ttu-id="b03d2-102">ASSEMBLYMETADATA, structure</span><span class="sxs-lookup"><span data-stu-id="b03d2-102">ASSEMBLYMETADATA Structure</span></span>
<span data-ttu-id="b03d2-103">Contient des informations sur l’assembly référencé, y compris sa version et son niveau de prise en charge des paramètres régionaux, des processeurs et systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b03d2-103">Contains information about the referenced assembly, including its version and its level of support for locales, processors, and operating systems.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b03d2-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b03d2-104">Syntax</span></span>  
  
```  
typedef struct {  
    USHORT  usMajorVersion;  
    USHORT  usMinorVersion;  
    USHORT  usBuildNumber;  
    USHORT  usRevisionNumber;  
    LPWSTR  szLocale;  
    ULONG   cbLocale;  
    DWORD*  rdwProcessor[];  
    ULONG   ulProcessor  
    OSINFO* rOS[];  
    ULONG   ulOS;  
} ASSEMBLYMETADATA;  
```  
  
## <a name="members"></a><span data-ttu-id="b03d2-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b03d2-105">Members</span></span>  
  
|<span data-ttu-id="b03d2-106">Membre</span><span class="sxs-lookup"><span data-stu-id="b03d2-106">Member</span></span>|<span data-ttu-id="b03d2-107">Description</span><span class="sxs-lookup"><span data-stu-id="b03d2-107">Description</span></span>|  
|------------|-----------------|  
|`usMajorVersion`|<span data-ttu-id="b03d2-108">Numéro de version principale de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="b03d2-108">The major version number of the referenced assembly.</span></span> <span data-ttu-id="b03d2-109">Cette valeur ne peut pas être zéro.</span><span class="sxs-lookup"><span data-stu-id="b03d2-109">This value cannot be zero.</span></span> <span data-ttu-id="b03d2-110">Si tous les bits de `usMajorVersion` sont définis, la version principale n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b03d2-110">If all the bits of `usMajorVersion` are set, the major version is not specified.</span></span>|  
|`usMinorVersion`|<span data-ttu-id="b03d2-111">Le numéro de version secondaire de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="b03d2-111">The minor version number of the referenced assembly.</span></span> <span data-ttu-id="b03d2-112">Cette valeur ne peut pas être zéro.</span><span class="sxs-lookup"><span data-stu-id="b03d2-112">This value cannot be zero.</span></span> <span data-ttu-id="b03d2-113">Si tous les bits de `usMinorVersion` sont définis, la version secondaire n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b03d2-113">If all the bits of `usMinorVersion` are set, the minor version is not specified.</span></span>|  
|`usBuildNumber`|<span data-ttu-id="b03d2-114">Le numéro de build de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="b03d2-114">The build number of the referenced assembly.</span></span> <span data-ttu-id="b03d2-115">Cette valeur ne peut pas être zéro.</span><span class="sxs-lookup"><span data-stu-id="b03d2-115">This value cannot be zero.</span></span> <span data-ttu-id="b03d2-116">Si tous les bits de `usBuildNumber` sont définis, le numéro de build n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="b03d2-116">If all the bits of `usBuildNumber` are set, the build number is not specified.</span></span>|  
|`usRevisionNumber`|<span data-ttu-id="b03d2-117">Le numéro de révision de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="b03d2-117">The revision number of the referenced assembly.</span></span> <span data-ttu-id="b03d2-118">Cette valeur ne peut pas être zéro.</span><span class="sxs-lookup"><span data-stu-id="b03d2-118">This value cannot be zero.</span></span> <span data-ttu-id="b03d2-119">Si tous les bits de `usRevisionNumber` sont définis, le numéro de révision n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="b03d2-119">If all the bits of `usRevisionNumber` are set, the revision number is not specified.</span></span>|  
|`szLocale`|<span data-ttu-id="b03d2-120">Une liste de noms de paramètres régionaux conformément à la spécification RFC1766, séparée par des points-virgules, spécifiant les paramètres régionaux pris en charge par l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="b03d2-120">A list of locale names conforming to the RFC1766 specification, separated by semicolons, specifying the locales supported by the referenced assembly.</span></span> <span data-ttu-id="b03d2-121">Une valeur null indique l’indépendance des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="b03d2-121">A null value indicates locale independence.</span></span> <span data-ttu-id="b03d2-122">**Remarque :** dans le .NET Framework version 1.0, vous ne pouvez pas spécifier plusieurs paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="b03d2-122">**Note:**  In the .NET Framework version 1.0 you cannot specify more than one locale.</span></span>|  
|`cbLocale`|<span data-ttu-id="b03d2-123">La taille en caractères larges de `szLocale`.</span><span class="sxs-lookup"><span data-stu-id="b03d2-123">The size in wide characters of `szLocale`.</span></span>|  
|`rdwProcessor`|<span data-ttu-id="b03d2-124">Un tableau d’identificateurs, tel que défini dans Winnt.h, pour les types de processeurs pris en charge par l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="b03d2-124">An array of identifiers, as defined in Winnt.h, for the processor types that are supported by the referenced assembly.</span></span> <span data-ttu-id="b03d2-125">Une valeur NULL indique l’indépendance des processeurs.</span><span class="sxs-lookup"><span data-stu-id="b03d2-125">A NULL value indicates processor independence.</span></span>|  
|`ulProcessor`|<span data-ttu-id="b03d2-126">La longueur de la `rdwProcessor` tableau.</span><span class="sxs-lookup"><span data-stu-id="b03d2-126">The length of the `rdwProcessor` array.</span></span>|  
|`rOS`|<span data-ttu-id="b03d2-127">Un tableau de [OSINFO](../../../../docs/framework/unmanaged-api/metadata/osinfo-structure.md) instances spécifiant les systèmes d’exploitation pris en charge par l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="b03d2-127">An array of [OSINFO](../../../../docs/framework/unmanaged-api/metadata/osinfo-structure.md) instances specifying the operating systems that are supported by the referenced assembly.</span></span> <span data-ttu-id="b03d2-128">Une valeur NULL indique l’indépendance du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b03d2-128">A NULL value indicates operating-system independence.</span></span>|  
|`ulOS`|<span data-ttu-id="b03d2-129">La longueur de la `rOS` tableau.</span><span class="sxs-lookup"><span data-stu-id="b03d2-129">The length of the `rOS` array.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b03d2-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b03d2-130">Requirements</span></span>  
 <span data-ttu-id="b03d2-131">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b03d2-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b03d2-132">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="b03d2-132">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b03d2-133">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b03d2-133">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b03d2-134">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b03d2-134">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b03d2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b03d2-135">See Also</span></span>  
 [<span data-ttu-id="b03d2-136">Structures de métadonnées</span><span class="sxs-lookup"><span data-stu-id="b03d2-136">Metadata Structures</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-structures.md)  
 [<span data-ttu-id="b03d2-137">IMetaDataAssemblyEmit, interface</span><span class="sxs-lookup"><span data-stu-id="b03d2-137">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)  
 [<span data-ttu-id="b03d2-138">OSINFO, structure</span><span class="sxs-lookup"><span data-stu-id="b03d2-138">OSINFO Structure</span></span>](../../../../docs/framework/unmanaged-api/metadata/osinfo-structure.md)
