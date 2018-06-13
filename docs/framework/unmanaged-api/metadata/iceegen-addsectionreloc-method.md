---
title: ICeeGen::AddSectionReloc, méthode
ms.date: 03/30/2017
api_name:
- ICeeGen.AddSectionReloc
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::AddSectionReloc
helpviewer_keywords:
- AddSectionReloc method [.NET Framework metadata]
- ICeeGen::AddSectionReloc method [.NET Framework metadata]
ms.assetid: b500a260-1d57-4953-95e1-c27063f7c8da
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c281d03c6e3774938cfa6e4b4b3a541738b38489
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444341"
---
# <a name="iceegenaddsectionreloc-method"></a><span data-ttu-id="51aff-102">ICeeGen::AddSectionReloc, méthode</span><span class="sxs-lookup"><span data-stu-id="51aff-102">ICeeGen::AddSectionReloc Method</span></span>
<span data-ttu-id="51aff-103">Ajoute une instruction .reloc au code base.</span><span class="sxs-lookup"><span data-stu-id="51aff-103">Adds a .reloc instruction to the code base.</span></span>  
  
 <span data-ttu-id="51aff-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="51aff-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="51aff-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51aff-105">Syntax</span></span>  
  
```  
HRESULT AddSectionReloc (  
   [in] HCEESECTION            section,  
   [in] ULONG                  offset,  
   [in] HCEESECTION            relativeTo,   
   [in] CeeSectionRelocType    relocType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="51aff-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51aff-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="51aff-107">[in] La section de code en mémoire à laquelle ajouter une instruction .reloc.</span><span class="sxs-lookup"><span data-stu-id="51aff-107">[in] The section of in-memory code to which to add a .reloc instruction.</span></span>  
  
 `offset`  
 <span data-ttu-id="51aff-108">[in] Le décalage de la section.</span><span class="sxs-lookup"><span data-stu-id="51aff-108">[in] The offset of the section.</span></span>  
  
 `relativeTo`  
 <span data-ttu-id="51aff-109">[in] La section à laquelle `offset` fait référence.</span><span class="sxs-lookup"><span data-stu-id="51aff-109">[in] The section to which `offset` refers.</span></span>  
  
 `relocType`  
 <span data-ttu-id="51aff-110">[in] Parmi les [CeeSectionRelocType](../../../../docs/framework/unmanaged-api/metadata/ceesectionreloctype-enumeration.md) valeurs indiquant le genre d’instruction .reloc à ajouter.</span><span class="sxs-lookup"><span data-stu-id="51aff-110">[in] One of the [CeeSectionRelocType](../../../../docs/framework/unmanaged-api/metadata/ceesectionreloctype-enumeration.md) values, indicating the kind of .reloc instruction to add.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="51aff-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="51aff-111">Requirements</span></span>  
 <span data-ttu-id="51aff-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="51aff-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="51aff-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="51aff-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="51aff-114">**Bibliothèque :** utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="51aff-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="51aff-115">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="51aff-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51aff-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51aff-116">See Also</span></span>  
 [<span data-ttu-id="51aff-117">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="51aff-117">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
