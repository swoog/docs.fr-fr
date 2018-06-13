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
ms.openlocfilehash: 401c23e44cc473d0a27a82a00343852693cb0f2e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429343"
---
# <a name="idefinitionidentity-interface"></a><span data-ttu-id="43217-102">IDefinitionIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="43217-102">IDefinitionIdentity Interface</span></span>
<span data-ttu-id="43217-103">Représente la signature unique du code qui définit l’application dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="43217-103">Represents the unique signature of the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="43217-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="43217-104">Methods</span></span>  
  
|<span data-ttu-id="43217-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="43217-105">Method</span></span>|<span data-ttu-id="43217-106">Description</span><span class="sxs-lookup"><span data-stu-id="43217-106">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionIdentity::Clone`|<span data-ttu-id="43217-107">Obtient un pointeur d’interface vers un nouveau `IDefinitionIdentity` objet qui est identique à ce `IDefinitionIdentity`, à l’exception des modifications d’attribut spécifiées.</span><span class="sxs-lookup"><span data-stu-id="43217-107">Gets an interface pointer to a new `IDefinitionIdentity` object that is identical to this `IDefinitionIdentity`, except for the specified attribute changes.</span></span>|  
|`IDefinitionIdentity::EnumAttributes`|<span data-ttu-id="43217-108">Obtient un pointeur d’interface vers un [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) objet qui contient les attributs associés à ce `IDefinitionIdentity`.</span><span class="sxs-lookup"><span data-stu-id="43217-108">Gets an interface pointer to an [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) object that contains the attributes associated with this `IDefinitionIdentity`.</span></span>|  
|`IDefinitionIdentity::GetAttribute`|<span data-ttu-id="43217-109">Obtient la valeur de l’attribut avec le nom spécifié dans l’espace de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="43217-109">Gets the value of the attribute with the specified name in the specified namespace.</span></span>|  
|`IDefinitionIdentity::SetAttribute`|<span data-ttu-id="43217-110">Définit l’attribut qui porte le nom spécifié dans l’espace de noms spécifié à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="43217-110">Sets the attribute that has the specified name in the specified namespace to the specified value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="43217-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="43217-111">Requirements</span></span>  
 <span data-ttu-id="43217-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="43217-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43217-113">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="43217-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="43217-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43217-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43217-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43217-115">See Also</span></span>  
 [<span data-ttu-id="43217-116">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="43217-116">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
