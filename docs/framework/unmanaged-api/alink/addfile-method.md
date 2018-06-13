---
title: AddFile Method1
ms.date: 03/30/2017
api_name:
- IALink.AddFile
- AddFile
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AddFile
helpviewer_keywords:
- AddFile method
ms.assetid: 9e707abb-f905-4568-9356-12aa21d1b11c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 57a350fadfa77fdad545ca7ccf2f63d28607c2ba
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33403918"
---
# <a name="addfile-method1"></a><span data-ttu-id="99706-102">AddFile Method1</span><span class="sxs-lookup"><span data-stu-id="99706-102">AddFile Method1</span></span>
<span data-ttu-id="99706-103">Ajoute des fichiers à l’assembly.</span><span class="sxs-lookup"><span data-stu-id="99706-103">Adds files to the assembly.</span></span> <span data-ttu-id="99706-104">Peut également être utilisé pour créer des modules indépendants.</span><span class="sxs-lookup"><span data-stu-id="99706-104">Can also be used to create unbound modules.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="99706-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99706-105">Syntax</span></span>  
  
```  
HRESULT AddFile(  
    mdAssembly      AssemblyID,  
    LPCWSTR         pszFilename,  
    DWORD           dwFlags,  
    IMetaDataEmit*  pEmitter,  
    mdFile*         pFileToken  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="99706-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99706-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="99706-107">ID unique de l’assembly à augmenter.</span><span class="sxs-lookup"><span data-stu-id="99706-107">Unique ID of the assembly to be augmented.</span></span>  
  
 `pszFilename`  
 <span data-ttu-id="99706-108">Nom qualifié complet du fichier à ajouter.</span><span class="sxs-lookup"><span data-stu-id="99706-108">Fully qualified name of file to be added.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="99706-109">Indicateurs de COM + FileDef tels que `ffContainsNoMetaData` et `ffWriteable`.</span><span class="sxs-lookup"><span data-stu-id="99706-109">COM+ FileDef flags such as `ffContainsNoMetaData` and `ffWriteable`.</span></span> <span data-ttu-id="99706-110">`dwFlags` est passé à [DefineFile, méthode](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span><span class="sxs-lookup"><span data-stu-id="99706-110">`dwFlags` is passed to [DefineFile Method](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-definefile-method.md).</span></span>  
  
 `pEmitter`  
 <span data-ttu-id="99706-111">[IMetaDataEmit (Interface)](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface à utiliser pour émettre des métadonnées, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="99706-111">[IMetaDataEmit Interface](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface to be used to emit metadata, if necessary.</span></span>  
  
 `pFileToken`  
 <span data-ttu-id="99706-112">Pointeur vers l’emplacement de stockage de l’ID unique du fichier ajouté.</span><span class="sxs-lookup"><span data-stu-id="99706-112">Pointer to where the unique ID of the added file will be stored.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="99706-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="99706-113">Return Value</span></span>  
 <span data-ttu-id="99706-114">Retourne S_OK si la méthode réussit.</span><span class="sxs-lookup"><span data-stu-id="99706-114">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="99706-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="99706-115">Requirements</span></span>  
 <span data-ttu-id="99706-116">Requiert alink.h.</span><span class="sxs-lookup"><span data-stu-id="99706-116">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99706-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99706-117">See Also</span></span>  
 [<span data-ttu-id="99706-118">IALink, interface</span><span class="sxs-lookup"><span data-stu-id="99706-118">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="99706-119">IALink2, interface</span><span class="sxs-lookup"><span data-stu-id="99706-119">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="99706-120">API ALink</span><span class="sxs-lookup"><span data-stu-id="99706-120">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
