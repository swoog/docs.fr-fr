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
ms.openlocfilehash: 939e815f4d3adc5f6e1c8b8fc85c9f4b89372501
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54571481"
---
# <a name="assemblyoptions-enumeration"></a><span data-ttu-id="61e2e-102">Énumération AssemblyOptions</span><span class="sxs-lookup"><span data-stu-id="61e2e-102">AssemblyOptions Enumeration</span></span>
<span data-ttu-id="61e2e-103">Énumère les options de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="61e2e-103">Enumerates the assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="61e2e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61e2e-104">Syntax</span></span>  
  
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
  
## <a name="fields"></a><span data-ttu-id="61e2e-105">Champs</span><span class="sxs-lookup"><span data-stu-id="61e2e-105">Fields</span></span>  
  
|<span data-ttu-id="61e2e-106">Champ</span><span class="sxs-lookup"><span data-stu-id="61e2e-106">Field</span></span>|<span data-ttu-id="61e2e-107">Description</span><span class="sxs-lookup"><span data-stu-id="61e2e-107">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="61e2e-108">optAssemTitle</span><span class="sxs-lookup"><span data-stu-id="61e2e-108">optAssemTitle</span></span>|<span data-ttu-id="61e2e-109">Chaîne - représente le titre de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="61e2e-109">String - Represents the assembly title.</span></span>|  
|<span data-ttu-id="61e2e-110">optAssemDescription</span><span class="sxs-lookup"><span data-stu-id="61e2e-110">optAssemDescription</span></span>|<span data-ttu-id="61e2e-111">Chaîne - contient la description de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="61e2e-111">String - Contains the assembly description.</span></span>|  
|<span data-ttu-id="61e2e-112">optAssemConfig</span><span class="sxs-lookup"><span data-stu-id="61e2e-112">optAssemConfig</span></span>|<span data-ttu-id="61e2e-113">Chaîne - contient la configuration de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="61e2e-113">String - Contains the assembly configuration.</span></span>|  
|<span data-ttu-id="61e2e-114">optAssemOS</span><span class="sxs-lookup"><span data-stu-id="61e2e-114">optAssemOS</span></span>|<span data-ttu-id="61e2e-115">Chaîne - encodée comme : « dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion ».</span><span class="sxs-lookup"><span data-stu-id="61e2e-115">String - Encoded as: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span></span>|  
|<span data-ttu-id="61e2e-116">optAssemProcessor</span><span class="sxs-lookup"><span data-stu-id="61e2e-116">optAssemProcessor</span></span>|<span data-ttu-id="61e2e-117">ULONG</span><span class="sxs-lookup"><span data-stu-id="61e2e-117">ULONG</span></span>|  
|<span data-ttu-id="61e2e-118">optAssemLocale</span><span class="sxs-lookup"><span data-stu-id="61e2e-118">optAssemLocale</span></span>|<span data-ttu-id="61e2e-119">Chaîne - contient les paramètres régionaux d’assembly.</span><span class="sxs-lookup"><span data-stu-id="61e2e-119">String - Contains the assembly locale.</span></span>|  
|<span data-ttu-id="61e2e-120">optAssemVersion</span><span class="sxs-lookup"><span data-stu-id="61e2e-120">optAssemVersion</span></span>|<span data-ttu-id="61e2e-121">Chaîne - encodée sous la forme : « Major.Minor.Build.Revision ».</span><span class="sxs-lookup"><span data-stu-id="61e2e-121">String - Encoded as: "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="61e2e-122">optAssemCompany</span><span class="sxs-lookup"><span data-stu-id="61e2e-122">optAssemCompany</span></span>|<span data-ttu-id="61e2e-123">Chaîne - contient la société.</span><span class="sxs-lookup"><span data-stu-id="61e2e-123">String - Contains the company.</span></span>|  
|<span data-ttu-id="61e2e-124">optAssemProduct</span><span class="sxs-lookup"><span data-stu-id="61e2e-124">optAssemProduct</span></span>|<span data-ttu-id="61e2e-125">Chaîne - contient le nom du produit.</span><span class="sxs-lookup"><span data-stu-id="61e2e-125">String - Contains the product name.</span></span>|  
|<span data-ttu-id="61e2e-126">optAssemProductVersion</span><span class="sxs-lookup"><span data-stu-id="61e2e-126">optAssemProductVersion</span></span>|<span data-ttu-id="61e2e-127">Chaîne (également appelé InformationalVersion).</span><span class="sxs-lookup"><span data-stu-id="61e2e-127">String (also known as InformationalVersion).</span></span>|  
|<span data-ttu-id="61e2e-128">optAssemCopyright</span><span class="sxs-lookup"><span data-stu-id="61e2e-128">optAssemCopyright</span></span>|<span data-ttu-id="61e2e-129">Chaîne - contient les informations de copyright.</span><span class="sxs-lookup"><span data-stu-id="61e2e-129">String - Contains the copyright information.</span></span>|  
|<span data-ttu-id="61e2e-130">optAssemTrademark</span><span class="sxs-lookup"><span data-stu-id="61e2e-130">optAssemTrademark</span></span>|<span data-ttu-id="61e2e-131">Chaîne - contient les informations de marque.</span><span class="sxs-lookup"><span data-stu-id="61e2e-131">String - Contains the trademark information.</span></span>|  
|<span data-ttu-id="61e2e-132">optAssemKeyFile</span><span class="sxs-lookup"><span data-stu-id="61e2e-132">optAssemKeyFile</span></span>|<span data-ttu-id="61e2e-133">String (nom de fichier).</span><span class="sxs-lookup"><span data-stu-id="61e2e-133">String (file name).</span></span>|  
|<span data-ttu-id="61e2e-134">optAssemKeyName</span><span class="sxs-lookup"><span data-stu-id="61e2e-134">optAssemKeyName</span></span>|<span data-ttu-id="61e2e-135">Chaîne (le nom de clé).</span><span class="sxs-lookup"><span data-stu-id="61e2e-135">String (The key name).</span></span>|  
|<span data-ttu-id="61e2e-136">optAssemAlgID</span><span class="sxs-lookup"><span data-stu-id="61e2e-136">optAssemAlgID</span></span>|<span data-ttu-id="61e2e-137">ULONG</span><span class="sxs-lookup"><span data-stu-id="61e2e-137">ULONG</span></span>|  
|<span data-ttu-id="61e2e-138">optAssemFlags</span><span class="sxs-lookup"><span data-stu-id="61e2e-138">optAssemFlags</span></span>|<span data-ttu-id="61e2e-139">ULONG</span><span class="sxs-lookup"><span data-stu-id="61e2e-139">ULONG</span></span>|  
|<span data-ttu-id="61e2e-140">optAssemHalfSign</span><span class="sxs-lookup"><span data-stu-id="61e2e-140">optAssemHalfSign</span></span>|<span data-ttu-id="61e2e-141">Bool (également appelé DelaySign).</span><span class="sxs-lookup"><span data-stu-id="61e2e-141">Bool (Also known as DelaySign).</span></span>|  
|<span data-ttu-id="61e2e-142">optAssemFileVersion</span><span class="sxs-lookup"><span data-stu-id="61e2e-142">optAssemFileVersion</span></span>|<span data-ttu-id="61e2e-143">Chaîne - codée comme « Major.Minor.Build.Revision » - identique à la version de produit.</span><span class="sxs-lookup"><span data-stu-id="61e2e-143">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span></span>|  
|<span data-ttu-id="61e2e-144">optAssemSatelliteVer</span><span class="sxs-lookup"><span data-stu-id="61e2e-144">optAssemSatelliteVer</span></span>|<span data-ttu-id="61e2e-145">Chaîne - encodée sous la forme « Major.Minor.Build.Revision ».</span><span class="sxs-lookup"><span data-stu-id="61e2e-145">String - Encoded as "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="61e2e-146">optLastAssemOption</span><span class="sxs-lookup"><span data-stu-id="61e2e-146">optLastAssemOption</span></span>|<span data-ttu-id="61e2e-147">Un compteur du nombre d’éléments.</span><span class="sxs-lookup"><span data-stu-id="61e2e-147">A counter of the number of elements.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="61e2e-148">Spécifications</span><span class="sxs-lookup"><span data-stu-id="61e2e-148">Requirements</span></span>  
 <span data-ttu-id="61e2e-149">**En-tête :** alink.h</span><span class="sxs-lookup"><span data-stu-id="61e2e-149">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="61e2e-150">**Bibliothèque**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="61e2e-150">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="61e2e-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61e2e-151">See also</span></span>
- [<span data-ttu-id="61e2e-152">Al.exe (Assembly Linker)</span><span class="sxs-lookup"><span data-stu-id="61e2e-152">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)
