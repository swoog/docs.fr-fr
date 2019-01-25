---
title: AddImport, Method1
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
ms.openlocfilehash: d2daed0450e04137621788e830bbedb467bd57c0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54706337"
---
# <a name="addimport-method1"></a><span data-ttu-id="57780-102">AddImport, Method1</span><span class="sxs-lookup"><span data-stu-id="57780-102">AddImport Method1</span></span>
<span data-ttu-id="57780-103">Ajoute des importations à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="57780-103">Adds imports to the assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57780-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57780-104">Syntax</span></span>  
  
```  
HRESULT AddImport(  
    mdAssembly      AssemblyID,  
    mdToken         ImportToken,  
    DWORD           dwFlags,  
    mdFile*         pFileToken  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="57780-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57780-105">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="57780-106">ID unique de l’assembly à augmenter.</span><span class="sxs-lookup"><span data-stu-id="57780-106">Unique ID of assembly to be augmented.</span></span>  
  
 `ImportToken`  
 <span data-ttu-id="57780-107">ID unique récupéré à partir de [ImportFile, méthode](../../../../docs/framework/unmanaged-api/alink/importfile-method.md), du fichier à importer.</span><span class="sxs-lookup"><span data-stu-id="57780-107">Unique ID, retrieved from [ImportFile Method](../../../../docs/framework/unmanaged-api/alink/importfile-method.md), of file to be imported.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="57780-108">Indicateurs de COM + FileDef tels que `ffContainsNoMetaData` et `ffWriteable`.</span><span class="sxs-lookup"><span data-stu-id="57780-108">COM+ FileDef flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="57780-109">`dwFlags` est passé à [DefineFile, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="57780-109">`dwFlags` is passed to [DefineFile Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="57780-110">Pointeur vers le jeton qui reçoit l’ID pour le fichier résultant.</span><span class="sxs-lookup"><span data-stu-id="57780-110">Pointer to token that receives the ID for the resulting file.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="57780-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="57780-111">Return Value</span></span>  
 <span data-ttu-id="57780-112">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="57780-112">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57780-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="57780-113">Requirements</span></span>  
 <span data-ttu-id="57780-114">Nécessite alink.h</span><span class="sxs-lookup"><span data-stu-id="57780-114">Requires alink.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57780-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57780-115">See also</span></span>
- [<span data-ttu-id="57780-116">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="57780-116">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)
- [<span data-ttu-id="57780-117">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="57780-117">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)
- [<span data-ttu-id="57780-118">API ALink</span><span class="sxs-lookup"><span data-stu-id="57780-118">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
