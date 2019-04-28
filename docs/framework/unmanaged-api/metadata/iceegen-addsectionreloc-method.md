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
ms.openlocfilehash: 7d50f7488c2b231ea66c12cc4903469d9e2337fb
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61905643"
---
# <a name="iceegenaddsectionreloc-method"></a><span data-ttu-id="419d7-102">ICeeGen::AddSectionReloc, méthode</span><span class="sxs-lookup"><span data-stu-id="419d7-102">ICeeGen::AddSectionReloc Method</span></span>
<span data-ttu-id="419d7-103">Ajoute une instruction .reloc à la base de code.</span><span class="sxs-lookup"><span data-stu-id="419d7-103">Adds a .reloc instruction to the code base.</span></span>  
  
 <span data-ttu-id="419d7-104">Cette méthode est obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="419d7-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="419d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="419d7-105">Syntax</span></span>  
  
```  
HRESULT AddSectionReloc (  
   [in] HCEESECTION            section,  
   [in] ULONG                  offset,  
   [in] HCEESECTION            relativeTo,   
   [in] CeeSectionRelocType    relocType  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="419d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="419d7-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="419d7-107">[in] La section de code en mémoire à laquelle ajouter une instruction .reloc.</span><span class="sxs-lookup"><span data-stu-id="419d7-107">[in] The section of in-memory code to which to add a .reloc instruction.</span></span>  
  
 `offset`  
 <span data-ttu-id="419d7-108">[in] Le décalage de la section.</span><span class="sxs-lookup"><span data-stu-id="419d7-108">[in] The offset of the section.</span></span>  
  
 `relativeTo`  
 <span data-ttu-id="419d7-109">[in] La section à laquelle `offset` fait référence.</span><span class="sxs-lookup"><span data-stu-id="419d7-109">[in] The section to which `offset` refers.</span></span>  
  
 `relocType`  
 <span data-ttu-id="419d7-110">[in] Parmi les [CeeSectionRelocType](../../../../docs/framework/unmanaged-api/metadata/ceesectionreloctype-enumeration.md) valeurs indiquant le genre d’instruction .reloc à ajouter.</span><span class="sxs-lookup"><span data-stu-id="419d7-110">[in] One of the [CeeSectionRelocType](../../../../docs/framework/unmanaged-api/metadata/ceesectionreloctype-enumeration.md) values, indicating the kind of .reloc instruction to add.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="419d7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="419d7-111">Requirements</span></span>  
 <span data-ttu-id="419d7-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="419d7-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="419d7-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="419d7-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="419d7-114">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="419d7-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="419d7-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="419d7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="419d7-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="419d7-116">See also</span></span>

- [<span data-ttu-id="419d7-117">ICeeGen, interface</span><span class="sxs-lookup"><span data-stu-id="419d7-117">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
