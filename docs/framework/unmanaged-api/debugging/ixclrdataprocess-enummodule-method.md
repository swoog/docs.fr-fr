---
title: IXCLRDataProcess::EnumModule (méthode)
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EnumModule Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EnumModule Method
helpviewer.keywords:
- IXCLRDataProcess::EnumModule Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: a0398d18f9568754231082d63b4c6a2c865d8c6f
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57363304"
---
# <a name="ixclrdataprocessenummodule-method"></a><span data-ttu-id="634f0-102">IXCLRDataProcess::EnumModule (méthode)</span><span class="sxs-lookup"><span data-stu-id="634f0-102">IXCLRDataProcess::EnumModule Method</span></span>

<span data-ttu-id="634f0-103">Énumère les modules de ce processus.</span><span class="sxs-lookup"><span data-stu-id="634f0-103">Enumerates the modules of this process.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="634f0-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="634f0-104">Syntax</span></span>

```
HRESULT EnumModule(
    [in, out] CLRDATA_ENUM  *handle,
    [out] IXCLRDataModule  **mod
);
```

## <a name="parameters"></a><span data-ttu-id="634f0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="634f0-105">Parameters</span></span>

`handle`\
<span data-ttu-id="634f0-106">[in, out] Un handle pour énumérer les modules.</span><span class="sxs-lookup"><span data-stu-id="634f0-106">[in, out] A handle for enumerating the modules.</span></span>

`mod`\
<span data-ttu-id="634f0-107">[out] Le module énuméré.</span><span class="sxs-lookup"><span data-stu-id="634f0-107">[out] The enumerated module.</span></span>

## <a name="remarks"></a><span data-ttu-id="634f0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="634f0-108">Remarks</span></span>

<span data-ttu-id="634f0-109">La méthode fournie fait partie de la `IXCLRDataProcess` interface et correspond à l’emplacement de la table de la méthode virtuelle de 25.</span><span class="sxs-lookup"><span data-stu-id="634f0-109">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="634f0-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="634f0-110">Requirements</span></span>

<span data-ttu-id="634f0-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="634f0-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="634f0-112">**En-tête :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="634f0-112">**Header:** None</span></span>  
<span data-ttu-id="634f0-113">**Bibliothèque :** Aucun.</span><span class="sxs-lookup"><span data-stu-id="634f0-113">**Library:** None</span></span>  
<span data-ttu-id="634f0-114">**Versions du .NET Framework :** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="634f0-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  

## <a name="see-also"></a><span data-ttu-id="634f0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="634f0-115">See also</span></span>

- [<span data-ttu-id="634f0-116">Énumération de CLRDataSourceType</span><span class="sxs-lookup"><span data-stu-id="634f0-116">CLRDataSourceType Enumeration</span></span>](clrdatasourcetype-enumeration.md)
- [<span data-ttu-id="634f0-117">Débogage</span><span class="sxs-lookup"><span data-stu-id="634f0-117">Debugging</span></span>](index.md)
- [<span data-ttu-id="634f0-118">Interface de IXCLRDataModule</span><span class="sxs-lookup"><span data-stu-id="634f0-118">IXCLRDataModule Interface</span></span>](ixclrdatamodule-interface.md)
- [<span data-ttu-id="634f0-119">Interface de IXCLRDataProcess</span><span class="sxs-lookup"><span data-stu-id="634f0-119">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
