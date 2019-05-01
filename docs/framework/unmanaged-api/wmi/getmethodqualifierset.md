---
title: Getmethodqualifierset, fonction (référence des API non managées)
description: La getmethodqualifierset, fonction récupère le jeu de qualificateurs d’une méthode.
ms.date: 11/06/2017
api_name:
- GetMethodQualifierSet
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetMethodQualifierSet
helpviewer_keywords:
- GetMethodQualifierSet function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9257ba57e0d087e3d6b9c7bb995b49a6b814c5f1
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62040740"
---
# <a name="getmethodqualifierset-function"></a><span data-ttu-id="25760-103">GetMethodQualifierSet, fonction</span><span class="sxs-lookup"><span data-stu-id="25760-103">GetMethodQualifierSet function</span></span>

<span data-ttu-id="25760-104">Récupère le jeu de qualificateurs pour une méthode particulière.</span><span class="sxs-lookup"><span data-stu-id="25760-104">Retrieves the qualifier set for a particular method.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="25760-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25760-105">Syntax</span></span>

```cpp
HRESULT GetMethodQualifierSet (
   [in] int                 vFunc,
   [in] IWbemClassObject*   ptr,
   [in] LPCWSTR             wszMethod,
   [out] IWbemQualifierSet  **ppQualSet
);
```

## <a name="parameters"></a><span data-ttu-id="25760-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25760-106">Parameters</span></span>

`vFunc`\
<span data-ttu-id="25760-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="25760-107">[in] This parameter is unused.</span></span>

`ptr`\
<span data-ttu-id="25760-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="25760-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszMethod`\
<span data-ttu-id="25760-109">[in] Le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="25760-109">[in] The method  name.</span></span> <span data-ttu-id="25760-110">`wszMethod` doit pointer vers un valide `LPCWSTR`.</span><span class="sxs-lookup"><span data-stu-id="25760-110">`wszMethod` must point to a valid `LPCWSTR`.</span></span>

`ppQualSet`\
<span data-ttu-id="25760-111">[out] Reçoit le pointeur d’interface qui autorise l’accès pour les qualificateurs de la méthode.</span><span class="sxs-lookup"><span data-stu-id="25760-111">[out] Receives the interface pointer that allows access to the qualifiers of the method.</span></span> <span data-ttu-id="25760-112">`ppQualSet` ne peut pas avoir la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="25760-112">`ppQualSet` cannot be `null`.</span></span> <span data-ttu-id="25760-113">Si une erreur se produit, un nouvel objet n’est pas retourné, et le pointeur est défini pour pointer vers `null`.</span><span class="sxs-lookup"><span data-stu-id="25760-113">If an error occurs, a new object is not returned, and the pointer is set to point to `null`.</span></span>

## <a name="return-value"></a><span data-ttu-id="25760-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="25760-114">Return value</span></span>

<span data-ttu-id="25760-115">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="25760-115">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="25760-116">Constante</span><span class="sxs-lookup"><span data-stu-id="25760-116">Constant</span></span>  |<span data-ttu-id="25760-117">Value</span><span class="sxs-lookup"><span data-stu-id="25760-117">Value</span></span>  |<span data-ttu-id="25760-118">Description</span><span class="sxs-lookup"><span data-stu-id="25760-118">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="25760-119">0x80041002</span><span class="sxs-lookup"><span data-stu-id="25760-119">0x80041002</span></span> | <span data-ttu-id="25760-120">La méthode spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="25760-120">The specified method does not exist.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="25760-121">0x80041008</span><span class="sxs-lookup"><span data-stu-id="25760-121">0x80041008</span></span> | <span data-ttu-id="25760-122">Un paramètre est `null`.</span><span class="sxs-lookup"><span data-stu-id="25760-122">A parameter is `null`.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="25760-123">0</span><span class="sxs-lookup"><span data-stu-id="25760-123">0</span></span> | <span data-ttu-id="25760-124">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="25760-124">The function call was successful.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="25760-125">Notes</span><span class="sxs-lookup"><span data-stu-id="25760-125">Remarks</span></span>

<span data-ttu-id="25760-126">Cette fonction encapsule un appel à la [IWbemClassObject::GetMethodQualifierSet](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) (méthode).</span><span class="sxs-lookup"><span data-stu-id="25760-126">This function wraps a call to the [IWbemClassObject::GetMethodQualifierSet](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) method.</span></span>

<span data-ttu-id="25760-127">Un appel à cette fonction est prise en charge uniquement si l’objet actuel est une définition de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="25760-127">A call to this function is supported only if the current object is a CIM class definition.</span></span> <span data-ttu-id="25760-128">Manipulation de la méthode n’est pas disponible pour [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointeurs qui pointent vers des instances CIM.</span><span class="sxs-lookup"><span data-stu-id="25760-128">Method manipulation is not available for [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointers that point to CIM instances.</span></span>

<span data-ttu-id="25760-129">Étant donné que chaque méthode peut avoir son propre qualificateurs, le [IWbemQualifierSet pointeur](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) permet à l’appelant ajouter, modifier ou supprimer ces qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="25760-129">Because each method may have its own qualifiers, the [IWbemQualifierSet pointer](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) lets the caller add, edit, or delete these qualifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="25760-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25760-130">Requirements</span></span>

<span data-ttu-id="25760-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="25760-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="25760-132">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="25760-132">**Header:** WMINet_Utils.idl</span></span>

<span data-ttu-id="25760-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="25760-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="25760-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25760-134">See also</span></span>

- [<span data-ttu-id="25760-135">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="25760-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)