---
title: IEnumReferenceIdentity, interface
ms.date: 03/30/2017
api_name:
- IEnumReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumReferenceIdentity
helpviewer_keywords:
- IEnumReferenceIdentity interface [.NET Framework fusion]
ms.assetid: a17b3155-7216-4e16-8c9f-abce21f549e7
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 766b17bae0c58d9872ff9c118f330ebc3220257e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59123485"
---
# <a name="ienumreferenceidentity-interface"></a><span data-ttu-id="24391-102">IEnumReferenceIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="24391-102">IEnumReferenceIdentity Interface</span></span>
<span data-ttu-id="24391-103">Sert d’énumérateur pour une collection de `IReferenceIdentity` objets.</span><span class="sxs-lookup"><span data-stu-id="24391-103">Serves as an enumerator for a collection of `IReferenceIdentity` objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="24391-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="24391-104">Methods</span></span>  
  
|<span data-ttu-id="24391-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="24391-105">Method</span></span>|<span data-ttu-id="24391-106">Description</span><span class="sxs-lookup"><span data-stu-id="24391-106">Description</span></span>|  
|------------|-----------------|  
|`IEnumReferenceIdentity::Clone`|<span data-ttu-id="24391-107">Obtient un pointeur d’interface vers un nouveau `IEnumReferenceIdentity` qui contient les mêmes membres que cela `IEnumReferenceIdentity`.</span><span class="sxs-lookup"><span data-stu-id="24391-107">Gets an interface pointer to a new `IEnumReferenceIdentity` that contains the same members as this `IEnumReferenceIdentity`.</span></span>|  
|`IEnumReferenceIdentity::Next`|<span data-ttu-id="24391-108">Obtient le nombre spécifié de `IReferenceIdentity` objets, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="24391-108">Gets the specified number of `IReferenceIdentity` objects, starting at the current position.</span></span>|  
|`IEnumReferenceIdentity::Reset`|<span data-ttu-id="24391-109">Déplace le pointeur d’instruction au début de ce `IEnumReferenceIdentity`.</span><span class="sxs-lookup"><span data-stu-id="24391-109">Moves the instruction pointer to the beginning of this `IEnumReferenceIdentity`.</span></span>|  
|`IEnumReferenceIdentity::Skip`|<span data-ttu-id="24391-110">Déplace le pointeur d’instruction par le nombre spécifié d’éléments, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="24391-110">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="24391-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24391-111">Requirements</span></span>  
 <span data-ttu-id="24391-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="24391-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24391-113">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="24391-113">**Header:** Isolation.h</span></span>  
  
 **<span data-ttu-id="24391-114">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="24391-114">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="24391-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24391-115">See also</span></span>

- [<span data-ttu-id="24391-116">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="24391-116">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="24391-117">IReferenceIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="24391-117">IReferenceIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/ireferenceidentity-interface.md)
