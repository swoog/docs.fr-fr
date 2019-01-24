---
title: IMetaDataFilter, interface
ms.date: 03/30/2017
api_name:
- IMetaDataFilter
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataFilter
helpviewer_keywords:
- IMetaDataFilter interface [.NET Framework metadata]
ms.assetid: ec0856ef-8c56-40ba-bf60-86e0ce8b337f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 0e1975a5063217299ddbcdce6f625d5a1285d5b4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642553"
---
# <a name="imetadatafilter-interface"></a><span data-ttu-id="830fc-102">IMetaDataFilter, interface</span><span class="sxs-lookup"><span data-stu-id="830fc-102">IMetaDataFilter Interface</span></span>
<span data-ttu-id="830fc-103">Fournit des méthodes pour marquer et filtrer des jetons de métadonnées pour éviter de répéter des actions qui ont déjà été prises.</span><span class="sxs-lookup"><span data-stu-id="830fc-103">Provides methods for marking and filtering metadata tokens to avoid repeating actions that have already been taken.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="830fc-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="830fc-104">Methods</span></span>  
  
|<span data-ttu-id="830fc-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="830fc-105">Method</span></span>|<span data-ttu-id="830fc-106">Description</span><span class="sxs-lookup"><span data-stu-id="830fc-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="830fc-107">IsTokenMarked, méthode</span><span class="sxs-lookup"><span data-stu-id="830fc-107">IsTokenMarked Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-istokenmarked-method.md)|<span data-ttu-id="830fc-108">Obtient une valeur indiquant si le jeton de métadonnées spécifié a été traité.</span><span class="sxs-lookup"><span data-stu-id="830fc-108">Gets a value indicating whether the specified metadata token has been processed.</span></span>|  
|[<span data-ttu-id="830fc-109">MarkToken, méthode</span><span class="sxs-lookup"><span data-stu-id="830fc-109">MarkToken Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-marktoken-method.md)|<span data-ttu-id="830fc-110">Définit une valeur qui indique que le jeton de métadonnées spécifié a été traité.</span><span class="sxs-lookup"><span data-stu-id="830fc-110">Sets a value indicating that the specified metadata token has been processed.</span></span>|  
|[<span data-ttu-id="830fc-111">UnmarkAll, méthode</span><span class="sxs-lookup"><span data-stu-id="830fc-111">UnmarkAll Method</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-unmarkall-method.md)|<span data-ttu-id="830fc-112">Supprime les marques de traitement de tous les jetons dans la portée de métadonnées actuelle.</span><span class="sxs-lookup"><span data-stu-id="830fc-112">Removes the processing marks from all the tokens in the current metadata scope.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="830fc-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="830fc-113">Requirements</span></span>  
 <span data-ttu-id="830fc-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="830fc-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="830fc-115">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="830fc-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="830fc-116">**Bibliothèque :** Utilisé en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="830fc-116">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="830fc-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="830fc-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="830fc-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="830fc-118">See also</span></span>
- [<span data-ttu-id="830fc-119">Interfaces de métadonnées</span><span class="sxs-lookup"><span data-stu-id="830fc-119">Metadata Interfaces</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-interfaces.md)
