---
title: Supprimer (fonction) (référence des API non managées)
description: La fonction de suppression supprime la propriété spécifiée et toutes ses qualificateurs à partir d’une définition de classe CIM.
ms.date: 11/06/2017
api_name:
- Delete
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Delete
helpviewer_keywords:
- Delete function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 791e75aa60fd651dde1555339e31664a3523e1eb
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43777179"
---
# <a name="delete-function"></a><span data-ttu-id="0a9c7-103">Supprimer (fonction)</span><span class="sxs-lookup"><span data-stu-id="0a9c7-103">Delete function</span></span>
<span data-ttu-id="0a9c7-104">Supprime la propriété spécifiée et toutes ses qualificateurs d’une définition de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-104">Deletes the specified property and all of its qualifiers from a CIM class definition.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="0a9c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a9c7-105">Syntax</span></span>  
  
```  
HRESULT Delete (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName 
); 
```  

## <a name="parameters"></a><span data-ttu-id="0a9c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a9c7-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="0a9c7-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="0a9c7-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszName`  
<span data-ttu-id="0a9c7-109">[in] Le nom de la propriété à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-109">[in] The name of the property to delete.</span></span> <span data-ttu-id="0a9c7-110">`wszName` doit être un pointeur désignant une valide `LPCWSTR`.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-110">`wszName` must be a pointer to a valid `LPCWSTR`.</span></span>

## <a name="return-value"></a><span data-ttu-id="0a9c7-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0a9c7-111">Return value</span></span>

<span data-ttu-id="0a9c7-112">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="0a9c7-112">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="0a9c7-113">Constante</span><span class="sxs-lookup"><span data-stu-id="0a9c7-113">Constant</span></span>  |<span data-ttu-id="0a9c7-114">Value</span><span class="sxs-lookup"><span data-stu-id="0a9c7-114">Value</span></span>  |<span data-ttu-id="0a9c7-115">Description</span><span class="sxs-lookup"><span data-stu-id="0a9c7-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="0a9c7-116">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="0a9c7-116">0x80041001</span></span> | <span data-ttu-id="0a9c7-117">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-117">An unspecified error has occurred.</span></span> |
| `WBEM_E_INVALID_OPERATION` | <span data-ttu-id="0a9c7-118">0x80041016</span><span class="sxs-lookup"><span data-stu-id="0a9c7-118">0x80041016</span></span> | <span data-ttu-id="0a9c7-119">La propriété ne peut pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-119">The property cannot be deleted.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="0a9c7-120">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="0a9c7-120">0x80041008</span></span> | <span data-ttu-id="0a9c7-121">`wszzName` n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-121">`wszzName` is invalid.</span></span> |
| `WBEM_E_NOT_FOUND` | <span data-ttu-id="0a9c7-122">0x80041002</span><span class="sxs-lookup"><span data-stu-id="0a9c7-122">0x80041002</span></span> | <span data-ttu-id="0a9c7-123">La propriété spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-123">The specified property does not exist.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="0a9c7-124">0x80041006</span><span class="sxs-lookup"><span data-stu-id="0a9c7-124">0x80041006</span></span> | <span data-ttu-id="0a9c7-125">Il n’est pas suffisamment de mémoire pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-125">There is not enough memory to complete the operation.</span></span> |
| `WBEM_E_PROPAGATED_PROPERTY` | <span data-ttu-id="0a9c7-126">0x8004101c</span><span class="sxs-lookup"><span data-stu-id="0a9c7-126">0x8004101c</span></span> | <span data-ttu-id="0a9c7-127">La propriété est héritée d’une classe de base.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-127">The property is inherited from a base class.</span></span> |
| `WBEM_E_SYSTEM_PROPERTY` | | <span data-ttu-id="0a9c7-128">La propriété est une propriété système.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-128">The property is a system property.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="0a9c7-129">0</span><span class="sxs-lookup"><span data-stu-id="0a9c7-129">0</span></span> | <span data-ttu-id="0a9c7-130">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-130">The function call was successful.</span></span>  |
| `WBEM_E_RESET_TO_DEFAULT` | <span data-ttu-id="0a9c7-131">0x80041030</span><span class="sxs-lookup"><span data-stu-id="0a9c7-131">0x80041030</span></span> | <span data-ttu-id="0a9c7-132">La fonction supprimée d’une valeur par défaut de remplacement pour la classe en cours.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-132">The function deleted an override default value for the current class.</span></span> <span data-ttu-id="0a9c7-133">La valeur par défaut pour cette propriété dans la classe parente a été reactiviated.</span><span class="sxs-lookup"><span data-stu-id="0a9c7-133">The default value for this property in the parent class has been reactiviated.</span></span> | 

## <a name="remarks"></a><span data-ttu-id="0a9c7-134">Notes</span><span class="sxs-lookup"><span data-stu-id="0a9c7-134">Remarks</span></span>

<span data-ttu-id="0a9c7-135">Cette fonction encapsule un appel à la [IWbemClassObject::Delete](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-delete) (méthode).</span><span class="sxs-lookup"><span data-stu-id="0a9c7-135">This function wraps a call to the [IWbemClassObject::Delete](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-delete) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a9c7-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a9c7-136">Requirements</span></span>  
 <span data-ttu-id="0a9c7-137">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0a9c7-137">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a9c7-138">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="0a9c7-138">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="0a9c7-139">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0a9c7-139">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a9c7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a9c7-140">See also</span></span>  
[<span data-ttu-id="0a9c7-141">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="0a9c7-141">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
