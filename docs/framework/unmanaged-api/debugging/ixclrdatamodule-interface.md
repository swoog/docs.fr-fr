---
title: IXCLRDataModule Interface
ms.date: 01/16/2019
api.name:
- IXCLRDataModule Interface
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule Interface
helpviewer.keywords:
- IXCLRDataModule Interface [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: e306834166051ae48fd283d51f18d9458091578f
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416449"
---
# <a name="ixclrdatamodule-interface"></a><span data-ttu-id="5db81-102">IXCLRDataModule Interface</span><span class="sxs-lookup"><span data-stu-id="5db81-102">IXCLRDataModule Interface</span></span>

<span data-ttu-id="5db81-103">Fournit des méthodes pour obtenir des informations sur un module chargé.</span><span class="sxs-lookup"><span data-stu-id="5db81-103">Provides methods for querying information about a loaded module.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="5db81-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5db81-104">Methods</span></span>

| <span data-ttu-id="5db81-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="5db81-105">Method</span></span>                                                                                                                                | <span data-ttu-id="5db81-106">Description</span><span class="sxs-lookup"><span data-stu-id="5db81-106">Description</span></span>                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="5db81-107">GetMethodDefinitionByToken</span><span class="sxs-lookup"><span data-stu-id="5db81-107">GetMethodDefinitionByToken</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getmethoddefinitionbytoken-method.md) | <span data-ttu-id="5db81-108">Obtient la définition de méthode correspondant à un jeton de métadonnées donné.</span><span class="sxs-lookup"><span data-stu-id="5db81-108">Gets the method definition corresponding to a given metadata token.</span></span> |
| [<span data-ttu-id="5db81-109">Requête</span><span class="sxs-lookup"><span data-stu-id="5db81-109">Request</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-request-method.md)                                       | <span data-ttu-id="5db81-110">Demandes pour remplir la mémoire tampon spécifiée avec les données du module.</span><span class="sxs-lookup"><span data-stu-id="5db81-110">Requests to populate the buffer given with the module's data.</span></span>       |
| [<span data-ttu-id="5db81-111">GetVersionId</span><span class="sxs-lookup"><span data-stu-id="5db81-111">GetVersionId</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getversionid-method.md)                             | <span data-ttu-id="5db81-112">Obtient l’ID de version. du module</span><span class="sxs-lookup"><span data-stu-id="5db81-112">Gets the module's version ID.</span></span>                                       |

## <a name="remarks"></a><span data-ttu-id="5db81-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5db81-113">Remarks</span></span>

<span data-ttu-id="5db81-114">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="5db81-114">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="5db81-115">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="5db81-115">However, it's a COM interface that derives from `IUnknown` with GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="5db81-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5db81-116">Requirements</span></span>

<span data-ttu-id="5db81-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5db81-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="5db81-118">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="5db81-118">**Header:** None</span></span>  
<span data-ttu-id="5db81-119">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="5db81-119">**Library:** None</span></span>  
<span data-ttu-id="5db81-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="5db81-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="5db81-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5db81-121">See Also</span></span>

- [<span data-ttu-id="5db81-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="5db81-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="5db81-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="5db81-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
