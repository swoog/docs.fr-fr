---
title: ImportFileEx, méthode
ms.date: 03/30/2017
api_name:
- IALink2.ImportFileEx
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- ImportFileEx
helpviewer_keywords:
- ImportFileEx method
ms.assetid: ad276f3f-b303-46ac-97e0-66a377adaa4f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: a0381ee61a0128a8ae303d44198f8d391b4531a9
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54660617"
---
# <a name="importfileex-method"></a><span data-ttu-id="0434e-102">ImportFileEx, méthode</span><span class="sxs-lookup"><span data-stu-id="0434e-102">ImportFileEx Method</span></span>
<span data-ttu-id="0434e-103">Importations indiqué assembly ou module indépendant.</span><span class="sxs-lookup"><span data-stu-id="0434e-103">Imports indicated assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0434e-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0434e-104">Syntax</span></span>  
  
```  
HRESULT ImportFileEx(  
    LPCWSTR pszFilename,  
    LPCWSTR pszTargetName,  
    BOOL fSmartImport,  
    DWORD dwOpenFlags,  
    mdToken* pImportToken,  
    IMetaDataAssemblyImport** ppAssemblyScope,  
    DWORD* pdwCountOfScopes  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0434e-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0434e-105">Parameters</span></span>  
 `pszFilename`  
 <span data-ttu-id="0434e-106">Nom qualifié complet du fichier à partir duquel importer.</span><span class="sxs-lookup"><span data-stu-id="0434e-106">Fully qualified name of file from which to import.</span></span>  
  
 `pszTargetName`  
 <span data-ttu-id="0434e-107">Nom facultatif du fichier cible.</span><span class="sxs-lookup"><span data-stu-id="0434e-107">Optional name of target file.</span></span>  
  
 `fSmartImport`  
 <span data-ttu-id="0434e-108">Si la valeur est TRUE, ImportTypes est utilisé, sinon l’importation doit être effectuée manuellement.</span><span class="sxs-lookup"><span data-stu-id="0434e-108">If TRUE, ImportTypes is used, otherwise importing must be performed manually.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="0434e-109">Indicateurs à passer à [OpenScope, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md).</span><span class="sxs-lookup"><span data-stu-id="0434e-109">Flags to be passed along to [OpenScope Method](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-openscope-method.md).</span></span>  
  
 `pImportToken`  
 <span data-ttu-id="0434e-110">Reçoit l’ID du fichier en cours d’importation.</span><span class="sxs-lookup"><span data-stu-id="0434e-110">Receives ID of the file being imported.</span></span>  
  
 `ppAssemblyScope`  
 <span data-ttu-id="0434e-111">Reçoit la portée d’importation assembly [IMetaDataAssemblyImport, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="0434e-111">Receives assembly import scope [IMetaDataAssemblyImport Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md) interface.</span></span> <span data-ttu-id="0434e-112">A la valeur null si le fichier n’est pas un assembly.</span><span class="sxs-lookup"><span data-stu-id="0434e-112">Is set to NULL if file is not an assembly.</span></span>  
  
 `pdwCountOfScopes`  
 <span data-ttu-id="0434e-113">Reçoit le nombre de fichiers importés et/ou étendues.</span><span class="sxs-lookup"><span data-stu-id="0434e-113">Receives count of imported files and/or scopes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0434e-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0434e-114">Return Value</span></span>  
 <span data-ttu-id="0434e-115">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="0434e-115">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0434e-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0434e-116">Requirements</span></span>  
 <span data-ttu-id="0434e-117">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="0434e-117">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0434e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0434e-118">See also</span></span>
- [<span data-ttu-id="0434e-119">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="0434e-119">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="0434e-120">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="0434e-120">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="0434e-121">API ALink</span><span class="sxs-lookup"><span data-stu-id="0434e-121">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
