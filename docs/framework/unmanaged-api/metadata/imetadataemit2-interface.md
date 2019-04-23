---
title: IMetaDataEmit2, interface
ms.date: 03/30/2017
api_name:
- IMetaDataEmit2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit2
helpviewer_keywords:
- IMetaDataEmit2 interface [.NET Framework metadata]
ms.assetid: 866dc96b-bbfc-4c0f-80c2-38ce93072106
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 87b5b60d75d5d28e100ec75192d0cacf51765927
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59200192"
---
# <a name="imetadataemit2-interface"></a><span data-ttu-id="c0297-102">IMetaDataEmit2, interface</span><span class="sxs-lookup"><span data-stu-id="c0297-102">IMetaDataEmit2 Interface</span></span>
<span data-ttu-id="c0297-103">Étend la [IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface principalement pour fournir la capacité de travailler avec les types génériques.</span><span class="sxs-lookup"><span data-stu-id="c0297-103">Extends the [IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md) interface primarily to provide the ability to work with generic types.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c0297-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0297-104">Methods</span></span>  
  
|<span data-ttu-id="c0297-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-105">Method</span></span>|<span data-ttu-id="c0297-106">Description</span><span class="sxs-lookup"><span data-stu-id="c0297-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c0297-107">DefineGenericParam, méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-107">DefineGenericParam Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definegenericparam-method.md)|<span data-ttu-id="c0297-108">Crée une définition pour un paramètre de type générique et obtient un jeton pour ce paramètre de type générique.</span><span class="sxs-lookup"><span data-stu-id="c0297-108">Creates a definition for a generic type parameter, and gets a token to that generic type parameter.</span></span>|  
|[<span data-ttu-id="c0297-109">DefineMethodSpec, méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-109">DefineMethodSpec Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-definemethodspec-method.md)|<span data-ttu-id="c0297-110">Crée une instance d’une méthode générique et obtient un jeton pour la définition.</span><span class="sxs-lookup"><span data-stu-id="c0297-110">Creates a generic instance of a method, and gets a token to the definition.</span></span>|  
|[<span data-ttu-id="c0297-111">GetDeltaSaveSize, méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-111">GetDeltaSaveSize Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-getdeltasavesize-method.md)|<span data-ttu-id="c0297-112">Obtient une valeur qui indique la différence de taille des données qui sont requis pour exprimer les modifications pour la session active modifier et continuer.</span><span class="sxs-lookup"><span data-stu-id="c0297-112">Gets a value indicating the difference in size of the data that is required to express the changes for the current edit-and-continue session.</span></span>|  
|[<span data-ttu-id="c0297-113">ResetENCLog, méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-113">ResetENCLog Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-resetenclog-method.md)|<span data-ttu-id="c0297-114">Réinitialise le journal modifier et continuer et démarre une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="c0297-114">Resets the edit-and-continue log and starts a new session.</span></span>|  
|[<span data-ttu-id="c0297-115">SaveDelta, méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-115">SaveDelta Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedelta-method.md)|<span data-ttu-id="c0297-116">Enregistre les modifications de la session active modifier et continuer dans le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0297-116">Saves changes from the current edit-and-continue session to the specified file.</span></span>|  
|[<span data-ttu-id="c0297-117">SaveDeltaToMemory, méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-117">SaveDeltaToMemory Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedeltatomemory-method.md)|<span data-ttu-id="c0297-118">Enregistre les modifications de la session active modifier et continuer à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c0297-118">Saves changes from the current edit-and-continue session to memory.</span></span>|  
|[<span data-ttu-id="c0297-119">SaveDeltaToStream, méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-119">SaveDeltaToStream Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-savedeltatostream-method.md)|<span data-ttu-id="c0297-120">Enregistre les modifications de la session active modifier et continuer dans le flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0297-120">Saves changes from the current edit-and-continue session to the specified stream.</span></span>|  
|[<span data-ttu-id="c0297-121">SetGenericParamProps, méthode</span><span class="sxs-lookup"><span data-stu-id="c0297-121">SetGenericParamProps Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-setgenericparamprops-method.md)|<span data-ttu-id="c0297-122">Définit les valeurs de propriété pour la définition de paramètre générique référencé par le jeton spécifié.</span><span class="sxs-lookup"><span data-stu-id="c0297-122">Sets property values for the generic parameter definition referenced by the specified token.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c0297-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0297-123">Requirements</span></span>  
 <span data-ttu-id="c0297-124">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c0297-124">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c0297-125">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="c0297-125">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c0297-126">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c0297-126">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c0297-127">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c0297-127">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0297-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0297-128">See also</span></span>

- [<span data-ttu-id="c0297-129">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="c0297-129">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
- [<span data-ttu-id="c0297-130">IMetaDataEmit, interface</span><span class="sxs-lookup"><span data-stu-id="c0297-130">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
