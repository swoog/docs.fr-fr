---
title: Clone, fonction (référence des API non managées)
description: La fonction de clonage retourne un nouvel objet qui est un clone complet de l’objet actuel.
ms.date: 11/06/2017
api_name:
- Clone
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Clone
helpviewer_keywords:
- Clone function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5cd87cb619ef2dc1e0548c7553585b7e51e94c4f
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42924773"
---
# <a name="clone-function"></a><span data-ttu-id="eab0d-103">Clone, fonction</span><span class="sxs-lookup"><span data-stu-id="eab0d-103">Clone function</span></span>
<span data-ttu-id="eab0d-104">Retourne un nouvel objet qui est un clone complet de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="eab0d-104">Returns a new object that is a complete clone of the current object.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="eab0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eab0d-105">Syntax</span></span>  
  
```  
HRESULT Clone (
   [in] int                  vFunc, 
   [in] IWbemClassObject*    ptr, 
   [out] IWbemClassObject**  ppCopy
); 
```  

## <a name="parameters"></a><span data-ttu-id="eab0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eab0d-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="eab0d-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="eab0d-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="eab0d-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="eab0d-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`ppCopy`  
<span data-ttu-id="eab0d-109">[out] Un nouvel objet qui est une liste complète isolés de `ptr`.</span><span class="sxs-lookup"><span data-stu-id="eab0d-109">[out] A new object that is a complete lone of `ptr`.</span></span> <span data-ttu-id="eab0d-110">Cet argument ne peut pas être `null` s’il reçoit la copie de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="eab0d-110">This argument cannot be `null` if it receives the copy of the current object.</span></span>

## <a name="return-value"></a><span data-ttu-id="eab0d-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="eab0d-111">Return value</span></span>

<span data-ttu-id="eab0d-112">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="eab0d-112">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="eab0d-113">Constante</span><span class="sxs-lookup"><span data-stu-id="eab0d-113">Constant</span></span>  |<span data-ttu-id="eab0d-114">Value</span><span class="sxs-lookup"><span data-stu-id="eab0d-114">Value</span></span>  |<span data-ttu-id="eab0d-115">Description</span><span class="sxs-lookup"><span data-stu-id="eab0d-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="eab0d-116">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="eab0d-116">0x80041001</span></span> | <span data-ttu-id="eab0d-117">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="eab0d-117">There has been a general failure.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="eab0d-118">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="eab0d-118">0x80041008</span></span> | <span data-ttu-id="eab0d-119">`null` a été spécifié en tant que paramètre, et n’est pas autorisé dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="eab0d-119">`null` was specified as a parameter, and it is not legal in this usage.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="eab0d-120">0x80041006</span><span class="sxs-lookup"><span data-stu-id="eab0d-120">0x80041006</span></span> | <span data-ttu-id="eab0d-121">Pas assez de mémoire est disponible pour cloner l’objet.</span><span class="sxs-lookup"><span data-stu-id="eab0d-121">Not enough memory is available to clone the object.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="eab0d-122">0</span><span class="sxs-lookup"><span data-stu-id="eab0d-122">0</span></span> | <span data-ttu-id="eab0d-123">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="eab0d-123">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="eab0d-124">Notes</span><span class="sxs-lookup"><span data-stu-id="eab0d-124">Remarks</span></span>

<span data-ttu-id="eab0d-125">Cette fonction encapsule un appel à la [IWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) (méthode).</span><span class="sxs-lookup"><span data-stu-id="eab0d-125">This function wraps a call to the [IWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

<span data-ttu-id="eab0d-126">L’objet cloné est un objet COM qui a un décompte de références de 1.</span><span class="sxs-lookup"><span data-stu-id="eab0d-126">The cloned object is a COM object that has a reference count of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab0d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eab0d-127">Requirements</span></span>  
 <span data-ttu-id="eab0d-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eab0d-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eab0d-129">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="eab0d-129">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="eab0d-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="eab0d-130">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eab0d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eab0d-131">See also</span></span>  
[<span data-ttu-id="eab0d-132">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="eab0d-132">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
