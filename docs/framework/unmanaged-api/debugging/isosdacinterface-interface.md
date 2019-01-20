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
ms.openlocfilehash: 745ecfbffaad841e1ceb9216802644ba9dd5b94e
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416383"
---
# <a name="isosdacinterface-interface"></a><span data-ttu-id="d445a-102">Interface de ISOSDacInterface</span><span class="sxs-lookup"><span data-stu-id="d445a-102">ISOSDacInterface Interface</span></span>

<span data-ttu-id="d445a-103">Fournit des méthodes d’assistance pour accéder aux données à partir de `SOS`.</span><span class="sxs-lookup"><span data-stu-id="d445a-103">Provides helper methods to access data from `SOS`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="d445a-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d445a-104">Methods</span></span>

| <span data-ttu-id="d445a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d445a-105">Method</span></span>                                                                                                               | <span data-ttu-id="d445a-106">Description</span><span class="sxs-lookup"><span data-stu-id="d445a-106">Description</span></span>                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="d445a-107">GetMethodDescData</span><span class="sxs-lookup"><span data-stu-id="d445a-107">GetMethodDescData</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmethoddescdata-method.md) | <span data-ttu-id="d445a-108">Obtient les données de la donnée [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d445a-108">Gets the data for the given [MethodDesc](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md).</span></span> |

## <a name="remarks"></a><span data-ttu-id="d445a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d445a-109">Remarks</span></span>

<span data-ttu-id="d445a-110">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d445a-110">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="d445a-111">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="d445a-111">However, it's a COM interface that derives from `IUnknown` with GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="d445a-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d445a-112">Requirements</span></span>

<span data-ttu-id="d445a-113">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d445a-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="d445a-114">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="d445a-114">**Header:** None</span></span>  
<span data-ttu-id="d445a-115">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="d445a-115">**Library:** None</span></span>  
<span data-ttu-id="d445a-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d445a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="d445a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d445a-117">See Also</span></span>

- [<span data-ttu-id="d445a-118">Débogage</span><span class="sxs-lookup"><span data-stu-id="d445a-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="d445a-119">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d445a-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
