---
title: IEnumIDENTITY_ATTRIBUTE, interface
ms.date: 03/30/2017
api_name:
- IEnumIDENTITY_ATTRIBUTE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumIDENTITY_ATTRIBUTE
helpviewer_keywords:
- IEnumIDENTITY_ATTRIBUTE interface [.NET Framework fusion]
ms.assetid: c2ec2748-e9ae-4e1b-80db-6fcec5cb81a1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d725228f2a7359d415673fdcb90d0cabae1a40be
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59175524"
---
# <a name="ienumidentityattribute-interface"></a><span data-ttu-id="020b5-102">IEnumIDENTITY_ATTRIBUTE, interface</span><span class="sxs-lookup"><span data-stu-id="020b5-102">IEnumIDENTITY_ATTRIBUTE Interface</span></span>
<span data-ttu-id="020b5-103">Sert d’énumérateur pour les attributs de l’objet de code dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="020b5-103">Serves as an enumerator for the attributes of the code object in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="020b5-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="020b5-104">Methods</span></span>  
  
|<span data-ttu-id="020b5-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="020b5-105">Method</span></span>|<span data-ttu-id="020b5-106">Description</span><span class="sxs-lookup"><span data-stu-id="020b5-106">Description</span></span>|  
|------------|-----------------|  
|`IEnumIDENTITY_ATTRIBUTE::Clone`|<span data-ttu-id="020b5-107">Obtient un pointeur d’interface vers un nouveau `IEnumIDENTITY_ATTRIBUTE` qui contient les mêmes membres que cela `IEnumIDENTITY_ATTRIBUTE`.</span><span class="sxs-lookup"><span data-stu-id="020b5-107">Gets an interface pointer to a new `IEnumIDENTITY_ATTRIBUTE` that contains the same members as this `IEnumIDENTITY_ATTRIBUTE`.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::CurrentIntoBuffer`|<span data-ttu-id="020b5-108">Écrit les données contenues dans les éléments de ce `IEnumIDENTITY_ATTRIBUTE` vers la mémoire tampon de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="020b5-108">Writes the data contained in the elements of this `IEnumIDENTITY_ATTRIBUTE` to the specified data buffer.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Next`|<span data-ttu-id="020b5-109">Obtient le nombre spécifié d’attributs, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="020b5-109">Gets the specified number of attributes, starting at the current position.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Reset`|<span data-ttu-id="020b5-110">Déplace le pointeur d’instruction au début de ce `IEnumIDENTITY_ATTRIBUTE`.</span><span class="sxs-lookup"><span data-stu-id="020b5-110">Moves the instruction pointer to the beginning of this `IEnumIDENTITY_ATTRIBUTE`.</span></span>|  
|`IEnumIDENTITY_ATTRIBUTE::Skip`|<span data-ttu-id="020b5-111">Déplace le pointeur d’instruction par le nombre spécifié d’éléments, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="020b5-111">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="020b5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="020b5-112">Requirements</span></span>  
 <span data-ttu-id="020b5-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="020b5-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="020b5-114">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="020b5-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="020b5-115">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="020b5-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="020b5-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="020b5-116">See also</span></span>

- [<span data-ttu-id="020b5-117">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="020b5-117">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
