---
title: Get, fonction (référence des API non managées)
description: La fonction Get récupère la valeur de propriété spécifiée.
ms.date: 11/06/2017
api_name:
- Get
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Get
helpviewer_keywords:
- Get function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7534d760f902f80d42c6c20c57a34d52012997a7
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57369654"
---
# <a name="get-function"></a><span data-ttu-id="cedaa-103">Get, fonction</span><span class="sxs-lookup"><span data-stu-id="cedaa-103">Get function</span></span>

<span data-ttu-id="cedaa-104">Récupère la valeur de propriété spécifiée si elle existe.</span><span class="sxs-lookup"><span data-stu-id="cedaa-104">Retrieves the specified property value if it exists.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="cedaa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cedaa-105">Syntax</span></span>

```
HRESULT Get (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName,
   [in] LONG              lFlags,
   [out] VARIANT*         pVal,
   [out] CIMTYPE*         pvtType,
   [out] LONG*            plFlavor
); 
```

## <a name="parameters"></a><span data-ttu-id="cedaa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cedaa-106">Parameters</span></span>

`vFunc`\
<span data-ttu-id="cedaa-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cedaa-107">[in] This parameter is unused.</span></span>

`ptr`\
<span data-ttu-id="cedaa-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="cedaa-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszName`\
<span data-ttu-id="cedaa-109">[in] Le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cedaa-109">[in] The name of the property.</span></span>

`lFlags`\
<span data-ttu-id="cedaa-110">[in] Réservée.</span><span class="sxs-lookup"><span data-stu-id="cedaa-110">[in] Reserved.</span></span> <span data-ttu-id="cedaa-111">Ce paramètre doit être 0.</span><span class="sxs-lookup"><span data-stu-id="cedaa-111">This parameter must be 0.</span></span>

`pVal`\
<span data-ttu-id="cedaa-112">[out] Si la fonction a été retournée avec succès, contient la valeur de la `wszName` propriété.</span><span class="sxs-lookup"><span data-stu-id="cedaa-112">[out] If the function returns successfully, contains the value of the `wszName` property.</span></span> <span data-ttu-id="cedaa-113">Le `pval` argument reçoit le type correct et la valeur du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="cedaa-113">The `pval` argument is assigned the correct type and value for the qualifier.</span></span>

`pvtType`\
<span data-ttu-id="cedaa-114">[out] Si la fonction a été retournée avec succès, contient un [constante de type CIM](/windows/desktop/api/wbemcli/ne-wbemcli-tag_cimtype_enumeration) qui indique le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="cedaa-114">[out] If the function returns successfully, contains a [CIM-type constant](/windows/desktop/api/wbemcli/ne-wbemcli-tag_cimtype_enumeration) that indicates the property type.</span></span> <span data-ttu-id="cedaa-115">Sa valeur peut également être `null`.</span><span class="sxs-lookup"><span data-stu-id="cedaa-115">Its value can also be `null`.</span></span> 

`plFlavor`\
<span data-ttu-id="cedaa-116">[out] Si la fonction a été retournée avec succès, reçoit des informations sur l’origine de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cedaa-116">[out] If the function returns successfully, receives information about the origin of the property.</span></span> <span data-ttu-id="cedaa-117">Sa valeur peut être `null`, ou l’une des constantes WBEM_FLAVOR_TYPE suivantes définies dans le *WbemCli.h* fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cedaa-117">Its value can be `null`, or one of the following WBEM_FLAVOR_TYPE constants defined in the *WbemCli.h* header file:</span></span> 

|<span data-ttu-id="cedaa-118">Constante</span><span class="sxs-lookup"><span data-stu-id="cedaa-118">Constant</span></span>  |<span data-ttu-id="cedaa-119">Value</span><span class="sxs-lookup"><span data-stu-id="cedaa-119">Value</span></span>  |<span data-ttu-id="cedaa-120">Description</span><span class="sxs-lookup"><span data-stu-id="cedaa-120">Description</span></span>  |
|---------|---------|---------|
| `WBEM_FLAVOR_ORIGIN_SYSTEM` | <span data-ttu-id="cedaa-121">0x40</span><span class="sxs-lookup"><span data-stu-id="cedaa-121">0x40</span></span> | <span data-ttu-id="cedaa-122">La propriété est une propriété système standard.</span><span class="sxs-lookup"><span data-stu-id="cedaa-122">The property is a standard system property.</span></span> |
| `WBEM_FLAVOR_ORIGIN_PROPAGATED` | <span data-ttu-id="cedaa-123">0x20</span><span class="sxs-lookup"><span data-stu-id="cedaa-123">0x20</span></span> | <span data-ttu-id="cedaa-124">Pour une classe : La propriété est héritée de la classe parente.</span><span class="sxs-lookup"><span data-stu-id="cedaa-124">For a class: The property is inherited from the parent class.</span></span> <br> <span data-ttu-id="cedaa-125">Pour une instance : La propriété, tandis que héritée de la classe parente, n’a pas été modifiée par l’instance.</span><span class="sxs-lookup"><span data-stu-id="cedaa-125">For an instance: The property, while inherited from the parent class, has not been modified by the instance.</span></span>  |
| `WBEM_FLAVOR_ORIGIN_LOCAL` | <span data-ttu-id="cedaa-126">0</span><span class="sxs-lookup"><span data-stu-id="cedaa-126">0</span></span> | <span data-ttu-id="cedaa-127">Pour une classe : La propriété appartient à la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="cedaa-127">For a class: The property belongs to the derived class.</span></span> <br> <span data-ttu-id="cedaa-128">Pour une instance : Cette propriété est modifiée par l’instance ; Autrement dit, une valeur a été fournie, ou un qualificateur a été ajouté ou modifié.</span><span class="sxs-lookup"><span data-stu-id="cedaa-128">For an instance: The property is modified by the instance; that is, a value was supplied, or a qualifier was added or modified.</span></span> |

## <a name="return-value"></a><span data-ttu-id="cedaa-129">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cedaa-129">Return value</span></span>

<span data-ttu-id="cedaa-130">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="cedaa-130">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="cedaa-131">Constante</span><span class="sxs-lookup"><span data-stu-id="cedaa-131">Constant</span></span>  |<span data-ttu-id="cedaa-132">Value</span><span class="sxs-lookup"><span data-stu-id="cedaa-132">Value</span></span>  |<span data-ttu-id="cedaa-133">Description</span><span class="sxs-lookup"><span data-stu-id="cedaa-133">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="cedaa-134">0x80041001</span><span class="sxs-lookup"><span data-stu-id="cedaa-134">0x80041001</span></span> | <span data-ttu-id="cedaa-135">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="cedaa-135">There has been a general failure.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="cedaa-136">0x80041008</span><span class="sxs-lookup"><span data-stu-id="cedaa-136">0x80041008</span></span> | <span data-ttu-id="cedaa-137">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="cedaa-137">One or more parameters are not valid.</span></span> |
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="cedaa-138">0x80041002</span><span class="sxs-lookup"><span data-stu-id="cedaa-138">0x80041002</span></span> | <span data-ttu-id="cedaa-139">La propriété spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="cedaa-139">The specified property was not found.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="cedaa-140">0x80041006</span><span class="sxs-lookup"><span data-stu-id="cedaa-140">0x80041006</span></span> | <span data-ttu-id="cedaa-141">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="cedaa-141">Not enough memory is available to complete the operation.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="cedaa-142">0</span><span class="sxs-lookup"><span data-stu-id="cedaa-142">0</span></span> | <span data-ttu-id="cedaa-143">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="cedaa-143">The function call was successful.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="cedaa-144">Notes</span><span class="sxs-lookup"><span data-stu-id="cedaa-144">Remarks</span></span>

<span data-ttu-id="cedaa-145">Cette fonction encapsule un appel à la [IWbemClassObject::Get](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get) (méthode).</span><span class="sxs-lookup"><span data-stu-id="cedaa-145">This function wraps a call to the [IWbemClassObject::Get](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="cedaa-146">Le `Get` fonction peut également retourner les propriétés système.</span><span class="sxs-lookup"><span data-stu-id="cedaa-146">The `Get` function can also return system properties.</span></span>

<span data-ttu-id="cedaa-147">Le `pVal` argument reçoit le type correct et la valeur pour le qualificateur et le modèle COM [VariantInit](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) (fonction)</span><span class="sxs-lookup"><span data-stu-id="cedaa-147">The `pVal` argument is assigned the correct type and value for the qualifier and the COM [VariantInit](https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) function</span></span>

## <a name="requirements"></a><span data-ttu-id="cedaa-148">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cedaa-148">Requirements</span></span>

 <span data-ttu-id="cedaa-149">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cedaa-149">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

 <span data-ttu-id="cedaa-150">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="cedaa-150">**Header:** WMINet_Utils.idl</span></span>

 <span data-ttu-id="cedaa-151">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="cedaa-151">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="cedaa-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cedaa-152">See also</span></span>

- [<span data-ttu-id="cedaa-153">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="cedaa-153">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)