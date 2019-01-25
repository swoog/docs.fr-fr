---
title: IDefinitionIdentity, interface
ms.date: 03/30/2017
api_name:
- IDefinitionIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDefinitionIdentity
helpviewer_keywords:
- IDefinitionIdentity interface [.NET Framework fusion]
ms.assetid: ce5ba888-5fbe-4efd-91cf-f0ff94d8428b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: fb97c545d2d57ef589b5a7a5b3618eaa2b6f364f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54686996"
---
# <a name="idefinitionidentity-interface"></a><span data-ttu-id="c1930-102">IDefinitionIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="c1930-102">IDefinitionIdentity Interface</span></span>
<span data-ttu-id="c1930-103">Représente la signature unique du code qui définit l’application dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="c1930-103">Represents the unique signature of the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c1930-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c1930-104">Methods</span></span>  
  
|<span data-ttu-id="c1930-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="c1930-105">Method</span></span>|<span data-ttu-id="c1930-106">Description</span><span class="sxs-lookup"><span data-stu-id="c1930-106">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionIdentity::Clone`|<span data-ttu-id="c1930-107">Obtient un pointeur d’interface vers un nouveau `IDefinitionIdentity` objet qui est identique à ce `IDefinitionIdentity`, sauf pour les modifications de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1930-107">Gets an interface pointer to a new `IDefinitionIdentity` object that is identical to this `IDefinitionIdentity`, except for the specified attribute changes.</span></span>|  
|`IDefinitionIdentity::EnumAttributes`|<span data-ttu-id="c1930-108">Obtient un pointeur d’interface vers un [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) objet qui contient les attributs associés à ce `IDefinitionIdentity`.</span><span class="sxs-lookup"><span data-stu-id="c1930-108">Gets an interface pointer to an [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) object that contains the attributes associated with this `IDefinitionIdentity`.</span></span>|  
|`IDefinitionIdentity::GetAttribute`|<span data-ttu-id="c1930-109">Obtient la valeur de l’attribut avec le nom spécifié dans l’espace de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="c1930-109">Gets the value of the attribute with the specified name in the specified namespace.</span></span>|  
|`IDefinitionIdentity::SetAttribute`|<span data-ttu-id="c1930-110">Définit l’attribut ayant le nom spécifié dans l’espace de noms spécifié à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c1930-110">Sets the attribute that has the specified name in the specified namespace to the specified value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c1930-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c1930-111">Requirements</span></span>  
 <span data-ttu-id="c1930-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c1930-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c1930-113">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="c1930-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="c1930-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c1930-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1930-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1930-115">See also</span></span>
- [<span data-ttu-id="c1930-116">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="c1930-116">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
