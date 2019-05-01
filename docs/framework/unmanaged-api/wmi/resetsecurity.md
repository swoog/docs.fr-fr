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
ms.openlocfilehash: e937690c184d810549e8ab11ef1fc2273a45c5f5
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62049243"
---
# <a name="resetsecurity-function"></a><span data-ttu-id="ebe71-103">ResetSecurity (fonction)</span><span class="sxs-lookup"><span data-stu-id="ebe71-103">ResetSecurity function</span></span>
<span data-ttu-id="ebe71-104">Assigne le jeton d’emprunt d’identité fourni au thread actif.</span><span class="sxs-lookup"><span data-stu-id="ebe71-104">Assigns the supplied impersonation token to the current thread.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="ebe71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebe71-105">Syntax</span></span>  
  
```  
HRESULT ResetSecurity (
   [in] HANDLE token
); 
```  

## <a name="parameters"></a><span data-ttu-id="ebe71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebe71-106">Parameters</span></span>

`token`  
<span data-ttu-id="ebe71-107">[in] Le jeton d’emprunt d’identité à associer avec le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="ebe71-107">[in] The impersonation token to associate with the current thread.</span></span> <span data-ttu-id="ebe71-108">Sa valeur peut être `null`.</span><span class="sxs-lookup"><span data-stu-id="ebe71-108">Its value can be `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="ebe71-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ebe71-109">Return value</span></span>

<span data-ttu-id="ebe71-110">Si la fonction réussit, la valeur de retour est `S_OK` (0).</span><span class="sxs-lookup"><span data-stu-id="ebe71-110">If the function succeeds, the return value is `S_OK` (0).</span></span>

<span data-ttu-id="ebe71-111">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="ebe71-111">If the function fails, the return value is a non-zero error code.</span></span> <span data-ttu-id="ebe71-112">Pour obtenir les informations d’erreur étendues, appelez le [GetErrorInfo](geterrorinfo.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="ebe71-112">To get extended error information, call the [GetErrorInfo](geterrorinfo.md) function.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="ebe71-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebe71-113">Requirements</span></span>  
 <span data-ttu-id="ebe71-114">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ebe71-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ebe71-115">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="ebe71-115">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="ebe71-116">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="ebe71-116">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebe71-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe71-117">See also</span></span>

- [<span data-ttu-id="ebe71-118">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="ebe71-118">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
