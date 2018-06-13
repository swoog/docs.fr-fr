---
title: VerifyClientKey (fonction) (référence des API non managées)
description: La fonction VerifyClientKey garantit que la clé du client a la sécurité appropriée.
ms.date: 11/06/2017
api_name:
- VerifyClientKey
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- VerifyClientKey
helpviewer_keywords:
- VerifyClientKey function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ea8a74633d3e950f6cf7ba87c00a9efa45206545
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33459562"
---
# <a name="verifyclientkey-function"></a><span data-ttu-id="baf8e-103">VerifyClientKey (fonction)</span><span class="sxs-lookup"><span data-stu-id="baf8e-103">VerifyClientKey function</span></span>
<span data-ttu-id="baf8e-104">Garantit que la clé du client dispose de la sécurité appropriée.</span><span class="sxs-lookup"><span data-stu-id="baf8e-104">Ensures that the client key has the correct security.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="baf8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="baf8e-105">Syntax</span></span>  
  
```  
LONG VerifyClientKey(); 
```  

## <a name="return-value"></a><span data-ttu-id="baf8e-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="baf8e-106">Return value</span></span>

<span data-ttu-id="baf8e-107">Si la fonction réussit, la valeur de retour est `ERROR_SUCCESS` (0).</span><span class="sxs-lookup"><span data-stu-id="baf8e-107">If the function succeeds, the return value is `ERROR_SUCCESS` (0).</span></span>

<span data-ttu-id="baf8e-108">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans *WinError.h*.</span><span class="sxs-lookup"><span data-stu-id="baf8e-108">If the function fails, the return value is a non-zero error code defined in *WinError.h*.</span></span>

## <a name="requirements"></a><span data-ttu-id="baf8e-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="baf8e-109">Requirements</span></span>  
 <span data-ttu-id="baf8e-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="baf8e-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="baf8e-111">**En-tête :** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="baf8e-111">**Header:** WMINet_Utils.def</span></span>  
  
 <span data-ttu-id="baf8e-112">**Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="baf8e-112">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="baf8e-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="baf8e-113">See also</span></span>  
[<span data-ttu-id="baf8e-114">WMI et les compteurs de Performance (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="baf8e-114">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
