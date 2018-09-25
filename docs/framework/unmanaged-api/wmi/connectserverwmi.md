---
title: ConnectServerWmi (fonction) (référence des API non managées)
description: La fonction ConnectServerWmi utilise DCOM pour créer une connexion à un espace de noms WMI.
ms.date: 11/06/2017
api_name:
- ConnectServerWmi
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- ConnectServerWmi
helpviewer_keywords:
- ConnectServerWmi function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 244df48606f6d971d6b6e246c4f9b73f916cbdcd
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47083252"
---
# <a name="connectserverwmi-function"></a><span data-ttu-id="0b43e-103">ConnectServerWmi (fonction)</span><span class="sxs-lookup"><span data-stu-id="0b43e-103">ConnectServerWmi function</span></span>
<span data-ttu-id="0b43e-104">Crée une connexion via DCOM à un espace de noms WMI sur un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b43e-104">Creates a connection through DCOM to a WMI namespace on a specified computer.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="0b43e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b43e-105">Syntax</span></span>  
  
```  
HRESULT ConnectServerWmi (
   [in] BSTR               strNetworkResource,
   [in] BSTR               strUser,
   [in] BSTR               strPassword,
   [in] BSTR               strLocale,
   [in] long               lSecurityFlags,
   [in] BSTR               strAuthority,
   [in] IWbemContext*      pCtx,
   [out] IWbemServices**   ppNamespace,
   [in] DWORD              impLevel, 
   [in] DWORD              authLevel
);
```  
## <a name="parameters"></a><span data-ttu-id="0b43e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b43e-106">Parameters</span></span>

<span data-ttu-id="0b43e-107">`strNetworkResource` [in] Pointeur vers un valide `BSTR` qui contient le chemin d’accès de l’objet de l’espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="0b43e-107">`strNetworkResource` [in] Pointer to a valid `BSTR` that contains the object path of the correct WMI namespace.</span></span> <span data-ttu-id="0b43e-108">Consultez le [notes](#remarks) section pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0b43e-108">See the [Remarks](#remarks) section for more information.</span></span>

<span data-ttu-id="0b43e-109">`strUser` [in] Un pointeur vers une valide `BSTR` qui contient le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b43e-109">`strUser` [in] A pointer to a valid `BSTR` that contains the user name.</span></span> <span data-ttu-id="0b43e-110">Un `null` valeur indique le contexte de sécurité actuel.</span><span class="sxs-lookup"><span data-stu-id="0b43e-110">A `null` value indicates the current security context.</span></span> <span data-ttu-id="0b43e-111">Si l’utilisateur provient d’un autre domaine que celui en cours, `strUser` peut également contenir le nom de domaine et d’utilisateur séparés par une barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="0b43e-111">If the user is from a different domain than the current one, `strUser` can also contain the domain and user name separated by a backslash.</span></span> <span data-ttu-id="0b43e-112">`strUser` peut également être dans le format nom utilisateur principal (UPN), tel que `userName@domainName`.</span><span class="sxs-lookup"><span data-stu-id="0b43e-112">`strUser` can also be in user principal name (UPN) format, such as `userName@domainName`.</span></span> <span data-ttu-id="0b43e-113">Consultez le [notes](#remarks) section pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0b43e-113">See the [Remarks](#remarks) section for more information.</span></span>

<span data-ttu-id="0b43e-114">`strPassword` [in] Un pointeur vers une valide `BSTR` qui contient le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="0b43e-114">`strPassword` [in] A pointer to a valid `BSTR` that contains the password.</span></span> <span data-ttu-id="0b43e-115">Un `null` indique le contexte de sécurité actuel.</span><span class="sxs-lookup"><span data-stu-id="0b43e-115">A `null` indicates the current security context.</span></span> <span data-ttu-id="0b43e-116">Une chaîne vide (« ») indique un mot de passe vide.</span><span class="sxs-lookup"><span data-stu-id="0b43e-116">An empty string ("") indicates a valid zero-length password.</span></span>

<span data-ttu-id="0b43e-117">`strLocale` [in] Un pointeur vers une valide `BSTR` qui indique les paramètres régionaux corrects pour la récupération d’informations.</span><span class="sxs-lookup"><span data-stu-id="0b43e-117">`strLocale` [in] A pointer to a valid `BSTR` that indicates the correct locale for information retrieval.</span></span> <span data-ttu-id="0b43e-118">Pour les identificateurs de paramètres régionaux Microsoft, le format de la chaîne est « MS\_*xxx*», où *xxx* est une chaîne au format hexadécimal qui indique l’identificateur de paramètres régionaux (LCID).</span><span class="sxs-lookup"><span data-stu-id="0b43e-118">For Microsoft locale identifiers, the format of the string is "MS\_*xxx*", where *xxx* is a string in hexadecimal form that indicates the locale identifier (LCID).</span></span> <span data-ttu-id="0b43e-119">Si une variable locale non valide est spécifié, la méthode retourne `WBEM_E_INVALID_PARAMETER` sauf sur Windows 7, où les paramètres régionaux par défaut du serveur sont utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="0b43e-119">If an invalid locale is specified, the method returns `WBEM_E_INVALID_PARAMETER` except on Windows 7, where the default locale of the server is used instead.</span></span> <span data-ttu-id="0b43e-120">Si « null1, les paramètres régionaux est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0b43e-120">If \`null1, the current locale is used.</span></span> 
 
<span data-ttu-id="0b43e-121">`lSecurityFlags` [in] Indicateurs à passer à la `ConnectServerWmi` (méthode).</span><span class="sxs-lookup"><span data-stu-id="0b43e-121">`lSecurityFlags` [in] Flags to pass to the `ConnectServerWmi` method.</span></span> <span data-ttu-id="0b43e-122">Une valeur de zéro (0) pour ce paramètre entraîne l’appel à `ConnectServerWmi` retourner uniquement une fois une connexion au serveur est établie.</span><span class="sxs-lookup"><span data-stu-id="0b43e-122">A value of zero (0) for this parameter results in the call to `ConnectServerWmi` returning only after a connection to the server is established.</span></span> <span data-ttu-id="0b43e-123">Cela peut entraîner une application ne répond ne pas indéfiniment si le serveur est rompu.</span><span class="sxs-lookup"><span data-stu-id="0b43e-123">This could result in an application not responding indefinitely if the server is broken.</span></span> <span data-ttu-id="0b43e-124">Les autres valeurs valides sont :</span><span class="sxs-lookup"><span data-stu-id="0b43e-124">The other valid values are:</span></span>

| <span data-ttu-id="0b43e-125">Constante</span><span class="sxs-lookup"><span data-stu-id="0b43e-125">Constant</span></span>  | <span data-ttu-id="0b43e-126">Value</span><span class="sxs-lookup"><span data-stu-id="0b43e-126">Value</span></span>  | <span data-ttu-id="0b43e-127">Description</span><span class="sxs-lookup"><span data-stu-id="0b43e-127">Description</span></span>  |
|---------|---------|---------|
| `CONNECT_REPOSITORY_ONLY` | <span data-ttu-id="0b43e-128">0 x 40</span><span class="sxs-lookup"><span data-stu-id="0b43e-128">0x40</span></span> | <span data-ttu-id="0b43e-129">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="0b43e-129">Reserved for internal use.</span></span> <span data-ttu-id="0b43e-130">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="0b43e-130">Do not use.</span></span> |
| `WBEM_FLAG_CONNECT_USE_MAX_WAIT` | <span data-ttu-id="0b43e-131">0 x 80</span><span class="sxs-lookup"><span data-stu-id="0b43e-131">0x80</span></span> | <span data-ttu-id="0b43e-132">`ConnectServerWmi` retourne en deux minutes ou moins.</span><span class="sxs-lookup"><span data-stu-id="0b43e-132">`ConnectServerWmi` returns in two minutes or less.</span></span> |

<span data-ttu-id="0b43e-133">`strAuthority` [in] Le nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b43e-133">`strAuthority` [in] The domain name of the user.</span></span> <span data-ttu-id="0b43e-134">Il peut afficher les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b43e-134">It can have the following values:</span></span>

| <span data-ttu-id="0b43e-135">Value</span><span class="sxs-lookup"><span data-stu-id="0b43e-135">Value</span></span> | <span data-ttu-id="0b43e-136">Description</span><span class="sxs-lookup"><span data-stu-id="0b43e-136">Description</span></span> |
|---------|---------|
| <span data-ttu-id="0b43e-137">vide</span><span class="sxs-lookup"><span data-stu-id="0b43e-137">blank</span></span> | <span data-ttu-id="0b43e-138">L’authentification NTLM est utilisée et le domaine NTLM de l’utilisateur actuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0b43e-138">NTLM authentication is used, and the NTLM domain of the current user is used.</span></span> <span data-ttu-id="0b43e-139">Si `strUser` Spécifie le domaine (l’emplacement recommandé), il ne doit pas être spécifié ici.</span><span class="sxs-lookup"><span data-stu-id="0b43e-139">If `strUser` specifies the domain (the recommended location), it must not be specified here.</span></span> <span data-ttu-id="0b43e-140">La fonction retourne `WBEM_E_INVALID_PARAMETER` si vous spécifiez le domaine dans les deux paramètres.</span><span class="sxs-lookup"><span data-stu-id="0b43e-140">The function returns `WBEM_E_INVALID_PARAMETER` if you specify the domain in both parameters.</span></span> |
| <span data-ttu-id="0b43e-141">Kerberos :*nom principal*</span><span class="sxs-lookup"><span data-stu-id="0b43e-141">Kerberos:*principal name*</span></span> | <span data-ttu-id="0b43e-142">L’authentification Kerberos est utilisée, et ce paramètre contient un nom principal Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0b43e-142">Kerberos authentication is used, and this parameter contains a Kerberos principal name.</span></span> |
| <span data-ttu-id="0b43e-143">Valeur NTLMDOMAIN :*nom de domaine*</span><span class="sxs-lookup"><span data-stu-id="0b43e-143">NTLMDOMAIN:*domain name*</span></span> | <span data-ttu-id="0b43e-144">L’authentification NT LAN Manager est utilisée, et ce paramètre contient un nom de domaine NTLM.</span><span class="sxs-lookup"><span data-stu-id="0b43e-144">NT LAN Manager authentication is used, and this parameter contains an NTLM domain name.</span></span> |

`pCtx`   
<span data-ttu-id="0b43e-145">[in] En règle générale, ce paramètre est `null`.</span><span class="sxs-lookup"><span data-stu-id="0b43e-145">[in] Typically, this parameter is is `null`.</span></span> <span data-ttu-id="0b43e-146">Sinon, il est un pointeur vers un [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) objet requis par un ou plusieurs fournisseurs de la classe dynamique.</span><span class="sxs-lookup"><span data-stu-id="0b43e-146">Otherwise, it is a pointer to an [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) object required by one or more dynamic class providers.</span></span> 

`ppNamespace`  
<span data-ttu-id="0b43e-147">[out] Lorsque la fonction retourne, reçoit un pointeur vers un [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) objet lié à l’espace de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="0b43e-147">[out] When the function returns, receives a pointer to an [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) object bound to the specified namespace.</span></span> <span data-ttu-id="0b43e-148">Il est défini pour pointer vers `null` lorsqu’il existe une erreur.</span><span class="sxs-lookup"><span data-stu-id="0b43e-148">It is set to point to `null` when there is an error.</span></span>

`impLevel`  
<span data-ttu-id="0b43e-149">[in] Le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="0b43e-149">[in] The impersonation level.</span></span>

`authLevel`  
<span data-ttu-id="0b43e-150">[in] Le niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="0b43e-150">[in] The authorization level.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b43e-151">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0b43e-151">Return value</span></span>

<span data-ttu-id="0b43e-152">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="0b43e-152">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="0b43e-153">Constante</span><span class="sxs-lookup"><span data-stu-id="0b43e-153">Constant</span></span>  |<span data-ttu-id="0b43e-154">Value</span><span class="sxs-lookup"><span data-stu-id="0b43e-154">Value</span></span>  |<span data-ttu-id="0b43e-155">Description</span><span class="sxs-lookup"><span data-stu-id="0b43e-155">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="0b43e-156">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="0b43e-156">0x80041001</span></span> | <span data-ttu-id="0b43e-157">Il y a eu une défaillance générale.</span><span class="sxs-lookup"><span data-stu-id="0b43e-157">There has been a general failure.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="0b43e-158">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="0b43e-158">0x80041008</span></span> | <span data-ttu-id="0b43e-159">Un paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0b43e-159">A parameter is not valid.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="0b43e-160">0x80041006</span><span class="sxs-lookup"><span data-stu-id="0b43e-160">0x80041006</span></span> | <span data-ttu-id="0b43e-161">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0b43e-161">Not enough memory is available to complete the operation.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="0b43e-162">0</span><span class="sxs-lookup"><span data-stu-id="0b43e-162">0</span></span> | <span data-ttu-id="0b43e-163">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="0b43e-163">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="0b43e-164">Notes</span><span class="sxs-lookup"><span data-stu-id="0b43e-164">Remarks</span></span>

<span data-ttu-id="0b43e-165">Cette fonction encapsule un appel à la [IWbemLocator::ConnectServer](https://msdn.microsoft.com/libraryaa391769%28v=vs.85%29.aspx) (méthode).</span><span class="sxs-lookup"><span data-stu-id="0b43e-165">This function wraps a call to the [IWbemLocator::ConnectServer](https://msdn.microsoft.com/libraryaa391769%28v=vs.85%29.aspx) method.</span></span>

 <span data-ttu-id="0b43e-166">Pour un accès local à l’espace de noms par défaut, `strNetworkResource` peut être un chemin d’accès de l’objet simple : « root\default » ou «\\.\root\default ».</span><span class="sxs-lookup"><span data-stu-id="0b43e-166">For local access to the default namespace, `strNetworkResource` can be a simple object path: "root\default" or "\\.\root\default".</span></span> <span data-ttu-id="0b43e-167">Pour accéder à l’espace de noms par défaut sur un ordinateur distant à l’aide de la mise en réseau COM ou compatible avec Microsoft, incluent le nom d’ordinateur : «\\myserver\root\default ».</span><span class="sxs-lookup"><span data-stu-id="0b43e-167">For access to the default namespace on a remote computer using COM or Microsoft-compatible networking, include the computer name: "\\myserver\root\default".</span></span> <span data-ttu-id="0b43e-168">Le nom d’ordinateur peut être une adresse IP ou nom DNS.</span><span class="sxs-lookup"><span data-stu-id="0b43e-168">The computer name also can be a DNS name or IP address.</span></span> <span data-ttu-id="0b43e-169">Le `ConnectServerWmi` fonction peut également se connecter avec les ordinateurs qui exécutent IPv6 à l’aide d’une adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="0b43e-169">The `ConnectServerWmi` function can also connect with computers running IPv6 using an IPv6 address.</span></span>

<span data-ttu-id="0b43e-170">`strUser` ne peut pas être une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="0b43e-170">`strUser` cannot be an empty string.</span></span> <span data-ttu-id="0b43e-171">Si le domaine est spécifié dans `strAuthority`, il ne doit pas également figurer dans `strUser`, ou la fonction retourne `WBEM_E_INVALID_PARAMETER`.</span><span class="sxs-lookup"><span data-stu-id="0b43e-171">If the domain is specified in `strAuthority`, it must not also be included in `strUser`, or the function returns `WBEM_E_INVALID_PARAMETER`.</span></span>


## <a name="requirements"></a><span data-ttu-id="0b43e-172">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b43e-172">Requirements</span></span>  
 <span data-ttu-id="0b43e-173">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0b43e-173">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0b43e-174">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="0b43e-174">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="0b43e-175">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="0b43e-175">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b43e-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b43e-176">See also</span></span>  
[<span data-ttu-id="0b43e-177">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="0b43e-177">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
