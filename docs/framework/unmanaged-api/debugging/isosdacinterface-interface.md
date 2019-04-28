---
title: ISOSDacInterface, interface
ms.date: 02/01/2019
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
ms.openlocfilehash: ccaf479fc4fb90007b4999e95ee03bdd0529321e
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61922146"
---
# <a name="isosdacinterface-interface"></a><span data-ttu-id="e4131-102">ISOSDacInterface, interface</span><span class="sxs-lookup"><span data-stu-id="e4131-102">ISOSDacInterface Interface</span></span>

<span data-ttu-id="e4131-103">Fournit des méthodes d’assistance pour accéder aux données à partir de `SOS`.</span><span class="sxs-lookup"><span data-stu-id="e4131-103">Provides helper methods to access data from `SOS`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="e4131-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4131-104">Methods</span></span>

| <span data-ttu-id="e4131-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="e4131-105">Method</span></span>                                                                                                               | <span data-ttu-id="e4131-106">Description</span><span class="sxs-lookup"><span data-stu-id="e4131-106">Description</span></span>                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="e4131-107">GetMethodDescData</span><span class="sxs-lookup"><span data-stu-id="e4131-107">GetMethodDescData</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmethoddescdata-method.md) | <span data-ttu-id="e4131-108">Obtient les données pour le pointeur MethodDesc donné.</span><span class="sxs-lookup"><span data-stu-id="e4131-108">Gets the data for the given MethodDesc pointer.</span></span> |
| [<span data-ttu-id="e4131-109">GetMethodDescPtrFromIP</span><span class="sxs-lookup"><span data-stu-id="e4131-109">GetMethodDescPtrFromIP</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmethoddescptrfromip-method.md) | <span data-ttu-id="e4131-110">Récupère le pointeur de la MethodDesc correspondant de la méthode contenant l’adresse d’instruction natif donné.</span><span class="sxs-lookup"><span data-stu-id="e4131-110">Retrieves the pointer of the MethodDesc corresponding the method containing the given native instruction address.</span></span> |
| [<span data-ttu-id="e4131-111">GetModuleData</span><span class="sxs-lookup"><span data-stu-id="e4131-111">GetModuleData</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmoduledata-method.md)| <span data-ttu-id="e4131-112">Extrait les données correspondant au module chargé à une adresse donnée.</span><span class="sxs-lookup"><span data-stu-id="e4131-112">Fetches the data corresponding to the module loaded at a given address.</span></span> |

## <a name="remarks"></a><span data-ttu-id="e4131-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e4131-113">Remarks</span></span>

<span data-ttu-id="e4131-114">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e4131-114">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="e4131-115">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="e4131-115">However, it's a COM interface that derives from `IUnknown` with GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4131-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4131-116">Requirements</span></span>

<span data-ttu-id="e4131-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e4131-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="e4131-118">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="e4131-118">**Header:** None</span></span>  
<span data-ttu-id="e4131-119">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="e4131-119">**Library:** None</span></span>  
<span data-ttu-id="e4131-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="e4131-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="e4131-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4131-121">See also</span></span>

- [<span data-ttu-id="e4131-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="e4131-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="e4131-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="e4131-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
