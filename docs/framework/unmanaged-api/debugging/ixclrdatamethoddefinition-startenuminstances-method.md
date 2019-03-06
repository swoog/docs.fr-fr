---
title: IXCLRDataMethodDefinition::StartEnumInstances (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataMethodDefinition::StartEnumInstances Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataMethodDefinition::StartEnumInstances Method
helpviewer.keywords:
- IXCLRDataMethodDefinition::StartEnumInstances Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: e92eea9677731756bdbfcbdcfac1531861fb5dce
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57361341"
---
# <a name="ixclrdatamethoddefinitionstartenuminstances-method"></a><span data-ttu-id="f6e73-102">IXCLRDataMethodDefinition::StartEnumInstances (méthode)</span><span class="sxs-lookup"><span data-stu-id="f6e73-102">IXCLRDataMethodDefinition::StartEnumInstances Method</span></span>

<span data-ttu-id="f6e73-103">Fournit un handle pour l’énumération des instances de méthode pour une donnée `IXCLRDataAppDomain`.</span><span class="sxs-lookup"><span data-stu-id="f6e73-103">Provides a handle for the enumeration of method instances for a given `IXCLRDataAppDomain`.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="f6e73-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6e73-104">Syntax</span></span>

```
HRESULT StartEnumInstances(
    [in] IXCLRDataAppDomain* appDomain,
    [out] CLRDATA_ENUM *handle
);
```

## <a name="parameters"></a><span data-ttu-id="f6e73-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6e73-105">Parameters</span></span>

`appDomain`\
<span data-ttu-id="f6e73-106">[in] Un AppDomain pour l’énumération.</span><span class="sxs-lookup"><span data-stu-id="f6e73-106">[in] An AppDomain for the enumeration.</span></span>

`handle`\
<span data-ttu-id="f6e73-107">[out] Un handle pour énumérer les instances.</span><span class="sxs-lookup"><span data-stu-id="f6e73-107">[out] A handle for enumerating the instances.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6e73-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f6e73-108">Remarks</span></span>

<span data-ttu-id="f6e73-109">La méthode fournie fait partie de la `IXCLRDataMethodDefinition` interface et correspond à la troisième emplacement de la table de la méthode virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f6e73-109">The provided method is part of the `IXCLRDataMethodDefinition` interface and corresponds to the third slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e73-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f6e73-110">Requirements</span></span>

<span data-ttu-id="f6e73-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f6e73-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="f6e73-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="f6e73-112">**Header:** None</span></span>  
<span data-ttu-id="f6e73-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="f6e73-113">**Library:** None</span></span>  
<span data-ttu-id="f6e73-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f6e73-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6e73-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f6e73-115">See also</span></span>

- [<span data-ttu-id="f6e73-116">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="f6e73-116">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="f6e73-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="f6e73-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="f6e73-118">Interface de IXCLRDataMethodDefinition</span><span class="sxs-lookup"><span data-stu-id="f6e73-118">IXCLRDataMethodDefinition Interface</span></span>](ixclrdatamethoddefinition-interface.md)