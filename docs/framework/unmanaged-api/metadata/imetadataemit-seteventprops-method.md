---
title: IMetaDataEmit::SetEventProps, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetEventProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetEventProps
helpviewer_keywords:
- IMetaDataEmit::SetEventProps method [.NET Framework metadata]
- SetEventProps method [.NET Framework metadata]
ms.assetid: 3b039e50-63ec-4730-99ff-2327408de477
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 42dc78ff3c58b67801cd99512781d8c8509dd272
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447338"
---
# <a name="imetadataemitseteventprops-method"></a><span data-ttu-id="4bc91-102">IMetaDataEmit::SetEventProps, méthode</span><span class="sxs-lookup"><span data-stu-id="4bc91-102">IMetaDataEmit::SetEventProps Method</span></span>
<span data-ttu-id="4bc91-103">Définit ou met à jour la fonctionnalité spécifiée d’un événement défini par un appel antérieur à [IMetaDataEmit::DefineEvent](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineevent-method.md).</span><span class="sxs-lookup"><span data-stu-id="4bc91-103">Sets or updates the specified feature of an event defined by a prior call to [IMetaDataEmit::DefineEvent](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineevent-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4bc91-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bc91-104">Syntax</span></span>  
  
```  
HRESULT SetEventProps (  
    [in]  mdEvent     ev,   
    [in]  DWORD       dwEventFlags,   
    [in]  mdToken     tkEventType,   
    [in]  mdMethodDef mdAddOn,   
    [in]  mdMethodDef mdRemoveOn,   
    [in]  mdMethodDef mdFire,   
    [in]  mdMethodDef rmdOtherMethods[]   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4bc91-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4bc91-105">Parameters</span></span>  
 `ev`  
 <span data-ttu-id="4bc91-106">[in] Le jeton d’événement.</span><span class="sxs-lookup"><span data-stu-id="4bc91-106">[in] The event token.</span></span>  
  
 `dwEventFlags`  
 <span data-ttu-id="4bc91-107">[in] Indicateurs d’événement.</span><span class="sxs-lookup"><span data-stu-id="4bc91-107">[in] Event flags.</span></span> <span data-ttu-id="4bc91-108">Il s’agit d’un masque de bits de `CorEventAttr` valeurs.</span><span class="sxs-lookup"><span data-stu-id="4bc91-108">This is a bitmask of `CorEventAttr` values.</span></span>  
  
 `tkEventType`  
 <span data-ttu-id="4bc91-109">[in] Le jeton pour la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="4bc91-109">[in] The token for the event class.</span></span> <span data-ttu-id="4bc91-110">Il s’agit soit un `mdTypeDef` ou un `mdTypeRef` jeton.</span><span class="sxs-lookup"><span data-stu-id="4bc91-110">This is either a `mdTypeDef` or a `mdTypeRef` token.</span></span>  
  
 `mdAddOn`  
 <span data-ttu-id="4bc91-111">[in] La méthode utilisée pour s’abonner à l’événement, ou null.</span><span class="sxs-lookup"><span data-stu-id="4bc91-111">[in] The method used to subscribe to the event, or null.</span></span>  
  
 `mdRemoveOn`  
 <span data-ttu-id="4bc91-112">[in] La méthode utilisée pour annuler l’abonnement à l’événement, ou null.</span><span class="sxs-lookup"><span data-stu-id="4bc91-112">[in] The method used to unsubscribe to the event, or null.</span></span>  
  
 `mdFire`  
 <span data-ttu-id="4bc91-113">[in] La méthode utilisée (par une classe dérivée) pour déclencher l’événement.</span><span class="sxs-lookup"><span data-stu-id="4bc91-113">[in] The method used (by a derived class) to raise the event.</span></span>  
  
 `rmdOtherMethods[]`  
 <span data-ttu-id="4bc91-114">[in] Tableau de jetons pour les autres méthodes associées à l’événement.</span><span class="sxs-lookup"><span data-stu-id="4bc91-114">[in] An array of tokens for other methods associated with the event.</span></span> <span data-ttu-id="4bc91-115">Le dernier élément du tableau doit être `mdMethodDefNil`.</span><span class="sxs-lookup"><span data-stu-id="4bc91-115">The last element of the array must be `mdMethodDefNil`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4bc91-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4bc91-116">Requirements</span></span>  
 <span data-ttu-id="4bc91-117">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4bc91-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4bc91-118">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="4bc91-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4bc91-119">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4bc91-119">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4bc91-120">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4bc91-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4bc91-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bc91-121">See Also</span></span>  
 [<span data-ttu-id="4bc91-122">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="4bc91-122">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="4bc91-123">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="4bc91-123">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
