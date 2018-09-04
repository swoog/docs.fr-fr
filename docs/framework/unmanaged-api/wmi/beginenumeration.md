---
title: BeginEnumeration, fonction (référence des API non managées)
description: La fonction BeginEnumeration réinitialise l’énumérateur au début de l’énumération
ms.date: 11/06/2017
api_name:
- BeginEnumeration
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- BeginEnumeration
helpviewer_keywords:
- BeginEnumeration function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 08406f7d93671b406b3c7cd8719a7a0e5e423184
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43523500"
---
# <a name="beginenumeration-function"></a><span data-ttu-id="ab1db-103">BeginEnumeration, fonction</span><span class="sxs-lookup"><span data-stu-id="ab1db-103">BeginEnumeration function</span></span>
<span data-ttu-id="ab1db-104">Réinitialise l’énumérateur au début de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="ab1db-104">Resets an enumerator back to the beginning of the enumeration.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="ab1db-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab1db-105">Syntax</span></span>  
  
```  
HRESULT BeginEnumeration (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LONG              lEnumFlags
); 
```  

## <a name="parameters"></a><span data-ttu-id="ab1db-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab1db-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="ab1db-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ab1db-107">[in] This parameter is unused.</span></span>

<span data-ttu-id="ab1db-108">`ptr` [in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="ab1db-108">`ptr` [in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`lEnumFlags`  
<span data-ttu-id="ab1db-109">[in] Une combinaison au niveau du bit des indicateurs ou des valeurs décrites dans le [notes](#remarks) section qui contrôle les propriétés incluses dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="ab1db-109">[in] A bitwise combination of the flags or values described in the [Remarks](#remarks) section that controls the properties included in the enumeration.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab1db-110">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ab1db-110">Return value</span></span>

<span data-ttu-id="ab1db-111">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="ab1db-111">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="ab1db-112">Constante</span><span class="sxs-lookup"><span data-stu-id="ab1db-112">Constant</span></span>  |<span data-ttu-id="ab1db-113">Value</span><span class="sxs-lookup"><span data-stu-id="ab1db-113">Value</span></span>  |<span data-ttu-id="ab1db-114">Description</span><span class="sxs-lookup"><span data-stu-id="ab1db-114">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="ab1db-115">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="ab1db-115">0x80041008</span></span> | <span data-ttu-id="ab1db-116">La combinaison d’indicateurs dans `lEnumFlags` n’est pas valide ou non valide argument a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="ab1db-116">The combination of flags in `lEnumFlags` is invalid, or an invalid argument was specified.</span></span> |
|`WBEM_E_UNEXPECTED` | <span data-ttu-id="ab1db-117">0x8004101d</span><span class="sxs-lookup"><span data-stu-id="ab1db-117">0x8004101d</span></span> | <span data-ttu-id="ab1db-118">Un deuxième appel à `BeginEnumeration` a été effectuée sans appel intermédiaire à [ `EndEnumeration` ](endenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="ab1db-118">A second call to `BeginEnumeration` was made without an intervening call to [`EndEnumeration`](endenumeration.md).</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="ab1db-119">0x80041006</span><span class="sxs-lookup"><span data-stu-id="ab1db-119">0x80041006</span></span> | <span data-ttu-id="ab1db-120">Pas assez de mémoire est disponible pour commencer une nouvelle énumération.</span><span class="sxs-lookup"><span data-stu-id="ab1db-120">Not enough memory is available to begin a new enumeration.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="ab1db-121">0</span><span class="sxs-lookup"><span data-stu-id="ab1db-121">0</span></span> | <span data-ttu-id="ab1db-122">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="ab1db-122">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="ab1db-123">Notes</span><span class="sxs-lookup"><span data-stu-id="ab1db-123">Remarks</span></span>

<span data-ttu-id="ab1db-124">Cette fonction encapsule un appel à la [IWbemClassObject::BeginEnumeration](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ab1db-124">This function wraps a call to the [IWbemClassObject::BeginEnumeration](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) method.</span></span>

<span data-ttu-id="ab1db-125">Les indicateurs qui peuvent être passés en tant que le `lEnumFlags` argument sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code.</span><span class="sxs-lookup"><span data-stu-id="ab1db-125">The flags that can be passed as the `lEnumFlags` argument are defined in the *WbemCli.h* header file, or you can define them as constants in your code.</span></span>  <span data-ttu-id="ab1db-126">Vous pouvez combiner un indicateur de chaque groupe avec n’importe quel indicateur à partir d’un autre groupe.</span><span class="sxs-lookup"><span data-stu-id="ab1db-126">You can combine one flag from each group with any flag from any other group.</span></span> <span data-ttu-id="ab1db-127">Toutefois, les indicateurs à partir du même groupe sont mutuellement exclusifs.</span><span class="sxs-lookup"><span data-stu-id="ab1db-127">However, flags from the same group are mutually exclusive.</span></span> 

<span data-ttu-id="ab1db-128">**Groupe 1**</span><span class="sxs-lookup"><span data-stu-id="ab1db-128">**Group 1**</span></span>

|<span data-ttu-id="ab1db-129">Constante</span><span class="sxs-lookup"><span data-stu-id="ab1db-129">Constant</span></span>  |<span data-ttu-id="ab1db-130">Value</span><span class="sxs-lookup"><span data-stu-id="ab1db-130">Value</span></span>  |<span data-ttu-id="ab1db-131">Description</span><span class="sxs-lookup"><span data-stu-id="ab1db-131">Description</span></span>  |
|---------|---------|---------|
|`WBEM_FLAG_KEYS_ONLY` | <span data-ttu-id="ab1db-132">0 x 4</span><span class="sxs-lookup"><span data-stu-id="ab1db-132">0x4</span></span> | <span data-ttu-id="ab1db-133">Inclure les propriétés qui constituent la clé uniquement.</span><span class="sxs-lookup"><span data-stu-id="ab1db-133">Include properties that constitute the key only.</span></span> |
|`WBEM_FLAG_REFS_ONLY` | <span data-ttu-id="ab1db-134">0 x 8</span><span class="sxs-lookup"><span data-stu-id="ab1db-134">0x8</span></span> | <span data-ttu-id="ab1db-135">Inclure les propriétés qui sont des références d’objet.</span><span class="sxs-lookup"><span data-stu-id="ab1db-135">Include properties that are object references only.</span></span> |

<span data-ttu-id="ab1db-136">**Groupe 2**</span><span class="sxs-lookup"><span data-stu-id="ab1db-136">**Group 2**</span></span>

<span data-ttu-id="ab1db-137">Constante</span><span class="sxs-lookup"><span data-stu-id="ab1db-137">Constant</span></span>  |<span data-ttu-id="ab1db-138">Value</span><span class="sxs-lookup"><span data-stu-id="ab1db-138">Value</span></span>  |<span data-ttu-id="ab1db-139">Description</span><span class="sxs-lookup"><span data-stu-id="ab1db-139">Description</span></span>  |
|---------|---------|---------|
|`WBEM_FLAG_SYSTEM_ONLY` | <span data-ttu-id="ab1db-140">0 x 30</span><span class="sxs-lookup"><span data-stu-id="ab1db-140">0x30</span></span> | <span data-ttu-id="ab1db-141">Limiter l’énumération aux propriétés du système.</span><span class="sxs-lookup"><span data-stu-id="ab1db-141">Limit the enumeration to system properties only.</span></span> |
|`WBEM_FLAG_NONSYSTEM_ONLY` | <span data-ttu-id="ab1db-142">0 x 40</span><span class="sxs-lookup"><span data-stu-id="ab1db-142">0x40</span></span> | <span data-ttu-id="ab1db-143">Les propriétés locales et propagées mais exclut les propriétés système à partir de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="ab1db-143">Include local and propagated properties but exclude system properties from the enumeration.</span></span> |

<span data-ttu-id="ab1db-144">Pour les classes :</span><span class="sxs-lookup"><span data-stu-id="ab1db-144">For classes:</span></span>

<span data-ttu-id="ab1db-145">Constante</span><span class="sxs-lookup"><span data-stu-id="ab1db-145">Constant</span></span>  |<span data-ttu-id="ab1db-146">Value</span><span class="sxs-lookup"><span data-stu-id="ab1db-146">Value</span></span>  |<span data-ttu-id="ab1db-147">Description</span><span class="sxs-lookup"><span data-stu-id="ab1db-147">Description</span></span>  |
|---------|---------|---------|
|`WBEM_FLAG_CLASS_OVERRIDES_ONLY` | <span data-ttu-id="ab1db-148">0 x 100</span><span class="sxs-lookup"><span data-stu-id="ab1db-148">0x100</span></span> | <span data-ttu-id="ab1db-149">Limiter l’énumération aux propriétés de substitution dans la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="ab1db-149">Limit the enumeration to properties overridden in the class definition.</span></span> |
|`WBEM_FLAG_CLASS_LOCAL_AND_OVERRIDES` | <span data-ttu-id="ab1db-150">0 x 100</span><span class="sxs-lookup"><span data-stu-id="ab1db-150">0x100</span></span> | <span data-ttu-id="ab1db-151">Limiter l’énumération aux propriétés de substitution dans la définition de classe en cours et de nouvelles propriétés définies dans la classe.</span><span class="sxs-lookup"><span data-stu-id="ab1db-151">Limit the enumeration to properties overridden in the current class definition and to new properties defined in the class.</span></span> |
| `WBEM_MASK_CLASS_CONDITION` | <span data-ttu-id="ab1db-152">0 x 300</span><span class="sxs-lookup"><span data-stu-id="ab1db-152">0x300</span></span> | <span data-ttu-id="ab1db-153">Un masque (au lieu d’un indicateur) à appliquer par rapport à un `lEnumFlags` valeur à vérifier si `WBEM_FLAG_CLASS_OVERRIDES_ONLY` ou `WBEM_FLAG_CLASS_LOCAL_AND_OVERRIDES` est définie.</span><span class="sxs-lookup"><span data-stu-id="ab1db-153">A mask (rather than a flag) to apply against a `lEnumFlags` value to check if either `WBEM_FLAG_CLASS_OVERRIDES_ONLY` or `WBEM_FLAG_CLASS_LOCAL_AND_OVERRIDES` is set.</span></span> |
| `WBEM_FLAG_LOCAL_ONLY` | <span data-ttu-id="ab1db-154">0x10</span><span class="sxs-lookup"><span data-stu-id="ab1db-154">0x10</span></span> | <span data-ttu-id="ab1db-155">Limiter l’énumération aux propriétés qui sont définies ou modifiées dans la classe elle-même.</span><span class="sxs-lookup"><span data-stu-id="ab1db-155">Limit the enumeration to properties that are defined or modified in the class itself.</span></span> |
| `WBEM_FLAG_PROPAGATED_ONLY` |  <span data-ttu-id="ab1db-156">0 x 20</span><span class="sxs-lookup"><span data-stu-id="ab1db-156">0x20</span></span> | <span data-ttu-id="ab1db-157">Limiter l’énumération de propriétés qui sont héritées de classes de base.</span><span class="sxs-lookup"><span data-stu-id="ab1db-157">Limit the enumeration to properties that are inherited from base classes.</span></span> |

<span data-ttu-id="ab1db-158">Pour les instances :</span><span class="sxs-lookup"><span data-stu-id="ab1db-158">For instances:</span></span>

<span data-ttu-id="ab1db-159">Constante</span><span class="sxs-lookup"><span data-stu-id="ab1db-159">Constant</span></span>  |<span data-ttu-id="ab1db-160">Value</span><span class="sxs-lookup"><span data-stu-id="ab1db-160">Value</span></span>  |<span data-ttu-id="ab1db-161">Description</span><span class="sxs-lookup"><span data-stu-id="ab1db-161">Description</span></span>  |
|---------|---------|---------|
| `WBEM_FLAG_LOCAL_ONLY` | <span data-ttu-id="ab1db-162">0x10</span><span class="sxs-lookup"><span data-stu-id="ab1db-162">0x10</span></span> | <span data-ttu-id="ab1db-163">Limiter l’énumération aux propriétés qui sont définies ou modifiées dans la classe elle-même.</span><span class="sxs-lookup"><span data-stu-id="ab1db-163">Limit the enumeration to properties that are defined or modified in the class itself.</span></span> |
| `WBEM_FLAG_PROPAGATED_ONLY` |  <span data-ttu-id="ab1db-164">0 x 20</span><span class="sxs-lookup"><span data-stu-id="ab1db-164">0x20</span></span> | <span data-ttu-id="ab1db-165">Limiter l’énumération de propriétés qui sont héritées de classes de base.</span><span class="sxs-lookup"><span data-stu-id="ab1db-165">Limit the enumeration to properties that are inherited from base classes.</span></span> |


## <a name="requirements"></a><span data-ttu-id="ab1db-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab1db-166">Requirements</span></span>  
 <span data-ttu-id="ab1db-167">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab1db-167">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab1db-168">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="ab1db-168">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="ab1db-169">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="ab1db-169">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab1db-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab1db-170">See also</span></span>  
[<span data-ttu-id="ab1db-171">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="ab1db-171">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
