---
title: ImportFileEx2, méthode
ms.date: 03/30/2017
api_name:
- IALink2.ImportFileEx2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFileEx2
helpviewer_keywords:
- ImportFileEx2 method
ms.assetid: 02c789fd-16fc-48c6-9619-56e87e2a37ca
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 784e58e0c5c2329705671580d53763f2ac30f0b2
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59201349"
---
# <a name="importfileex2-method"></a><span data-ttu-id="d9dce-102">ImportFileEx2, méthode</span><span class="sxs-lookup"><span data-stu-id="d9dce-102">ImportFileEx2 Method</span></span>
<span data-ttu-id="d9dce-103">Importe des assemblys et modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="d9dce-103">Imports assemblies and unbound modules.</span></span> <span data-ttu-id="d9dce-104">Cette méthode est comparable à [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md), mais fonctionne même si le fichier importé n’existe pas sur le disque.</span><span class="sxs-lookup"><span data-stu-id="d9dce-104">This method is like [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md), but works even if the file being imported does not exist on disk.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9dce-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9dce-105">Syntax</span></span>  
  
```  
HRESULT ImportFileEx2(  
    LPCWSTR pszFilename,  
    LPCWSTR pszTargetName,  
    IMetaDataAssemblyImport* pAssemblyScopeIn,  
    BOOL fSmartImport,  
    DWORD dwOpenFlags,  
    mdToken* pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD* pdwCountOfScopes  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="d9dce-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9dce-106">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="d9dce-107">Nom du fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="d9dce-107">Name of file to be imported.</span></span>  
  
 `pszTargetName`  
 <span data-ttu-id="d9dce-108">Nom facultatif du fichier cible.</span><span class="sxs-lookup"><span data-stu-id="d9dce-108">Optional name of target file.</span></span>  
  
 `pAssemblyScopeIn`  
 <span data-ttu-id="d9dce-109">Portée d’importation facultative [IMetaDataAssemblyImport, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="d9dce-109">Optional import scope [IMetaDataAssemblyImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span></span>  
  
 `fSmartImport`  
 <span data-ttu-id="d9dce-110">Si la valeur est TRUE, ImportTypes est utilisé, sinon l’importation doit être effectuée manuellement.</span><span class="sxs-lookup"><span data-stu-id="d9dce-110">If TRUE, ImportTypes is used, otherwise importing must be performed manually.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="d9dce-111">Indicateurs à passer à [OpenScope, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md).</span><span class="sxs-lookup"><span data-stu-id="d9dce-111">Flags to be passed along to [OpenScope Method](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md).</span></span>  
  
 `pImportToken`  
 <span data-ttu-id="d9dce-112">Reçoit l’ID unique du fichier ou l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d9dce-112">Receives unique ID for the assembly or file.</span></span>  
  
 `ppAssemblyScope`  
 <span data-ttu-id="d9dce-113">Reçoit la portée d’importation assembly [IMetaDataAssemblyImport, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="d9dce-113">Receives assembly import scope [IMetaDataAssemblyImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span></span> <span data-ttu-id="d9dce-114">Peut être NULL si le fichier n'est pas un assembly.</span><span class="sxs-lookup"><span data-stu-id="d9dce-114">Can be NULL if the file is not an assembly.</span></span>  
  
 `pdwCountOfScopes`  
 <span data-ttu-id="d9dce-115">Reçoit le nombre de fichiers et/ou de portées importés.</span><span class="sxs-lookup"><span data-stu-id="d9dce-115">Receives the number of files and/or scopes imported.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d9dce-116">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d9dce-116">Return Value</span></span>  
 <span data-ttu-id="d9dce-117">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="d9dce-117">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9dce-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9dce-118">Requirements</span></span>  
 <span data-ttu-id="d9dce-119">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="d9dce-119">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9dce-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9dce-120">See also</span></span>

- [<span data-ttu-id="d9dce-121">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="d9dce-121">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="d9dce-122">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="d9dce-122">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="d9dce-123">API ALink</span><span class="sxs-lookup"><span data-stu-id="d9dce-123">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
