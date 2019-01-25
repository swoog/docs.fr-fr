---
title: Interface de ISOSDacInterface
ms.date: 01/16/2019
api.name:
- ISOSDacInterface Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface Interface
helpviewer.keywords:
- ISOSDacInterface Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 5e037cf6fb88fff4886733ff4152dca0a827e0a3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54491026"
---
# <a name="isosdacinterface-interface"></a><span data-ttu-id="d800d-102">Interface de ISOSDacInterface</span><span class="sxs-lookup"><span data-stu-id="d800d-102">ISOSDacInterface Interface</span></span>

<span data-ttu-id="d800d-103">Fournit des méthodes d’assistance pour accéder aux données à partir de `SOS`.</span><span class="sxs-lookup"><span data-stu-id="d800d-103">Provides helper methods to access data from `SOS`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="d800d-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d800d-104">Methods</span></span>

| <span data-ttu-id="d800d-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d800d-105">Method</span></span>                                                                                                               | <span data-ttu-id="d800d-106">Description</span><span class="sxs-lookup"><span data-stu-id="d800d-106">Description</span></span>                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="d800d-107">GetMethodDescData</span><span class="sxs-lookup"><span data-stu-id="d800d-107">GetMethodDescData</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmethoddescdata-method.md) | <span data-ttu-id="d800d-108">Obtient les données de la donnée [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d800d-108">Gets the data for the given [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="d800d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d800d-109">Remarks</span></span>

<span data-ttu-id="d800d-110">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d800d-110">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="d800d-111">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="d800d-111">However, it's a COM interface that derives from `IUnknown` with GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="d800d-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d800d-112">Requirements</span></span>

<span data-ttu-id="d800d-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d800d-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="d800d-114">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="d800d-114">**Header:** None</span></span>  
<span data-ttu-id="d800d-115">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="d800d-115">**Library:** None</span></span>  
<span data-ttu-id="d800d-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d800d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="d800d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d800d-117">See also</span></span>

- [<span data-ttu-id="d800d-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="d800d-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="d800d-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d800d-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
