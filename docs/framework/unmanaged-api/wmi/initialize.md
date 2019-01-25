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
ms.openlocfilehash: f56ce2da5cc1b79fded3788ddb9631d2c8a2fa7f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54693650"
---
# <a name="initialize-function"></a><span data-ttu-id="da7d4-103">Initialiser (fonction)</span><span class="sxs-lookup"><span data-stu-id="da7d4-103">Initialize function</span></span>
<span data-ttu-id="da7d4-104">Effectue l’initialisation WMI.</span><span class="sxs-lookup"><span data-stu-id="da7d4-104">Performs WMI initialization.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="da7d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da7d4-105">Syntax</span></span> 
```  
HRESULT Initialize(
   [in] boolean bAllowIManagementObjectQI
); 
```  
## <a name="parameters"></a><span data-ttu-id="da7d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da7d4-106">Parameters</span></span>

`bAllowIManagementObjectQI`   
<span data-ttu-id="da7d4-107">[in] `true` pour indiquer que les appels à destination de QueryInterface sur les objets WMI sont autorisées ; `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="da7d4-107">[in] `true` to indicate that calls to QueryInterface on WMI objects are allowed; `false` otherwise.</span></span>

## <a name="return-value"></a><span data-ttu-id="da7d4-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="da7d4-108">Return value</span></span>

<span data-ttu-id="da7d4-109">La fonction retourne toujours `S_OK` (0).</span><span class="sxs-lookup"><span data-stu-id="da7d4-109">The function always returns `S_OK` (0).</span></span>
  
## <a name="requirements"></a><span data-ttu-id="da7d4-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="da7d4-110">Requirements</span></span>  
 <span data-ttu-id="da7d4-111">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="da7d4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da7d4-112">**En-tête :** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="da7d4-112">**Header:** WMINet_Utils.def</span></span>  
  
 <span data-ttu-id="da7d4-113">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="da7d4-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da7d4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da7d4-114">See also</span></span>
- [<span data-ttu-id="da7d4-115">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="da7d4-115">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
