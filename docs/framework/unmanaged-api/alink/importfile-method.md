---
title: ImportFile, méthode
ms.date: 03/30/2017
api_name:
- IALink.ImportFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFile
helpviewer_keywords:
- ImportFile method
ms.assetid: bcbe321f-b83a-4e9a-9f10-8d913e244dc9
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 69e48c6c3179ced167fdc39ae4df859f161727ec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59077249"
---
# <a name="importfile-method"></a><span data-ttu-id="9a04b-102">ImportFile, méthode</span><span class="sxs-lookup"><span data-stu-id="9a04b-102">ImportFile Method</span></span>
<span data-ttu-id="9a04b-103">Importe des assemblys et modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="9a04b-103">Imports assemblies and unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9a04b-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a04b-104">Syntax</span></span>  
  
```  
HRESULT ImportFile(  
    LPCWSTR pszFilename,  
    LPCWSTR pszTargetName,  
    BOOL fSmartImport,  
    mdToken* pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD* pdwCountOfScopes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a04b-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a04b-105">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="9a04b-106">Nom qualifié complet du fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="9a04b-106">Fully qualified name of file to be imported.</span></span>  
  
 `pszTargetName`  
 <span data-ttu-id="9a04b-107">Nom de fichier de sortie facultatif qui peut être utilisé pour renommer le fichier car il est lié dans l’assembly.</span><span class="sxs-lookup"><span data-stu-id="9a04b-107">Optional output file name that can be used to rename the file as it is linked into the assembly.</span></span>  
  
 `fSmartImport`  
 <span data-ttu-id="9a04b-108">Si la valeur est TRUE, ImportTypes est utilisé, sinon l’importation doit être effectuée manuellement.</span><span class="sxs-lookup"><span data-stu-id="9a04b-108">If TRUE, ImportTypes is used, otherwise importing must be performed manually.</span></span>  
  
 `pImportToken`  
 <span data-ttu-id="9a04b-109">Pointeur vers le jeton où un ID de fichier unique sera stocké.</span><span class="sxs-lookup"><span data-stu-id="9a04b-109">Pointer to token where a unique file ID will be stored.</span></span> <span data-ttu-id="9a04b-110">Le fichier peut être un assembly ou un fichier.</span><span class="sxs-lookup"><span data-stu-id="9a04b-110">The file can be an assembly or a file.</span></span>  
  
 `ppAssemblyScope`  
 <span data-ttu-id="9a04b-111">Reçoit le pointeur vers [IMetaDataAssemblyImport, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md).</span><span class="sxs-lookup"><span data-stu-id="9a04b-111">Receives pointer to [IMetaDataAssemblyImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md).</span></span> <span data-ttu-id="9a04b-112">Peut être NULL si le fichier n'est pas un assembly.</span><span class="sxs-lookup"><span data-stu-id="9a04b-112">Can be NULL if the file is not an assembly.</span></span>  
  
 `pdwCountOfScopes`  
 <span data-ttu-id="9a04b-113">Pointeur vers le nombre de fichiers et/ou des étendues qui ont été importés.</span><span class="sxs-lookup"><span data-stu-id="9a04b-113">Pointer to the count of files and/or scopes that have been imported.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9a04b-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9a04b-114">Return Value</span></span>  
 <span data-ttu-id="9a04b-115">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="9a04b-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9a04b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a04b-116">Requirements</span></span>  
 <span data-ttu-id="9a04b-117">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="9a04b-117">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9a04b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a04b-118">See also</span></span>

- [<span data-ttu-id="9a04b-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="9a04b-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="9a04b-120">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="9a04b-120">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="9a04b-121">API ALink</span><span class="sxs-lookup"><span data-stu-id="9a04b-121">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
