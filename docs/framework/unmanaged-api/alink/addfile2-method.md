---
title: AddFile2, méthode
ms.date: 03/30/2017
api_name:
- AddFile2
- IALink2.AddFile2
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AddFile2
helpviewer_keywords:
- AddFile2 method
ms.assetid: 03bc49bf-a89b-4fb6-a88d-97482e061195
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 7a651be40773607e0db215eadf884ed642e6e3b1
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59126930"
---
# <a name="addfile2-method"></a><span data-ttu-id="8a090-102">AddFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="8a090-102">AddFile2 Method</span></span>
<span data-ttu-id="8a090-103">Ajoute des fichiers à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="8a090-103">Adds files to the assembly.</span></span> <span data-ttu-id="8a090-104">Peut également être utilisé pour créer des modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="8a090-104">Can also be used to create unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a090-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a090-105">Syntax</span></span>  
  
```  
HRESULT AddFile2(  
    mdAssembly AssemblyID,  
    LPCWSTR pszFilename,  
    DWORD dwFlags,  
    IMetaDataEmit2* pEmitter,  
    mdFile* pFileToken  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="8a090-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a090-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="8a090-107">ID de l’assembly auquel le fichier est ajouté.</span><span class="sxs-lookup"><span data-stu-id="8a090-107">ID for the assembly to which the file is added.</span></span>  
  
 `pszFilename`  
 <span data-ttu-id="8a090-108">Nom du fichier à ajouter.</span><span class="sxs-lookup"><span data-stu-id="8a090-108">Name of the file to be added.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="8a090-109">COM + `FileDef` indicateurs tels que `ffContainsNoMetaData` et `ffWriteable`.</span><span class="sxs-lookup"><span data-stu-id="8a090-109">COM+ `FileDef` flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="8a090-110">`dwFlags` est passé à [DefineFile, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="8a090-110">`dwFlags` is passed to [DefineFile Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="8a090-111">Interface à [IMetaDataEmit2, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="8a090-111">Interface to [IMetaDataEmit2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface.</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="8a090-112">Reçoit l’ID du fichier à ajouter.</span><span class="sxs-lookup"><span data-stu-id="8a090-112">Receives ID for the file being added.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="8a090-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8a090-113">Return Value</span></span>  
 <span data-ttu-id="8a090-114">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="8a090-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a090-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a090-115">Requirements</span></span>  
 <span data-ttu-id="8a090-116">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="8a090-116">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a090-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a090-117">See also</span></span>

- [<span data-ttu-id="8a090-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="8a090-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="8a090-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="8a090-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="8a090-120">API ALink</span><span class="sxs-lookup"><span data-stu-id="8a090-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
