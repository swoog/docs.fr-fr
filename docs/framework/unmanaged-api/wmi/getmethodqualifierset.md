---
title: GetMethodQualifierSet (fonction) (référence des API non managées)
description: La fonction GetMethodQualifierSet récupère le jeu de qualificateurs d’une méthode.
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
ms.openlocfilehash: 2b1f73e999738fbb59342aeab391132ac454c8dd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33459109"
---
# <a name="getmethodqualifierset-function"></a><span data-ttu-id="cc28f-103">GetMethodQualifierSet (fonction)</span><span class="sxs-lookup"><span data-stu-id="cc28f-103">GetMethodQualifierSet function</span></span>
<span data-ttu-id="cc28f-104">Récupère le qualificateur défini pour une méthode particulière.</span><span class="sxs-lookup"><span data-stu-id="cc28f-104">Retrieves the qualifier set for a particular method.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="cc28f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc28f-105">Syntax</span></span>  
  
```  
HRESULT GetMethodQualifierSet (
   [in] int                 vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LPCWSTR             wszMethod,
   [out] IWbemQualifierSet  **ppQualSet
); 
```  

## <a name="parameters"></a><span data-ttu-id="cc28f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc28f-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="cc28f-107">[in] Ce paramètre est inutilisé.</span><span class="sxs-lookup"><span data-stu-id="cc28f-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="cc28f-108">[in] Un pointeur vers un [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instance.</span><span class="sxs-lookup"><span data-stu-id="cc28f-108">[in] A pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instance.</span></span>

`wszMethod`  
<span data-ttu-id="cc28f-109">[in] Le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="cc28f-109">[in] The method  name.</span></span> <span data-ttu-id="cc28f-110">`wszMethod` doit pointer vers un valide `LPCWSTR`.</span><span class="sxs-lookup"><span data-stu-id="cc28f-110">`wszMethod` must point to a valid `LPCWSTR`.</span></span> 

`ppQualSet`  
<span data-ttu-id="cc28f-111">[out] Reçoit le pointeur d’interface qui autorise l’accès pour les qualificateurs de la méthode.</span><span class="sxs-lookup"><span data-stu-id="cc28f-111">[out] Receives the interface pointer that allows access to the qualifiers of the method.</span></span> <span data-ttu-id="cc28f-112">`ppQualSet` ne peut pas avoir la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="cc28f-112">`ppQualSet` cannot be `null`.</span></span> <span data-ttu-id="cc28f-113">Si une erreur se produit, un nouvel objet n’est pas retourné, et le pointeur est défini pour pointer vers `null`.</span><span class="sxs-lookup"><span data-stu-id="cc28f-113">If an error occurs, a new object is not returned, and the pointer is set to point to `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="cc28f-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cc28f-114">Return value</span></span>

<span data-ttu-id="cc28f-115">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="cc28f-115">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="cc28f-116">Constante</span><span class="sxs-lookup"><span data-stu-id="cc28f-116">Constant</span></span>  |<span data-ttu-id="cc28f-117">Value</span><span class="sxs-lookup"><span data-stu-id="cc28f-117">Value</span></span>  |<span data-ttu-id="cc28f-118">Description</span><span class="sxs-lookup"><span data-stu-id="cc28f-118">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="cc28f-119">0x80041002</span><span class="sxs-lookup"><span data-stu-id="cc28f-119">0x80041002</span></span> | <span data-ttu-id="cc28f-120">La méthode spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="cc28f-120">The specified method does not exist.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="cc28f-121">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="cc28f-121">0x80041008</span></span> | <span data-ttu-id="cc28f-122">Un paramètre est `null`.</span><span class="sxs-lookup"><span data-stu-id="cc28f-122">A parameter is `null`.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="cc28f-123">0</span><span class="sxs-lookup"><span data-stu-id="cc28f-123">0</span></span> | <span data-ttu-id="cc28f-124">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="cc28f-124">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="cc28f-125">Notes</span><span class="sxs-lookup"><span data-stu-id="cc28f-125">Remarks</span></span>

<span data-ttu-id="cc28f-126">Cette fonction encapsule un appel à la [IWbemClassObject::GetMethodQualifierSet](https://msdn.microsoft.com/library/aa391446(v=vs.85).aspx) (méthode).</span><span class="sxs-lookup"><span data-stu-id="cc28f-126">This function wraps a call to the [IWbemClassObject::GetMethodQualifierSet](https://msdn.microsoft.com/library/aa391446(v=vs.85).aspx) method.</span></span> 

<span data-ttu-id="cc28f-127">Un appel à cette fonction est prise en charge uniquement si l’objet actuel est une définition de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="cc28f-127">A call to this function is supported only if the current object is a CIM class definition.</span></span> <span data-ttu-id="cc28f-128">Manipulation de la méthode n’est pas disponible pour [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) ponters qui pointent vers les instances CIM.</span><span class="sxs-lookup"><span data-stu-id="cc28f-128">Method manipulation is not available for [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) ponters that point to CIM instances.</span></span>

<span data-ttu-id="cc28f-129">Étant donné que chaque méthode peut avoir son propre qualificateurs, le [IWbemQualifierSet pointeur](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx) permet d’ajouter, modifier ou supprimer ces qualificateurs de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="cc28f-129">Because each method may have its own qualifiers, the [IWbemQualifierSet pointer](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx) lets the caller add, edit, or delete these qualifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc28f-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cc28f-130">Requirements</span></span>  
<span data-ttu-id="cc28f-131">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cc28f-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc28f-132">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="cc28f-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="cc28f-133">**Versions du .NET framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="cc28f-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc28f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc28f-134">See also</span></span>  
[<span data-ttu-id="cc28f-135">WMI et les compteurs de Performance (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="cc28f-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
