---
title: PutClassWmi (fonction) (référence des API non managées)
description: La fonction PutClassWmi crée une nouvelle classe ou mettre à jour.
ms.date: 11/06/2017
api_name:
- PutClassWmi
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- PutClassWmi
helpviewer_keywords:
- PutClassWmi function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: de08662a825a84f19a40863cf73481d89364ebd0
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47090199"
---
# <a name="putclasswmi-function"></a><span data-ttu-id="e5d79-103">PutClassWmi (fonction)</span><span class="sxs-lookup"><span data-stu-id="e5d79-103">PutClassWmi function</span></span>
<span data-ttu-id="e5d79-104">Crée une classe ou met à jour une classe existante.</span><span class="sxs-lookup"><span data-stu-id="e5d79-104">Creates a new class or updates an existing one.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="e5d79-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5d79-105">Syntax</span></span>  
  
```  
HRESULT PutClassWmi (
   [in] IWbemClassObject*    pObject,
   [in] long                 lFlags,
   [in] IWbemContext*        pCtx,
   [out] IWbemCallResult**   ppCallResult
); 
```  

## <a name="parameters"></a><span data-ttu-id="e5d79-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5d79-106">Parameters</span></span>

`pObject`    
<span data-ttu-id="e5d79-107">[in] Pointeur vers une définition de classe valide.</span><span class="sxs-lookup"><span data-stu-id="e5d79-107">[in] A pointer to a valid class definition.</span></span> <span data-ttu-id="e5d79-108">Il doit être initialisé correctement avec toutes les valeurs de propriété requise.</span><span class="sxs-lookup"><span data-stu-id="e5d79-108">It must be correctly initialized with all the required property values.</span></span>

`lFlags`   
<span data-ttu-id="e5d79-109">[in] Combinaison d’indicateurs qui affectent le comportement de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="e5d79-109">[in] A combination of flags that affect the behavior of this function.</span></span> <span data-ttu-id="e5d79-110">Les valeurs suivantes sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="e5d79-110">The following values are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span> 

|<span data-ttu-id="e5d79-111">Constante</span><span class="sxs-lookup"><span data-stu-id="e5d79-111">Constant</span></span>  |<span data-ttu-id="e5d79-112">Value</span><span class="sxs-lookup"><span data-stu-id="e5d79-112">Value</span></span>  |<span data-ttu-id="e5d79-113">Description</span><span class="sxs-lookup"><span data-stu-id="e5d79-113">Description</span></span>  |
|---------|---------|---------|
| `WBEM_FLAG_USE_AMENDED_QUALIFIERS` | <span data-ttu-id="e5d79-114">0 x 20000</span><span class="sxs-lookup"><span data-stu-id="e5d79-114">0x20000</span></span> | <span data-ttu-id="e5d79-115">Si le jeu, WMI ne stocke pas les qualificateurs avec la version modifiée.</span><span class="sxs-lookup"><span data-stu-id="e5d79-115">If set, WMI does not store any qualifiers with the amended flavor.</span></span> </br> <span data-ttu-id="e5d79-116">Si ce n’est pas ensemble, il est supposé que cet objet n’est pas localisé, et tous les qualificateurs sont storedwith cette instance.</span><span class="sxs-lookup"><span data-stu-id="e5d79-116">If not set, it is assumed that this object is not localized, and all qualifiers are storedwith this instance.</span></span> |
| `WBEM_FLAG_CREATE_OR_UPDATE` | <span data-ttu-id="e5d79-117">0</span><span class="sxs-lookup"><span data-stu-id="e5d79-117">0</span></span> | <span data-ttu-id="e5d79-118">Créer la classe si elle n’existe pas, ou remplacer si elle existe déjà.</span><span class="sxs-lookup"><span data-stu-id="e5d79-118">Create the class if it does not exist, or overwrite it if it exists already.</span></span> |
| `WBEM_FLAG_UPDATE_ONLY` | <span data-ttu-id="e5d79-119">1</span><span class="sxs-lookup"><span data-stu-id="e5d79-119">1</span></span> | <span data-ttu-id="e5d79-120">Mettre à jour de la classe.</span><span class="sxs-lookup"><span data-stu-id="e5d79-120">Update the class.</span></span> <span data-ttu-id="e5d79-121">La classe doit exister pour l’appel réussisse.</span><span class="sxs-lookup"><span data-stu-id="e5d79-121">The class must exist for the call to be successful.</span></span> |
| `WBEM_FLAG_CREATE_ONLY` | <span data-ttu-id="e5d79-122">2</span><span class="sxs-lookup"><span data-stu-id="e5d79-122">2</span></span> | <span data-ttu-id="e5d79-123">Créer la classe.</span><span class="sxs-lookup"><span data-stu-id="e5d79-123">Create the class.</span></span> <span data-ttu-id="e5d79-124">L’appel échoue si la classe existe déjà.</span><span class="sxs-lookup"><span data-stu-id="e5d79-124">The call fails if the class already exists.</span></span> |
| `WBEM_FLAG_RETURN_IMMEDIATELY` | <span data-ttu-id="e5d79-125">0x10</span><span class="sxs-lookup"><span data-stu-id="e5d79-125">0x10</span></span> | <span data-ttu-id="e5d79-126">L’indicateur provoque un appel semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="e5d79-126">The flag causes a semisynchronous call.</span></span> |
| `WBEM_FLAG_OWNER_UPDATE` | <span data-ttu-id="e5d79-127">0 x 10000</span><span class="sxs-lookup"><span data-stu-id="e5d79-127">0x10000</span></span> | <span data-ttu-id="e5d79-128">Fournisseurs de push doivent spécifier cet indicateur lors de l’appel `PutClassWmi` pour indiquer que cette classe a changé.</span><span class="sxs-lookup"><span data-stu-id="e5d79-128">Push providers must specify this flag when calling `PutClassWmi` to indicate that this class has changed.</span></span> |
| `WBEM_FLAG_UPDATE_COMPATIBLE` | <span data-ttu-id="e5d79-129">0</span><span class="sxs-lookup"><span data-stu-id="e5d79-129">0</span></span> | <span data-ttu-id="e5d79-130">Permet à une classe à mettre à jour s’il existe aucune classe dérivée et aucune instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e5d79-130">Allows a class to be updated if there are no derived classes and no instances of that class.</span></span> <span data-ttu-id="e5d79-131">Autorise également les mises à jour dans tous les cas si la modification consiste simplement à des qualificateurs sans importance, telles que le qualificateur de Description.</span><span class="sxs-lookup"><span data-stu-id="e5d79-131">It also allows updates in all cases if the change is just to unimportant qualifiers, such as the Description qualifier.</span></span> <span data-ttu-id="e5d79-132">Si la classe a des instances ou les modifications doivent qualificateurs importants, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="e5d79-132">If the class has instances or changes are to important qualifiers, the update fails.</span></span> |
| `WBEM_FLAG_UPDATE_SAFE_MODE` | <span data-ttu-id="e5d79-133">0 x 20</span><span class="sxs-lookup"><span data-stu-id="e5d79-133">0x20</span></span> | <span data-ttu-id="e5d79-134">Permet des mises à jour des classes même s’il existe des classes enfants tant que la modification n’entraîne pas de tous les conflits avec les classes enfants.</span><span class="sxs-lookup"><span data-stu-id="e5d79-134">Allows updates of classes even if there are child classes as long as the change does not cause any conflicts with child classes.</span></span> <span data-ttu-id="e5d79-135">Par exemple, cet indicateur permet une nouvelle propriété à ajouter à la classe de base qui n’a pas été précédemment mentionnée dans les classes enfants.</span><span class="sxs-lookup"><span data-stu-id="e5d79-135">For example, this flag allows a new property to be added to the base class that was not previously mentioned in any of the child classes.</span></span> <span data-ttu-id="e5d79-136">Si la classe a des instances, la mise à jour échoue.</span><span class="sxs-lookup"><span data-stu-id="e5d79-136">If the class has instances, the update fails.</span></span> |
| `WBEM_FLAG_UPDATE_FORCE_MODE` | <span data-ttu-id="e5d79-137">0 x 40</span><span class="sxs-lookup"><span data-stu-id="e5d79-137">0x40</span></span> | <span data-ttu-id="e5d79-138">force les mises à jour des classes lorsque les classes enfants en conflit existent.</span><span class="sxs-lookup"><span data-stu-id="e5d79-138">forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="e5d79-139">Par exemple, cet indicateur de force une mise à jour si un qualificateur de classe est défini dans une classe enfant et la classe de base essaie d’ajouter le même qualificateur qui est en conflit avec thte un existant.</span><span class="sxs-lookup"><span data-stu-id="e5d79-139">For example, this flag forces an update if a class qualifier is defined in a child class, and the base class tries to add the same qualifier which conflicts with thte existing one.</span></span> <span data-ttu-id="e5d79-140">En mode de force, conflit de tis est résolu par la suppression du qualificateur dans la classe enfant.</span><span class="sxs-lookup"><span data-stu-id="e5d79-140">In force mode, tis conflict is resolved by deleting the conflicting qualifier in the child class.</span></span> |

`pCtx`  
<span data-ttu-id="e5d79-141">[in] En règle générale, cette valeur est `null`.</span><span class="sxs-lookup"><span data-stu-id="e5d79-141">[in] Typically, this value is `null`.</span></span> <span data-ttu-id="e5d79-142">Sinon, il est un pointeur vers un [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) instance qui peut être utilisé par le fournisseur qui fournit les classes demandées.</span><span class="sxs-lookup"><span data-stu-id="e5d79-142">Otherwise, it is a pointer to an [IWbemContext](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) instance that can be used by the provider that is providing the requested classes.</span></span> 

`ppCallResult`  
<span data-ttu-id="e5d79-143">[out] Si `null`, ce paramètre n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="e5d79-143">[out] If `null`, this parameter is unused.</span></span> <span data-ttu-id="e5d79-144">Si `lFlags` contient `WBEM_FLAG_RETURN_IMMEDIATELY`, la fonction retourne immédiatement avec `WBEM_S_NO_ERROR`.</span><span class="sxs-lookup"><span data-stu-id="e5d79-144">If `lFlags` contains `WBEM_FLAG_RETURN_IMMEDIATELY`, the function returns immediately with `WBEM_S_NO_ERROR`.</span></span> <span data-ttu-id="e5d79-145">Le `ppCallResult` paramètre reçoit un pointeur vers un nouveau [IWbemCallResult](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult) objet.</span><span class="sxs-lookup"><span data-stu-id="e5d79-145">The `ppCallResult` parameter receives a pointer to a new [IWbemCallResult](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcallresult) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5d79-146">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e5d79-146">Return value</span></span>

<span data-ttu-id="e5d79-147">Les valeurs suivantes est retournées par cette fonction sont définies dans le *WbemCli.h* fichier d’en-tête, ou vous pouvez les définir en tant que constantes dans votre code :</span><span class="sxs-lookup"><span data-stu-id="e5d79-147">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="e5d79-148">Constante</span><span class="sxs-lookup"><span data-stu-id="e5d79-148">Constant</span></span>  |<span data-ttu-id="e5d79-149">Value</span><span class="sxs-lookup"><span data-stu-id="e5d79-149">Value</span></span>  |<span data-ttu-id="e5d79-150">Description</span><span class="sxs-lookup"><span data-stu-id="e5d79-150">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_ACCESS_DENIED` | <span data-ttu-id="e5d79-151">0 x 80041003</span><span class="sxs-lookup"><span data-stu-id="e5d79-151">0x80041003</span></span> | <span data-ttu-id="e5d79-152">L’utilisateur n’a pas d’autorisation pour créer ou modifier des classes.</span><span class="sxs-lookup"><span data-stu-id="e5d79-152">The user does not have permission to create or modify classes.</span></span> |
| `WBEM_E_FAILED` | <span data-ttu-id="e5d79-153">0 x 80041001</span><span class="sxs-lookup"><span data-stu-id="e5d79-153">0x80041001</span></span> | <span data-ttu-id="e5d79-154">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e5d79-154">An unspecified error has occurred.</span></span> |
| `WBEM_E_INVALID_CLASS` | <span data-ttu-id="e5d79-155">0 x 80041010</span><span class="sxs-lookup"><span data-stu-id="e5d79-155">0x80041010</span></span> | <span data-ttu-id="e5d79-156">La classe spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e5d79-156">The specified class is not valid.</span></span> <span data-ttu-id="e5d79-157">En règle générale, cela indique que `pObject` spécifie un objet d’instance.</span><span class="sxs-lookup"><span data-stu-id="e5d79-157">Typically, this indicates that `pObject` specifies an instance object.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="e5d79-158">0 x 80041008</span><span class="sxs-lookup"><span data-stu-id="e5d79-158">0x80041008</span></span> | <span data-ttu-id="e5d79-159">Un paramètre n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e5d79-159">A parameter is not valid.</span></span> |
| `WBEM_E_INVALID OPERATION` | <span data-ttu-id="e5d79-160">0x80041016</span><span class="sxs-lookup"><span data-stu-id="e5d79-160">0x80041016</span></span> | <span data-ttu-id="e5d79-161">Le nom de la classe spécifiée n’est pas valid.</span><span class="sxs-lookup"><span data-stu-id="e5d79-161">The specified class name is not valid.</span></span> |
| `WBEM_E_CLASS_HAS_CHILDREN` | <span data-ttu-id="e5d79-162">0x80041025</span><span class="sxs-lookup"><span data-stu-id="e5d79-162">0x80041025</span></span> | <span data-ttu-id="e5d79-163">Une tentative a été effectuée pour apporter une modification qui invaliderait une sous-classe.</span><span class="sxs-lookup"><span data-stu-id="e5d79-163">An attempt was made to make a change that would invalidate a subclass.</span></span> |
| `WBEM_E_ALREADY_EXISTS` | <span data-ttu-id="e5d79-164">0x80041019</span><span class="sxs-lookup"><span data-stu-id="e5d79-164">0x80041019</span></span> | <span data-ttu-id="e5d79-165">Le `WBEM_FLAG_CREATE_ONLY` indicateur a été spécifié, mais la classe existe déjà.</span><span class="sxs-lookup"><span data-stu-id="e5d79-165">The `WBEM_FLAG_CREATE_ONLY` flag was specified, but the class already exists.</span></span> |
| `WBEM_E_NOT_FOUND` | <span data-ttu-id="e5d79-166">0x80041002</span><span class="sxs-lookup"><span data-stu-id="e5d79-166">0x80041002</span></span> | <span data-ttu-id="e5d79-167">`WBEM_FLAG_UPDATE_ONLY` a été spécifié dans `lFlags`, et la classe est introuvable.</span><span class="sxs-lookup"><span data-stu-id="e5d79-167">`WBEM_FLAG_UPDATE_ONLY` was specified in `lFlags`, and the class was not found.</span></span> |
| `WBEM_E_INCOMPLETE_CLASS` | <span data-ttu-id="e5d79-168">0x80041020</span><span class="sxs-lookup"><span data-stu-id="e5d79-168">0x80041020</span></span> | <span data-ttu-id="e5d79-169">Les propriétés requises pour les classes ont pas toutes été définies.</span><span class="sxs-lookup"><span data-stu-id="e5d79-169">The required properties for classes have not all been set.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="e5d79-170">0x80041006</span><span class="sxs-lookup"><span data-stu-id="e5d79-170">0x80041006</span></span> | <span data-ttu-id="e5d79-171">Mémoire est insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e5d79-171">Not enough memory is available to complete the operation.</span></span> |
| `WBEM_E_SHUTTING_DOWN` | <span data-ttu-id="e5d79-172">0x80041033</span><span class="sxs-lookup"><span data-stu-id="e5d79-172">0x80041033</span></span> | <span data-ttu-id="e5d79-173">WMI s’est probablement arrêté et redémarrage.</span><span class="sxs-lookup"><span data-stu-id="e5d79-173">WMI was probably stopped and restarting.</span></span> <span data-ttu-id="e5d79-174">Appelez [ConnectServerWmi](connectserverwmi.md) à nouveau.</span><span class="sxs-lookup"><span data-stu-id="e5d79-174">Call [ConnectServerWmi](connectserverwmi.md) again.</span></span> |
| `WBEM_E_TRANSPORT_FAILURE` | <span data-ttu-id="e5d79-175">0x80041015</span><span class="sxs-lookup"><span data-stu-id="e5d79-175">0x80041015</span></span> | <span data-ttu-id="e5d79-176">Le lien remote procedure call (RPC) entre les processus en cours et WMI a échoué.</span><span class="sxs-lookup"><span data-stu-id="e5d79-176">The remote procedure call (RPC) link between the current process and WMI has failed.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="e5d79-177">0</span><span class="sxs-lookup"><span data-stu-id="e5d79-177">0</span></span> | <span data-ttu-id="e5d79-178">L’appel de fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="e5d79-178">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="e5d79-179">Notes</span><span class="sxs-lookup"><span data-stu-id="e5d79-179">Remarks</span></span>

<span data-ttu-id="e5d79-180">Cette fonction encapsule un appel à la [IWbemServices::PutClass](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass) (méthode).</span><span class="sxs-lookup"><span data-stu-id="e5d79-180">This function wraps a call to the [IWbemServices::PutClass](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass) method.</span></span>

<span data-ttu-id="e5d79-181">L’utilisateur ne peut pas créer les classes dont les noms commencent ou finir par un trait de soulignement chacater</span><span class="sxs-lookup"><span data-stu-id="e5d79-181">The user may not create classes with names that begin or end with an underscore chacater</span></span>

<span data-ttu-id="e5d79-182">Si l’appel de fonction échoue, vous pouvez obtenir des informations d’erreur supplémentaires en appelant le [GetErrorInfo](geterrorinfo.md) (fonction).</span><span class="sxs-lookup"><span data-stu-id="e5d79-182">If the function call fails, you can obtain additional error information by calling the [GetErrorInfo](geterrorinfo.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d79-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5d79-183">Requirements</span></span>  
 <span data-ttu-id="e5d79-184">**Plateformes :** Consultez [Configuration requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e5d79-184">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e5d79-185">**En-tête :** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="e5d79-185">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="e5d79-186">**Versions du .NET Framework :** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="e5d79-186">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5d79-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5d79-187">See also</span></span>  
[<span data-ttu-id="e5d79-188">WMI et compteurs de performances (référence des API non managées)</span><span class="sxs-lookup"><span data-stu-id="e5d79-188">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
