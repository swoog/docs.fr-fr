---
title: IMetaDataEmit::SetHandler, méthode
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetHandler
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetHandler
helpviewer_keywords:
- IMetaDataEmit::SetHandler method [.NET Framework metadata]
- SetHandler method [.NET Framework metadata]
ms.assetid: c6c1aaaf-e2cd-407c-b73e-fbe6ffd83bb3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 60c9266806ef6b5d7e2e1c3a219a4485bc22d7f3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445518"
---
# <a name="imetadataemitsethandler-method"></a><span data-ttu-id="22d55-102">IMetaDataEmit::SetHandler, méthode</span><span class="sxs-lookup"><span data-stu-id="22d55-102">IMetaDataEmit::SetHandler Method</span></span>
<span data-ttu-id="22d55-103">Définit la méthode référencée par le `IUnknown` pointeur en tant que notification de rappel pour le jeton remappe.</span><span class="sxs-lookup"><span data-stu-id="22d55-103">Sets the method referenced by the specified `IUnknown` pointer as a notification callback for token remaps.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22d55-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22d55-104">Syntax</span></span>  
  
```  
HRESULT SetHandler (   
    [in]  IUnknown    *pUnk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="22d55-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22d55-105">Parameters</span></span>  
 `pUnk`  
 <span data-ttu-id="22d55-106">[in] Le Gestionnaire d’inscription.</span><span class="sxs-lookup"><span data-stu-id="22d55-106">[in] The handler to register.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="22d55-107">Notes</span><span class="sxs-lookup"><span data-stu-id="22d55-107">Remarks</span></span>  
 <span data-ttu-id="22d55-108">Le moteur de métadonnées envoie la notification à l’aide de la méthode est fournie par `SetHandler`, pour les compilateurs qui ne génèrent pas d’enregistrements de manière optimisée et qui souhaitent optimiser les enregistrements sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="22d55-108">The metadata engine sends notification by using the method that is provided by `SetHandler`, to compilers that do not generate records in an optimized way and that would like to optimize saved records.</span></span>  
  
 <span data-ttu-id="22d55-109">Si la méthode de rappel n’est pas fournie via `SetHandler`, aucune optimisation ne se fera sur Enregistrer, sauf dans lequel importent les plusieurs étendues ont été fusionnées à l’aide de `IMapToken` de fusion pour chaque étendue.</span><span class="sxs-lookup"><span data-stu-id="22d55-109">If the callback method is not provided through `SetHandler`, no optimization will be performed on save except where several import scopes have been merged using `IMapToken` on merge for each scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22d55-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="22d55-110">Requirements</span></span>  
 <span data-ttu-id="22d55-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="22d55-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22d55-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="22d55-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="22d55-113">**Bibliothèque :** utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="22d55-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="22d55-114">**Versions du .NET framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22d55-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22d55-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22d55-115">See Also</span></span>  
 [<span data-ttu-id="22d55-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="22d55-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="22d55-117">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="22d55-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
