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
ms.openlocfilehash: bf9cca10a580af7991889de6993e931347fc27ea
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59120956"
---
# <a name="clone-function"></a><span data-ttu-id="ab43e-103">Clone, fonction</span><span class="sxs-lookup"><span data-stu-id="ab43e-103">Clone function</span></span>
<span data-ttu-id="ab43e-104">Retourne un nouvel objet qui est un clone complet de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="ab43e-104">Returns a new object that is a complete clone of the current object.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="ab43e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab43e-105">Syntax</span></span>  
  
```  
HRESULT Clone (
   [in] int                  vFunc, 
   [in] IWbemClassObject*    ptr, 
   [out] IWbemClassObject**  ppCopy
); 
```  

## <a name="parameters"></a><span data-ttu-id="ab43e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab43e-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="ab43e-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="ab43e-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="ab43e-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="ab43e-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`ppCopy`  
<span data-ttu-id="ab43e-109">[out] Un nouvel objet qui est une liste complète isolés de `ptr`.</span><span class="sxs-lookup"><span data-stu-id="ab43e-109">[out] A new object that is a complete lone of `ptr`.</span></span> <span data-ttu-id="ab43e-110">Cet argument ne peut pas être `null` s’il reçoit la copie de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="ab43e-110">This argument cannot be `null` if it receives the copy of the current object.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab43e-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ab43e-111">Return value</span></span>

<span data-ttu-id="ab43e-112">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="ab43e-112">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="ab43e-113">Constante</span><span class="sxs-lookup"><span data-stu-id="ab43e-113">Constant</span></span>  |<span data-ttu-id="ab43e-114">Value</span><span class="sxs-lookup"><span data-stu-id="ab43e-114">Value</span></span>  |<span data-ttu-id="ab43e-115">Description</span><span class="sxs-lookup"><span data-stu-id="ab43e-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="ab43e-116">0x80041001</span><span class="sxs-lookup"><span data-stu-id="ab43e-116">0x80041001</span></span> | <span data-ttu-id="ab43e-117">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="ab43e-117">There has been a general failure.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="ab43e-118">0x80041008</span><span class="sxs-lookup"><span data-stu-id="ab43e-118">0x80041008</span></span> | <span data-ttu-id="ab43e-119">`null` a été spécifié en tant que paramètre, et n’est pas autorisé dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="ab43e-119">`null` was specified as a parameter, and it is not legal in this usage.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="ab43e-120">0x80041006</span><span class="sxs-lookup"><span data-stu-id="ab43e-120">0x80041006</span></span> | <span data-ttu-id="ab43e-121">Pas assez de mémoire est disponible pour cloner l’objet.</span><span class="sxs-lookup"><span data-stu-id="ab43e-121">Not enough memory is available to clone the object.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="ab43e-122">0</span><span class="sxs-lookup"><span data-stu-id="ab43e-122">0</span></span> | <span data-ttu-id="ab43e-123">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="ab43e-123">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="ab43e-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ab43e-124">Remarks</span></span>

<span data-ttu-id="ab43e-125">Cette fonction encapsule un appel à la [IWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) (méthode).</span><span class="sxs-lookup"><span data-stu-id="ab43e-125">This function wraps a call to the [IWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

<span data-ttu-id="ab43e-126">L’objet cloné est un objet COM qui a un décompte de références de 1.</span><span class="sxs-lookup"><span data-stu-id="ab43e-126">The cloned object is a COM object that has a reference count of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab43e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab43e-127">Requirements</span></span>  
 <span data-ttu-id="ab43e-128">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab43e-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab43e-129">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="ab43e-129">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="ab43e-130">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="ab43e-130">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab43e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab43e-131">See also</span></span>

- [<span data-ttu-id="ab43e-132">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="ab43e-132">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
