---
title: IReferenceIdentity, interface
ms.date: 03/30/2017
api_name:
- IReferenceIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IReferenceIdentity
helpviewer_keywords:
- IReferenceIdentity interface [.NET Framework fusion]
ms.assetid: 9180ac5a-7019-4716-9f83-8a91d157239a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4708fa173725e4c91a13f5b92cdbb1fdf8a8a4d1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432101"
---
# <a name="ireferenceidentity-interface"></a><span data-ttu-id="34eda-102">IReferenceIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="34eda-102">IReferenceIdentity Interface</span></span>
<span data-ttu-id="34eda-103">Représente une référence à la signature unique d’un objet de code.</span><span class="sxs-lookup"><span data-stu-id="34eda-103">Represents a reference to the unique signature of a code object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="34eda-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="34eda-104">Methods</span></span>  
  
|<span data-ttu-id="34eda-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="34eda-105">Method</span></span>|<span data-ttu-id="34eda-106">Description</span><span class="sxs-lookup"><span data-stu-id="34eda-106">Description</span></span>|  
|------------|-----------------|  
|`IReferenceIdentity::Clone`|<span data-ttu-id="34eda-107">Obtient un pointeur d’interface vers un nouveau `IReferenceIdentity` instance qui est identique à ce `IReferenceIdentity`, à l’exception des modifications d’attribut spécifiées.</span><span class="sxs-lookup"><span data-stu-id="34eda-107">Gets an interface pointer to a new `IReferenceIdentity` instance that is identical to this `IReferenceIdentity`, except for the specified attribute changes.</span></span>|  
|`IReferenceIdentity::EnumAttributes`|<span data-ttu-id="34eda-108">Obtient un pointeur d’interface vers un `IEnumIDENTITY_ATTRIBUTE` instance qui contient les attributs associés à ce `IReferenceIdentity`.</span><span class="sxs-lookup"><span data-stu-id="34eda-108">Gets an interface pointer to an `IEnumIDENTITY_ATTRIBUTE` instance that contains the attributes associated with this `IReferenceIdentity`.</span></span>|  
|`IReferenceIdentity::GetAttribute`|<span data-ttu-id="34eda-109">Obtient la valeur de l’attribut dans l’espace de noms spécifié, avec le nom spécifié.</span><span class="sxs-lookup"><span data-stu-id="34eda-109">Gets the value of the attribute in the specified namespace, with the specified name.</span></span>|  
|`IReferenceIdentity::SetAttribute`|<span data-ttu-id="34eda-110">Définit l’attribut qui possède l’espace de noms et le nom spécifié à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="34eda-110">Sets the attribute that has the specified namespace and the specified name to the specified value.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="34eda-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="34eda-111">Requirements</span></span>  
 <span data-ttu-id="34eda-112">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="34eda-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="34eda-113">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="34eda-113">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="34eda-114">**Versions du .NET framework :** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="34eda-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34eda-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34eda-115">See Also</span></span>  
 [<span data-ttu-id="34eda-116">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="34eda-116">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)  
 [<span data-ttu-id="34eda-117">IEnumIDENTITY_ATTRIBUTE, interface</span><span class="sxs-lookup"><span data-stu-id="34eda-117">IEnumIDENTITY_ATTRIBUTE Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/ienumidentity-attribute-interface.md)
