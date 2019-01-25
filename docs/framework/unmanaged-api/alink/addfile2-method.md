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
ms.openlocfilehash: 078820649543479e65ec35daa6e1cc2876581ddc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54693199"
---
# <a name="addfile2-method"></a><span data-ttu-id="a95df-102">AddFile2, méthode</span><span class="sxs-lookup"><span data-stu-id="a95df-102">AddFile2 Method</span></span>
<span data-ttu-id="a95df-103">Ajoute des fichiers à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="a95df-103">Adds files to the assembly.</span></span> <span data-ttu-id="a95df-104">Peut également être utilisé pour créer des modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="a95df-104">Can also be used to create unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a95df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a95df-105">Syntax</span></span>  
  
```  
HRESULT AddFile2(  
    mdAssembly AssemblyID,  
    LPCWSTR pszFilename,  
    DWORD dwFlags,  
    IMetaDataEmit2* pEmitter,  
    mdFile* pFileToken  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a95df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a95df-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="a95df-107">ID de l’assembly auquel le fichier est ajouté.</span><span class="sxs-lookup"><span data-stu-id="a95df-107">ID for the assembly to which the file is added.</span></span>  
  
 `pszFilename`  
 <span data-ttu-id="a95df-108">Nom du fichier à ajouter.</span><span class="sxs-lookup"><span data-stu-id="a95df-108">Name of the file to be added.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="a95df-109">COM + `FileDef` indicateurs tels que `ffContainsNoMetaData` et `ffWriteable`.</span><span class="sxs-lookup"><span data-stu-id="a95df-109">COM+ `FileDef` flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="a95df-110">`dwFlags` est passé à [DefineFile, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="a95df-110">`dwFlags` is passed to [DefineFile Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="a95df-111">Interface à [IMetaDataEmit2, Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface.</span><span class="sxs-lookup"><span data-stu-id="a95df-111">Interface to [IMetaDataEmit2 Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md) interface.</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="a95df-112">Reçoit l’ID du fichier à ajouter.</span><span class="sxs-lookup"><span data-stu-id="a95df-112">Receives ID for the file being added.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a95df-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a95df-113">Return Value</span></span>  
 <span data-ttu-id="a95df-114">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="a95df-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a95df-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a95df-115">Requirements</span></span>  
 <span data-ttu-id="a95df-116">Nécessite alink.h.</span><span class="sxs-lookup"><span data-stu-id="a95df-116">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a95df-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a95df-117">See also</span></span>
- [<span data-ttu-id="a95df-118">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="a95df-118">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="a95df-119">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="a95df-119">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="a95df-120">API ALink</span><span class="sxs-lookup"><span data-stu-id="a95df-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
