---
title: IMetaDataAssemblyImport::FindExportedTypeByName, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.FindExportedTypeByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::FindExportedTypeByName
helpviewer_keywords:
- FindExportedTypeByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindExportedTypeByName method [.NET Framework metadata]
ms.assetid: 46264b2c-574d-4dde-aafc-77187a104fdd
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 048c7234fcb2592ea0dade135a32341a6e0f404f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444917"
---
# <a name="imetadataassemblyimportfindexportedtypebyname-method"></a><span data-ttu-id="619b8-102">IMetaDataAssemblyImport::FindExportedTypeByName, méthode</span><span class="sxs-lookup"><span data-stu-id="619b8-102">IMetaDataAssemblyImport::FindExportedTypeByName Method</span></span>
<span data-ttu-id="619b8-103">Obtient un pointeur vers un type exporté, étant donné son nom et le type englobant.</span><span class="sxs-lookup"><span data-stu-id="619b8-103">Gets a pointer to an exported type, given its name and enclosing type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="619b8-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="619b8-104">Syntax</span></span>  
  
```  
HRESULT FindExportedTypeByName (  
    [in]  LPCWSTR           szName,   
    [in]  mdToken           mdtExportedType,   
    [out] mdExportedType    *ptkExportedType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="619b8-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="619b8-105">Parameters</span></span>  
 `szName`  
 <span data-ttu-id="619b8-106">[in] Le nom du type exporté.</span><span class="sxs-lookup"><span data-stu-id="619b8-106">[in] The name of the exported type.</span></span>  
  
 `mdtExportedType`  
 <span data-ttu-id="619b8-107">[in] Le jeton de métadonnées pour la classe englobante du type exporté.</span><span class="sxs-lookup"><span data-stu-id="619b8-107">[in] The metadata token for the enclosing class of the exported type.</span></span> <span data-ttu-id="619b8-108">Cette valeur est `mdExportedTypeNil` si exporté demandé type n’est pas un type imbriqué.</span><span class="sxs-lookup"><span data-stu-id="619b8-108">This value is `mdExportedTypeNil` if the requested exported type is not a nested type.</span></span>  
  
 `ptkExportedType`  
 <span data-ttu-id="619b8-109">[out] Un pointeur vers le `mdExportedType` jeton qui représente le type exporté.</span><span class="sxs-lookup"><span data-stu-id="619b8-109">[out] A pointer to the `mdExportedType` token that represents the exported type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="619b8-110">Notes</span><span class="sxs-lookup"><span data-stu-id="619b8-110">Remarks</span></span>  
 <span data-ttu-id="619b8-111">Le `FindExportedTypeByName` méthode utilise les règles standards employées par le common language runtime pour résoudre les références.</span><span class="sxs-lookup"><span data-stu-id="619b8-111">The `FindExportedTypeByName` method uses the standard rules employed by the common language runtime for resolving references.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="619b8-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="619b8-112">Requirements</span></span>  
 <span data-ttu-id="619b8-113">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="619b8-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="619b8-114">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="619b8-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="619b8-115">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="619b8-115">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="619b8-116">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="619b8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="619b8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="619b8-117">See Also</span></span>  
 [<span data-ttu-id="619b8-118">IMetaDataAssemblyImport, interface</span><span class="sxs-lookup"><span data-stu-id="619b8-118">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)  
 [<span data-ttu-id="619b8-119">Méthode de localisation des assemblys par le runtime</span><span class="sxs-lookup"><span data-stu-id="619b8-119">How the Runtime Locates Assemblies</span></span>](../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
