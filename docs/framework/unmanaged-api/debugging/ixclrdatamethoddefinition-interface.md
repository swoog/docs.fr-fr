---
title: Interface de IXCLRDataMethodDefinition
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition Interface
helpviewer.keywords:
- IXCLRDataMethodDefinition Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 4b1e8cb1cf34bb1c5ade1353351aab953e2b734a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54644245"
---
# <a name="ixclrdatamethoddefinition-interface"></a><span data-ttu-id="468f7-102">Interface de IXCLRDataMethodDefinition</span><span class="sxs-lookup"><span data-stu-id="468f7-102">IXCLRDataMethodDefinition Interface</span></span>

<span data-ttu-id="468f7-103">Fournit des méthodes pour obtenir des informations sur une définition de méthode.</span><span class="sxs-lookup"><span data-stu-id="468f7-103">Provides methods for querying information about a method definition.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="468f7-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="468f7-104">Methods</span></span>

<span data-ttu-id="468f7-105">Les méthodes suivantes sont certaines des méthodes disponibles dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="468f7-105">The following methods are some of the methods available in the interface.</span></span>

| <span data-ttu-id="468f7-106">Méthode</span><span class="sxs-lookup"><span data-stu-id="468f7-106">Method</span></span>                                                                                                                          | <span data-ttu-id="468f7-107">Description</span><span class="sxs-lookup"><span data-stu-id="468f7-107">Description</span></span>                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="468f7-108">StartEnumInstances</span><span class="sxs-lookup"><span data-stu-id="468f7-108">StartEnumInstances</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-startenuminstances-method.md) | <span data-ttu-id="468f7-109">Fournit un handle pour l’énumération des instances de méthode pour une donnée `IXCLRDataAppDomain`.</span><span class="sxs-lookup"><span data-stu-id="468f7-109">Provides a handle for the enumeration of method instances for a given `IXCLRDataAppDomain`.</span></span> |
| [<span data-ttu-id="468f7-110">EnumInstance</span><span class="sxs-lookup"><span data-stu-id="468f7-110">EnumInstance</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-enuminstance-method.md)             | <span data-ttu-id="468f7-111">Énumère les instances de cette définition de méthode.</span><span class="sxs-lookup"><span data-stu-id="468f7-111">Enumerates the instances of this method definition.</span></span>                                         |
| [<span data-ttu-id="468f7-112">EndEnumInstances</span><span class="sxs-lookup"><span data-stu-id="468f7-112">EndEnumInstances</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethoddefinition-endenuminstances-method.md)     | <span data-ttu-id="468f7-113">Libère les ressources utilisées par les itérateurs internes utilisés pendant l’énumération de l’instance.</span><span class="sxs-lookup"><span data-stu-id="468f7-113">Releases the resources used by internal iterators used during instance enumeration.</span></span>         |

## <a name="remarks"></a><span data-ttu-id="468f7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="468f7-114">Remarks</span></span>

<span data-ttu-id="468f7-115">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="468f7-115">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="468f7-116">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `AAF60008-FB2C-420b-8FB1-42D244A54A97` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="468f7-116">However, it's a COM interface that derives from `IUnknown` with GUID `AAF60008-FB2C-420b-8FB1-42D244A54A97` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="468f7-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="468f7-117">Requirements</span></span>

<span data-ttu-id="468f7-118">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="468f7-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="468f7-119">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="468f7-119">**Header:** None</span></span>  
<span data-ttu-id="468f7-120">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="468f7-120">**Library:** None</span></span>  
<span data-ttu-id="468f7-121">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="468f7-121">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="468f7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="468f7-122">See also</span></span>

- [<span data-ttu-id="468f7-123">Débogage</span><span class="sxs-lookup"><span data-stu-id="468f7-123">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="468f7-124">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="468f7-124">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
