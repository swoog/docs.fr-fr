---
title: AddImport, méthode
ms.date: 03/30/2017
api_name:
- AddImport
- IALink.AddImport
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AddImport
helpviewer_keywords:
- AddImport method
ms.assetid: 4fedf8a0-08c8-43d0-aa00-20f2a521c991
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: bbe8a43f44d59249abc713c95fce31f1fb9a5993
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61775633"
---
# <a name="addimport-method"></a><span data-ttu-id="cdb1c-102">AddImport, méthode</span><span class="sxs-lookup"><span data-stu-id="cdb1c-102">AddImport Method</span></span>
<span data-ttu-id="cdb1c-103">Ajoute des importations à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="cdb1c-103">Adds imports to the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cdb1c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdb1c-104">Syntax</span></span>  
  
```  
HRESULT AddImport(  
    mdAssembly      AssemblyID,  
    mdToken         ImportToken,  
    DWORD           dwFlags,  
    mdFile*         pFileToken  
) PURE;  
```  
  
## <a name="parameters"></a><span data-ttu-id="cdb1c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdb1c-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="cdb1c-106">ID unique de l’assembly à augmenter.</span><span class="sxs-lookup"><span data-stu-id="cdb1c-106">Unique ID of assembly to be augmented.</span></span>  
  
 `ImportToken`  
 <span data-ttu-id="cdb1c-107">ID unique récupéré à partir de [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md), du fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="cdb1c-107">Unique ID, retrieved from [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md), of file to be imported.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="cdb1c-108">Indicateurs de COM + FileDef tels que `ffContainsNoMetaData` et `ffWriteable`.</span><span class="sxs-lookup"><span data-stu-id="cdb1c-108">COM+ FileDef flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="cdb1c-109">`dwFlags` est passé à [DefineFile, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="cdb1c-109">`dwFlags` is passed to [DefineFile Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="cdb1c-110">Pointeur vers le jeton qui reçoit l’ID pour le fichier résultant.</span><span class="sxs-lookup"><span data-stu-id="cdb1c-110">Pointer to token that receives the ID for the resulting file.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cdb1c-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cdb1c-111">Return Value</span></span>  
 <span data-ttu-id="cdb1c-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="cdb1c-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cdb1c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdb1c-113">Requirements</span></span>  
 <span data-ttu-id="cdb1c-114">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="cdb1c-114">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdb1c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdb1c-115">See also</span></span>

- [<span data-ttu-id="cdb1c-116">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="cdb1c-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="cdb1c-117">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="cdb1c-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="cdb1c-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="cdb1c-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
