---
title: IDefinitionAppId, interface
ms.date: 03/30/2017
api_name:
- IDefinitionAppId
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IDefinitionAppId
helpviewer_keywords:
- IDefinitionAppId interface [.NET Framework fusion]
ms.assetid: e72f2550-bdec-4a20-a2f4-2e14847266c1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2735355097a1f3f581b3a4bc74f08d8f2ebf3bd8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430378"
---
# <a name="idefinitionappid-interface"></a><span data-ttu-id="a5a0b-102">IDefinitionAppId, interface</span><span class="sxs-lookup"><span data-stu-id="a5a0b-102">IDefinitionAppId Interface</span></span>
<span data-ttu-id="a5a0b-103">Représente un identificateur unique pour le code qui définit l’application dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="a5a0b-103">Represents a unique identifier for the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a5a0b-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a5a0b-104">Methods</span></span>  
  
|<span data-ttu-id="a5a0b-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="a5a0b-105">Method</span></span>|<span data-ttu-id="a5a0b-106">Description</span><span class="sxs-lookup"><span data-stu-id="a5a0b-106">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionAppId::get_Codebase`|<span data-ttu-id="a5a0b-107">Obtient une chaîne mise en forme qui représente le code dans cette `IDefinitionAppId` objet.</span><span class="sxs-lookup"><span data-stu-id="a5a0b-107">Gets a formatted string that represents the code in this `IDefinitionAppId` object.</span></span>|  
|`IDefinitionAppId::put_Codebase`|<span data-ttu-id="a5a0b-108">Définit le code de ce `IDefinitionAppId` mis en forme de l’objet spécifié à la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="a5a0b-108">Sets the code of this `IDefinitionAppId` object to the specified formatted string value.</span></span>|  
|`IDefinitionAppId::EnumAppPath`|<span data-ttu-id="a5a0b-109">Obtient un pointeur d’interface vers un [IEnumDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/ienumdefinitionidentity-interface.md) objet qui contient les assemblys dans le chemin d’accès d’application actuel.</span><span class="sxs-lookup"><span data-stu-id="a5a0b-109">Gets an interface pointer to an [IEnumDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/ienumdefinitionidentity-interface.md) object that contains the assemblies in the current application path.</span></span>|  
|`IDefinitionAppId::SetAppPath`|<span data-ttu-id="a5a0b-110">Définit le chemin d’accès de l’application pour l’assembly dans la portée actuelle avec la valeur référencée par le [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="a5a0b-110">Sets the application path for the assembly in the current scope to the value referenced by the specified [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) object.</span></span>|  
|`IDefinitionAppId::get_SubscriptionId`|<span data-ttu-id="a5a0b-111">Obtient un pointeur vers une représentation sous forme de chaîne de l’identificateur de jeton pour un abonnement à cette `IDefinitionAppId` objet.</span><span class="sxs-lookup"><span data-stu-id="a5a0b-111">Gets a pointer to a string representation of the token identifier for a subscription to this `IDefinitionAppId` object.</span></span>|  
|`IDefinitionAppId::put_SubscriptionId`|<span data-ttu-id="a5a0b-112">Définit l’identificateur de jeton pour un abonnement à cette `IDefinitionAppId` objet à la valeur de chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a5a0b-112">Sets the token identifier for a subscription to this `IDefinitionAppId` object to the specified string value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a5a0b-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a5a0b-113">Requirements</span></span>  
 <span data-ttu-id="a5a0b-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a5a0b-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a5a0b-115">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="a5a0b-115">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="a5a0b-116">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a5a0b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5a0b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5a0b-117">See Also</span></span>  
 [<span data-ttu-id="a5a0b-118">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="a5a0b-118">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
