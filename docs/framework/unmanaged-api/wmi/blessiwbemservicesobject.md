---
title: Blessiwbemservicesobject, fonction (référence des API non managées)
description: Blessiwbemservicesobject, de la fonction indique si les informations d’identification de l’utilisateur autorisent l’accès à un objet IWbemServices
ms.date: 11/06/2017
api_name:
- BlessIWbemServicesObject
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- BlessIWbemServicesObject
helpviewer_keywords:
- BlessIWbemServicesObject function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a561c5af868968624ee9ee81050d87b17c4591be
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54624416"
---
# <a name="blessiwbemservicesobject-function"></a><span data-ttu-id="bf8c2-103">Blessiwbemservicesobject, fonction</span><span class="sxs-lookup"><span data-stu-id="bf8c2-103">BlessIWbemServicesObject function</span></span>
<span data-ttu-id="bf8c2-104">Indique si les informations d’identification utilisateur autorisent l’accès à une certaine [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) objet.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-104">Indicates whether the user credentials permit access to a specified [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) object.</span></span>   
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="bf8c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf8c2-105">Syntax</span></span>  
  
```  
HRESULT BlessIWbemServicesObject (
   [in] IUnknown* pIUnknown,
   [in] BSTR strUser, 
   [in] BSTR strPassword, 
   [in] BSTR strAuthority, 
   [in] DWORD impLevel, 
   [in] DWORD authnLevel
);
```  

## <a name="parameters"></a><span data-ttu-id="bf8c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf8c2-106">Parameters</span></span>

`pIWbemServices`  
<span data-ttu-id="bf8c2-107">[in] Pointeur vers un objet de service WMI.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-107">[in] A pointer to a WMI service object.</span></span>

`strUser`  
<span data-ttu-id="bf8c2-108">[in] Le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-108">[in] The user name.</span></span>

`strPassword`  
<span data-ttu-id="bf8c2-109">[in] Le mot de passe associé `strUser`.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-109">[in] The password associated with `strUser`.</span></span>

<span data-ttu-id="bf8c2-110">`strAuthority` [in] Le nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-110">`strAuthority` [in] The domain name of the user.</span></span> <span data-ttu-id="bf8c2-111">Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-111">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

<span data-ttu-id="bf8c2-112">`impLevel` [in] Le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-112">`impLevel` [in] The impersonation level.</span></span>

<span data-ttu-id="bf8c2-113">`authnLevel` [in] Le niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-113">`authnLevel` [in] The authorization level.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf8c2-114">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bf8c2-114">Return value</span></span>

<span data-ttu-id="bf8c2-115">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WinError.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="bf8c2-115">The following values returned by this function are defined in the *WinError.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="bf8c2-116">Constante</span><span class="sxs-lookup"><span data-stu-id="bf8c2-116">Constant</span></span>  |<span data-ttu-id="bf8c2-117">Value</span><span class="sxs-lookup"><span data-stu-id="bf8c2-117">Value</span></span>  |<span data-ttu-id="bf8c2-118">Description</span><span class="sxs-lookup"><span data-stu-id="bf8c2-118">Description</span></span>  |
|---------|---------|---------|
| `E_INVALIDARG` | <span data-ttu-id="bf8c2-119">0x80070057</span><span class="sxs-lookup"><span data-stu-id="bf8c2-119">0x80070057</span></span> | <span data-ttu-id="bf8c2-120">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-120">One or more arguments are invalid.</span></span> |
| `E_POINTER` | <span data-ttu-id="bf8c2-121">0x80004003</span><span class="sxs-lookup"><span data-stu-id="bf8c2-121">0x80004003</span></span> | <span data-ttu-id="bf8c2-122">`pIWbemServices` a la valeur `null`.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-122">`pIWbemServices` is `null`.</span></span> | 
| `E_FAIL` | <span data-ttu-id="bf8c2-123">0x80000008</span><span class="sxs-lookup"><span data-stu-id="bf8c2-123">0x80000008</span></span> | <span data-ttu-id="bf8c2-124">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-124">An unspecified error has occurred.</span></span> |
| `E_OUTOFMEMORY` | <span data-ttu-id="bf8c2-125">0x80000002</span><span class="sxs-lookup"><span data-stu-id="bf8c2-125">0x80000002</span></span> | <span data-ttu-id="bf8c2-126">Mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-126">Insufficient memory is available to perform the operation.</span></span> | 
| `S_OK` | <span data-ttu-id="bf8c2-127">0</span><span class="sxs-lookup"><span data-stu-id="bf8c2-127">0</span></span> | <span data-ttu-id="bf8c2-128">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="bf8c2-128">The function call was successful.</span></span> | 

## <a name="requirements"></a><span data-ttu-id="bf8c2-129">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bf8c2-129">Requirements</span></span>  
 <span data-ttu-id="bf8c2-130">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bf8c2-130">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bf8c2-131">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="bf8c2-131">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="bf8c2-132">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="bf8c2-132">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf8c2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf8c2-133">See also</span></span>
- [<span data-ttu-id="bf8c2-134">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="bf8c2-134">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
