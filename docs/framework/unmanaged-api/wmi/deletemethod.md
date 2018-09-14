---
title: DeleteMethod, fonction (référence des API non managées)
description: La fonction DeleteMethod supprime la méthode spécifiée à partir d’une définition de classe CIM.
ms.date: 11/06/2017
api_name:
- DeleteMethod
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- DeleteMethod
helpviewer_keywords:
- DeleteMethod function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 5996ce41c80cb54c4fcb9104c2993c85bcc2b466
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45510232"
---
# <a name="deletemethod-function"></a><span data-ttu-id="f31ee-103">DeleteMethod, fonction</span><span class="sxs-lookup"><span data-stu-id="f31ee-103">DeleteMethod function</span></span>
<span data-ttu-id="f31ee-104">Supprime la méthode spécifiée à partir d’une définition de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="f31ee-104">Deletes the specified method from a CIM class definition.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="f31ee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f31ee-105">Syntax</span></span>  
  
```  
HRESULT Delete (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName 
); 
```  

## <a name="parameters"></a><span data-ttu-id="f31ee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f31ee-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="f31ee-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f31ee-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="f31ee-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="f31ee-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszName`  
<span data-ttu-id="f31ee-109">[in] Le nom de la méthode à supprimer de la table de la classe.</span><span class="sxs-lookup"><span data-stu-id="f31ee-109">[in] The name of the method to remove from the class table.</span></span> <span data-ttu-id="f31ee-110">`wszName` doit être un pointeur désignant une valide `LPCWSTR`.</span><span class="sxs-lookup"><span data-stu-id="f31ee-110">`wszName` must be a pointer to a valid `LPCWSTR`.</span></span>

## <a name="return-value"></a><span data-ttu-id="f31ee-111">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f31ee-111">Return value</span></span>

<span data-ttu-id="f31ee-112">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="f31ee-112">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="f31ee-113">Constante</span><span class="sxs-lookup"><span data-stu-id="f31ee-113">Constant</span></span>  |<span data-ttu-id="f31ee-114">Value</span><span class="sxs-lookup"><span data-stu-id="f31ee-114">Value</span></span>  |<span data-ttu-id="f31ee-115">Description</span><span class="sxs-lookup"><span data-stu-id="f31ee-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_NOT_FOUND` | <span data-ttu-id="f31ee-116">0x80041002</span><span class="sxs-lookup"><span data-stu-id="f31ee-116">0x80041002</span></span> | <span data-ttu-id="f31ee-117">La méthode spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f31ee-117">The specified method does not exist.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="f31ee-118">0x80041006</span><span class="sxs-lookup"><span data-stu-id="f31ee-118">0x80041006</span></span> | <span data-ttu-id="f31ee-119">Il n’est pas suffisamment de mémoire pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f31ee-119">There is not enough memory to complete the operation.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="f31ee-120">0</span><span class="sxs-lookup"><span data-stu-id="f31ee-120">0</span></span> | <span data-ttu-id="f31ee-121">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="f31ee-121">The function call was successful.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="f31ee-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f31ee-122">Remarks</span></span>

<span data-ttu-id="f31ee-123">Cette fonction encapsule un appel à la [IWbemClassObject::DeleteMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-deletemethod) (méthode).</span><span class="sxs-lookup"><span data-stu-id="f31ee-123">This function wraps a call to the [IWbemClassObject::DeleteMethod](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-deletemethod) method.</span></span>

<span data-ttu-id="f31ee-124">Suppression de la méthode n’est pas prise en charge pour [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointeurs qui pointent vers des instances CIM.</span><span class="sxs-lookup"><span data-stu-id="f31ee-124">Method deletion is not supported for [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) pointers that point to CIM instances.</span></span>

## <a name="requirements"></a><span data-ttu-id="f31ee-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f31ee-125">Requirements</span></span>  
 <span data-ttu-id="f31ee-126">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f31ee-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f31ee-127">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="f31ee-127">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="f31ee-128">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f31ee-128">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f31ee-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f31ee-129">See also</span></span>  
[<span data-ttu-id="f31ee-130">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="f31ee-130">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
