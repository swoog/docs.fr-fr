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
ms.openlocfilehash: 5bd705ef549de3a8018efe731ef8735ef7b6b915
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61697236"
---
# <a name="idefinitionappid-interface"></a><span data-ttu-id="01273-102">IDefinitionAppId, interface</span><span class="sxs-lookup"><span data-stu-id="01273-102">IDefinitionAppId Interface</span></span>
<span data-ttu-id="01273-103">Représente un identificateur unique pour le code qui définit l’application dans la portée actuelle.</span><span class="sxs-lookup"><span data-stu-id="01273-103">Represents a unique identifier for the code that defines the application in the current scope.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="01273-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="01273-104">Methods</span></span>  
  
|<span data-ttu-id="01273-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="01273-105">Method</span></span>|<span data-ttu-id="01273-106">Description</span><span class="sxs-lookup"><span data-stu-id="01273-106">Description</span></span>|  
|------------|-----------------|  
|`IDefinitionAppId::get_Codebase`|<span data-ttu-id="01273-107">Obtient une chaîne mise en forme qui représente le code de cette `IDefinitionAppId` objet.</span><span class="sxs-lookup"><span data-stu-id="01273-107">Gets a formatted string that represents the code in this `IDefinitionAppId` object.</span></span>|  
|`IDefinitionAppId::put_Codebase`|<span data-ttu-id="01273-108">Définit le code de cet `IDefinitionAppId` objet spécifié à la mise en forme la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="01273-108">Sets the code of this `IDefinitionAppId` object to the specified formatted string value.</span></span>|  
|`IDefinitionAppId::EnumAppPath`|<span data-ttu-id="01273-109">Obtient un pointeur d’interface vers un [IEnumDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/ienumdefinitionidentity-interface.md) objet qui contient les assemblys dans le chemin d’accès d’application actuel.</span><span class="sxs-lookup"><span data-stu-id="01273-109">Gets an interface pointer to an [IEnumDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/ienumdefinitionidentity-interface.md) object that contains the assemblies in the current application path.</span></span>|  
|`IDefinitionAppId::SetAppPath`|<span data-ttu-id="01273-110">Définit le chemin d’accès de l’application pour l’assembly dans la portée actuelle à la valeur référencée par le [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) objet.</span><span class="sxs-lookup"><span data-stu-id="01273-110">Sets the application path for the assembly in the current scope to the value referenced by the specified [IDefinitionIdentity](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md) object.</span></span>|  
|`IDefinitionAppId::get_SubscriptionId`|<span data-ttu-id="01273-111">Obtient un pointeur vers une représentation sous forme de chaîne de l’identificateur de jeton pour un abonnement à ce `IDefinitionAppId` objet.</span><span class="sxs-lookup"><span data-stu-id="01273-111">Gets a pointer to a string representation of the token identifier for a subscription to this `IDefinitionAppId` object.</span></span>|  
|`IDefinitionAppId::put_SubscriptionId`|<span data-ttu-id="01273-112">Définit l’identificateur de jeton pour un abonnement à ce `IDefinitionAppId` objet à la valeur de chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="01273-112">Sets the token identifier for a subscription to this `IDefinitionAppId` object to the specified string value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="01273-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01273-113">Requirements</span></span>  
 <span data-ttu-id="01273-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="01273-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01273-115">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="01273-115">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="01273-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="01273-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01273-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01273-117">See also</span></span>

- [<span data-ttu-id="01273-118">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="01273-118">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
