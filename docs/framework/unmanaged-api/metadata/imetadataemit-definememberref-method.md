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
ms.openlocfilehash: ad2b3e5c452a5fc79e7a1cc0342cfc1d119a5fbd
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57481987"
---
# <a name="imetadataemitdefinememberref-method"></a><span data-ttu-id="df2da-102">IMetaDataEmit::DefineMemberRef, méthode</span><span class="sxs-lookup"><span data-stu-id="df2da-102">IMetaDataEmit::DefineMemberRef Method</span></span>
<span data-ttu-id="df2da-103">Définit une référence à un membre d’un module en dehors de la portée actuelle et obtient un jeton pour cette définition de référence.</span><span class="sxs-lookup"><span data-stu-id="df2da-103">Defines a reference to a member of a module outside the current scope, and gets a token to that reference definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df2da-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df2da-104">Syntax</span></span>  
  
```  
HRESULT DefineMemberRef (   
    [in]  mdToken           tkImport,   
    [in]  LPCWSTR           szName,   
    [in]  PCCOR_SIGNATURE   pvSigBlob,   
    [in]  ULONG             cbSigBlob,   
    [out] mdMemberRef       *pmr   
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="df2da-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df2da-105">Parameters</span></span>  
 `tkImport`  
 <span data-ttu-id="df2da-106">[in] Jeton pour la classe ou une interface, le membre cible si le membre n’est pas global ; Si le membre est global, le `mdModuleRef` jeton pour cet autre fichier.</span><span class="sxs-lookup"><span data-stu-id="df2da-106">[in] Token for the target member's class or interface, if the member is not global; if the member is global, the `mdModuleRef` token for that other file.</span></span>  
  
 `szName`  
 <span data-ttu-id="df2da-107">[in] Le nom du membre cible.</span><span class="sxs-lookup"><span data-stu-id="df2da-107">[in] The name of the target member.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="df2da-108">[in] La signature du membre cible.</span><span class="sxs-lookup"><span data-stu-id="df2da-108">[in] The signature of the target member.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="df2da-109">[in] Le nombre d’octets dans `pvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="df2da-109">[in] The count of bytes in `pvSigBlob`.</span></span>  
  
 `pmr`  
 <span data-ttu-id="df2da-110">[out] Le `mdMemberRef` jeton attribué.</span><span class="sxs-lookup"><span data-stu-id="df2da-110">[out] The `mdMemberRef` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df2da-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="df2da-111">Requirements</span></span>  
 <span data-ttu-id="df2da-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="df2da-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df2da-113">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="df2da-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="df2da-114">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="df2da-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="df2da-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df2da-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df2da-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df2da-116">See also</span></span>
- [<span data-ttu-id="df2da-117">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="df2da-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="df2da-118">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="df2da-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
