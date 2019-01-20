---
title: IXCLRDataModule::GetVersionId (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetVersionId Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetVersionId Method
helpviewer.keywords:
- IXCLRDataModule::GetVersionId Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: ac4111abdf6a471aca1eca72a86e33698debbff6
ms.sourcegitcommit: b56d59ad42140d277f2acbd003b74d655fdbc9f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/19/2019
ms.locfileid: "54416402"
---
# <a name="ixclrdatamodulegetversionid-method"></a><span data-ttu-id="63e98-102">IXCLRDataModule::GetVersionId (méthode)</span><span class="sxs-lookup"><span data-stu-id="63e98-102">IXCLRDataModule::GetVersionId Method</span></span>

<span data-ttu-id="63e98-103">Obtient l’identificateur de version du module.</span><span class="sxs-lookup"><span data-stu-id="63e98-103">Gets the module's version identifier.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="63e98-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63e98-104">Syntax</span></span>

```
HRESULT GetVersionId(
    [out] GUID* vid
);
```

### <a name="parameters"></a><span data-ttu-id="63e98-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63e98-105">Parameters</span></span>

<span data-ttu-id="63e98-106">`vid` [out] Identificateur de version du module.</span><span class="sxs-lookup"><span data-stu-id="63e98-106">`vid` [out] The module's version identifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="63e98-107">Notes</span><span class="sxs-lookup"><span data-stu-id="63e98-107">Remarks</span></span>

<span data-ttu-id="63e98-108">La méthode fournie fait partie de la `IXCLRDataModule` interface et correspond à l’emplacement 40E de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="63e98-108">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 40th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e98-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="63e98-109">Requirements</span></span>

<span data-ttu-id="63e98-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="63e98-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="63e98-111">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="63e98-111">**Header:** None</span></span>  
<span data-ttu-id="63e98-112">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="63e98-112">**Library:** None</span></span>  
<span data-ttu-id="63e98-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="63e98-113">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="63e98-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63e98-114">See Also</span></span>

- [<span data-ttu-id="63e98-115">Débogage</span><span class="sxs-lookup"><span data-stu-id="63e98-115">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="63e98-116">Interface de IXCLRDataModule</span><span class="sxs-lookup"><span data-stu-id="63e98-116">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
