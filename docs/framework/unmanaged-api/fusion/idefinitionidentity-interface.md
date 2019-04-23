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
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59192665"
---
# <a name="idefinitionidentity-interface"></a><span data-ttu-id="f6cbb-102">IDefinitionIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="f6cbb-102">IDefinitionIdentity Interface</span></span>
<span data-ttu-id="f6cbb-103">Représente la signature unique du code qui définit l’application dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="f6cbb-103">Represents the unique signature of the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="f6cbb-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="f6cbb-104">Methods</span></span>  
  
|<span data-ttu-id="f6cbb-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="f6cbb-105">Method</span></span>|<span data-ttu-id="f6cbb-106">Description</span><span class="sxs-lookup"><span data-stu-id="f6cbb-106">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionIdentity::Clone`|<span data-ttu-id="f6cbb-107">Obtient un pointeur d’interface vers un nouveau `IDefinitionIdentity` objet qui est identique à ce `IDefinitionIdentity`, sauf pour les modifications de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="f6cbb-107">Gets an interface pointer to a new `IDefinitionIdentity` object that is identical to this `IDefinitionIdentity`, except for the specified attribute changes.</span></span>|  
|`IDefinitionIdentity::EnumAttributes`|<span data-ttu-id="f6cbb-108">Obtient un pointeur d’interface vers un [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) objet qui contient les attributs associés à ce `IDefinitionIdentity`.</span><span class="sxs-lookup"><span data-stu-id="f6cbb-108">Gets an interface pointer to an [IEnumIDENTITY_ATTRIBUTE](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md) object that contains the attributes associated with this `IDefinitionIdentity`.</span></span>|  
|`IDefinitionIdentity::GetAttribute`|<span data-ttu-id="f6cbb-109">Obtient la valeur de l’attribut avec le nom spécifié dans l’espace de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="f6cbb-109">Gets the value of the attribute with the specified name in the specified namespace.</span></span>|  
|`IDefinitionIdentity::SetAttribute`|<span data-ttu-id="f6cbb-110">Définit l’attribut ayant le nom spécifié dans l’espace de noms spécifié à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f6cbb-110">Sets the attribute that has the specified name in the specified namespace to the specified value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f6cbb-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6cbb-111">Requirements</span></span>  
 <span data-ttu-id="f6cbb-112">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f6cbb-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f6cbb-113">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="f6cbb-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="f6cbb-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f6cbb-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6cbb-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6cbb-115">See also</span></span>

- [<span data-ttu-id="f6cbb-116">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="f6cbb-116">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
