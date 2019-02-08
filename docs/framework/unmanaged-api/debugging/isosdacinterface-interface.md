---
title: Interface de ISOSDacInterface
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
ms.sourcegitcommit: 3500c4845f96a91a438a02ef2c6b4eef45a5e2af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55827927"
---
# <a name="isosdacinterface-interface"></a><span data-ttu-id="d1d5c-102">Interface de ISOSDacInterface</span><span class="sxs-lookup"><span data-stu-id="d1d5c-102">ISOSDacInterface Interface</span></span>

<span data-ttu-id="d1d5c-103">Fournit des méthodes d’assistance pour accéder aux données à partir de `SOS`.</span><span class="sxs-lookup"><span data-stu-id="d1d5c-103">Provides helper methods to access data from `SOS`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="d1d5c-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d1d5c-104">Methods</span></span>

| <span data-ttu-id="d1d5c-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="d1d5c-105">Method</span></span>                                                                                                               | <span data-ttu-id="d1d5c-106">Description</span><span class="sxs-lookup"><span data-stu-id="d1d5c-106">Description</span></span>                                                                                                                   |
| -------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| [<span data-ttu-id="d1d5c-107">GetMethodDescData</span><span class="sxs-lookup"><span data-stu-id="d1d5c-107">GetMethodDescData</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmethoddescdata-method.md) | <span data-ttu-id="d1d5c-108">Obtient les données pour le pointeur MethodDesc donné.</span><span class="sxs-lookup"><span data-stu-id="d1d5c-108">Gets the data for the given MethodDesc pointer.</span></span> |
| [<span data-ttu-id="d1d5c-109">GetMethodDescPtrFromIP</span><span class="sxs-lookup"><span data-stu-id="d1d5c-109">GetMethodDescPtrFromIP</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmethoddescptrfromip-method.md) | <span data-ttu-id="d1d5c-110">Récupère le pointeur de la MethodDesc correspondant de la méthode contenant l’adresse d’instruction natif donné.</span><span class="sxs-lookup"><span data-stu-id="d1d5c-110">Retrieves the pointer of the MethodDesc corresponding the method containing the given native instruction address.</span></span> |
| [<span data-ttu-id="d1d5c-111">GetModuleData</span><span class="sxs-lookup"><span data-stu-id="d1d5c-111">GetModuleData</span></span>](../../../../docs/framework/unmanaged-api/debugging/isosdacinterface-getmoduledata-method.md)| <span data-ttu-id="d1d5c-112">Extrait les données correspondant au module chargé à une adresse donnée.</span><span class="sxs-lookup"><span data-stu-id="d1d5c-112">Fetches the data corresponding to the module loaded at a given address.</span></span> |

## <a name="remarks"></a><span data-ttu-id="d1d5c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d1d5c-113">Remarks</span></span>

<span data-ttu-id="d1d5c-114">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d1d5c-114">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="d1d5c-115">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="d1d5c-115">However, it's a COM interface that derives from `IUnknown` with GUID `436f00f2-b42a-4b9f-870c-e73db66ae930` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d5c-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d1d5c-116">Requirements</span></span>

<span data-ttu-id="d1d5c-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d1d5c-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="d1d5c-118">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="d1d5c-118">**Header:** None</span></span>  
<span data-ttu-id="d1d5c-119">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="d1d5c-119">**Library:** None</span></span>  
<span data-ttu-id="d1d5c-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d1d5c-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="d1d5c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1d5c-121">See also</span></span>

- [<span data-ttu-id="d1d5c-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="d1d5c-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="d1d5c-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="d1d5c-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
