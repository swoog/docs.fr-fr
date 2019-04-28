---
title: Getpropertyhandle, fonction (référence des API non managées)
description: Getpropertyhandle, de la fonction retourne un handle unique qui identifie une propriété.
ms.date: 11/06/2017
api_name:
- GetPropertyHandle
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetPropertyHandle
helpviewer_keywords:
- GetPropertyHandle function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 92d48caf7de873850135c7410a5e4b5861131212
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61723236"
---
# <a name="getpropertyhandle-function"></a><span data-ttu-id="31835-103">GetPropertyHandle, fonction</span><span class="sxs-lookup"><span data-stu-id="31835-103">GetPropertyHandle function</span></span>

<span data-ttu-id="31835-104">Retourne un handle unique qui identifie une propriété.</span><span class="sxs-lookup"><span data-stu-id="31835-104">Returns a unique handle that identifies a property.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="31835-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31835-105">Syntax</span></span>

```cpp
HRESULT GetPropertyHandle (
   [in] int                  vFunc,
   [in] IWbemObjectAccess*   ptr,
   [in] LPCWSTR              wszPropertyName,
   [out] CIMTYPE*            pType,
   [out] long*               pHandle
);
```

## <a name="parameters"></a><span data-ttu-id="31835-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31835-106">Parameters</span></span>

`vFunc`\
<span data-ttu-id="31835-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="31835-107">[in] This parameter is unused.</span></span>

`ptr`\
<span data-ttu-id="31835-108">[in] Un pointeur vers un [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) instance.</span><span class="sxs-lookup"><span data-stu-id="31835-108">[in] A pointer to an [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) instance.</span></span>

`wszPropertyName`\
<span data-ttu-id="31835-109">[in] Se terminant par null chaîne de caractères encodés UTF16 qui contient le nom de propriété.</span><span class="sxs-lookup"><span data-stu-id="31835-109">[in] A null-terminated string of UTF16-encoded characters that contains the property name.</span></span>

`pType`\
<span data-ttu-id="31835-110">[out] Un pointeur vers un [ `CIMTYPE` ](/windows/desktop/api/wbemcli/ne-wbemcli-tag_cimtype_enumeration) membre d’énumération qui représente le type CIM de la propriété.</span><span class="sxs-lookup"><span data-stu-id="31835-110">[out] A pointer to a [`CIMTYPE`](/windows/desktop/api/wbemcli/ne-wbemcli-tag_cimtype_enumeration) enumeration member that represents the CIM type of the property.</span></span>

`pHandle`\
<span data-ttu-id="31835-111">[out] Pointeur vers un entier qui contient le descripteur de propriété.</span><span class="sxs-lookup"><span data-stu-id="31835-111">[out] A pointer to an integer that contains the property handle.</span></span>

## <a name="return-value"></a><span data-ttu-id="31835-112">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="31835-112">Return value</span></span>

<span data-ttu-id="31835-113">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="31835-113">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="31835-114">Constante</span><span class="sxs-lookup"><span data-stu-id="31835-114">Constant</span></span>  |<span data-ttu-id="31835-115">Value</span><span class="sxs-lookup"><span data-stu-id="31835-115">Value</span></span>  |<span data-ttu-id="31835-116">Description</span><span class="sxs-lookup"><span data-stu-id="31835-116">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="31835-117">0x80041002</span><span class="sxs-lookup"><span data-stu-id="31835-117">0x80041002</span></span> | <span data-ttu-id="31835-118">Le nom de la propriété spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="31835-118">The specified property name was not found.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="31835-119">0x80041008</span><span class="sxs-lookup"><span data-stu-id="31835-119">0x80041008</span></span> | <span data-ttu-id="31835-120">Un paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="31835-120">A parameter is not valid.</span></span> |
|`WBEM_E_NOT_SUPPORTED` | <span data-ttu-id="31835-121">0x8004100c</span><span class="sxs-lookup"><span data-stu-id="31835-121">0x8004100c</span></span> | <span data-ttu-id="31835-122">La propriété demandée est de type sont `CIM_OBJECT` ou `CIM_ARRAY`.</span><span class="sxs-lookup"><span data-stu-id="31835-122">The requested property is of type are `CIM_OBJECT` or `CIM_ARRAY`.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="31835-123">0</span><span class="sxs-lookup"><span data-stu-id="31835-123">0</span></span> | <span data-ttu-id="31835-124">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="31835-124">The function call was successful.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="31835-125">Notes</span><span class="sxs-lookup"><span data-stu-id="31835-125">Remarks</span></span>

<span data-ttu-id="31835-126">Cette fonction encapsule un appel à la [IWbemClassObject::GetPropertyHandle](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) (méthode).</span><span class="sxs-lookup"><span data-stu-id="31835-126">This function wraps a call to the [IWbemClassObject::GetPropertyHandle](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle) method.</span></span>

<span data-ttu-id="31835-127">Vous pouvez utiliser ce handle pour identifier les propriétés lorsque vous utilisez [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) méthodes pour lire ou écrire des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="31835-127">You can use this handle to identify properties when using  [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) methods to read or write property values.</span></span>

<span data-ttu-id="31835-128">Handles peuvent être récupérées pour les propriétés de tous les types de données autre que `CIM_OBJECT` et `CIM_ARRAY`.</span><span class="sxs-lookup"><span data-stu-id="31835-128">Handles can be retrieved for properties of all data types other than `CIM_OBJECT` and `CIM_ARRAY`.</span></span> <span data-ttu-id="31835-129">Retourné handles travail sur toutes les instances d’une classe.</span><span class="sxs-lookup"><span data-stu-id="31835-129">Returned handles work across all instances of a class.</span></span>

## <a name="requirements"></a><span data-ttu-id="31835-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31835-130">Requirements</span></span>

<span data-ttu-id="31835-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="31835-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="31835-132">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="31835-132">**Header:** WMINet_Utils.idl</span></span>

<span data-ttu-id="31835-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="31835-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="31835-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31835-134">See also</span></span>

- [<span data-ttu-id="31835-135">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="31835-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)