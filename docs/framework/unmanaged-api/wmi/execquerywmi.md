---
title: Execquerywmi, fonction (référence des API non managées)
description: Execquerywmi, de la fonction exécute une requête pour récupérer des objets.
ms.date: 11/06/2017
api_name:
- ExecQueryWmi
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- ExecQueryWmi
helpviewer_keywords:
- ExecQueryWmi function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 402bbcb9ad5e462a55c5ec2716417f512f03ee19
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57373216"
---
# <a name="execquerywmi-function"></a><span data-ttu-id="63d61-103">Execquerywmi, fonction</span><span class="sxs-lookup"><span data-stu-id="63d61-103">ExecQueryWmi function</span></span>

<span data-ttu-id="63d61-104">Exécute une requête pour récupérer des objets.</span><span class="sxs-lookup"><span data-stu-id="63d61-104">Executes a query to retrieve objects.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="63d61-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63d61-105">Syntax</span></span>

```cpp
HRESULT ExecQueryWmi (
   [in] BSTR                    strQueryLanguage,
   [in] BSTR                    strQuery,
   [in] long                    lFlags,
   [in] IWbemContext*           pCtx,
   [out] IEnumWbemClassObject** ppEnum,
   [in] DWORD                   authLevel,
   [in] DWORD                   impLevel,
   [in] IWbemServices*          pCurrentNamespace,
   [in] BSTR                    strUser,
   [in] BSTR                    strPassword,
   [in] BSTR                    strAuthority
);
```

## <a name="parameters"></a><span data-ttu-id="63d61-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63d61-106">Parameters</span></span>

`strQueryLanguage`\
<span data-ttu-id="63d61-107">[in] Chaîne avec le langage de requête valide pris en charge par la gestion de Windows.</span><span class="sxs-lookup"><span data-stu-id="63d61-107">[in] A string with the valid query language supported by Windows Management.</span></span> <span data-ttu-id="63d61-108">Il doit être « WQL », l’acronyme de langage de requête WMI.</span><span class="sxs-lookup"><span data-stu-id="63d61-108">It must be "WQL", the acronym for WMI Query Language.</span></span>

`strQuery`\
<span data-ttu-id="63d61-109">[in] Le texte de la requête.</span><span class="sxs-lookup"><span data-stu-id="63d61-109">[in] The text of the query.</span></span> <span data-ttu-id="63d61-110">Ce paramètre ne peut pas être `null`.</span><span class="sxs-lookup"><span data-stu-id="63d61-110">This parameter cannot be `null`.</span></span>

`lFlags`\
<span data-ttu-id="63d61-111">[in] Combinaison d’indicateurs qui affectent le comportement de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="63d61-111">[in] A combination of flags that affect the behavior of this function.</span></span> <span data-ttu-id="63d61-112">Les valeurs suivantes sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="63d61-112">The following values are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

| <span data-ttu-id="63d61-113">Constante</span><span class="sxs-lookup"><span data-stu-id="63d61-113">Constant</span></span> | <span data-ttu-id="63d61-114">Value</span><span class="sxs-lookup"><span data-stu-id="63d61-114">Value</span></span>  | <span data-ttu-id="63d61-115">Description</span><span class="sxs-lookup"><span data-stu-id="63d61-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_FLAG_USE_AMENDED_QUALIFIERS` | <span data-ttu-id="63d61-116">0x20000</span><span class="sxs-lookup"><span data-stu-id="63d61-116">0x20000</span></span> | <span data-ttu-id="63d61-117">Si l’ensemble, la fonction récupère les qualificateurs stockées dans l’espace de noms localisé des paramètres régionaux de la connexion actuelle.</span><span class="sxs-lookup"><span data-stu-id="63d61-117">If set, the function retrieves the amended qualifiers stored in the localized namespace of the current connection's locale.</span></span> <br/> <span data-ttu-id="63d61-118">Si ce n’est pas le cas, ensemble, la fonction récupère uniquement les qualificateurs stockées dans l’espace de noms immédiate.</span><span class="sxs-lookup"><span data-stu-id="63d61-118">If not set, the function retrieves only the qualifiers stored in the immediate namespace.</span></span> |
| `WBEM_FLAG_RETURN_IMMEDIATELY` | <span data-ttu-id="63d61-119">0x10</span><span class="sxs-lookup"><span data-stu-id="63d61-119">0x10</span></span> | <span data-ttu-id="63d61-120">L’indicateur provoque un appel semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="63d61-120">The flag causes a semisynchronous call.</span></span> |
| `WBEM_FLAG_FORWARD_ONLY` | <span data-ttu-id="63d61-121">0x20</span><span class="sxs-lookup"><span data-stu-id="63d61-121">0x20</span></span> | <span data-ttu-id="63d61-122">La fonction retourne un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="63d61-122">The function returns a forward-only enumerator.</span></span> <span data-ttu-id="63d61-123">En règle générale, les énumérateurs avant uniquement sont plus rapides et utilisent moins de mémoire que les énumérateurs classiques, mais ils ne permettent pas d’appels à [Clone](clone.md).</span><span class="sxs-lookup"><span data-stu-id="63d61-123">Typically, forward-only enumerators are faster and use less memory than conventional enumerators, but they do not allow calls to [Clone](clone.md).</span></span> |
| `WBEM_FLAG_BIDIRECTIONAL` | <span data-ttu-id="63d61-124">0</span><span class="sxs-lookup"><span data-stu-id="63d61-124">0</span></span> | <span data-ttu-id="63d61-125">WMI conserve les pointeurs vers les objets dans l’énumération jusqu'à ce qu’ils sont libérés.</span><span class="sxs-lookup"><span data-stu-id="63d61-125">WMI retains pointers to objects in the enumeration until they are released.</span></span> |
| `WBEM_FLAG_ENSURE_LOCATABLE` | <span data-ttu-id="63d61-126">0x100</span><span class="sxs-lookup"><span data-stu-id="63d61-126">0x100</span></span> | <span data-ttu-id="63d61-127">Permet de s’assurer que les objets retournés ont suffisamment d’informations dans leur par conséquent, ces propriétés système, telles que **__PATH**, **__RELPATH**, et **__SERVER**, ne sont pas `null`.</span><span class="sxs-lookup"><span data-stu-id="63d61-127">Ensures that any returned objects have enough information in them so that system properties, such as **__PATH**, **__RELPATH**, and **__SERVER**, are not `null`.</span></span> |
| `WBEM_FLAG_PROTOTYPE` | <span data-ttu-id="63d61-128">2</span><span class="sxs-lookup"><span data-stu-id="63d61-128">2</span></span> | <span data-ttu-id="63d61-129">Cet indicateur est utilisé pour le prototypage.</span><span class="sxs-lookup"><span data-stu-id="63d61-129">This flag is used for prototyping.</span></span> <span data-ttu-id="63d61-130">Il ne s’exécute pas la requête et retourne à la place un objet qui ressemble à un objet de résultat par défaut.</span><span class="sxs-lookup"><span data-stu-id="63d61-130">It does not execute the query and instead returns an object that looks like a typical result object.</span></span> |
| `WBEM_FLAG_DIRECT_READ` | <span data-ttu-id="63d61-131">0x200</span><span class="sxs-lookup"><span data-stu-id="63d61-131">0x200</span></span> | <span data-ttu-id="63d61-132">Entraîne un accès direct au fournisseur pour la classe spécifiée sans tenir compte de sa classe parente ou n’importe quelles sous-classes.</span><span class="sxs-lookup"><span data-stu-id="63d61-132">Causes direct access to the provider for the class specified without regard to its parent class or any subclasses.</span></span> |

<span data-ttu-id="63d61-133">Les indicateurs recommandées sont `WBEM_FLAG_RETURN_IMMEDIATELY` et `WBEM_FLAG_FORWARD_ONLY` pour de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="63d61-133">The recommended flags are `WBEM_FLAG_RETURN_IMMEDIATELY` and `WBEM_FLAG_FORWARD_ONLY` for best performance.</span></span>

`pCtx`\
<span data-ttu-id="63d61-134">[in] En règle générale, cette valeur est `null`.</span><span class="sxs-lookup"><span data-stu-id="63d61-134">[in] Typically, this value is `null`.</span></span> <span data-ttu-id="63d61-135">Sinon, il est un pointeur vers un [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) instance qui peut être utilisé par le fournisseur qui fournit les classes demandées.</span><span class="sxs-lookup"><span data-stu-id="63d61-135">Otherwise, it is a pointer to an [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) instance that can be used by the provider that is providing the requested classes.</span></span>

`ppEnum`\
<span data-ttu-id="63d61-136">[out] Si aucune erreur ne se produit, reçoit le pointeur vers l’énumérateur qui permet à l’appelant récupérer les instances dans le jeu de résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="63d61-136">[out] If no error occurs, receives the pointer to the enumerator that allows the caller to retrieve the instances in the query's result set.</span></span> <span data-ttu-id="63d61-137">La requête peut avoir un jeu de résultats avec zéro instances.</span><span class="sxs-lookup"><span data-stu-id="63d61-137">The query can have a result set with zero instances.</span></span> <span data-ttu-id="63d61-138">Consultez le [notes](#remarks) section pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="63d61-138">See the [Remarks](#remarks) section for more information.</span></span>

`authLevel`\
<span data-ttu-id="63d61-139">[in] Le niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="63d61-139">[in] The authorization level.</span></span>

`impLevel`\
<span data-ttu-id="63d61-140">[in] Le niveau d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="63d61-140">[in] The impersonation level.</span></span>

`pCurrentNamespace`\
<span data-ttu-id="63d61-141">[in] Un pointeur vers un [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) objet qui représente l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="63d61-141">[in] A pointer to an [IWbemServices](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) object that represents the current namespace.</span></span>

`strUser`\
<span data-ttu-id="63d61-142">[in] Le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63d61-142">[in] The user name.</span></span> <span data-ttu-id="63d61-143">Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="63d61-143">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

`strPassword`\
<span data-ttu-id="63d61-144">[in] Le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="63d61-144">[in] The password.</span></span> <span data-ttu-id="63d61-145">Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="63d61-145">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

`strAuthority`\
<span data-ttu-id="63d61-146">[in] Le nom de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63d61-146">[in] The domain name of the user.</span></span> <span data-ttu-id="63d61-147">Consultez le [ConnectServerWmi](connectserverwmi.md) (fonction) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="63d61-147">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

## <a name="return-value"></a><span data-ttu-id="63d61-148">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="63d61-148">Return value</span></span>

<span data-ttu-id="63d61-149">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="63d61-149">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="63d61-150">Constante</span><span class="sxs-lookup"><span data-stu-id="63d61-150">Constant</span></span>  |<span data-ttu-id="63d61-151">Value</span><span class="sxs-lookup"><span data-stu-id="63d61-151">Value</span></span>  |<span data-ttu-id="63d61-152">Description</span><span class="sxs-lookup"><span data-stu-id="63d61-152">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_ACCESS_DENIED` | <span data-ttu-id="63d61-153">0x80041003</span><span class="sxs-lookup"><span data-stu-id="63d61-153">0x80041003</span></span> | <span data-ttu-id="63d61-154">L’utilisateur n’a pas l’autorisation d’afficher un ou plusieurs des classes qui la fonction peut retourner.</span><span class="sxs-lookup"><span data-stu-id="63d61-154">The user does not have permission to view one or more of the classes that the function can return.</span></span> |
| `WBEM_E_FAILED` | <span data-ttu-id="63d61-155">0x80041001</span><span class="sxs-lookup"><span data-stu-id="63d61-155">0x80041001</span></span> | <span data-ttu-id="63d61-156">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="63d61-156">An unspecified error has occurred.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="63d61-157">0x80041008</span><span class="sxs-lookup"><span data-stu-id="63d61-157">0x80041008</span></span> | <span data-ttu-id="63d61-158">Un paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="63d61-158">A parameter is not valid.</span></span> |
| `WBEM_E_INVALID_QUERY` | <span data-ttu-id="63d61-159">0x80041017</span><span class="sxs-lookup"><span data-stu-id="63d61-159">0x80041017</span></span> | <span data-ttu-id="63d61-160">La requête a dû à une erreur de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="63d61-160">The query had a syntax error.</span></span> |
| `WBEM_E_INVALID_QUERY_TYPE` | <span data-ttu-id="63d61-161">0x80041018</span><span class="sxs-lookup"><span data-stu-id="63d61-161">0x80041018</span></span> | <span data-ttu-id="63d61-162">Le langage de requête demandé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="63d61-162">The requested query language is not supported.</span></span> |
| `WBEM_E_QUOTA_VIOLATION` | <span data-ttu-id="63d61-163">0x8004106c</span><span class="sxs-lookup"><span data-stu-id="63d61-163">0x8004106c</span></span> | <span data-ttu-id="63d61-164">La requête est trop complexe.</span><span class="sxs-lookup"><span data-stu-id="63d61-164">The query is too complex.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="63d61-165">0x80041006</span><span class="sxs-lookup"><span data-stu-id="63d61-165">0x80041006</span></span> | <span data-ttu-id="63d61-166">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="63d61-166">Not enough memory is available to complete the operation.</span></span> |
| `WBEM_E_SHUTTING_DOWN` | <span data-ttu-id="63d61-167">0x80041033</span><span class="sxs-lookup"><span data-stu-id="63d61-167">0x80041033</span></span> | <span data-ttu-id="63d61-168">WMI s’est probablement arrêté et redémarrage.</span><span class="sxs-lookup"><span data-stu-id="63d61-168">WMI was probably stopped and restarting.</span></span> <span data-ttu-id="63d61-169">Appelez [ConnectServerWmi](connectserverwmi.md) à nouveau.</span><span class="sxs-lookup"><span data-stu-id="63d61-169">Call [ConnectServerWmi](connectserverwmi.md) again.</span></span> |
| `WBEM_E_TRANSPORT_FAILURE` | <span data-ttu-id="63d61-170">0x80041015</span><span class="sxs-lookup"><span data-stu-id="63d61-170">0x80041015</span></span> | <span data-ttu-id="63d61-171">Le lien remote procedure call (RPC) entre les processus en cours et WMI a échoué.</span><span class="sxs-lookup"><span data-stu-id="63d61-171">The remote procedure call (RPC) link between the current process and WMI has failed.</span></span> |
| `WBEM_E_NOT_FOUND` | <span data-ttu-id="63d61-172">0x80041002</span><span class="sxs-lookup"><span data-stu-id="63d61-172">0x80041002</span></span> | <span data-ttu-id="63d61-173">La requête spécifie une classe qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="63d61-173">The query specifies a class that does not exist.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="63d61-174">0</span><span class="sxs-lookup"><span data-stu-id="63d61-174">0</span></span> | <span data-ttu-id="63d61-175">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="63d61-175">The function call was successful.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="63d61-176">Notes</span><span class="sxs-lookup"><span data-stu-id="63d61-176">Remarks</span></span>

<span data-ttu-id="63d61-177">Cette fonction encapsule un appel à la [IWbemServices::ExecQuery](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery) (méthode).</span><span class="sxs-lookup"><span data-stu-id="63d61-177">This function wraps a call to the [IWbemServices::ExecQuery](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execquery) method.</span></span>

<span data-ttu-id="63d61-178">Cette fonction traite la requête spécifiée dans le `strQuery` paramètre et crée un énumérateur par le biais duquel l’appelant peut accéder les résultats de requête.</span><span class="sxs-lookup"><span data-stu-id="63d61-178">This function processes the query specified in the `strQuery` parameter and creates an enumerator through which the caller can access the query results.</span></span> <span data-ttu-id="63d61-179">L’énumérateur est un pointeur vers un [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject) interface ; la requête résultats sont des instances d’objets de classe accessibles via le [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) interface.</span><span class="sxs-lookup"><span data-stu-id="63d61-179">The enumerator is a pointer to an [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject) interface; the query results are instances of class objects made available through the [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) interface.</span></span>

<span data-ttu-id="63d61-180">Il existe des limites au nombre de `AND` et `OR` mots clés qui peuvent être utilisées dans les requêtes WQL.</span><span class="sxs-lookup"><span data-stu-id="63d61-180">There are limits to the number of `AND` and `OR` keywords that can be used in WQL queries.</span></span> <span data-ttu-id="63d61-181">Grand nombre de mots clés WQL utilisés dans une requête complexe peut provoquer de WMI retourner le `WBEM_E_QUOTA_VIOLATION` (ou 0x8004106c) code d’erreur comme un `HRESULT` valeur.</span><span class="sxs-lookup"><span data-stu-id="63d61-181">Large numbers of WQL keywords used in a complex query can cause WMI to return the `WBEM_E_QUOTA_VIOLATION` (or 0x8004106c) error code as an `HRESULT` value.</span></span> <span data-ttu-id="63d61-182">La limite des mots clés WQL dépend de la complexité de la requête est.</span><span class="sxs-lookup"><span data-stu-id="63d61-182">The limit of WQL keywords depends on how complex the query is.</span></span>

<span data-ttu-id="63d61-183">Si l’appel de fonction échoue, vous pouvez obtenir des informations d’erreur supplémentaires en appelant le [GetErrorInfo](geterrorinfo.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="63d61-183">If the function call fails, you can obtain additional error information by calling the [GetErrorInfo](geterrorinfo.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d61-184">Spécifications</span><span class="sxs-lookup"><span data-stu-id="63d61-184">Requirements</span></span>

<span data-ttu-id="63d61-185">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="63d61-185">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>

<span data-ttu-id="63d61-186">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="63d61-186">**Header:** WMINet_Utils.idl</span></span>

<span data-ttu-id="63d61-187">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="63d61-187">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="63d61-188">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63d61-188">See also</span></span>

- [<span data-ttu-id="63d61-189">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="63d61-189">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)