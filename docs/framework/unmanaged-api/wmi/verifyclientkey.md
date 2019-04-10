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
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59214713"
---
# <a name="verifyclientkey-function"></a><span data-ttu-id="ced43-103">VerifyClientKey (fonction)</span><span class="sxs-lookup"><span data-stu-id="ced43-103">VerifyClientKey function</span></span>
<span data-ttu-id="ced43-104">Garantit que la clé du client offre une sécurité correcte.</span><span class="sxs-lookup"><span data-stu-id="ced43-104">Ensures that the client key has the correct security.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="ced43-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ced43-105">Syntax</span></span>  
  
```  
LONG VerifyClientKey(); 
```  

## <a name="return-value"></a><span data-ttu-id="ced43-106">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ced43-106">Return value</span></span>

<span data-ttu-id="ced43-107">Si la fonction réussit, la valeur de retour est `ERROR_SUCCESS` (0).</span><span class="sxs-lookup"><span data-stu-id="ced43-107">If the function succeeds, the return value is `ERROR_SUCCESS` (0).</span></span>

<span data-ttu-id="ced43-108">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans *WinError.h*.</span><span class="sxs-lookup"><span data-stu-id="ced43-108">If the function fails, the return value is a non-zero error code defined in *WinError.h*.</span></span>

## <a name="requirements"></a><span data-ttu-id="ced43-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ced43-109">Requirements</span></span>  
 <span data-ttu-id="ced43-110">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ced43-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ced43-111">**En-tête :** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="ced43-111">**Header:** WMINet_Utils.def</span></span>  
  
 **<span data-ttu-id="ced43-112">Versions de .NET Framework :</span><span class="sxs-lookup"><span data-stu-id="ced43-112">.NET Framework Versions:</span></span>** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ced43-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ced43-113">See also</span></span>

- [<span data-ttu-id="ced43-114">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="ced43-114">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
