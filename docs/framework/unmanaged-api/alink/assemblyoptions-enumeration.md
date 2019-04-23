---
title: Énumération AssemblyOptions
ms.date: 03/30/2017
api_name:
- AssemblyOptions
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyOptions
helpviewer_keywords:
- Alink API, AssemblyOptions enumeration
- AssemblyOptions enumeration
ms.assetid: 84f83921-64cb-49e3-ac8b-22a0b77b18a8
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 293787d7798768ff2b4e2fb8fec9ed201fdb85ff
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59085413"
---
# <a name="assemblyoptions-enumeration"></a><span data-ttu-id="3459c-102">Énumération AssemblyOptions</span><span class="sxs-lookup"><span data-stu-id="3459c-102">AssemblyOptions Enumeration</span></span>
<span data-ttu-id="3459c-103">Énumère les options de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3459c-103">Enumerates the assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3459c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3459c-104">Syntax</span></span>  
  
```  
typedef enum _AssemblyOptions {  
    optAssemTitle = 0,  
    optAssemDescription,  
    optAssemConfig,  
    optAssemOS,  
    optAssemProcessor,  
    optAssemLocale,  
    optAssemVersion,  
    optAssemCompany,  
    optAssemProduct,  
    optAssemProductVersion,  
    optAssemCopyright,  
    optAssemTrademark,  
    optAssemKeyFile,  
    optAssemKeyName,  
    optAssemAlgID,  
    optAssemFlags,  
    optAssemHalfSign,  
    optAssemFileVersion,  
    optAssemSatelliteVer,  
    optLastAssemOption  
}   AssemblyOptions;  
```  
  
## <a name="fields"></a><span data-ttu-id="3459c-105">Champs</span><span class="sxs-lookup"><span data-stu-id="3459c-105">Fields</span></span>  
  
|<span data-ttu-id="3459c-106">Champ</span><span class="sxs-lookup"><span data-stu-id="3459c-106">Field</span></span>|<span data-ttu-id="3459c-107">Description</span><span class="sxs-lookup"><span data-stu-id="3459c-107">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="3459c-108">optAssemTitle</span><span class="sxs-lookup"><span data-stu-id="3459c-108">optAssemTitle</span></span>|<span data-ttu-id="3459c-109">Chaîne - représente le titre de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3459c-109">String - Represents the assembly title.</span></span>|  
|<span data-ttu-id="3459c-110">optAssemDescription</span><span class="sxs-lookup"><span data-stu-id="3459c-110">optAssemDescription</span></span>|<span data-ttu-id="3459c-111">Chaîne - contient la description de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3459c-111">String - Contains the assembly description.</span></span>|  
|<span data-ttu-id="3459c-112">optAssemConfig</span><span class="sxs-lookup"><span data-stu-id="3459c-112">optAssemConfig</span></span>|<span data-ttu-id="3459c-113">Chaîne - contient la configuration de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3459c-113">String - Contains the assembly configuration.</span></span>|  
|<span data-ttu-id="3459c-114">optAssemOS</span><span class="sxs-lookup"><span data-stu-id="3459c-114">optAssemOS</span></span>|<span data-ttu-id="3459c-115">Chaîne - encodée comme : « dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion ».</span><span class="sxs-lookup"><span data-stu-id="3459c-115">String - Encoded as: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span></span>|  
|<span data-ttu-id="3459c-116">optAssemProcessor</span><span class="sxs-lookup"><span data-stu-id="3459c-116">optAssemProcessor</span></span>|<span data-ttu-id="3459c-117">ULONG</span><span class="sxs-lookup"><span data-stu-id="3459c-117">ULONG</span></span>|  
|<span data-ttu-id="3459c-118">optAssemLocale</span><span class="sxs-lookup"><span data-stu-id="3459c-118">optAssemLocale</span></span>|<span data-ttu-id="3459c-119">Chaîne - contient les paramètres régionaux d’assembly.</span><span class="sxs-lookup"><span data-stu-id="3459c-119">String - Contains the assembly locale.</span></span>|  
|<span data-ttu-id="3459c-120">optAssemVersion</span><span class="sxs-lookup"><span data-stu-id="3459c-120">optAssemVersion</span></span>|<span data-ttu-id="3459c-121">Chaîne - encodée sous la forme : « Major.Minor.Build.Revision ».</span><span class="sxs-lookup"><span data-stu-id="3459c-121">String - Encoded as: "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="3459c-122">optAssemCompany</span><span class="sxs-lookup"><span data-stu-id="3459c-122">optAssemCompany</span></span>|<span data-ttu-id="3459c-123">Chaîne - contient la société.</span><span class="sxs-lookup"><span data-stu-id="3459c-123">String - Contains the company.</span></span>|  
|<span data-ttu-id="3459c-124">optAssemProduct</span><span class="sxs-lookup"><span data-stu-id="3459c-124">optAssemProduct</span></span>|<span data-ttu-id="3459c-125">Chaîne - contient le nom du produit.</span><span class="sxs-lookup"><span data-stu-id="3459c-125">String - Contains the product name.</span></span>|  
|<span data-ttu-id="3459c-126">optAssemProductVersion</span><span class="sxs-lookup"><span data-stu-id="3459c-126">optAssemProductVersion</span></span>|<span data-ttu-id="3459c-127">Chaîne (également appelé InformationalVersion).</span><span class="sxs-lookup"><span data-stu-id="3459c-127">String (also known as InformationalVersion).</span></span>|  
|<span data-ttu-id="3459c-128">optAssemCopyright</span><span class="sxs-lookup"><span data-stu-id="3459c-128">optAssemCopyright</span></span>|<span data-ttu-id="3459c-129">Chaîne - contient les informations de copyright.</span><span class="sxs-lookup"><span data-stu-id="3459c-129">String - Contains the copyright information.</span></span>|  
|<span data-ttu-id="3459c-130">optAssemTrademark</span><span class="sxs-lookup"><span data-stu-id="3459c-130">optAssemTrademark</span></span>|<span data-ttu-id="3459c-131">Chaîne - contient les informations de marque.</span><span class="sxs-lookup"><span data-stu-id="3459c-131">String - Contains the trademark information.</span></span>|  
|<span data-ttu-id="3459c-132">optAssemKeyFile</span><span class="sxs-lookup"><span data-stu-id="3459c-132">optAssemKeyFile</span></span>|<span data-ttu-id="3459c-133">String (nom de fichier).</span><span class="sxs-lookup"><span data-stu-id="3459c-133">String (file name).</span></span>|  
|<span data-ttu-id="3459c-134">optAssemKeyName</span><span class="sxs-lookup"><span data-stu-id="3459c-134">optAssemKeyName</span></span>|<span data-ttu-id="3459c-135">Chaîne (le nom de clé).</span><span class="sxs-lookup"><span data-stu-id="3459c-135">String (The key name).</span></span>|  
|<span data-ttu-id="3459c-136">optAssemAlgID</span><span class="sxs-lookup"><span data-stu-id="3459c-136">optAssemAlgID</span></span>|<span data-ttu-id="3459c-137">ULONG</span><span class="sxs-lookup"><span data-stu-id="3459c-137">ULONG</span></span>|  
|<span data-ttu-id="3459c-138">optAssemFlags</span><span class="sxs-lookup"><span data-stu-id="3459c-138">optAssemFlags</span></span>|<span data-ttu-id="3459c-139">ULONG</span><span class="sxs-lookup"><span data-stu-id="3459c-139">ULONG</span></span>|  
|<span data-ttu-id="3459c-140">optAssemHalfSign</span><span class="sxs-lookup"><span data-stu-id="3459c-140">optAssemHalfSign</span></span>|<span data-ttu-id="3459c-141">Bool (également appelé DelaySign).</span><span class="sxs-lookup"><span data-stu-id="3459c-141">Bool (Also known as DelaySign).</span></span>|  
|<span data-ttu-id="3459c-142">optAssemFileVersion</span><span class="sxs-lookup"><span data-stu-id="3459c-142">optAssemFileVersion</span></span>|<span data-ttu-id="3459c-143">Chaîne - codée comme « Major.Minor.Build.Revision » - identique à la version de produit.</span><span class="sxs-lookup"><span data-stu-id="3459c-143">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span></span>|  
|<span data-ttu-id="3459c-144">optAssemSatelliteVer</span><span class="sxs-lookup"><span data-stu-id="3459c-144">optAssemSatelliteVer</span></span>|<span data-ttu-id="3459c-145">Chaîne - encodée sous la forme « Major.Minor.Build.Revision ».</span><span class="sxs-lookup"><span data-stu-id="3459c-145">String - Encoded as "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="3459c-146">optLastAssemOption</span><span class="sxs-lookup"><span data-stu-id="3459c-146">optLastAssemOption</span></span>|<span data-ttu-id="3459c-147">Un compteur du nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="3459c-147">A counter of the number of elements.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3459c-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3459c-148">Requirements</span></span>  
 <span data-ttu-id="3459c-149">**En-tête :** alink.h</span><span class="sxs-lookup"><span data-stu-id="3459c-149">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="3459c-150">**Bibliothèque**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="3459c-150">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3459c-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3459c-151">See also</span></span>

- [<span data-ttu-id="3459c-152">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="3459c-152">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
