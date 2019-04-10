---
title: IEnumDefinitionIdentity, interface
ms.date: 03/30/2017
api_name:
- IEnumDefinitionIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumDefinitionIdentity
helpviewer_keywords:
- IEnumDefinitionIdentity interface [.NET Framework fusion]
ms.assetid: 8263e75d-251b-4abc-8a1a-c62884142232
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d19ca92db6f57a004dca54f6e22db10603c9498a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59214843"
---
# <a name="ienumdefinitionidentity-interface"></a><span data-ttu-id="c2042-102">IEnumDefinitionIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="c2042-102">IEnumDefinitionIdentity Interface</span></span>
<span data-ttu-id="c2042-103">Sert d’énumérateur pour une collection de `IDefinitionIdentity` objets.</span><span class="sxs-lookup"><span data-stu-id="c2042-103">Serves as the enumerator for a collection of `IDefinitionIdentity` objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2042-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2042-104">Syntax</span></span>  
  
```  
IEnumDefinitionIdentity : IUnknown {  
  
    HRESULT Clone (  
        [out] IEnumDefinitionIdentity **ppIEnumDefinitionIdentity  
    );  
  
    HRESULT Next (  
        [in]  ULONG               celt,  
        [out, length_is(celt), size_is(*pceltWritten)]  
              IDefinitionIdentity *rgpIDefinitionIdentity[],  
        [out] ULONG               *pceltWritten  
    );  
  
    HRESULT Reset ();  
  
    HRESULT Skip (  
        [in] ULONG celt  
    );  
  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="c2042-105">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c2042-105">Methods</span></span>  
  
|<span data-ttu-id="c2042-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="c2042-106">Method</span></span>|<span data-ttu-id="c2042-107">Description</span><span class="sxs-lookup"><span data-stu-id="c2042-107">Description</span></span>|  
|------------|-----------------|  
|`IEnumDefinitionIdentity::Clone`|<span data-ttu-id="c2042-108">Obtient un pointeur d’interface vers un nouveau `IEnumDefinitionIdentity` objet qui contient les mêmes membres que cela `IEnumDefinitionIdentity`.</span><span class="sxs-lookup"><span data-stu-id="c2042-108">Gets an interface pointer to a new `IEnumDefinitionIdentity` object that contains the same members as this `IEnumDefinitionIdentity`.</span></span>|  
|`IEnumDefinitionIdentity::Next`|<span data-ttu-id="c2042-109">Obtient le nombre spécifié de `IDefinitionIdentity` objets, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="c2042-109">Gets the specified number of `IDefinitionIdentity` objects, starting at the current position.</span></span>|  
|`IEnumDefinitionIdentity::Reset`|<span data-ttu-id="c2042-110">Déplace le pointeur d’instruction au début de ce `IEnumDefinitionIdentity`.</span><span class="sxs-lookup"><span data-stu-id="c2042-110">Moves the instruction pointer to the beginning of this `IEnumDefinitionIdentity`.</span></span>|  
|`IEnumDefinitionIdentity::Skip`|<span data-ttu-id="c2042-111">Déplace le pointeur d’instruction par le nombre spécifié d’éléments, en commençant à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="c2042-111">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="c2042-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2042-112">Requirements</span></span>  
 <span data-ttu-id="c2042-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c2042-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2042-114">**En-tête :** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="c2042-114">**Header:** Isolation.h</span></span>  
  
 **<span data-ttu-id="c2042-115">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="c2042-115">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="c2042-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2042-116">See also</span></span>

- [<span data-ttu-id="c2042-117">Interfaces de fusion</span><span class="sxs-lookup"><span data-stu-id="c2042-117">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)
- [<span data-ttu-id="c2042-118">IDefinitionIdentity, interface</span><span class="sxs-lookup"><span data-stu-id="c2042-118">IDefinitionIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md)
