---
title: Informations de l’appelant
description: Décrit comment utiliser les attributs d’Argument appelant informations pour obtenir des informations de l’appelant à partir d’une méthode.
ms.date: 04/25/2017
ms.openlocfilehash: 13092df453b684d3ed4a93c842ea49c066157cb6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59316152"
---
# <a name="caller-information"></a><span data-ttu-id="5fe28-103">Informations de l’appelant</span><span class="sxs-lookup"><span data-stu-id="5fe28-103">Caller information</span></span>

<span data-ttu-id="5fe28-104">À l'aide des attributs d'informations de l'appelant, vous pouvez obtenir des informations sur l'appelant d'une méthode.</span><span class="sxs-lookup"><span data-stu-id="5fe28-104">By using Caller Info attributes, you can obtain information about the caller to a method.</span></span> <span data-ttu-id="5fe28-105">Vous pouvez obtenir le chemin d'accès du fichier de code source, le numéro de ligne dans le code source, puis le nom du membre de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="5fe28-105">You can obtain file path of the source code, the line number in the source code, and the member name of the caller.</span></span> <span data-ttu-id="5fe28-106">Ces informations sont utiles pour suivre, déboguer, et créer des outils de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="5fe28-106">This information is helpful for tracing, debugging, and creating diagnostic tools.</span></span>

<span data-ttu-id="5fe28-107">Pour obtenir ces informations, vous utilisez les attributs qui sont appliqués aux paramètres facultatifs, qui a une valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5fe28-107">To obtain this information, you use attributes that are applied to optional parameters, each of which has a default value.</span></span> <span data-ttu-id="5fe28-108">Le tableau suivant répertorie les attributs d’informations de l’appelant qui sont définies dans le [System.Runtime.CompilerServices](/dotnet/api/system.runtime.compilerservices) espace de noms :</span><span class="sxs-lookup"><span data-stu-id="5fe28-108">The following table lists the Caller Info attributes that are defined in the [System.Runtime.CompilerServices](/dotnet/api/system.runtime.compilerservices) namespace:</span></span>

|<span data-ttu-id="5fe28-109">Attribut</span><span class="sxs-lookup"><span data-stu-id="5fe28-109">Attribute</span></span>|<span data-ttu-id="5fe28-110">Description</span><span class="sxs-lookup"><span data-stu-id="5fe28-110">Description</span></span>|<span data-ttu-id="5fe28-111">Type</span><span class="sxs-lookup"><span data-stu-id="5fe28-111">Type</span></span>|
|---------|-----------|----|
|[<span data-ttu-id="5fe28-112">CallerFilePath</span><span class="sxs-lookup"><span data-stu-id="5fe28-112">CallerFilePath</span></span>](/dotnet/api/system.runtime.compilerservices.callerfilepathattribute)|<span data-ttu-id="5fe28-113">Chemin d’accès complet du fichier source qui contient l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5fe28-113">Full path of the source file that contains the caller.</span></span> <span data-ttu-id="5fe28-114">C’est le chemin d’accès au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="5fe28-114">This is the file path at compile time.</span></span>|`String`
|[<span data-ttu-id="5fe28-115">CallerLineNumber</span><span class="sxs-lookup"><span data-stu-id="5fe28-115">CallerLineNumber</span></span>](/dotnet/api/system.runtime.compilerservices.callerlinenumberattribute)|<span data-ttu-id="5fe28-116">Numéro de ligne dans le fichier source dans lequel la méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="5fe28-116">Line number in the source file at which the method is called.</span></span>|`Integer`|
|[<span data-ttu-id="5fe28-117">CallerMemberName</span><span class="sxs-lookup"><span data-stu-id="5fe28-117">CallerMemberName</span></span>](/dotnet/api/system.runtime.compilerservices.callermembernameattribute)|<span data-ttu-id="5fe28-118">Méthode ou nom de la propriété de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="5fe28-118">Method or property name of the caller.</span></span> <span data-ttu-id="5fe28-119">Consultez la section des noms de membres plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5fe28-119">See the Member Names section later in this topic.</span></span>|`String`|

## <a name="example"></a><span data-ttu-id="5fe28-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="5fe28-120">Example</span></span>

<span data-ttu-id="5fe28-121">L’exemple suivant montre comment vous pouvez utiliser ces attributs pour effectuer le suivi d’un appelant.</span><span class="sxs-lookup"><span data-stu-id="5fe28-121">The following example shows how you might use these attributes to trace a caller.</span></span>

```fsharp
open System.Diagnostics
open System.Runtime.CompilerServices
open System.Runtime.InteropServices

type Tracer() =
    member __.DoTrace(message: string,
                      [<CallerMemberName; Optional; DefaultParameterValue("")>] memberName: string,
                      [<CallerFilePath; Optional; DefaultParameterValue("")>] path: string,
                      [<CallerLineNumber; Optional; DefaultParameterValue(0)>] line: int) =
        Trace.WriteLine(sprintf "Message: %s" message)
        Trace.WriteLine(sprintf "Member name: %s" memberName)
        Trace.WriteLine(sprintf "Source file path: %s" path)
        Trace.WriteLine(sprintf "Source line number: %d" line)
```

## <a name="remarks"></a><span data-ttu-id="5fe28-122">Notes</span><span class="sxs-lookup"><span data-stu-id="5fe28-122">Remarks</span></span>

<span data-ttu-id="5fe28-123">Attributs d’informations de l’appelant peuvent uniquement être appliqués aux paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="5fe28-123">Caller Info attributes can only be applied to optional parameters.</span></span> <span data-ttu-id="5fe28-124">Les attributs d’informations d’appelant contraindre le compilateur à écrire la valeur appropriée pour chaque paramètre facultatif décoré avec un attribut d’informations de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5fe28-124">The Caller Info attributes cause the compiler to write the proper value for each optional parameter decorated with a Caller Info attribute.</span></span>

<span data-ttu-id="5fe28-125">Les valeurs d'informations de l'appelant sont émises en tant que littéraux en langage intermédiaire (IL) au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="5fe28-125">Caller Info values are emitted as literals into the Intermediate Language (IL) at compile time.</span></span> <span data-ttu-id="5fe28-126">Contrairement aux résultats de la [StackTrace](/dotnet/api/system.diagnostics.stacktrace) propriété pour les exceptions, les résultats ne sont pas affectés par l’obfuscation.</span><span class="sxs-lookup"><span data-stu-id="5fe28-126">Unlike the results of the [StackTrace](/dotnet/api/system.diagnostics.stacktrace) property for exceptions, the results aren't affected by obfuscation.</span></span>

<span data-ttu-id="5fe28-127">Vous pouvez fournir explicitement les arguments facultatifs pour contrôler ou masquer des informations de l'appelant.</span><span class="sxs-lookup"><span data-stu-id="5fe28-127">You can explicitly supply the optional arguments to control the caller information or to hide caller information.</span></span>

## <a name="member-names"></a><span data-ttu-id="5fe28-128">Noms de membres</span><span class="sxs-lookup"><span data-stu-id="5fe28-128">Member names</span></span>

<span data-ttu-id="5fe28-129">Vous pouvez utiliser la [ `CallerMemberName` ](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribut pour éviter de spécifier le nom du membre en tant qu’un `String` argument à la méthode appelée.</span><span class="sxs-lookup"><span data-stu-id="5fe28-129">You can use the [`CallerMemberName`](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribute to avoid specifying the member name as a `String` argument to the called method.</span></span> <span data-ttu-id="5fe28-130">À l’aide de cette technique, vous évitez le problème qui ne change pas la refactorisation renommer le `String` valeurs.</span><span class="sxs-lookup"><span data-stu-id="5fe28-130">By using this technique, you avoid the problem that Rename Refactoring doesn't change the `String` values.</span></span> <span data-ttu-id="5fe28-131">Cet avantage est particulièrement utile pour les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="5fe28-131">This benefit is especially useful for the following tasks:</span></span>

* <span data-ttu-id="5fe28-132">Utilisation du traçage et des programmes de diagnostic.</span><span class="sxs-lookup"><span data-stu-id="5fe28-132">Using tracing and diagnostic routines.</span></span>
* <span data-ttu-id="5fe28-133">Implémentation de la [INotifyPropertyChanged](/dotnet/api/system.componentmodel.inotifypropertychanged) interface lors de la liaison de données.</span><span class="sxs-lookup"><span data-stu-id="5fe28-133">Implementing the [INotifyPropertyChanged](/dotnet/api/system.componentmodel.inotifypropertychanged) interface when binding data.</span></span> <span data-ttu-id="5fe28-134">Cette interface permet à la propriété d'un objet de signaler à un contrôle dépendant que la propriété a été modifiée, afin que ce contrôle puisse afficher les informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="5fe28-134">This interface allows the property of an object to notify a bound control that the property has changed, so that the control can display the updated information.</span></span> <span data-ttu-id="5fe28-135">Sans le [ `CallerMemberName` ](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribut, vous devez spécifier le nom de propriété comme un littéral.</span><span class="sxs-lookup"><span data-stu-id="5fe28-135">Without the [`CallerMemberName`](/dotnet/api/system.runtime.compilerservices.callermembernameattribute) attribute, you must specify the property name as a literal.</span></span>

<span data-ttu-id="5fe28-136">Le graphique suivant montre le membre de noms qui sont retournés lorsque vous utilisez l’attribut CallerMemberName.</span><span class="sxs-lookup"><span data-stu-id="5fe28-136">The following chart shows the member names that are returned when you use the CallerMemberName attribute.</span></span>

|<span data-ttu-id="5fe28-137">Les appels se produisent à l'intérieur</span><span class="sxs-lookup"><span data-stu-id="5fe28-137">Calls occurs within</span></span>|<span data-ttu-id="5fe28-138">Résultat de nom de membre</span><span class="sxs-lookup"><span data-stu-id="5fe28-138">Member name result</span></span>|
|-------------------|------------------|
|<span data-ttu-id="5fe28-139">Méthode, propriété ou événement</span><span class="sxs-lookup"><span data-stu-id="5fe28-139">Method, property, or event</span></span>|<span data-ttu-id="5fe28-140">Le nom de la méthode, la propriété ou l'événement dont l'appel est originaire.</span><span class="sxs-lookup"><span data-stu-id="5fe28-140">The name of the method, property, or event from which the call originated.</span></span>|
|<span data-ttu-id="5fe28-141">Constructeur</span><span class="sxs-lookup"><span data-stu-id="5fe28-141">Constructor</span></span>|<span data-ttu-id="5fe28-142">La chaîne « .ctor »</span><span class="sxs-lookup"><span data-stu-id="5fe28-142">The string ".ctor"</span></span>|
|<span data-ttu-id="5fe28-143">Constructeur statique</span><span class="sxs-lookup"><span data-stu-id="5fe28-143">Static constructor</span></span>|<span data-ttu-id="5fe28-144">La chaîne « .cctor »</span><span class="sxs-lookup"><span data-stu-id="5fe28-144">The string ".cctor"</span></span>|
|<span data-ttu-id="5fe28-145">Destructeur</span><span class="sxs-lookup"><span data-stu-id="5fe28-145">Destructor</span></span>|<span data-ttu-id="5fe28-146">La chaîne « finalize »</span><span class="sxs-lookup"><span data-stu-id="5fe28-146">The string "Finalize"</span></span>|
|<span data-ttu-id="5fe28-147">Opérateurs définis par l'utilisateur ou conversions</span><span class="sxs-lookup"><span data-stu-id="5fe28-147">User-defined operators or conversions</span></span>|<span data-ttu-id="5fe28-148">Le nom généré pour le membre, par exemple, « op_Addition ».</span><span class="sxs-lookup"><span data-stu-id="5fe28-148">The generated name for the member, for example, "op_Addition".</span></span>|
|<span data-ttu-id="5fe28-149">Constructeur d'attribut</span><span class="sxs-lookup"><span data-stu-id="5fe28-149">Attribute constructor</span></span>|<span data-ttu-id="5fe28-150">Le nom du membre auquel l'attribut est appliqué.</span><span class="sxs-lookup"><span data-stu-id="5fe28-150">The name of the member to which the attribute is applied.</span></span> <span data-ttu-id="5fe28-151">Si l'attribut est un élément dans un membre (tel qu'un paramètre, une valeur de retour, ou un paramètre de type générique), le résultat est le nom du membre qui est associé à cet élément.</span><span class="sxs-lookup"><span data-stu-id="5fe28-151">If the attribute is any element within a member (such as a parameter, a return value, or a generic type parameter), this result is the name of the member that's associated with that element.</span></span>|
|<span data-ttu-id="5fe28-152">Aucun membre contenant (par exemple, niveau assembly ou attributs qui sont appliqués aux types)</span><span class="sxs-lookup"><span data-stu-id="5fe28-152">No containing member (for example, assembly-level or attributes that are applied to types)</span></span>|<span data-ttu-id="5fe28-153">Valeur par défaut du paramètre optionnel.</span><span class="sxs-lookup"><span data-stu-id="5fe28-153">The default value of the optional parameter.</span></span>|

## <a name="see-also"></a><span data-ttu-id="5fe28-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fe28-154">See also</span></span>

- [<span data-ttu-id="5fe28-155">Attributs</span><span class="sxs-lookup"><span data-stu-id="5fe28-155">Attributes</span></span>](attributes.md)
- [<span data-ttu-id="5fe28-156">Arguments nommés</span><span class="sxs-lookup"><span data-stu-id="5fe28-156">Named arguments</span></span>](parameters-and-arguments.md#named-arguments)
- [<span data-ttu-id="5fe28-157">Paramètres facultatifs</span><span class="sxs-lookup"><span data-stu-id="5fe28-157">Optional parameters</span></span>](parameters-and-arguments.md#optional-parameters)
