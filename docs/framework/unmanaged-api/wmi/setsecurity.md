---
title: SetSecurity (fonction) (référence des API non managées)
description: La fonction SetSecurity récupère le jeton d’emprunt d’identité du thread actif.
ms.date: 11/06/2017
api_name:
- SetSecurity
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- SetSecurity
helpviewer_keywords:
- SetSecurity function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5cecd8538b8f2b5d04cb9f1822751661ce9f8728
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636215"
---
# <a name="setsecurity-function"></a><span data-ttu-id="9fc7b-103">SetSecurity (fonction)</span><span class="sxs-lookup"><span data-stu-id="9fc7b-103">SetSecurity function</span></span>

<span data-ttu-id="9fc7b-104">Récupère le jeton d’emprunt d’identité associé au thread actif.</span><span class="sxs-lookup"><span data-stu-id="9fc7b-104">Retrieves the impersonation token associated with the current thread.</span></span> 

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="9fc7b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fc7b-105">Syntax</span></span>

```
HRESULT SetSecurity (
   [out] boolean* pNeedToReset, 
   [out] HANDLE* pCurrentThreadToken
); 
```

## <a name="parameters"></a><span data-ttu-id="9fc7b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fc7b-106">Parameters</span></span>

`pNeedToReset`\
<span data-ttu-id="9fc7b-107">[out] Lorsque la fonction est retournée, contient un pointeur vers un `boolean` qui indique si le jeton doit être réinitialisé en appelant le [ResetSecurity](resetsecurity.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="9fc7b-107">[out] When the function returns, contains a pointer to a `boolean` that indicates whether the token should be reset by calling the [ResetSecurity](resetsecurity.md) function.</span></span>

`token`\
<span data-ttu-id="9fc7b-108">[out] Lorsque la fonction est retournée, contient un pointeur vers le handle du jeton d’emprunt d’identité associé au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="9fc7b-108">[out] When the function returns, contains a pointer to the handle of the impersonation token associated with the current thread.</span></span> <span data-ttu-id="9fc7b-109">Sa valeur peut être `null` s’il n’existe aucun jeton associé au thread actuel.</span><span class="sxs-lookup"><span data-stu-id="9fc7b-109">Its value can be `null` if there is no token associated with the current thread.</span></span> 

## <a name="return-value"></a><span data-ttu-id="9fc7b-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9fc7b-110">Return value</span></span>

<span data-ttu-id="9fc7b-111">Si la fonction réussit, la valeur de retour est `S_OK` (0).</span><span class="sxs-lookup"><span data-stu-id="9fc7b-111">If the function succeeds, the return value is `S_OK` (0).</span></span>

<span data-ttu-id="9fc7b-112">Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="9fc7b-112">If the function fails, the return value is a non-zero error code.</span></span> <span data-ttu-id="9fc7b-113">Pour obtenir les informations d’erreur étendues, appelez le [GetErrorInfo](geterrorinfo.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="9fc7b-113">To get extended error information, call the [GetErrorInfo](geterrorinfo.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc7b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fc7b-114">Requirements</span></span>

 <span data-ttu-id="9fc7b-115">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9fc7b-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

 <span data-ttu-id="9fc7b-116">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="9fc7b-116">**Header:** WMINet_Utils.idl</span></span>

 <span data-ttu-id="9fc7b-117">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="9fc7b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="9fc7b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fc7b-118">See also</span></span>

- [<span data-ttu-id="9fc7b-119">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="9fc7b-119">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
