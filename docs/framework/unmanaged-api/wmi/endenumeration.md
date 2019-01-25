---
title: EndEnumeration, fonction (référence des API non managées)
description: La fonction EndEnumeration met fin à une énumération.
ms.date: 11/06/2017
api_name:
- EndEnumeration
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- EndEnumeration
helpviewer_keywords:
- EndEnumeration function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f80503277d6a5d748dffa7783a19c6353b2e7f8d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54505118"
---
# <a name="endenumeration-function"></a><span data-ttu-id="2aa3a-103">EndEnumeration, fonction</span><span class="sxs-lookup"><span data-stu-id="2aa3a-103">EndEnumeration function</span></span>
<span data-ttu-id="2aa3a-104">Met fin à une séquence d’énumération démarrée avec un appel à la [BeginEnumeration, fonction](beginenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="2aa3a-104">Terminates an enumeration sequence started with a call to the [BeginEnumeration function](beginenumeration.md).</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="2aa3a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2aa3a-105">Syntax</span></span>  
  
```  
HRESULT EndEnumeration (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr 
); 
```  

## <a name="parameters"></a><span data-ttu-id="2aa3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2aa3a-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="2aa3a-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="2aa3a-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="2aa3a-108">[in] Un pointeur vers un [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span><span class="sxs-lookup"><span data-stu-id="2aa3a-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>


## <a name="return-value"></a><span data-ttu-id="2aa3a-109">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2aa3a-109">Return value</span></span>

<span data-ttu-id="2aa3a-110">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="2aa3a-110">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="2aa3a-111">Constante</span><span class="sxs-lookup"><span data-stu-id="2aa3a-111">Constant</span></span>  |<span data-ttu-id="2aa3a-112">Value</span><span class="sxs-lookup"><span data-stu-id="2aa3a-112">Value</span></span>  |<span data-ttu-id="2aa3a-113">Description</span><span class="sxs-lookup"><span data-stu-id="2aa3a-113">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="2aa3a-114">0x80041001</span><span class="sxs-lookup"><span data-stu-id="2aa3a-114">0x80041001</span></span> | <span data-ttu-id="2aa3a-115">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="2aa3a-115">There has been a general failure.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="2aa3a-116">0</span><span class="sxs-lookup"><span data-stu-id="2aa3a-116">0</span></span> | <span data-ttu-id="2aa3a-117">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="2aa3a-117">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="2aa3a-118">Notes</span><span class="sxs-lookup"><span data-stu-id="2aa3a-118">Remarks</span></span>

<span data-ttu-id="2aa3a-119">Cette fonction encapsule un appel à la [IWbemClassObject::EndEnumeration](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) (méthode).</span><span class="sxs-lookup"><span data-stu-id="2aa3a-119">This function wraps a call to the [IWbemClassObject::EndEnumeration](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) method.</span></span>

<span data-ttu-id="2aa3a-120">Un appel à la `EndEnumeration` fonction n’est pas obligatoire, mais il est recommandé car il libère les ressources associées à l’énumération.</span><span class="sxs-lookup"><span data-stu-id="2aa3a-120">A call to the `EndEnumeration` function is not required, but it is recommended because it releases resources associated with the enumeration.</span></span> <span data-ttu-id="2aa3a-121">Toutefois, les ressources sont libérées automatiquement lors de l’énumération suivante est démarrée ou l’objet est libéré.</span><span class="sxs-lookup"><span data-stu-id="2aa3a-121">However, the resoruces are deallocated automatically when the next enumeration is started or the object is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="2aa3a-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="2aa3a-122">Requirements</span></span>  
 <span data-ttu-id="2aa3a-123">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2aa3a-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2aa3a-124">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="2aa3a-124">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="2aa3a-125">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2aa3a-125">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2aa3a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2aa3a-126">See also</span></span>
- [<span data-ttu-id="2aa3a-127">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="2aa3a-127">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
