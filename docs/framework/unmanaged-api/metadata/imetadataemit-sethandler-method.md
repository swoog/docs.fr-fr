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
ms.openlocfilehash: ac0e5db4a87b49d631bad4411f03fae8c1199aea
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59125630"
---
# <a name="imetadataemitsethandler-method"></a><span data-ttu-id="464c1-102">IMetaDataEmit::SetHandler, méthode</span><span class="sxs-lookup"><span data-stu-id="464c1-102">IMetaDataEmit::SetHandler Method</span></span>
<span data-ttu-id="464c1-103">Définit la méthode référencée par le `IUnknown` pointeur comme un rappel de notification pour remappages du jeton.</span><span class="sxs-lookup"><span data-stu-id="464c1-103">Sets the method referenced by the specified `IUnknown` pointer as a notification callback for token remaps.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="464c1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="464c1-104">Syntax</span></span>  
  
```  
HRESULT SetHandler (   
    [in]  IUnknown    *pUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="464c1-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="464c1-105">Parameters</span></span>  
 `pUnk`  
 <span data-ttu-id="464c1-106">[in] Gestionnaire à inscrire.</span><span class="sxs-lookup"><span data-stu-id="464c1-106">[in] The handler to register.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="464c1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="464c1-107">Remarks</span></span>  
 <span data-ttu-id="464c1-108">Le moteur de métadonnées envoie la notification à l’aide de la méthode qui est fournie par `SetHandler`, pour les compilateurs qui ne génèrent pas d’enregistrements de manière optimisée et qui souhaitent optimiser les enregistrements sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="464c1-108">The metadata engine sends notification by using the method that is provided by `SetHandler`, to compilers that do not generate records in an optimized way and that would like to optimize saved records.</span></span>  
  
 <span data-ttu-id="464c1-109">Si la méthode de rappel n’est pas fournie via `SetHandler`, aucune optimisation ne sera effectuée sur Enregistrer, à l’exception où plusieurs importent étendues ont été fusionnées à l’aide de `IMapToken` sur la fusion pour chaque étendue.</span><span class="sxs-lookup"><span data-stu-id="464c1-109">If the callback method is not provided through `SetHandler`, no optimization will be performed on save except where several import scopes have been merged using `IMapToken` on merge for each scope.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="464c1-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="464c1-110">Requirements</span></span>  
 <span data-ttu-id="464c1-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="464c1-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="464c1-112">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="464c1-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="464c1-113">**Bibliothèque :** Utilisé en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="464c1-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 **<span data-ttu-id="464c1-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="464c1-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="464c1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="464c1-115">See also</span></span>

- [<span data-ttu-id="464c1-116">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="464c1-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [<span data-ttu-id="464c1-117">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="464c1-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
