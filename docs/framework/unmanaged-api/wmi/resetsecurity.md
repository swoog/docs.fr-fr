---
title: ResetSecurity (fonction) (référence des API non managées)
description: La fonction ResetSecurity assigne un jeton d’emprunt d’identité pour le thread actuel.
ms.date: 11/06/2017
api_name:
- ResetSecurity
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- ResetSecurity
helpviewer_keywords:
- ResetSecurity function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 31e42b9e39ddb43025e18888572c394d742e38cf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33457904"
---
# <a name="resetsecurity-function"></a><span data-ttu-id="8aaee-103">ResetSecurity (fonction)</span><span class="sxs-lookup"><span data-stu-id="8aaee-103">ResetSecurity function</span></span>
<span data-ttu-id="8aaee-104">Assigne le jeton d’emprunt d’identité fournie pour le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="8aaee-104">Assigns the supplied impersonation token to the current thread.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="8aaee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8aaee-105">Syntax</span></span>  
  
```  
HRESULT ResetSecurity (
   [in] HANDLE token
); 
```  

## <a name="parameters"></a><span data-ttu-id="8aaee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8aaee-106">Parameters</span></span>

`token`  
<span data-ttu-id="8aaee-107">[in] Le jeton d’emprunt d’identité à associer au thread en cours.</span><span class="sxs-lookup"><span data-stu-id="8aaee-107">[in] The impersonation token to associate with the current thread.</span></span> <span data-ttu-id="8aaee-108">Sa valeur peut être `null`.</span><span class="sxs-lookup"><span data-stu-id="8aaee-108">Its value can be `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="8aaee-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8aaee-109">Return value</span></span>

<span data-ttu-id="8aaee-110">Si la fonction réussit, la valeur de retour est `S_OK` (0).</span><span class="sxs-lookup"><span data-stu-id="8aaee-110">If the function succeeds, the return value is `S_OK` (0).</span></span>

<span data-ttu-id="8aaee-111">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="8aaee-111">If the function fails, the return value is a non-zero error code.</span></span> <span data-ttu-id="8aaee-112">Pour obtenir des informations d’erreur plus complètes, appelez le [GetErrorInfo](geterrorinfo.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="8aaee-112">To get extended error information, call the [GetErrorInfo](geterrorinfo.md) function.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="8aaee-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8aaee-113">Requirements</span></span>  
 <span data-ttu-id="8aaee-114">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8aaee-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8aaee-115">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="8aaee-115">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="8aaee-116">**Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8aaee-116">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8aaee-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8aaee-117">See also</span></span>  
[<span data-ttu-id="8aaee-118">WMI et les compteurs de Performance (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="8aaee-118">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
