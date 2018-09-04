---
title: SpawnDerivedClass (fonction) (référence des API non managées)
description: La fonction SpawnDerivedClass crée un nouvel objet qui dérive d’un objet.
ms.date: 11/06/2017
api_name:
- SpawnDerivedClass
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- SpawnDerivedClass
helpviewer_keywords:
- SpawnDerivedClass function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 04df65a29584f7e2de44389d815b915a541e38f0
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43489797"
---
# <a name="spawnderivedclass-function"></a><span data-ttu-id="5d7d2-103">SpawnDerivedClass (fonction)</span><span class="sxs-lookup"><span data-stu-id="5d7d2-103">SpawnDerivedClass function</span></span>
<span data-ttu-id="5d7d2-104">Crée un objet de classe qui vient d’être dérivée d’un objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-104">Creates a newly derived class object from a specified object.</span></span>    
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="5d7d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d7d2-105">Syntax</span></span>  
  
```  
HRESULT SpawnDerivedClass (
   [in] int                  vFunc, 
   [in] IWbemClassObject*    ptr, 
   [in] LONG                 lFlags,
   [out] IWbemClassObject**  ppNewClass); 
```  

## <a name="parameters"></a><span data-ttu-id="5d7d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d7d2-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="5d7d2-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="5d7d2-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`lFlags`  
<span data-ttu-id="5d7d2-109">[in] Réservé.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-109">[in] Reserved.</span></span> <span data-ttu-id="5d7d2-110">Ce paramètre doit être 0.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-110">This parameter must be 0.</span></span>

`ppNewClass`  
<span data-ttu-id="5d7d2-111">[out] Reçoit le pointeur vers le nouvel objet de définition de classe.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-111">[out] Receives the pointer to the new class definition object.</span></span> <span data-ttu-id="5d7d2-112">Si une erreur se produit, un nouvel objet n’est pas retournée, et `ppNewClass` est gauche tels quels.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-112">If an error occurs, a new object is not returned, and `ppNewClass` is left unmodified.</span></span> <span data-ttu-id="5d7d2-113">Sa valeur ne peut pas être `null`.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-113">Its value cannot be `null`.</span></span>

## <a name="return-value"></a><span data-ttu-id="5d7d2-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5d7d2-114">Return value</span></span>

<span data-ttu-id="5d7d2-115">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="5d7d2-115">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="5d7d2-116">Constante</span><span class="sxs-lookup"><span data-stu-id="5d7d2-116">Constant</span></span>  |<span data-ttu-id="5d7d2-117">Value</span><span class="sxs-lookup"><span data-stu-id="5d7d2-117">Value</span></span>  |<span data-ttu-id="5d7d2-118">Description</span><span class="sxs-lookup"><span data-stu-id="5d7d2-118">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="5d7d2-119">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="5d7d2-119">0x80041001</span></span> | <span data-ttu-id="5d7d2-120">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-120">There has been a general failure.</span></span> |
| `WBEM_E_INVALID_OPERATION` | <span data-ttu-id="5d7d2-121">0x80041016</span><span class="sxs-lookup"><span data-stu-id="5d7d2-121">0x80041016</span></span> | <span data-ttu-id="5d7d2-122">Une opération non valide, telle que la génération d’une classe à partir d’une instance, a été demandée.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-122">An invalid operation, such as spawning a class from an instance, was requested.</span></span> |
| `WBEM_E_INCOMPLETE_CLASS` | <span data-ttu-id="5d7d2-123">La classe source n’a pas complètement a été définie ou inscrite avec la gestion de Windows, donc une nouvelle classe dérivée n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-123">The source class was not completely defined or registered with Windows Management, so a new derived class is not permitted.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="5d7d2-124">0x80041006</span><span class="sxs-lookup"><span data-stu-id="5d7d2-124">0x80041006</span></span> | <span data-ttu-id="5d7d2-125">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-125">Not enough memory is available to complete the operation.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="5d7d2-126">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="5d7d2-126">0x80041008</span></span> | <span data-ttu-id="5d7d2-127">`ppNewClass` a la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-127">`ppNewClass` is `null`.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="5d7d2-128">0</span><span class="sxs-lookup"><span data-stu-id="5d7d2-128">0</span></span> | <span data-ttu-id="5d7d2-129">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-129">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="5d7d2-130">Notes</span><span class="sxs-lookup"><span data-stu-id="5d7d2-130">Remarks</span></span>

<span data-ttu-id="5d7d2-131">Cette fonction encapsule un appel à la [IWbemClassObject::SpawnDerivedClass](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) (méthode).</span><span class="sxs-lookup"><span data-stu-id="5d7d2-131">This function wraps a call to the [IWbemClassObject::SpawnDerivedClass](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

<span data-ttu-id="5d7d2-132">`ptr` doit être une définition de classe qui devient la classe parente de l’objet généré.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-132">`ptr` must be a class definition that becomes the parent class of the spawned object.</span></span> <span data-ttu-id="5d7d2-133">L’objet retourné est une sous-classe de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-133">The returned object becomes a subclass of the current object.</span></span>

<span data-ttu-id="5d7d2-134">Le nouvel objet retourné dans `ppNewClass` devient automatiquement une sous-classe de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-134">The new object returned in `ppNewClass` automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="5d7d2-135">Ce comportement ne peut pas être remplacé.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-135">This behavior cannot be overridden.</span></span> <span data-ttu-id="5d7d2-136">Il n’existe aucune autre méthode par laquelle les sous-classes (classes dérivées) peuvent être créés.</span><span class="sxs-lookup"><span data-stu-id="5d7d2-136">There is no other method by which subclasses (derived classes) can be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7d2-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d7d2-137">Requirements</span></span>  
 <span data-ttu-id="5d7d2-138">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5d7d2-138">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5d7d2-139">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="5d7d2-139">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="5d7d2-140">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="5d7d2-140">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d7d2-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d7d2-141">See also</span></span>  
[<span data-ttu-id="5d7d2-142">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="5d7d2-142">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
