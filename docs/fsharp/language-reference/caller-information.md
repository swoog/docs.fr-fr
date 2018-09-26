---
title: 'Informations de l’appelant (F #)'
description: Décrit comment utiliser les attributs d’Argument appelant informations pour obtenir des informations de l’appelant à partir d’une méthode.
ms.date: 04/25/2017
ms.openlocfilehash: 0f2f4b16804d9156d234cc29d1f72ebe80a5b556
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47110012"
---
# <a name="caller-information"></a><span data-ttu-id="53766-103">Informations de l’appelant</span><span class="sxs-lookup"><span data-stu-id="53766-103">Caller information</span></span>

<span data-ttu-id="53766-104">À l'aide des attributs d'informations de l'appelant, vous pouvez obtenir des informations sur l'appelant d'une méthode.</span><span class="sxs-lookup"><span data-stu-id="53766-104">By using Caller Info attributes, you can obtain information about the caller to a method.</span></span> <span data-ttu-id="53766-105">Vous pouvez obtenir le chemin d'accès du fichier de code source, le numéro de ligne dans le code source, puis le nom du membre de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="53766-105">You can obtain file path of the source code, the line number in the source code, and the member name of the caller.</span></span> <span data-ttu-id="53766-106">Ces informations sont utiles pour suivre, déboguer, et créer des outils de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="53766-106">This information is helpful for tracing, debugging, and creating diagnostic tools.</span></span>

<span data-ttu-id="53766-107">Pour obtenir ces informations, vous utilisez les attributs qui sont appliqués aux paramètres facultatifs, qui a une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="53766-107">To obtain this information, you use attributes that are applied to optional parameters, each of which has a default value.</span></span> <span data-ttu-id="53766-108">Le tableau suivant répertorie les attributs d’informations de l’appelant qui sont définies dans le [System.Runtime.CompilerServices](/dotnet/api/system.runtime.compilerservices) espace de noms :</span><span class="sxs-lookup"><span data-stu-id="53766-108">The following table lists the Caller Info attributes that are defined in the [System.Runtime.CompilerServices](/dotnet/api/system.runtime.compilerservices) namespace:</span></span>

|<span data-ttu-id="53766-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="53766-109">Attribute</span></span>|<span data-ttu-id="53766-110">Description</span><span class="sxs-lookup"><span data-stu-id="53766-110">Description</span></span>|<span data-ttu-id="53766-111">Type</span><span class="sxs-lookup"><span data-stu-id="53766-111">Type</span></span>|
|---------|-----------|----|
|[<span data-ttu-id="53766-112">CallerFilePath</span><span class="sxs-lookup"><span data-stu-id="53766-112">CallerFilePath</span></span>](/dotnet/api/system.runtime.compilerservices.callerfilepathattribute)|<span data-ttu-id="53766-113">Chemin d’accès complet du fichier source qui contient l’appelant.</span><span class="sxs-lookup"><span data-stu-id="53766-113">Full path of the source file that contains the caller.</span></span> <span data-ttu-id="53766-114">C’est le chemin d’accès au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="53766-114">This is the file path at compile time.</span></span>|`String`
|[<span data-ttu-id="53766-115">CallerLineNumber</span><span class="sxs-lookup"><span data-stu-id="53766-115">CallerLineNumber</span></span>](/dotnet/api/system.runtime.compilerservices.callerlinenumberattribute)|<span data-ttu-id="53766-116">Numéro de ligne dans le fichier source dans lequel la méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="53766-116">Line number in the source file at which the method is called.</span></span>|`Integer`|
|[<span data-ttu-id="53766-117">CallerMemberName</span><span class="sxs-lookup"><span data-stu-id="53766-117">CallerMemberName</span></span>](/dotnet/api/system.runtime.compilerservices.callermembernameattribute)|<span data-ttu-id="53766-118">Méthode ou nom de la propriété de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="53766-118">Method or property name of the caller.</span></span> <span data-ttu-id="53766-119">Consultez la section des noms de membres plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="53766-119">See the Member Names section later in this topic.</span></span>|`String`|

## <a name="example"></a><span data-ttu-id="53766-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="53766-120">Example</span></span>

<span data-ttu-id="53766-121">L’exemple suivant montre comment vous pouvez utiliser ces attributs pour effectuer le suivi d’un appelant.</span><span class="sxs-lookup"><span data-stu-id="53766-121">The following example shows how you might use these attributes to trace a caller.</span></span>

```fsharp
open System.Diagnostics
open System.Runtime.CompilerServices

type Tracer() =
    member __.DoTrace(msg: string,
                      [<CallerMemberName>] ?memberName: string,
                      [<CallerFilePath>] ?path: string
                      [<CallerLineNumber>] ?line: int) =
        Trace.WriteLine(sprintf "Message: %s" message)
        match (memberName, path, line) with
        | Some m, Some p, Some l ->
            Trace.WriteLine(sprintf "Member name: %s" m)
            Trace.WriteLine(sprintf "Source file path: %s" p)
            Trace.WriteLine(sprintf "Source line number: %d" l)
        | _,_,_ -> ()
```

## <a name="remarks"></a><span data-ttu-id="53766-122">Notes</span><span class="sxs-lookup"><span data-stu-id="53766-122">Remarks</span></span>

<span data-ttu-id="53766-123">Attributs d’informations de l’appelant peuvent uniquement être appliqués aux paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="53766-123">Caller Info attributes can only be applied to optional parameters.</span></span> <span data-ttu-id="53766-124">Vous devez fournir une valeur explicite pour chaque paramètre facultatif.</span><span class="sxs-lookup"><span data-stu-id="53766-124">You must supply an explicit value for each optional parameter.</span></span> <span data-ttu-id="53766-125">Les attributs d’informations d’appelant contraindre le compilateur à écrire la valeur appropriée pour chaque paramètre facultatif décoré avec un attribut d’informations de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="53766-125">The Caller Info attributes cause the compiler to write the proper value for each optional parameter decorated with a Caller Info attribute.</span></span>

<span data-ttu-id="53766-126">Les valeurs d'informations de l'appelant sont émises en tant que littéraux en langage intermédiaire (IL) au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="53766-126">Caller Info values are emitted as literals into the Intermediate Language (IL) at compile time.</span></span> <span data-ttu-id="53766-127">Contrairement aux résultats de la [StackTrace](/dotnet/api/system.diagnostics.stacktrace) propriété pour les exceptions, les résultats ne sont pas affectés par l’obfuscation.</span><span class="sxs-lookup"><span data-stu-id="53766-127">Unlike the results of the [StackTrace](/dotnet/api/system.diagnostics.stacktrace) property for exceptions, the results aren't affected by obfuscation.</span></span>

<span data-ttu-id="53766-128">Vous pouvez fournir explicitement les arguments facultatifs pour contrôler ou masquer des informations de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="53766-128">You can explicitly supply the optional arguments to control the caller information or to hide caller information.</span></span>

## <a name="member-names"></a><span data-ttu-id="53766-129">Noms de membres</span><span class="sxs-lookup"><span data-stu-id="53766-129">Member names</span></span>

<span data-ttu-id="53766-130">Vous pouvez utiliser la [ `CallerMemberName` ](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribut pour éviter de spécifier le nom du membre en tant qu’un `String` argument à la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="53766-130">You can use the [`CallerMemberName`](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribute to avoid specifying the member name as a `String` argument to the called method.</span></span> <span data-ttu-id="53766-131">À l’aide de cette technique, vous évitez le problème qui ne change pas la refactorisation renommer le `String` valeurs.</span><span class="sxs-lookup"><span data-stu-id="53766-131">By using this technique, you avoid the problem that Rename Refactoring doesn't change the `String` values.</span></span> <span data-ttu-id="53766-132">Cet avantage est particulièrement utile pour les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="53766-132">This benefit is especially useful for the following tasks:</span></span>

* <span data-ttu-id="53766-133">Utilisation du traçage et des programmes de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="53766-133">Using tracing and diagnostic routines.</span></span>
* <span data-ttu-id="53766-134">Implémentation de la [INotifyPropertyChanged](/dotnet/api/system.componentmodel.inotifypropertychanged) interface lors de la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="53766-134">Implementing the [INotifyPropertyChanged](/dotnet/api/system.componentmodel.inotifypropertychanged) interface when binding data.</span></span> <span data-ttu-id="53766-135">Cette interface permet à la propriété d'un objet de signaler à un contrôle dépendant que la propriété a été modifiée, afin que ce contrôle puisse afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="53766-135">This interface allows the property of an object to notify a bound control that the property has changed, so that the control can display the updated information.</span></span> <span data-ttu-id="53766-136">Sans le [ `CallerMemberName` ](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribut, vous devez spécifier le nom de propriété comme un littéral.</span><span class="sxs-lookup"><span data-stu-id="53766-136">Without the [`CallerMemberName`](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribute, you must specify the property name as a literal.</span></span>

<span data-ttu-id="53766-137">Le graphique suivant montre le membre de noms qui sont retournés lorsque vous utilisez l’attribut CallerMemberName.</span><span class="sxs-lookup"><span data-stu-id="53766-137">The following chart shows the member names that are returned when you use the CallerMemberName attribute.</span></span>

|<span data-ttu-id="53766-138">Les appels se produisent à l'intérieur</span><span class="sxs-lookup"><span data-stu-id="53766-138">Calls occurs within</span></span>|<span data-ttu-id="53766-139">Résultat de nom de membre</span><span class="sxs-lookup"><span data-stu-id="53766-139">Member name result</span></span>|
|-------------------|------------------|
|<span data-ttu-id="53766-140">Méthode, propriété ou événement</span><span class="sxs-lookup"><span data-stu-id="53766-140">Method, property, or event</span></span>|<span data-ttu-id="53766-141">Le nom de la méthode, la propriété ou l'événement dont l'appel est originaire.</span><span class="sxs-lookup"><span data-stu-id="53766-141">The name of the method, property, or event from which the call originated.</span></span>|
|<span data-ttu-id="53766-142">Constructeur</span><span class="sxs-lookup"><span data-stu-id="53766-142">Constructor</span></span>|<span data-ttu-id="53766-143">La chaîne « .ctor »</span><span class="sxs-lookup"><span data-stu-id="53766-143">The string ".ctor"</span></span>|
|<span data-ttu-id="53766-144">Constructeur statique</span><span class="sxs-lookup"><span data-stu-id="53766-144">Static constructor</span></span>|<span data-ttu-id="53766-145">La chaîne « .cctor »</span><span class="sxs-lookup"><span data-stu-id="53766-145">The string ".cctor"</span></span>|
|<span data-ttu-id="53766-146">Destructeur</span><span class="sxs-lookup"><span data-stu-id="53766-146">Destructor</span></span>|<span data-ttu-id="53766-147">La chaîne « finalize »</span><span class="sxs-lookup"><span data-stu-id="53766-147">The string "Finalize"</span></span>|
|<span data-ttu-id="53766-148">Opérateurs définis par l'utilisateur ou conversions</span><span class="sxs-lookup"><span data-stu-id="53766-148">User-defined operators or conversions</span></span>|<span data-ttu-id="53766-149">Le nom généré pour le membre, par exemple, « op_Addition ».</span><span class="sxs-lookup"><span data-stu-id="53766-149">The generated name for the member, for example, "op_Addition".</span></span>|
|<span data-ttu-id="53766-150">Constructeur d'attribut</span><span class="sxs-lookup"><span data-stu-id="53766-150">Attribute constructor</span></span>|<span data-ttu-id="53766-151">Le nom du membre auquel l'attribut est appliqué.</span><span class="sxs-lookup"><span data-stu-id="53766-151">The name of the member to which the attribute is applied.</span></span> <span data-ttu-id="53766-152">Si l'attribut est un élément dans un membre (tel qu'un paramètre, une valeur de retour, ou un paramètre de type générique), le résultat est le nom du membre qui est associé à cet élément.</span><span class="sxs-lookup"><span data-stu-id="53766-152">If the attribute is any element within a member (such as a parameter, a return value, or a generic type parameter), this result is the name of the member that's associated with that element.</span></span>|
|<span data-ttu-id="53766-153">Aucun membre contenant (par exemple, niveau assembly ou attributs qui sont appliqués aux types)</span><span class="sxs-lookup"><span data-stu-id="53766-153">No containing member (for example, assembly-level or attributes that are applied to types)</span></span>|<span data-ttu-id="53766-154">Valeur par défaut du paramètre optionnel.</span><span class="sxs-lookup"><span data-stu-id="53766-154">The default value of the optional parameter.</span></span>|

## <a name="see-also"></a><span data-ttu-id="53766-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53766-155">See also</span></span>

- [<span data-ttu-id="53766-156">Attributs</span><span class="sxs-lookup"><span data-stu-id="53766-156">Attributes</span></span>](attributes.md)  
- [<span data-ttu-id="53766-157">Arguments nommés</span><span class="sxs-lookup"><span data-stu-id="53766-157">Named arguments</span></span>](parameters-and-arguments.md#named-arguments)  
- [<span data-ttu-id="53766-158">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="53766-158">Optional parameters</span></span>](parameters-and-arguments.md#optional-parameters)  
