---
title: GetMethod, fonction (référence des API non managées)
description: La fonction GetMethod récupère des informations sur une méthode.
ms.date: 11/06/2017
api_name:
- GetMethod
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetMethod
helpviewer_keywords:
- GetMethod function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a913de0ff20fba51295fd8282b58e3953be9bba2
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43554867"
---
# <a name="getmethod-function"></a><span data-ttu-id="ef2c9-103">GetMethod, fonction</span><span class="sxs-lookup"><span data-stu-id="ef2c9-103">GetMethod function</span></span>
<span data-ttu-id="ef2c9-104">Récupère les informations sur la méthode spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-104">Retrieves information about the specified method.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="ef2c9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef2c9-105">Syntax</span></span>  
  
```  
HRESULT GetMethod (
   [in] int                vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LPCWSTR             wszName,
   [in] LONG                lFlags,
   [out] IWbemClassObject** ppInSignature,
   [out] IWbemClassObject** ppOutSignature
); 
```  

## <a name="parameters"></a><span data-ttu-id="ef2c9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef2c9-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="ef2c9-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="ef2c9-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszName`  
<span data-ttu-id="ef2c9-109">[in] Le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-109">[in] The method name.</span></span> <span data-ttu-id="ef2c9-110">Ce paramètre ne peut pas être `null` et doit pointer vers un valide `LPCWSTR`.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-110">This parameter cannot be `null` and must point to a valid `LPCWSTR`.</span></span>

`lFlags`  
<span data-ttu-id="ef2c9-111">[in] Réservé.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-111">[in] Reserved.</span></span> <span data-ttu-id="ef2c9-112">Ce paramètre doit être 0.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-112">This parameter must be 0.</span></span>

`ppInSignature`   
<span data-ttu-id="ef2c9-113">[out] Un pointeur vers l’adresse d’un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance qui décrit le paramteers dans à la méthode.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-113">[out] A pointer to the address of an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance that describes the in paramteers to the method.</span></span> <span data-ttu-id="ef2c9-114">Ce paramètre est ignoré si elle est définie sur `null`.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-114">This parameter is ignored if it is set to `null`.</span></span> 

`ppOutSignature`  
<span data-ttu-id="ef2c9-115">[out] Un pointeur vers l’adresse d’un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance qui décrit les paramètres de sortie à la méthode.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-115">[out] A pointer to the address of an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance that describes the out parameters to the method.</span></span> <span data-ttu-id="ef2c9-116">Ce paramètre est ignoré si elle est définie sur `null`.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-116">This parameter is ignored if it is set to `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="ef2c9-117">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ef2c9-117">Return value</span></span>

<span data-ttu-id="ef2c9-118">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="ef2c9-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="ef2c9-119">Constante</span><span class="sxs-lookup"><span data-stu-id="ef2c9-119">Constant</span></span>  |<span data-ttu-id="ef2c9-120">Value</span><span class="sxs-lookup"><span data-stu-id="ef2c9-120">Value</span></span>  |<span data-ttu-id="ef2c9-121">Description</span><span class="sxs-lookup"><span data-stu-id="ef2c9-121">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="ef2c9-122">0x80041002</span><span class="sxs-lookup"><span data-stu-id="ef2c9-122">0x80041002</span></span> | <span data-ttu-id="ef2c9-123">La propriété spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-123">The specified property was not found.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="ef2c9-124">0x80041006</span><span class="sxs-lookup"><span data-stu-id="ef2c9-124">0x80041006</span></span> | <span data-ttu-id="ef2c9-125">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-125">Not enough memory is available to complete the operation.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="ef2c9-126">0</span><span class="sxs-lookup"><span data-stu-id="ef2c9-126">0</span></span> | <span data-ttu-id="ef2c9-127">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-127">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="ef2c9-128">Notes</span><span class="sxs-lookup"><span data-stu-id="ef2c9-128">Remarks</span></span>

<span data-ttu-id="ef2c9-129">Cette fonction encapsule un appel à la [IWbemClassObject::GetMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ef2c9-129">This function wraps a call to the [IWbemClassObject::GetMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod) method.</span></span>

<span data-ttu-id="ef2c9-130">Gestion de Windows peut définir le [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointeur vers `null` si la méthode n’a aucun paramètre in.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-130">Windows Management can set the [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointer to `null` if the method has no in parameters.</span></span>

<span data-ttu-id="ef2c9-131">Dans `ppInSignature` et `ppOutSignature` décrivent respectivement, en tant que propriétés dans les paramètres, in et out un `IWbemClassObject` instance de la classe système [_Parameters](/windows/desktop/WmiSdk/--parameters).</span><span class="sxs-lookup"><span data-stu-id="ef2c9-131">In `ppInSignature` and `ppOutSignature` describe in and out parameters, respectively, as properties in a `IWbemClassObject` instance of the system class [_Parameters](/windows/desktop/WmiSdk/--parameters).</span></span> <span data-ttu-id="ef2c9-132">Les propriétés dans `ppInsignature` sont nommés **Param *** n*, où *n* correspond à la position du paramètre dans la signature de méthode (tel que `Param1`, `Param2`, etc..).</span><span class="sxs-lookup"><span data-stu-id="ef2c9-132">The properties in `ppInsignature` are named **Param***n*, where *n* is the position of the parameter in the method signature (such as `Param1`, `Param2`, etc.).</span></span> <span data-ttu-id="ef2c9-133">Les propriétés dans `ppOutSignature` sont également appelés **Param *** n*, et la valeur de retour est nommée **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="ef2c9-133">The properties in `ppOutSignature` are also named **Param***n*, and the return value is named **ReturnValue**.</span></span> <span data-ttu-id="ef2c9-134">Pour plus d’informations et un exemple, consultez [IWbemClassObject::GetMethod méthode](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod).</span><span class="sxs-lookup"><span data-stu-id="ef2c9-134">For more information and an example, see [IWbemClassObject::GetMethod method](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef2c9-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef2c9-135">Requirements</span></span>  
<span data-ttu-id="ef2c9-136">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ef2c9-136">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef2c9-137">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="ef2c9-137">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="ef2c9-138">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="ef2c9-138">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef2c9-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef2c9-139">See also</span></span>  
[<span data-ttu-id="ef2c9-140">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="ef2c9-140">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
