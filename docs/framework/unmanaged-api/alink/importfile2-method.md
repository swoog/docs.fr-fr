---
title: ImportFile2, méthode
ms.date: 03/30/2017
api_name:
- IALink.ImportFile2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFile2
helpviewer_keywords:
- ImportFile2 method
ms.assetid: 9a6be861-c260-4a35-acea-3372ea515a0f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 88006703ba4a491ae458868a1431be618d37252a
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57471197"
---
# <a name="importfile2-method"></a><span data-ttu-id="e4d3e-102">ImportFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="e4d3e-102">ImportFile2 Method</span></span>
<span data-ttu-id="e4d3e-103">Importe des assemblys et modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-103">Imports assemblies and unbound modules.</span></span> <span data-ttu-id="e4d3e-104">Cette méthode est comparable à [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md), mais fonctionne même si le fichier importé n’existe pas sur le disque.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-104">This method is like [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md), but works even if the file being imported does not exist on disk.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4d3e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4d3e-105">Syntax</span></span>  
  
```  
HRESULT ImportFile2(  
    LPCWSTR         pszFilename,  
    LPCWSTR         pszTargetName,  
    IMetaDataAssemblyImport* pAssemblyScopeIn,  
    BOOL            fSmartImport,  
    mdToken*        pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD*          pdwCountOfScopes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="e4d3e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4d3e-106">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="e4d3e-107">Nom du fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-107">Name of file to be imported.</span></span>  
  
 `pszTargetName`  
 <span data-ttu-id="e4d3e-108">Nom de fichier de sortie facultatif qui peut être utilisé pour renommer le fichier car il est lié dans l’assembly.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-108">Optional output file name that can be used to rename the file as it is linked into the assembly.</span></span>  
  
 `pAssemblyScopeIn`  
 <span data-ttu-id="e4d3e-109">Portée facultative [IMetaDataAssemblyImport, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-109">Optional scope [IMetaDataAssemblyImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span></span>  
  
 `fSmartImport`  
 <span data-ttu-id="e4d3e-110">Si la valeur est TRUE, ImportTypes est utilisé, sinon l’importation doit être effectuée manuellement.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-110">If TRUE, ImportTypes is used, otherwise importing must be performed manually.</span></span>  
  
 `pImportToken`  
 <span data-ttu-id="e4d3e-111">Reçoit l’ID pour le fichier ou l’assembly.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-111">Receives the ID for the file or assembly.</span></span>  
  
 `ppAssemblyScope`  
 <span data-ttu-id="e4d3e-112">Reçoit le [IMetaDataAssemblyImport, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-112">Receives the [IMetaDataAssemblyImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span></span> <span data-ttu-id="e4d3e-113">NULL si le fichier n’est pas un assembly.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-113">NULL if the file is not an assembly.</span></span>  
  
 `pdwCountOfScopes`  
 <span data-ttu-id="e4d3e-114">Reçoit le trouvé de fichiers et/ou de portées importés.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-114">Receives the found of files and/or scopes imported.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e4d3e-115">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e4d3e-115">Return Value</span></span>  
 <span data-ttu-id="e4d3e-116">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-116">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4d3e-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e4d3e-117">Requirements</span></span>  
 <span data-ttu-id="e4d3e-118">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="e4d3e-118">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4d3e-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4d3e-119">See also</span></span>
- [<span data-ttu-id="e4d3e-120">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="e4d3e-120">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="e4d3e-121">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="e4d3e-121">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="e4d3e-122">API ALink</span><span class="sxs-lookup"><span data-stu-id="e4d3e-122">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
