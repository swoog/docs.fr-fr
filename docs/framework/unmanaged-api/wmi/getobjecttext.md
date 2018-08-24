---
title: Getobjecttext, fonction (référence des API non managées)
description: Getobjecttext, de la fonction retourne un rendu textuel d’un objet dans la syntaxe MOF.
ms.date: 11/06/2017
api_name:
- GetObjectText
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetObjectText
helpviewer_keywords:
- GetObjectText function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 24ba4b37cc8221df4e018d172996c0910ec07f7d
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42754487"
---
# <a name="getobjecttext-function"></a><span data-ttu-id="eb57f-103">Getobjecttext, fonction</span><span class="sxs-lookup"><span data-stu-id="eb57f-103">GetObjectText function</span></span>
<span data-ttu-id="eb57f-104">Retourne un rendu textuel de l’objet dans la syntaxe de Format MOF (Managed Object).</span><span class="sxs-lookup"><span data-stu-id="eb57f-104">Returns a textual rendering of the object in the Managed Object Format (MOF) syntax.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="eb57f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb57f-105">Syntax</span></span>  
  
```  
HRESULT GetObjectText (
   [in] int                vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LONG                lFlags,
   [out] BSTR*              pstrObjectText
); 
```  

## <a name="parameters"></a><span data-ttu-id="eb57f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb57f-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="eb57f-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="eb57f-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="eb57f-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="eb57f-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`lFlags`  
<span data-ttu-id="eb57f-109">[in] Généralement 0.</span><span class="sxs-lookup"><span data-stu-id="eb57f-109">[in] Normally 0.</span></span> <span data-ttu-id="eb57f-110">Si `WBEM_FLAG_NO_FLAVORS` (ou 0 x 1) est spécifiée, les qualificateurs sont inclus sans les informations de la propagation ou la version.</span><span class="sxs-lookup"><span data-stu-id="eb57f-110">If `WBEM_FLAG_NO_FLAVORS` (or 0x1) is specified, qualifiers are included without propagation or flavor information.</span></span>

`pstrObjectText`   
<span data-ttu-id="eb57f-111">[out] Un pointeur vers un `null` sur ENTRÉE.</span><span class="sxs-lookup"><span data-stu-id="eb57f-111">[out] A pointer to a `null` on entry.</span></span> <span data-ttu-id="eb57f-112">Moment du retour, qui vient d’être alloué `BSTR` qui contient un rendu de la syntaxe MOF de l’objet.</span><span class="sxs-lookup"><span data-stu-id="eb57f-112">On return, a newly allocated `BSTR` that contains a MOF syntax rendering of the object.</span></span>  

## <a name="return-value"></a><span data-ttu-id="eb57f-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="eb57f-113">Return value</span></span>

<span data-ttu-id="eb57f-114">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="eb57f-114">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="eb57f-115">Constante</span><span class="sxs-lookup"><span data-stu-id="eb57f-115">Constant</span></span>  |<span data-ttu-id="eb57f-116">Value</span><span class="sxs-lookup"><span data-stu-id="eb57f-116">Value</span></span>  |<span data-ttu-id="eb57f-117">Description</span><span class="sxs-lookup"><span data-stu-id="eb57f-117">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="eb57f-118">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="eb57f-118">0x80041001</span></span> | <span data-ttu-id="eb57f-119">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="eb57f-119">There has been a general failure.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="eb57f-120">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="eb57f-120">0x80041008</span></span> | <span data-ttu-id="eb57f-121">Un paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="eb57f-121">A parameter is not valid.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="eb57f-122">0x80041006</span><span class="sxs-lookup"><span data-stu-id="eb57f-122">0x80041006</span></span> | <span data-ttu-id="eb57f-123">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="eb57f-123">Not enough memory is available to complete the operation.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="eb57f-124">0</span><span class="sxs-lookup"><span data-stu-id="eb57f-124">0</span></span> | <span data-ttu-id="eb57f-125">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="eb57f-125">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="eb57f-126">Notes</span><span class="sxs-lookup"><span data-stu-id="eb57f-126">Remarks</span></span>

<span data-ttu-id="eb57f-127">Cette fonction encapsule un appel à la [IWbemClassObject::GetObjectText](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getobjecttext) (méthode).</span><span class="sxs-lookup"><span data-stu-id="eb57f-127">This function wraps a call to the [IWbemClassObject::GetObjectText](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getobjecttext) method.</span></span>

<span data-ttu-id="eb57f-128">Le texte MOF retourné ne contient pas toutes les informations sur l’objet, mais suffisamment d’informations pour le compilateur MOF être en mesure de recréer l’objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="eb57f-128">The MOF text returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to recreate the original object.</span></span> <span data-ttu-id="eb57f-129">Par exemple, aucun qualificateurs propagés ou les propriétés de la classe parent ne sont incluses.</span><span class="sxs-lookup"><span data-stu-id="eb57f-129">For instance, no propagated qualifiers or parent class properties are included.</span></span>

<span data-ttu-id="eb57f-130">L’algorithme suivant est utilisé pour reconstruire le texte des paramètres d’une méthode :</span><span class="sxs-lookup"><span data-stu-id="eb57f-130">The following algorithm is used to reconstruct the text of the parameters of a method:</span></span>

1. <span data-ttu-id="eb57f-131">Les paramètres sont resequenced dans l’ordre de leurs valeurs d’identificateur.</span><span class="sxs-lookup"><span data-stu-id="eb57f-131">Parameters are resequenced in the order of their identifier values.</span></span>
1. <span data-ttu-id="eb57f-132">Les paramètres sont spécifiés en tant que `[in]` et `[out]` sont combinés en un seul paramètre.</span><span class="sxs-lookup"><span data-stu-id="eb57f-132">Parameters that are specified as `[in]` and `[out]` are combined into a single parameter.</span></span>
 
<span data-ttu-id="eb57f-133">`pstrObjectText` doit être un pointeur vers un `null` lorsque la fonction est appelée ; il ne doit pas pointer vers une chaîne qui est valide avant l’appel de méthode, car le pointeur n’est pas libéré.</span><span class="sxs-lookup"><span data-stu-id="eb57f-133">`pstrObjectText` must be a pointer to a `null` when the function is called; it must not point to a string that is valid before the method call, because the pointer will not be deallocated.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb57f-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb57f-134">Requirements</span></span>  
<span data-ttu-id="eb57f-135">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eb57f-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb57f-136">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="eb57f-136">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="eb57f-137">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="eb57f-137">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb57f-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb57f-138">See also</span></span>  
[<span data-ttu-id="eb57f-139">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="eb57f-139">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
