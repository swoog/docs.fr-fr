---
title: VerifyClientKey (fonction) (référence des API non managées)
description: La fonction VerifyClientKey garantit que la clé du client a la sécurité correcte.
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
ms.openlocfilehash: 47fee26a0c4c25e4bff5bca94e5e26daaf98cccd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59214713"
---
# <a name="verifyclientkey-function"></a><span data-ttu-id="a4e00-103">VerifyClientKey (fonction)</span><span class="sxs-lookup"><span data-stu-id="a4e00-103">VerifyClientKey function</span></span>
<span data-ttu-id="a4e00-104">Garantit que la clé du client offre une sécurité correcte.</span><span class="sxs-lookup"><span data-stu-id="a4e00-104">Ensures that the client key has the correct security.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="a4e00-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4e00-105">Syntax</span></span>  
  
```  
LONG VerifyClientKey(); 
```  

## <a name="return-value"></a><span data-ttu-id="a4e00-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a4e00-106">Return value</span></span>

<span data-ttu-id="a4e00-107">Si la fonction réussit, la valeur de retour est `ERROR_SUCCESS` (0).</span><span class="sxs-lookup"><span data-stu-id="a4e00-107">If the function succeeds, the return value is `ERROR_SUCCESS` (0).</span></span>

<span data-ttu-id="a4e00-108">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans *WinError.h*.</span><span class="sxs-lookup"><span data-stu-id="a4e00-108">If the function fails, the return value is a non-zero error code defined in *WinError.h*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e00-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4e00-109">Requirements</span></span>  
 <span data-ttu-id="a4e00-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a4e00-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a4e00-111">**En-tête :** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="a4e00-111">**Header:** WMINet_Utils.def</span></span>  
  
 <span data-ttu-id="a4e00-112">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a4e00-112">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a4e00-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4e00-113">See also</span></span>

- [<span data-ttu-id="a4e00-114">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="a4e00-114">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
