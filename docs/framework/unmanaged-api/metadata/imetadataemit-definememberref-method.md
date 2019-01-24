---
title: IMetaDataEmit::DefineMemberRef, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineMemberRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineMemberRef
helpviewer_keywords:
- DefineMemberRef method [.NET Framework metadata]
- IMetaDataEmit::DefineMemberRef method [.NET Framework metadata]
ms.assetid: 21b5bcb8-ea75-4962-8acc-ad17584061e5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 578f79136f6ccc8a6b7eac644b2a5084d30d2ba0
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722827"
---
# <a name="imetadataemitdefinememberref-method"></a><span data-ttu-id="cfe83-102">IMetaDataEmit::DefineMemberRef, méthode</span><span class="sxs-lookup"><span data-stu-id="cfe83-102">IMetaDataEmit::DefineMemberRef Method</span></span>
<span data-ttu-id="cfe83-103">Définit une référence à un membre d’un module en dehors de la portée actuelle et obtient un jeton pour cette définition de référence.</span><span class="sxs-lookup"><span data-stu-id="cfe83-103">Defines a reference to a member of a module outside the current scope, and gets a token to that reference definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cfe83-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfe83-104">Syntax</span></span>  
  
```  
HRESULT DefineMemberRef (   
    [in]  mdToken           tkImport,   
    [in]  LPCWSTR           szName,   
    [in]  PCCOR_SIGNATURE   pvSigBlob,   
    [in]  ULONG             cbSigBlob,   
    [out] mdMemberRef       *pmr   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cfe83-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfe83-105">Parameters</span></span>  
 `tkImport`  
 <span data-ttu-id="cfe83-106">[in] Jeton pour la classe ou une interface, le membre cible si le membre n’est pas global ; Si le membre est global, le `mdModuleRef` jeton pour cet autre fichier.</span><span class="sxs-lookup"><span data-stu-id="cfe83-106">[in] Token for the target member's class or interface, if the member is not global; if the member is global, the `mdModuleRef` token for that other file.</span></span>  
  
 `szName`  
 <span data-ttu-id="cfe83-107">[in] Le nom du membre cible.</span><span class="sxs-lookup"><span data-stu-id="cfe83-107">[in] The name of the target member.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="cfe83-108">[in] La signature du membre cible.</span><span class="sxs-lookup"><span data-stu-id="cfe83-108">[in] The signature of the target member.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="cfe83-109">[in] Le nombre d’octets dans `pvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="cfe83-109">[in] The count of bytes in `pvSigBlob`.</span></span>  
  
 `pmr`  
 <span data-ttu-id="cfe83-110">[out] Le `mdMemberRef` jeton attribué.</span><span class="sxs-lookup"><span data-stu-id="cfe83-110">[out] The `mdMemberRef` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cfe83-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cfe83-111">Requirements</span></span>  
 <span data-ttu-id="cfe83-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cfe83-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cfe83-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="cfe83-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="cfe83-114">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cfe83-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cfe83-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cfe83-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfe83-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfe83-116">See also</span></span>
- [<span data-ttu-id="cfe83-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="cfe83-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="cfe83-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="cfe83-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
