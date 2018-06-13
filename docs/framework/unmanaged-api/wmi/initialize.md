---
title: Initialiser (fonction) (référence des API non managées)
description: La fonction d’initialisation effectue une initialisation WMI.
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
ms.openlocfilehash: 01de35a0cd4d359dfba0375a85fbce017e44b9f8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455753"
---
# <a name="initialize-function"></a><span data-ttu-id="32fb5-103">Initialiser (fonction)</span><span class="sxs-lookup"><span data-stu-id="32fb5-103">Initialize function</span></span>
<span data-ttu-id="32fb5-104">Effectue l’initialisation de WMI.</span><span class="sxs-lookup"><span data-stu-id="32fb5-104">Performs WMI initialization.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="32fb5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32fb5-105">Syntax</span></span> 
```  
HRESULT Initialize(
   [in] boolean bAllowIManagementObjectQI
); 
```  
## <a name="parameters"></a><span data-ttu-id="32fb5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32fb5-106">Parameters</span></span>

`bAllowIManagementObjectQI`   
<span data-ttu-id="32fb5-107">[in] `true` pour indiquer que les appels à destination de QueryInterface sur les objets WMI sont autorisées ; `false` dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="32fb5-107">[in] `true` to indicate that calls to QueryInterface on WMI objects are allowed; `false` otherwise.</span></span>

## <a name="return-value"></a><span data-ttu-id="32fb5-108">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="32fb5-108">Return value</span></span>

<span data-ttu-id="32fb5-109">La fonction retourne toujours `S_OK` (0).</span><span class="sxs-lookup"><span data-stu-id="32fb5-109">The function always returns `S_OK` (0).</span></span>
  
## <a name="requirements"></a><span data-ttu-id="32fb5-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="32fb5-110">Requirements</span></span>  
 <span data-ttu-id="32fb5-111">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="32fb5-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="32fb5-112">**En-tête :** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="32fb5-112">**Header:** WMINet_Utils.def</span></span>  
  
 <span data-ttu-id="32fb5-113">**Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="32fb5-113">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32fb5-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32fb5-114">See also</span></span>  
[<span data-ttu-id="32fb5-115">WMI et les compteurs de Performance (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="32fb5-115">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
