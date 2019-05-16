---
title: GetPropertyQualifierSet (fonction) (référence des API non managées)
description: La fonction GetPropertyQualifierSet récupère le qualificateur définie pour une propriété.
ms.date: 11/06/2017
api_name:
- GetPropertyQualifierSet
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetPropertyQualifierSet
helpviewer_keywords:
- GetPropertyQualifierSet function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 588c56c80cc55df3689178875a9a0500cd0ca7b8
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65636401"
---
# <a name="getpropertyqualifierset-function"></a><span data-ttu-id="39a7f-103">GetPropertyQualifierSet (fonction)</span><span class="sxs-lookup"><span data-stu-id="39a7f-103">GetPropertyQualifierSet function</span></span>

<span data-ttu-id="39a7f-104">Récupère le jeu de qualificateurs pour une propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="39a7f-104">Retrieves the qualifier set for a particular property.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="39a7f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39a7f-105">Syntax</span></span>

```cpp
HRESULT GetPropertyQualifierSet (
   [in] int                 vFunc,
   [in] IWbemClassObject*   ptr,
   [in] LPCWSTR             wszProperty,
   [out] IWbemQualifierSet  **ppQualSet
);
```

## <a name="parameters"></a><span data-ttu-id="39a7f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39a7f-106">Parameters</span></span>

`vFunc`\
<span data-ttu-id="39a7f-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="39a7f-107">[in] This parameter is unused.</span></span>

`ptr`\
<span data-ttu-id="39a7f-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="39a7f-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszMethod`\
<span data-ttu-id="39a7f-109">[in] Le nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="39a7f-109">[in] The property  name.</span></span> <span data-ttu-id="39a7f-110">`wszProperty` doit pointer vers un valide `LPCWSTR`.</span><span class="sxs-lookup"><span data-stu-id="39a7f-110">`wszProperty` must point to a valid `LPCWSTR`.</span></span>

`ppQualSet`\
<span data-ttu-id="39a7f-111">[out] Reçoit le pointeur d’interface qui autorise l’accès pour les qualificateurs de la propriété.</span><span class="sxs-lookup"><span data-stu-id="39a7f-111">[out] Receives the interface pointer that allows access to the qualifiers of the property.</span></span> <span data-ttu-id="39a7f-112">`ppQualSet` ne peut pas avoir la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="39a7f-112">`ppQualSet` cannot be `null`.</span></span> <span data-ttu-id="39a7f-113">Si une erreur se produit, un nouvel objet n’est pas retourné, et le pointeur est défini pour pointer vers `null`.</span><span class="sxs-lookup"><span data-stu-id="39a7f-113">If an error occurs, a new object is not returned, and the pointer is set to point to `null`.</span></span>

## <a name="return-value"></a><span data-ttu-id="39a7f-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="39a7f-114">Return value</span></span>

<span data-ttu-id="39a7f-115">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="39a7f-115">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="39a7f-116">Constante</span><span class="sxs-lookup"><span data-stu-id="39a7f-116">Constant</span></span>  |<span data-ttu-id="39a7f-117">Value</span><span class="sxs-lookup"><span data-stu-id="39a7f-117">Value</span></span>  |<span data-ttu-id="39a7f-118">Description</span><span class="sxs-lookup"><span data-stu-id="39a7f-118">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="39a7f-119">0x80041001</span><span class="sxs-lookup"><span data-stu-id="39a7f-119">0x80041001</span></span> | <span data-ttu-id="39a7f-120">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="39a7f-120">There has been a general failure.</span></span> |
| `WBEM_E_NOT_FOUND` | <span data-ttu-id="39a7f-121">0x80041002</span><span class="sxs-lookup"><span data-stu-id="39a7f-121">0x80041002</span></span> | <span data-ttu-id="39a7f-122">La méthode spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="39a7f-122">The specified method does not exist.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="39a7f-123">0x80041006</span><span class="sxs-lookup"><span data-stu-id="39a7f-123">0x80041006</span></span> | <span data-ttu-id="39a7f-124">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="39a7f-124">Not enough memory is available to complete the operation.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="39a7f-125">0x80041008</span><span class="sxs-lookup"><span data-stu-id="39a7f-125">0x80041008</span></span> | <span data-ttu-id="39a7f-126">Un paramètre est `null`.</span><span class="sxs-lookup"><span data-stu-id="39a7f-126">A parameter is `null`.</span></span> |
| `WBEM_E_SYSTEM_PROPERTY` | <span data-ttu-id="39a7f-127">0x80041030</span><span class="sxs-lookup"><span data-stu-id="39a7f-127">0x80041030</span></span> | <span data-ttu-id="39a7f-128">La fonction tente d’obtenir des qualificateurs de propriété système.</span><span class="sxs-lookup"><span data-stu-id="39a7f-128">The function attempts to get qualifiers of a system property.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="39a7f-129">0</span><span class="sxs-lookup"><span data-stu-id="39a7f-129">0</span></span> | <span data-ttu-id="39a7f-130">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="39a7f-130">The function call was successful.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="39a7f-131">Notes</span><span class="sxs-lookup"><span data-stu-id="39a7f-131">Remarks</span></span>

<span data-ttu-id="39a7f-132">Cette fonction encapsule un appel à la [IWbemClassObject::GetPropertyQualifierSet](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) (méthode).</span><span class="sxs-lookup"><span data-stu-id="39a7f-132">This function wraps a call to the [IWbemClassObject::GetPropertyQualifierSet](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) method.</span></span>

<span data-ttu-id="39a7f-133">Un appel à cette fonction est prise en charge uniquement si l’objet actuel est une définition de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="39a7f-133">A call to this function is supported only if the current object is a CIM class definition.</span></span> <span data-ttu-id="39a7f-134">Manipulation de la méthode n’est pas disponible pour [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointeurs qui pointent vers des instances CIM.</span><span class="sxs-lookup"><span data-stu-id="39a7f-134">Method manipulation is not available for [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointers that point to CIM instances.</span></span>

<span data-ttu-id="39a7f-135">Étant donné que chaque méthode peut avoir son propre qualificateurs, le [IWbemQualifierSet pointeur](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) permet à l’appelant ajouter, modifier ou supprimer ces qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="39a7f-135">Because each method may have its own qualifiers, the [IWbemQualifierSet pointer](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) lets the caller add, edit, or delete these qualifiers.</span></span>

<span data-ttu-id="39a7f-136">Étant donné que les propriétés système n’ont des qualificateurs d’aucun, la fonction retourne `WBEM_E_SYSTEM_PROPERTY` si vous tentez d’obtenir un [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) pointeur pour une propriété système.</span><span class="sxs-lookup"><span data-stu-id="39a7f-136">Because system properties have no qualifiers, the function returns `WBEM_E_SYSTEM_PROPERTY` if you attempt to obtain a [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) pointer for a system property.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a7f-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39a7f-137">Requirements</span></span>

<span data-ttu-id="39a7f-138">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="39a7f-138">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="39a7f-139">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="39a7f-139">**Header:** WMINet_Utils.idl</span></span>

<span data-ttu-id="39a7f-140">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="39a7f-140">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="39a7f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39a7f-141">See also</span></span>

- [<span data-ttu-id="39a7f-142">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="39a7f-142">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
