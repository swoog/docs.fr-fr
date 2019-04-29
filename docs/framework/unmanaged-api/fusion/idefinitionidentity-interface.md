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
ms.openlocfilehash: 4ff23330f307c10eac134048de39a6e19a67c75b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697535"
---
# <a name="idefinitionidentity-interface"></a><span data-ttu-id="b6d6b-102">IDefinitionIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="b6d6b-102">IDefinitionIdentity Interface</span></span>
<span data-ttu-id="b6d6b-103">Représente la signature unique du code qui définit l’application dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-103">Represents the unique signature of the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b6d6b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b6d6b-104">Methods</span></span>  
  
|<span data-ttu-id="b6d6b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="b6d6b-105">Method</span></span>|<span data-ttu-id="b6d6b-106">Description</span><span class="sxs-lookup"><span data-stu-id="b6d6b-106">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionIdentity::Clone`|<span data-ttu-id="b6d6b-107">Obtient un pointeur d’interface vers un nouveau `IDefinitionIdentity` objet qui est identique à ce `IDefinitionIdentity`, sauf pour les modifications de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-107">Gets an interface pointer to a new `IDefinitionIdentity` object that is identical to this `IDefinitionIdentity`, except for the specified attribute changes.</span></span>|  
|`IDefinitionIdentity::EnumAttributes`|<span data-ttu-id="b6d6b-108">Obtient un pointeur d’interface vers un [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) objet qui contient les attributs associés à ce `IDefinitionIdentity`.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-108">Gets an interface pointer to an [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) object that contains the attributes associated with this `IDefinitionIdentity`.</span></span>|  
|`IDefinitionIdentity::GetAttribute`|<span data-ttu-id="b6d6b-109">Obtient la valeur de l’attribut avec le nom spécifié dans l’espace de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-109">Gets the value of the attribute with the specified name in the specified namespace.</span></span>|  
|`IDefinitionIdentity::SetAttribute`|<span data-ttu-id="b6d6b-110">Définit l’attribut ayant le nom spécifié dans l’espace de noms spécifié à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-110">Sets the attribute that has the specified name in the specified namespace to the specified value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b6d6b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6d6b-111">Requirements</span></span>  
 <span data-ttu-id="b6d6b-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b6d6b-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b6d6b-113">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="b6d6b-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="b6d6b-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b6d6b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6d6b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6d6b-115">See also</span></span>

- [<span data-ttu-id="b6d6b-116">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="b6d6b-116">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
