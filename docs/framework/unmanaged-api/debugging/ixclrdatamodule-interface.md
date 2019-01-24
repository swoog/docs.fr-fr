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
ms.openlocfilehash: c8d6e36687fd43bbc59304eee64dd42eb78101e3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54676521"
---
# <a name="ixclrdatamodule-interface"></a><span data-ttu-id="986fc-102">IXCLRDataModule Interface</span><span class="sxs-lookup"><span data-stu-id="986fc-102">IXCLRDataModule Interface</span></span>

<span data-ttu-id="986fc-103">Fournit des méthodes pour obtenir des informations sur un module chargé.</span><span class="sxs-lookup"><span data-stu-id="986fc-103">Provides methods for querying information about a loaded module.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="methods"></a><span data-ttu-id="986fc-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="986fc-104">Methods</span></span>

| <span data-ttu-id="986fc-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="986fc-105">Method</span></span>                                                                                                                                | <span data-ttu-id="986fc-106">Description</span><span class="sxs-lookup"><span data-stu-id="986fc-106">Description</span></span>                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| [<span data-ttu-id="986fc-107">GetMethodDefinitionByToken</span><span class="sxs-lookup"><span data-stu-id="986fc-107">GetMethodDefinitionByToken</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getmethoddefinitionbytoken-method.md) | <span data-ttu-id="986fc-108">Obtient la définition de méthode correspondant à un jeton de métadonnées donné.</span><span class="sxs-lookup"><span data-stu-id="986fc-108">Gets the method definition corresponding to a given metadata token.</span></span> |
| [<span data-ttu-id="986fc-109">Requête</span><span class="sxs-lookup"><span data-stu-id="986fc-109">Request</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-request-method.md)                                       | <span data-ttu-id="986fc-110">Demandes pour remplir la mémoire tampon spécifiée avec les données du module.</span><span class="sxs-lookup"><span data-stu-id="986fc-110">Requests to populate the buffer given with the module's data.</span></span>       |
| [<span data-ttu-id="986fc-111">GetVersionId</span><span class="sxs-lookup"><span data-stu-id="986fc-111">GetVersionId</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-getversionid-method.md)                             | <span data-ttu-id="986fc-112">Obtient l’ID de version. du module</span><span class="sxs-lookup"><span data-stu-id="986fc-112">Gets the module's version ID.</span></span>                                       |

## <a name="remarks"></a><span data-ttu-id="986fc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="986fc-113">Remarks</span></span>

<span data-ttu-id="986fc-114">Cette interface réside dans le runtime et n’est pas exposée par le biais d’en-têtes ou les fichiers de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="986fc-114">This interface lives inside the runtime and is not exposed through any headers or library files.</span></span> <span data-ttu-id="986fc-115">Toutefois, il est une interface COM qui dérive de `IUnknown` avec le GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` qui peuvent être obtenues via les mécanismes COM habituels.</span><span class="sxs-lookup"><span data-stu-id="986fc-115">However, it's a COM interface that derives from `IUnknown` with GUID `88E32849-0A0A-4cb0-9022-7CD2E9E139E2` that can be obtained through the usual COM mechanisms.</span></span>

## <a name="requirements"></a><span data-ttu-id="986fc-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="986fc-116">Requirements</span></span>

<span data-ttu-id="986fc-117">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="986fc-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="986fc-118">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="986fc-118">**Header:** None</span></span>  
<span data-ttu-id="986fc-119">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="986fc-119">**Library:** None</span></span>  
<span data-ttu-id="986fc-120">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="986fc-120">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="986fc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="986fc-121">See also</span></span>

- [<span data-ttu-id="986fc-122">Débogage</span><span class="sxs-lookup"><span data-stu-id="986fc-122">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="986fc-123">Interfaces de débogage</span><span class="sxs-lookup"><span data-stu-id="986fc-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
