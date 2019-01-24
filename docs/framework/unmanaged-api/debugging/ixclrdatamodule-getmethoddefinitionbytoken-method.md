---
title: IXCLRDataModule::GetMethodDefinitionByToken Method
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetMethodDefinitionByToken Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method
helpviewer.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 1371b86f30324908a639b3b1bbae0ae007ba590a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54708088"
---
# <a name="ixclrdatamodulegetmethoddefinitionbytoken-method"></a><span data-ttu-id="ebe93-102">IXCLRDataModule::GetMethodDefinitionByToken Method</span><span class="sxs-lookup"><span data-stu-id="ebe93-102">IXCLRDataModule::GetMethodDefinitionByToken Method</span></span>

<span data-ttu-id="ebe93-103">Obtient la définition de méthode correspondant à un jeton de métadonnées donné.</span><span class="sxs-lookup"><span data-stu-id="ebe93-103">Gets the method definition corresponding to a given metadata token.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="ebe93-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebe93-104">Syntax</span></span>

```
HRESULT GetMethodDefinitionByToken(
    [in] mdMethodDef token,
    [out] IXCLRDataMethodDefinition** methodDefinition
);
```

### <a name="parameters"></a><span data-ttu-id="ebe93-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebe93-105">Parameters</span></span>

<span data-ttu-id="ebe93-106">`token` [in] Le jeton de méthode.</span><span class="sxs-lookup"><span data-stu-id="ebe93-106">`token` [in] The method token.</span></span>

<span data-ttu-id="ebe93-107">`methodDefinition` [out] La définition de méthode.</span><span class="sxs-lookup"><span data-stu-id="ebe93-107">`methodDefinition` [out] The method definition.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebe93-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ebe93-108">Remarks</span></span>

<span data-ttu-id="ebe93-109">La méthode fournie fait partie de la `IXCLRDataModule` interface et correspond à l’emplacement de la table de la méthode virtuelle de 25.</span><span class="sxs-lookup"><span data-stu-id="ebe93-109">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe93-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ebe93-110">Requirements</span></span>

<span data-ttu-id="ebe93-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ebe93-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="ebe93-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="ebe93-112">**Header:** None</span></span>  
<span data-ttu-id="ebe93-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="ebe93-113">**Library:** None</span></span>  
<span data-ttu-id="ebe93-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="ebe93-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  
 
## <a name="see-also"></a><span data-ttu-id="ebe93-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe93-115">See also</span></span>

- [<span data-ttu-id="ebe93-116">Débogage</span><span class="sxs-lookup"><span data-stu-id="ebe93-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="ebe93-117">Interface de IXCLRDataModule</span><span class="sxs-lookup"><span data-stu-id="ebe93-117">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)
