---
title: IXCLRDataMethodInstance, interface
ms.date: 02/01/2019
api.name:
- IXCLRDataMethodInstance Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodInstance Interface
helpviewer.keywords:
- IXCLRDataMethodInstance Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: f62cbdc4b3e73f0c27492f7ed20b35378654d399
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59152956"
---
# <a name="ixclrdatamethodinstance-interface"></a><span data-ttu-id="16615-102">IXCLRDataMethodInstance, interface</span><span class="sxs-lookup"><span data-stu-id="16615-102">IXCLRDataMethodInstance Interface</span></span>

<span data-ttu-id="16615-103">Fournit des méthodes pour obtenir des informations sur une instance de méthode.</span><span class="sxs-lookup"><span data-stu-id="16615-103">Provides methods for querying information about a method instance.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="16615-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="16615-104">Methods</span></span>

| <span data-ttu-id="16615-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="16615-105">Method</span></span>                                                                                                                  | <span data-ttu-id="16615-106">Description</span><span class="sxs-lookup"><span data-stu-id="16615-106">Description</span></span>                                 |
| ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| [<span data-ttu-id="16615-107">GetILAddressMap</span><span class="sxs-lookup"><span data-stu-id="16615-107">GetILAddressMap</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-getiladdressmap-method.md) | <span data-ttu-id="16615-108">Obtient le langage intermédiaire aux informations de mappage d’adresse.</span><span class="sxs-lookup"><span data-stu-id="16615-108">Gets the IL to address mapping information.</span></span> |
| [<span data-ttu-id="16615-109">GetRepresentativeEntryAddress</span><span class="sxs-lookup"><span data-stu-id="16615-109">GetRepresentativeEntryAddress</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamethodinstance-getrepresentativeentryaddress-method.md) | <span data-ttu-id="16615-110">Obtient l’adresse de point d’entrée plus représentatif de la compilation native de tous les points d’entrée possibles pour une méthode.</span><span class="sxs-lookup"><span data-stu-id="16615-110">Gets the most representative entry point address for the native compilation of all the possible entry points for a method.</span></span> |

## <a name="remarks"></a><span data-ttu-id="16615-111">Notes</span><span class="sxs-lookup"><span data-stu-id="16615-111">Remarks</span></span>

<span data-ttu-id="16615-112">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="16615-112">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="16615-113">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `ECD73800-22CA-4b0d-AB55-E9BA7E6318A5` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="16615-113">However, it's a COM interface that derives from `IUnknown` with GUID `ECD73800-22CA-4b0d-AB55-E9BA7E6318A5` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="16615-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16615-114">Requirements</span></span>

<span data-ttu-id="16615-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="16615-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="16615-116">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="16615-116">**Header:** None</span></span>  
<span data-ttu-id="16615-117">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="16615-117">**Library:** None</span></span>  
<span data-ttu-id="16615-118">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="16615-118">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="16615-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16615-119">See also</span></span>

- [<span data-ttu-id="16615-120">Débogage</span><span class="sxs-lookup"><span data-stu-id="16615-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="16615-121">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="16615-121">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
