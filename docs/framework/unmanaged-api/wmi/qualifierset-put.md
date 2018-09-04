---
title: QualifierSet_Put (fonction) (référence des API non managées)
description: La fonction QualifierSet_Put écrit qualificateur nommé et sa valeur.
ms.date: 11/06/2017
api_name:
- QualifierSet_Put
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_Put
helpviewer_keywords:
- QualifierSet_Put function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7b2e1b08d1091e482c6b02fe015a58219ff80768
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43517559"
---
# <a name="qualifiersetput-function"></a><span data-ttu-id="01210-103">QualifierSet_Put (fonction)</span><span class="sxs-lookup"><span data-stu-id="01210-103">QualifierSet_Put function</span></span>
<span data-ttu-id="01210-104">Écrit la valeur et le qualificateur nommés.</span><span class="sxs-lookup"><span data-stu-id="01210-104">Writes the named qualifier and value.</span></span> <span data-ttu-id="01210-105">Le nouveau qualificateur remplace la valeur précédente du même nom.</span><span class="sxs-lookup"><span data-stu-id="01210-105">The new qualifier overwrites the previous value of the same name.</span></span> <span data-ttu-id="01210-106">Si le qualificateur n’existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="01210-106">If the qualifier does not exist, it is created.</span></span> 

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="01210-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01210-107">Syntax</span></span>  
  
```  
HRESULT QualifierSet_Put (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LPCWSTR              wszName,
   [in] VARIANT*             pVal,
   [in] LONG                 lFlavor
); 
```  

## <a name="parameters"></a><span data-ttu-id="01210-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01210-108">Parameters</span></span>

`vFunc`   
<span data-ttu-id="01210-109">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="01210-109">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="01210-110">[in] Un pointeur vers un [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span><span class="sxs-lookup"><span data-stu-id="01210-110">[in] A pointer to an [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span></span>

`wszName`   
<span data-ttu-id="01210-111">[in] Le nom du qualificateur à écrire.</span><span class="sxs-lookup"><span data-stu-id="01210-111">[in] The name of the qualifier to write.</span></span>

<span data-ttu-id="01210-112">`pVal` [in] Un pointeur vers une valide `VARIANT` qui contient le qualificateur à écrire.</span><span class="sxs-lookup"><span data-stu-id="01210-112">`pVal` [in] A pointer to a valid `VARIANT` that contains the qualifier to write.</span></span> <span data-ttu-id="01210-113">Ce paramètre ne peut pas être `null`.</span><span class="sxs-lookup"><span data-stu-id="01210-113">This parameter cannot be `null`.</span></span>

<span data-ttu-id="01210-114">`lFlavor` [in] Une des constantes suivantes qui définit les types de qualificateurs souhaitée pour ce qualificateur.</span><span class="sxs-lookup"><span data-stu-id="01210-114">`lFlavor` [in] One of the following constants that defines the desired qualifier flavors for this qualifier.</span></span> <span data-ttu-id="01210-115">La valeur par défaut est `WBEM_FLAVOR_OVERRIDABLE` (0).</span><span class="sxs-lookup"><span data-stu-id="01210-115">The default value is `WBEM_FLAVOR_OVERRIDABLE` (0).</span></span>

|<span data-ttu-id="01210-116">Constante</span><span class="sxs-lookup"><span data-stu-id="01210-116">Constant</span></span>  |<span data-ttu-id="01210-117">Value</span><span class="sxs-lookup"><span data-stu-id="01210-117">Value</span></span>  |<span data-ttu-id="01210-118">Description</span><span class="sxs-lookup"><span data-stu-id="01210-118">Description</span></span>  |
|---------|---------|---------|
| `WBEM_FLAVOR_OVERRIDABLE` | <span data-ttu-id="01210-119">0</span><span class="sxs-lookup"><span data-stu-id="01210-119">0</span></span> | <span data-ttu-id="01210-120">Le qualificateur peut être substitué dans une classe dérivée ou une instance.</span><span class="sxs-lookup"><span data-stu-id="01210-120">The qualifier can be overridden in a derived class or instance.</span></span> <span data-ttu-id="01210-121">**Il s’agit de la valeur par défaut.**</span><span class="sxs-lookup"><span data-stu-id="01210-121">**This is the default value.**</span></span> |
| `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE` | <span data-ttu-id="01210-122">1</span><span class="sxs-lookup"><span data-stu-id="01210-122">1</span></span> | <span data-ttu-id="01210-123">Le qualificateur est propagé aux instances.</span><span class="sxs-lookup"><span data-stu-id="01210-123">The qualifier is propagated to instances.</span></span> |
| `WBEM_FLAVOR_GLAG_PROPAGATE_TO_DERIVED_CLASS` | <span data-ttu-id="01210-124">2</span><span class="sxs-lookup"><span data-stu-id="01210-124">2</span></span> | <span data-ttu-id="01210-125">Le qualificateur est propagé aux classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="01210-125">The qualifier is propagated to derived classes.</span></span> |
| <span data-ttu-id="01210-126">' WBEM_FLAVOR_NOT_OVERRIDABLE</span><span class="sxs-lookup"><span data-stu-id="01210-126">\`WBEM_FLAVOR_NOT_OVERRIDABLE</span></span> | <span data-ttu-id="01210-127">0x10</span><span class="sxs-lookup"><span data-stu-id="01210-127">0x10</span></span> | <span data-ttu-id="01210-128">Le qualificateur ne peut pas être écrasé dans une classe ou une instance dérivée.</span><span class="sxs-lookup"><span data-stu-id="01210-128">The qualifier cannot be overridden in a derived class or instance.</span></span> |
| <span data-ttu-id="01210-129">' WBEM_FLAVOR_AMENDED</span><span class="sxs-lookup"><span data-stu-id="01210-129">\`WBEM_FLAVOR_AMENDED</span></span> | <span data-ttu-id="01210-130">0 x 80</span><span class="sxs-lookup"><span data-stu-id="01210-130">0x80</span></span> | <span data-ttu-id="01210-131">Le qualificateur est localisé.</span><span class="sxs-lookup"><span data-stu-id="01210-131">The qualifier is localized.</span></span> |

## <a name="return-value"></a><span data-ttu-id="01210-132">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="01210-132">Return value</span></span>

<span data-ttu-id="01210-133">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="01210-133">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="01210-134">Constante</span><span class="sxs-lookup"><span data-stu-id="01210-134">Constant</span></span>  |<span data-ttu-id="01210-135">Value</span><span class="sxs-lookup"><span data-stu-id="01210-135">Value</span></span>  |<span data-ttu-id="01210-136">Description</span><span class="sxs-lookup"><span data-stu-id="01210-136">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_CANNOT_BE_KEY` | <span data-ttu-id="01210-137">0x8004101f</span><span class="sxs-lookup"><span data-stu-id="01210-137">0x8004101f</span></span> | <span data-ttu-id="01210-138">Il y a une tentative non conforme pour spécifier le **clé** qualificateur sur une propriété qui ne peut pas être une clé.</span><span class="sxs-lookup"><span data-stu-id="01210-138">There was an illegal attempt to specify the **Key** qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="01210-139">Les clés sont spécifiés om c ; définition ass pour un objet et ne peut pas être modifiée sur une base par instance.</span><span class="sxs-lookup"><span data-stu-id="01210-139">The keys are specified om tje c;ass definition for an object and cannot be altered on a per-instance basis.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="01210-140">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="01210-140">0x80041008</span></span> | <span data-ttu-id="01210-141">Un paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="01210-141">A parameter is not valid.</span></span> |
| `WBEM_E_INVALID_QUALIFIER_TYPE` | <span data-ttu-id="01210-142">0x80041029</span><span class="sxs-lookup"><span data-stu-id="01210-142">0x80041029</span></span> | <span data-ttu-id="01210-143">Le `pVal` paramètre n’est pas un type de qualificateur conforme.</span><span class="sxs-lookup"><span data-stu-id="01210-143">The `pVal` parameter is not of a legal qualifier type.</span></span> |
| `WBEM_E_OVERRIDE_NOT_ALLOWED` | <span data-ttu-id="01210-144">0x8004101a</span><span class="sxs-lookup"><span data-stu-id="01210-144">0x8004101a</span></span> | <span data-ttu-id="01210-145">Il n’est pas possible d’appeler le `QualifierSet_Put` substitutions des méthodes sur le qualificateur parce que l’objet propriétaire n’autorise pas.</span><span class="sxs-lookup"><span data-stu-id="01210-145">It is not possible to call the `QualifierSet_Put` method on the qualifier because the owning object does not permit overrides.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="01210-146">0</span><span class="sxs-lookup"><span data-stu-id="01210-146">0</span></span> | <span data-ttu-id="01210-147">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="01210-147">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="01210-148">Notes</span><span class="sxs-lookup"><span data-stu-id="01210-148">Remarks</span></span>

<span data-ttu-id="01210-149">Cette fonction encapsule un appel à la [IWbemQualifierSet::Put](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-put) (méthode).</span><span class="sxs-lookup"><span data-stu-id="01210-149">This function wraps a call to the [IWbemQualifierSet::Put](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="01210-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01210-150">Requirements</span></span>  
 <span data-ttu-id="01210-151">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="01210-151">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="01210-152">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="01210-152">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="01210-153">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="01210-153">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01210-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01210-154">See also</span></span>  
[<span data-ttu-id="01210-155">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="01210-155">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
