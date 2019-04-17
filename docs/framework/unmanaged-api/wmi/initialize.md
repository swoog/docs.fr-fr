---
title: Initialiser (fonction) (référence des API non managées)
description: La fonction d’initialisation effectue l’initialisation de WMI.
ms.date: 11/06/2017
api_name:
- Initialize
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Initialize
helpviewer_keywords:
- Initialize function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c71b2b6d6f102d19d30d480ee9bafcac3c204be
ms.sourcegitcommit: 438919211260bb415fc8f96ca3eabc33cf2d681d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2019
ms.locfileid: "59611079"
---
# <a name="initialize-function"></a><span data-ttu-id="4f36b-103">Initialiser (fonction)</span><span class="sxs-lookup"><span data-stu-id="4f36b-103">Initialize function</span></span>

<span data-ttu-id="4f36b-104">Effectue l’initialisation WMI.</span><span class="sxs-lookup"><span data-stu-id="4f36b-104">Performs WMI initialization.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="4f36b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f36b-105">Syntax</span></span>

```cpp
HRESULT Initialize(
   [in] boolean bAllowIManagementObjectQI
);
```

## <a name="parameters"></a><span data-ttu-id="4f36b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f36b-106">Parameters</span></span>

`bAllowIManagementObjectQI`

<span data-ttu-id="4f36b-107">[in] `true` pour indiquer que les appels à destination de QueryInterface sur les objets WMI sont autorisées ; `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4f36b-107">[in] `true` to indicate that calls to QueryInterface on WMI objects are allowed; `false` otherwise.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f36b-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4f36b-108">Return value</span></span>

<span data-ttu-id="4f36b-109">La fonction retourne toujours `S_OK` (0).</span><span class="sxs-lookup"><span data-stu-id="4f36b-109">The function always returns `S_OK` (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f36b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f36b-110">Requirements</span></span>

<span data-ttu-id="4f36b-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4f36b-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="4f36b-112">**En-tête :** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="4f36b-112">**Header:** WMINet_Utils.def</span></span>

<span data-ttu-id="4f36b-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="4f36b-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="4f36b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f36b-114">See also</span></span>

- [<span data-ttu-id="4f36b-115">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="4f36b-115">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
