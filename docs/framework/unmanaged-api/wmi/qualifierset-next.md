---
title: QualifierSet_Next (fonction) (référence des API non managées)
description: La fonction QualifierSet_Next récupère le qualificateur suivant dans une énumération.
ms.date: 11/06/2017
api_name:
- QualifierSet_Next
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_Next
helpviewer_keywords:
- QualifierSet_Next function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a8232691c697c51b5a480a68c6d952f294a63460
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33460225"
---
# <a name="qualifiersetnext-function"></a><span data-ttu-id="f2d10-103">QualifierSet_Next (fonction)</span><span class="sxs-lookup"><span data-stu-id="f2d10-103">QualifierSet_Next function</span></span>
<span data-ttu-id="f2d10-104">Récupère le qualificateur suivant dans une énumération démarrée avec un appel à la [QualifierSet_BeginEnumeration](qualifierset-beginenumeration.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="f2d10-104">Retrieves the next qualifier in an enumeration that started with a call to the [QualifierSet_BeginEnumeration](qualifierset-beginenumeration.md) function.</span></span>   

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="f2d10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2d10-105">Syntax</span></span>  
  
```  
HRESULT QualifierSet_Next (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LONG                 lFlags,
   [out] BSTR*               pstrName,        
   [out] VARIANT*            pVal,
   [out] LONG*               plFlavor                 
); 
```  

## <a name="parameters"></a><span data-ttu-id="f2d10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2d10-106">Parameters</span></span>

`vFunc`   
<span data-ttu-id="f2d10-107">[in] Ce paramètre est inutilisé.</span><span class="sxs-lookup"><span data-stu-id="f2d10-107">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="f2d10-108">[in] Un pointeur vers un [IWbemQualifierSet](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx) instance.</span><span class="sxs-lookup"><span data-stu-id="f2d10-108">[in] A pointer to an [IWbemQualifierSet](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx) instance.</span></span>

`lFlags`   
<span data-ttu-id="f2d10-109">[in] Réservé.</span><span class="sxs-lookup"><span data-stu-id="f2d10-109">[in] Reserved.</span></span> <span data-ttu-id="f2d10-110">Ce paramètre doit être 0.</span><span class="sxs-lookup"><span data-stu-id="f2d10-110">This parameter must be 0.</span></span>

`pstrName`   
<span data-ttu-id="f2d10-111">[out] Le nom du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="f2d10-111">[out] The name of the qualifier.</span></span> <span data-ttu-id="f2d10-112">Si `null`, ce paramètre est ignoré ; sinon, `pstrName` ne doit pas pointer vers un valide `BSTR` ou une fuite de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="f2d10-112">If `null`, this parameter is ignored; otherwise, `pstrName` should not point to a valid `BSTR` or a memory leak occurs.</span></span> <span data-ttu-id="f2d10-113">Si non null, la fonction toujours alloue un nouveau `BSTR` lorsqu’elle retourne `WBEM_S_NO_ERROR`.</span><span class="sxs-lookup"><span data-stu-id="f2d10-113">If not null, the function always allocates a new `BSTR` when it returns `WBEM_S_NO_ERROR`.</span></span>

`pVal`   
<span data-ttu-id="f2d10-114">[out] Cas de réussite, la valeur du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="f2d10-114">[out] When successful, the value for the qualifier.</span></span> <span data-ttu-id="f2d10-115">Si la fonction échoue, la `VARIANT` vers lequel pointe `pVal` n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="f2d10-115">If the function fails, the `VARIANT` pointed to by `pVal` is not modified.</span></span> <span data-ttu-id="f2d10-116">Si ce paramètre est `null`, le paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f2d10-116">If this parameter is `null`, the parameter is ignored.</span></span>

`plFlavor`   
<span data-ttu-id="f2d10-117">[out] Pointeur vers un entier LONG qui reçoit le type de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="f2d10-117">[out] A pointer to a LONG that receives the qualifier flavor.</span></span> <span data-ttu-id="f2d10-118">Si les informations de version ne sont pas souhaitées, ce paramètre peut être `null`.</span><span class="sxs-lookup"><span data-stu-id="f2d10-118">If flavor information is not desired, this parameter can be `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="f2d10-119">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f2d10-119">Return value</span></span>

<span data-ttu-id="f2d10-120">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="f2d10-120">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="f2d10-121">Constante</span><span class="sxs-lookup"><span data-stu-id="f2d10-121">Constant</span></span>  |<span data-ttu-id="f2d10-122">Value</span><span class="sxs-lookup"><span data-stu-id="f2d10-122">Value</span></span>  |<span data-ttu-id="f2d10-123">Description</span><span class="sxs-lookup"><span data-stu-id="f2d10-123">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="f2d10-124">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="f2d10-124">0x80041008</span></span> | <span data-ttu-id="f2d10-125">Un paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f2d10-125">A parameter is not valid.</span></span> |
|`WBEM_E_UNEXPECTED` | <span data-ttu-id="f2d10-126">0x8004101d</span><span class="sxs-lookup"><span data-stu-id="f2d10-126">0x8004101d</span></span> | <span data-ttu-id="f2d10-127">L’appelant n’a pas appelé [QualifierSet_BeginEnumeration](qualifierset-beginenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f2d10-127">The caller did not call [QualifierSet_BeginEnumeration](qualifierset-beginenumeration.md).</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="f2d10-128">0x80041006</span><span class="sxs-lookup"><span data-stu-id="f2d10-128">0x80041006</span></span> | <span data-ttu-id="f2d10-129">Pas assez de mémoire est disponible pour commencer une nouvelle énumération.</span><span class="sxs-lookup"><span data-stu-id="f2d10-129">Not enough memory is available to begin a new enumeration.</span></span> |
| `WBEM_S_NO_MORE_DATA` | <span data-ttu-id="f2d10-130">0x40005</span><span class="sxs-lookup"><span data-stu-id="f2d10-130">0x40005</span></span> | <span data-ttu-id="f2d10-131">Aucun qualificateur plus n’est laissées dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="f2d10-131">No more qualifiers are left in the enumeration.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="f2d10-132">0</span><span class="sxs-lookup"><span data-stu-id="f2d10-132">0</span></span> | <span data-ttu-id="f2d10-133">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="f2d10-133">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="f2d10-134">Notes</span><span class="sxs-lookup"><span data-stu-id="f2d10-134">Remarks</span></span>

<span data-ttu-id="f2d10-135">Cette fonction encapsule un appel à la [IWbemQualifierSet::Next](https://msdn.microsoft.com/library/aa391870(v=vs.85).aspx) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f2d10-135">This function wraps a call to the [IWbemQualifierSet::Next](https://msdn.microsoft.com/library/aa391870(v=vs.85).aspx) method.</span></span>

<span data-ttu-id="f2d10-136">Vous appelez le `QualifierSet_Next` fonction à plusieurs reprises pour énumérer tous les qualificateurs jusqu'à ce que le retour de fonction `WBEM_S_NO_MORE_DATA`.</span><span class="sxs-lookup"><span data-stu-id="f2d10-136">You call the `QualifierSet_Next` function repeatedly to enumerate all the qualifiers until the function return `WBEM_S_NO_MORE_DATA`.</span></span> <span data-ttu-id="f2d10-137">Pour terminer l’énumération au début, appelez le [QualifierSet_EndEnumeration](qualifierset-endenumeration.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="f2d10-137">To terminate the enumeration early, call the [QualifierSet_EndEnumeration](qualifierset-endenumeration.md) function.</span></span>

<span data-ttu-id="f2d10-138">L’ordre des qualificateurs retournée lors de l’énumération n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f2d10-138">The order of the qualifiers returned during the enumeration is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2d10-139">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f2d10-139">Requirements</span></span>  
 <span data-ttu-id="f2d10-140">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f2d10-140">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2d10-141">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="f2d10-141">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="f2d10-142">**Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f2d10-142">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2d10-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2d10-143">See also</span></span>  
[<span data-ttu-id="f2d10-144">WMI et les compteurs de Performance (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="f2d10-144">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
