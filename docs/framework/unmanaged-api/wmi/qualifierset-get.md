---
title: QualifierSet_Get (fonction) (référence des API non managées)
description: La fonction QualifierSet_Get Obtient un qualificateur nommé.
ms.date: 11/06/2017
api_name:
- QualifierSet_Get
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_Get
helpviewer_keywords:
- QualifierSet_Get function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b0dc76a2732bf9c1e4f3a26fa2d045bfbcd837ec
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59181088"
---
# <a name="qualifiersetget-function"></a><span data-ttu-id="50b47-103">QualifierSet_Get (fonction)</span><span class="sxs-lookup"><span data-stu-id="50b47-103">QualifierSet_Get function</span></span>
<span data-ttu-id="50b47-104">Obtient le qualificateur nommé spécifié.</span><span class="sxs-lookup"><span data-stu-id="50b47-104">Gets the specified named qualifier.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="50b47-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50b47-105">Syntax</span></span>  
  
```  
HRESULT QualifierSet_Get (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LPCWSTR              wszName,
   [in] LONG                 lFlags,
   [out] VARIANT*            pVal,
   [out] LONG*               plFlavor                 
); 
```  

## <a name="parameters"></a><span data-ttu-id="50b47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50b47-106">Parameters</span></span>

`vFunc`   
<span data-ttu-id="50b47-107">[in] Ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="50b47-107">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="50b47-108">[in] Un pointeur vers un [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span><span class="sxs-lookup"><span data-stu-id="50b47-108">[in] A pointer to an [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span></span>

`wszName`   
<span data-ttu-id="50b47-109">[in] Le nom du qualificateur dont la valeur est demandée.</span><span class="sxs-lookup"><span data-stu-id="50b47-109">[in] The name of the qualifier whose value is requested.</span></span>

`lFlags`   
<span data-ttu-id="50b47-110">[in] Réservée.</span><span class="sxs-lookup"><span data-stu-id="50b47-110">[in] Reserved.</span></span> <span data-ttu-id="50b47-111">Ce paramètre doit être 0.</span><span class="sxs-lookup"><span data-stu-id="50b47-111">This parameter must be 0.</span></span>

`pVal`   
<span data-ttu-id="50b47-112">[out] Cas de réussite, le type correct et la valeur du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="50b47-112">[out] When successful, the correct type and value for the qualifier.</span></span> <span data-ttu-id="50b47-113">Si la fonction échoue, le `VARIANT` vers lequel pointe `pVal` n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="50b47-113">If the function fails, the `VARIANT` pointed to by `pVal` is not modified.</span></span> <span data-ttu-id="50b47-114">Si ce paramètre est `null`, le paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="50b47-114">If this parameter is `null`, the parameter is ignored.</span></span>

`plFlavor`   
<span data-ttu-id="50b47-115">[out] Pointeur vers un entier LONG qui reçoit les bits de la version qualificateur pour le qualificateur demandé.</span><span class="sxs-lookup"><span data-stu-id="50b47-115">[out] A pointer to a LONG that receives the qualifier flavor bits for the requested qualifier.</span></span> <span data-ttu-id="50b47-116">Si les informations de version ne sont pas souhaitées, ce paramètre peut être `null`.</span><span class="sxs-lookup"><span data-stu-id="50b47-116">If flavor information is not desired, this parameter can be `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="50b47-117">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="50b47-117">Return value</span></span>

<span data-ttu-id="50b47-118">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="50b47-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="50b47-119">Constante</span><span class="sxs-lookup"><span data-stu-id="50b47-119">Constant</span></span>  |<span data-ttu-id="50b47-120">Value</span><span class="sxs-lookup"><span data-stu-id="50b47-120">Value</span></span>  |<span data-ttu-id="50b47-121">Description</span><span class="sxs-lookup"><span data-stu-id="50b47-121">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="50b47-122">0x80041008</span><span class="sxs-lookup"><span data-stu-id="50b47-122">0x80041008</span></span> | <span data-ttu-id="50b47-123">Un paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="50b47-123">A parameter is not valid.</span></span> |
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="50b47-124">0x80041002</span><span class="sxs-lookup"><span data-stu-id="50b47-124">0x80041002</span></span> | <span data-ttu-id="50b47-125">Le qualificateur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="50b47-125">The specified qualifier does not exist.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="50b47-126">0</span><span class="sxs-lookup"><span data-stu-id="50b47-126">0</span></span> | <span data-ttu-id="50b47-127">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="50b47-127">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="50b47-128">Notes</span><span class="sxs-lookup"><span data-stu-id="50b47-128">Remarks</span></span>

<span data-ttu-id="50b47-129">Cette fonction encapsule un appel à la [IWbemQualifierSet::Get](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-get) (méthode).</span><span class="sxs-lookup"><span data-stu-id="50b47-129">This function wraps a call to the [IWbemQualifierSet::Get](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-get) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b47-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50b47-130">Requirements</span></span>  
 <span data-ttu-id="50b47-131">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="50b47-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50b47-132">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="50b47-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="50b47-133">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="50b47-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50b47-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50b47-134">See also</span></span>

- [<span data-ttu-id="50b47-135">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="50b47-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
