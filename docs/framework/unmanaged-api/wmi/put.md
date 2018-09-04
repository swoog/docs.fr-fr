---
title: Fonction Put (référence des API non managées)
description: La fonction Put affecte une nouvelle valeur à une propriété nommée.
ms.date: 11/06/2017
api_name:
- Put
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Put
helpviewer_keywords:
- Put function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1ec8fe889885b555cbf9a95cd34b7330efff27f2
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43518754"
---
# <a name="put-function"></a><span data-ttu-id="efb7e-103">Fonction Put</span><span class="sxs-lookup"><span data-stu-id="efb7e-103">Put function</span></span>
<span data-ttu-id="efb7e-104">Affecte une nouvelle valeur à une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="efb7e-104">Sets a named property to a new value.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="efb7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efb7e-105">Syntax</span></span>  
  
```  
HRESULT Put (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName,
   [in] LONG              lFlags,
   [in] VARIANT*          pVal,
   [in] CIMTYPE           vtType
); 
```  

## <a name="parameters"></a><span data-ttu-id="efb7e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efb7e-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="efb7e-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="efb7e-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="efb7e-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="efb7e-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszName`  
<span data-ttu-id="efb7e-109">[in] Le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="efb7e-109">[in] The name of the property.</span></span> <span data-ttu-id="efb7e-110">Ce paramètre ne peut pas être `null`.</span><span class="sxs-lookup"><span data-stu-id="efb7e-110">This parameter cannot be `null`.</span></span>

`lFlags`  
<span data-ttu-id="efb7e-111">[in] Réservé.</span><span class="sxs-lookup"><span data-stu-id="efb7e-111">[in] Reserved.</span></span> <span data-ttu-id="efb7e-112">Ce paramètre doit être 0.</span><span class="sxs-lookup"><span data-stu-id="efb7e-112">This parameter must be 0.</span></span>

`pVal`   
<span data-ttu-id="efb7e-113">[in] Un pointeur vers une valide `VARIANT` qui devient la nouvelle valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="efb7e-113">[in] A pointer to a valid `VARIANT` that becomes the new property value.</span></span> <span data-ttu-id="efb7e-114">Si `pVal` est `null` ou pointe vers un `VARIANT` de type `VT_NULL`, la propriété est définie sur `null`.</span><span class="sxs-lookup"><span data-stu-id="efb7e-114">If `pVal` is `null` or points to a `VARIANT` of type `VT_NULL`, the property is set to `null`.</span></span> 

`vtType`  
<span data-ttu-id="efb7e-115">[in] Le type de `VARIANT` vers lequel pointe `pVal`.</span><span class="sxs-lookup"><span data-stu-id="efb7e-115">[in] The type of `VARIANT` pointed to by `pVal`.</span></span> <span data-ttu-id="efb7e-116">Consultez le [notes](#remarks) section pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="efb7e-116">See the [Remarks](#remarks) section for more information.</span></span>
 

## <a name="return-value"></a><span data-ttu-id="efb7e-117">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="efb7e-117">Return value</span></span>

<span data-ttu-id="efb7e-118">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="efb7e-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="efb7e-119">Constante</span><span class="sxs-lookup"><span data-stu-id="efb7e-119">Constant</span></span>  |<span data-ttu-id="efb7e-120">Value</span><span class="sxs-lookup"><span data-stu-id="efb7e-120">Value</span></span>  |<span data-ttu-id="efb7e-121">Description</span><span class="sxs-lookup"><span data-stu-id="efb7e-121">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="efb7e-122">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="efb7e-122">0x80041001</span></span> | <span data-ttu-id="efb7e-123">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="efb7e-123">There has been a general failure.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="efb7e-124">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="efb7e-124">0x80041008</span></span> | <span data-ttu-id="efb7e-125">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="efb7e-125">One or more parameters are not valid.</span></span> |
|`WBEM_E_INVALID_PROPERTY_TYPE` | <span data-ttu-id="efb7e-126">0x8004102a</span><span class="sxs-lookup"><span data-stu-id="efb7e-126">0x8004102a</span></span> | <span data-ttu-id="efb7e-127">Le type de propriété n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="efb7e-127">The property type is not recognized.</span></span> <span data-ttu-id="efb7e-128">Cette valeur est retournée lors de la création des instances de classe si la classe existe déjà.</span><span class="sxs-lookup"><span data-stu-id="efb7e-128">This value is returned when creating class instances if the class already exists.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="efb7e-129">0x80041006</span><span class="sxs-lookup"><span data-stu-id="efb7e-129">0x80041006</span></span> | <span data-ttu-id="efb7e-130">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="efb7e-130">Not enough memory is available to complete the operation.</span></span> |
| `WBEM_E_TYPE_MISMATCH` | <span data-ttu-id="efb7e-131">0 x 80041005</span><span class="sxs-lookup"><span data-stu-id="efb7e-131">0x80041005</span></span> | <span data-ttu-id="efb7e-132">Pour les instances : indique que `pVal` pointe vers un `VARIANT` d’un type incorrect pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="efb7e-132">For instances: Indicates that `pVal` points to a `VARIANT` of an incorrect type for the property.</span></span> <br/> <span data-ttu-id="efb7e-133">Pour les définitions de classe : la propriété existe déjà dans la classe parente et le nouveau type de COM est différent de l’ancien type COM.</span><span class="sxs-lookup"><span data-stu-id="efb7e-133">For class definitions: The property already exists in the parent class, and the new COM type is different from the old COM type.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="efb7e-134">0</span><span class="sxs-lookup"><span data-stu-id="efb7e-134">0</span></span> | <span data-ttu-id="efb7e-135">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="efb7e-135">The function call was successful.</span></span> |
  
## <a name="remarks"></a><span data-ttu-id="efb7e-136">Notes</span><span class="sxs-lookup"><span data-stu-id="efb7e-136">Remarks</span></span>

<span data-ttu-id="efb7e-137">Cette fonction encapsule un appel à la [IWbemClassObject::Put](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put) (méthode).</span><span class="sxs-lookup"><span data-stu-id="efb7e-137">This function wraps a call to the [IWbemClassObject::Put](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

<span data-ttu-id="efb7e-138">Cette fonction remplace toujours la valeur de propriété actuelle avec un autre.</span><span class="sxs-lookup"><span data-stu-id="efb7e-138">This function always overwrites the current property value with a new one.</span></span> <span data-ttu-id="efb7e-139">Si le [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointe vers une définition de classe, `Put` crée ou met à jour la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="efb7e-139">If the [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) points to a class definition, `Put` creates or updates the property value.</span></span> <span data-ttu-id="efb7e-140">Lorsque [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointe vers une instance CIM, `Put` met à jour la valeur de propriété uniquement ; `Put` Impossible de créer une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="efb7e-140">When [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) points to a CIM instance, `Put` updates the property value only; `Put` cannot create a property value.</span></span>

<span data-ttu-id="efb7e-141">Le `__CLASS` système propriété est uniquement accessible en écriture lors de la création de classe, lorsqu’il ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="efb7e-141">The `__CLASS` system property is only writable during class creation, when it may not be left blank.</span></span> <span data-ttu-id="efb7e-142">Toutes les autres propriétés système sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="efb7e-142">All other system properties are read-only.</span></span>

<span data-ttu-id="efb7e-143">Un utilisateur ne peut pas créer des propriétés dont les noms commencent ou finir par un trait de soulignement (« _ »).</span><span class="sxs-lookup"><span data-stu-id="efb7e-143">A user cannot create properties with names that begin or end with an underscore ("_").</span></span> <span data-ttu-id="efb7e-144">Cela est réservé pour les propriétés et les classes système.</span><span class="sxs-lookup"><span data-stu-id="efb7e-144">This is reserved for system classes and properties.</span></span>

<span data-ttu-id="efb7e-145">Si la propriété définie le `Put` fonction existe dans la classe parente, la valeur par défaut de la propriété est modifiée, sauf si le type de propriété ne correspond pas au type de classe de parent.</span><span class="sxs-lookup"><span data-stu-id="efb7e-145">If the property set by the `Put` function exists in the parent class, the default value of the property is changed unless the property type does not match the parent class type.</span></span> <span data-ttu-id="efb7e-146">Si la propriété n’existe pas et il n’est pas une incompatibilité de type, la propriété est de type créé.</span><span class="sxs-lookup"><span data-stu-id="efb7e-146">If the property does not exist and it is not a type mismatch, the property is ceated.</span></span>

<span data-ttu-id="efb7e-147">Utilisez le `vtType` paramètre uniquement lors de la création de nouvelles propriétés dans une définition de classe CIM et `pVal` est `null` ou pointe vers un `VARIANT` de type `VT_NULL`.</span><span class="sxs-lookup"><span data-stu-id="efb7e-147">Use the `vtType` parameter only when creating new properties in a CIM class definition and `pVal` is `null` or points to a `VARIANT` of type `VT_NULL`.</span></span> <span data-ttu-id="efb7e-148">Dans ce cas, le `vType` paramètre spécifie le type CIM de la propriété.</span><span class="sxs-lookup"><span data-stu-id="efb7e-148">In this case, the `vType` parameter specifies the CIM type of the property.</span></span> <span data-ttu-id="efb7e-149">Dans tous les autres cas, `vtType` doit être 0.</span><span class="sxs-lookup"><span data-stu-id="efb7e-149">In every other case, `vtType` must be 0.</span></span> <span data-ttu-id="efb7e-150">`vtType` doit également être 0 si l’objet sous-jacent est une instance (même si `Val` est `null`), car le type de la propriété est fixe et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="efb7e-150">`vtType` must also be 0 if the underlying object is an instance (even if `Val` is `null`) because the type of the property is fixed and cannot be changed.</span></span>   

## <a name="example"></a><span data-ttu-id="efb7e-151">Exemple</span><span class="sxs-lookup"><span data-stu-id="efb7e-151">Example</span></span>

<span data-ttu-id="efb7e-152">Pour obtenir un exemple, consultez le [IWbemClassObject::Put](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put) (méthode).</span><span class="sxs-lookup"><span data-stu-id="efb7e-152">For an example, see the [IWbemClassObject::Put](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb7e-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efb7e-153">Requirements</span></span>  
 <span data-ttu-id="efb7e-154">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="efb7e-154">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="efb7e-155">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="efb7e-155">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="efb7e-156">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="efb7e-156">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efb7e-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efb7e-157">See also</span></span>  
[<span data-ttu-id="efb7e-158">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="efb7e-158">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
