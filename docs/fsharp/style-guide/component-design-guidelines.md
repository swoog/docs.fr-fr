---
title: 'Règles de conception du composant F #'
description: 'Découvrez les instructions pour l’écriture de composants F # destinés à la consommation par les autres appelants.'
ms.date: 05/14/2018
ms.openlocfilehash: 7e71710b1bc2fe3e8d7a5a091513a1432650dc04
ms.sourcegitcommit: 43924acbdbb3981d103e11049bbe460457d42073
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/23/2018
---
# <a name="f-component-design-guidelines"></a><span data-ttu-id="3395e-103">Règles de conception du composant F #</span><span class="sxs-lookup"><span data-stu-id="3395e-103">F# component design guidelines</span></span>

<span data-ttu-id="3395e-104">Ce document est un ensemble de règles de conception de composant pour F # de programmation, selon les F # composant règles de conception, v14, Microsoft Research, et [une autre version](https://fsharp.org/specs/component-design-guidelines/) à l’origine organisé et géré par le Software Foundation F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-104">This document is a set of component design guidelines for F# programming, based on the F# Component Design Guidelines, v14, Microsoft Research, and [another version](https://fsharp.org/specs/component-design-guidelines/) originally curated and maintained by the F# Software Foundation.</span></span>

<span data-ttu-id="3395e-105">Ce document suppose que vous êtes familiarisé avec la programmation F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-105">This document assumes you are familiar with F# programming.</span></span> <span data-ttu-id="3395e-106">Un grand merci de la Communauté pour obtenir des commentaires utiles sur les différentes versions de ce guide et leurs contributions F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-106">Many thanks to the F# community for their contributions and helpful feedback on various versions of this guide.</span></span>

## <a name="overview"></a><span data-ttu-id="3395e-107">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="3395e-107">Overview</span></span>

<span data-ttu-id="3395e-108">Ce document présente certains des problèmes liés à la conception du composant F # et de codage.</span><span class="sxs-lookup"><span data-stu-id="3395e-108">This document looks at some of the issues related to F# component design and coding.</span></span> <span data-ttu-id="3395e-109">Un composant peut signifier que les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="3395e-109">A component can mean any of the following:</span></span>

* <span data-ttu-id="3395e-110">Une couche dans votre projet F # qui a des consommateurs externes dans ce projet.</span><span class="sxs-lookup"><span data-stu-id="3395e-110">A layer in your F# project that has external consumers within that project.</span></span>
* <span data-ttu-id="3395e-111">Une bibliothèque destinée à la consommation par le code F # sur les limites de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3395e-111">A library intended for consumption by F# code across assembly boundaries.</span></span>
* <span data-ttu-id="3395e-112">Une bibliothèque destinée à la consommation par n’importe quel langage .NET sur les limites de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3395e-112">A library intended for consumption by any .NET language across assembly boundaries.</span></span>
* <span data-ttu-id="3395e-113">Une bibliothèque prévue pour la distribution via un référentiel de packages, tels que [NuGet](https://nuget.org).</span><span class="sxs-lookup"><span data-stu-id="3395e-113">A library intended for distribution via a package repository, such as [NuGet](https://nuget.org).</span></span>

<span data-ttu-id="3395e-114">Suivent des techniques décrites dans cet article la [cinq principes du bon code F #](index.md#five-principles-of-good-f-code)et donc utiliser des fonctionnalités et de l’objet de programmation comme il convient.</span><span class="sxs-lookup"><span data-stu-id="3395e-114">Techniques described in this article follow the [Five principles of good F# code](index.md#five-principles-of-good-f-code), and thus utilize both functional and object programming as appropriate.</span></span>

<span data-ttu-id="3395e-115">Quelle que soit la méthode, le Concepteur de composant et de la bibliothèque fait face à un nombre de problèmes prosaïques et pratiques lorsque vous tentez de créer une API qui n’est plus facilement utilisable par les développeurs.</span><span class="sxs-lookup"><span data-stu-id="3395e-115">Regardless of the methodology, the component and library designer faces a number of practical and prosaic issues when trying to craft an API that is most easily usable by developers.</span></span> <span data-ttu-id="3395e-116">Application consciencieux de la [la conception de bibliothèque .NET](../../standard/design-guidelines/index.md) sera vous diriger vers la création d’un ensemble cohérent d’API est agréable à consommer.</span><span class="sxs-lookup"><span data-stu-id="3395e-116">Conscientious application of the [.NET Library Design Guidelines](../../standard/design-guidelines/index.md) will steer you towards creating a consistent set of APIs that are pleasant to consume.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="3395e-117">Indications générales</span><span class="sxs-lookup"><span data-stu-id="3395e-117">General guidelines</span></span>

<span data-ttu-id="3395e-118">Il existe quelques instructions universelles qui s’appliquent aux bibliothèques F #, quel que soit le public concerné par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3395e-118">There are a few universal guidelines that apply to F# libraries, regardless of the intended audience for the library.</span></span>

### <a name="learn-the-net-library-design-guidelines"></a><span data-ttu-id="3395e-119">Découvrez les règles de conception de bibliothèque .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-119">Learn the .NET Library Design Guidelines</span></span>

<span data-ttu-id="3395e-120">Quel que soit le type de F # vous effectuez de codage, il est utile de disposer d’une connaissance de la [la conception de bibliothèque .NET](../../standard/design-guidelines/index.md).</span><span class="sxs-lookup"><span data-stu-id="3395e-120">Regardless of the kind of F# coding you are doing, it is valuable to have a working knowledge of the [.NET Library Design Guidelines](../../standard/design-guidelines/index.md).</span></span> <span data-ttu-id="3395e-121">La plupart des autres F # et aux programmeurs .NET seront connaissance de ces instructions et attendre le code .NET pour se conformer à leur.</span><span class="sxs-lookup"><span data-stu-id="3395e-121">Most other F# and .NET programmers will be familiar with these guidelines, and expect .NET code to conform to them.</span></span>

<span data-ttu-id="3395e-122">Les règles de conception de bibliothèque .NET fournissent des recommandations générales concernant d’affectation de noms, la conception des classes et interfaces, conception de membres (propriétés, méthodes, événements, etc.) et bien plus encore et sont utile premier point de référence pour une variété de guide de conception.</span><span class="sxs-lookup"><span data-stu-id="3395e-122">The .NET Library Design Guidelines provide general guidance regarding naming, designing classes and interfaces, member design (properties, methods, events, etc.) and more, and are a useful first point of reference for a variety of design guidance.</span></span>

### <a name="add-xml-documentation-comments-to-your-code"></a><span data-ttu-id="3395e-123">Ajouter des commentaires de documentation XML à votre code</span><span class="sxs-lookup"><span data-stu-id="3395e-123">Add XML documentation comments to your code</span></span>

<span data-ttu-id="3395e-124">Documentation XML sur les API publiques vous assurer que les utilisateurs peuvent obtenir excellent Intellisense et info Express à l’aide de ces types et membres et activer construction documentation fichiers pour la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3395e-124">XML documentation on public APIs ensure that users can get great Intellisense and Quickinfo when using these types and members, and enable building documentation files for the library.</span></span> <span data-ttu-id="3395e-125">Consultez le [Documentation XML](../language-reference/xml-documentation.md) sur différentes balises xml qui peuvent être utilisés pour le balisage supplémentaire dans les commentaires de xmldoc.</span><span class="sxs-lookup"><span data-stu-id="3395e-125">See the [XML Documentation](../language-reference/xml-documentation.md) about various xml tags that can be used for additional markup within xmldoc comments.</span></span>

```fsharp
/// A class for representing (x,y) coordinates
type Point =

    /// Computes the distance between this point and another
    member DistanceTo : otherPoint:Point -> float
```

<span data-ttu-id="3395e-126">Vous pouvez utiliser des commentaires XML forme abrégée (`/// comment`), ou les commentaires XML standard (`///<summary>comment</summary>`).</span><span class="sxs-lookup"><span data-stu-id="3395e-126">You can use either the short form XML comments (`/// comment`), or standard XML comments (`///<summary>comment</summary>`).</span></span>

### <a name="consider-using-explicit-signature-files-fsi-for-stable-library-and-component-apis"></a><span data-ttu-id="3395e-127">Envisagez d’utiliser des fichiers de signature explicite (.fsi) pour la bibliothèque stable et API de composant</span><span class="sxs-lookup"><span data-stu-id="3395e-127">Consider using explicit signature files (.fsi) for stable library and component APIs</span></span>

<span data-ttu-id="3395e-128">À l’aide des fichiers de signature explicite dans une bibliothèque F # fournit un résumé succinct des API publique, qui permet de se pour assurer que vous connaissez la surface publique complète de la bibliothèque, ainsi que fournit une séparation nette entre la documentation public et internes détails d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="3395e-128">Using explicit signatures files in an F# library provides a succinct summary of public API, which both helps to ensure that you know the full public surface of your library, as well as provides a clean separation between public documentation and internal implementation details.</span></span> <span data-ttu-id="3395e-129">Notez que les fichiers de signature ajoutent friction à l’évolution de l’API publique, en exigeant que les modifications à apporter dans les fichiers de l’implémentation et la signature.</span><span class="sxs-lookup"><span data-stu-id="3395e-129">Note that signature files add friction to changing the public API, by requiring changes to be made in both the implementation and signature files.</span></span> <span data-ttu-id="3395e-130">Par conséquent, les fichiers de signature en général uniquement convient lorsqu’une API a deviennent consolidée et est censée ne sont plus changer de manière significative.</span><span class="sxs-lookup"><span data-stu-id="3395e-130">As a result, signature files should typically only be introduced when an API has become solidified and is no longer expected to change significantly.</span></span>

### <a name="always-follow-best-practices-for-using-strings-in-net"></a><span data-ttu-id="3395e-131">Suivez toujours les meilleures pratiques pour l’utilisation de chaînes dans .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-131">Always follow best practices for using strings in .NET</span></span>

<span data-ttu-id="3395e-132">Suivez [meilleures pratiques pour l’utilisation de chaînes dans .NET](../../standard/base-types/best-practices-strings.md) des conseils.</span><span class="sxs-lookup"><span data-stu-id="3395e-132">Follow [Best Practices for Using Strings in .NET](../../standard/base-types/best-practices-strings.md) guidance.</span></span> <span data-ttu-id="3395e-133">En particulier, l’état toujours explicitement *intention culturelle* dans la conversion et la comparaison de chaînes (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="3395e-133">In particular, always explicitly state *cultural intent* in the conversion and comparison of strings (where applicable).</span></span>

## <a name="guidelines-for-f-facing-libraries"></a><span data-ttu-id="3395e-134">Instructions pour F #-faisant face à des bibliothèques</span><span class="sxs-lookup"><span data-stu-id="3395e-134">Guidelines for F#-facing libraries</span></span>

<span data-ttu-id="3395e-135">Cette section présente des recommandations pour le développement publique F #-faisant face à des bibliothèques. Autrement dit, les bibliothèques exposer des API publiques qui sont destinés à être consommés par les développeurs de F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-135">This section presents recommendations for developing public F#-facing libraries; that is, libraries exposing public APIs that are intended to be consumed by F# developers.</span></span> <span data-ttu-id="3395e-136">Il existe une variété de recommandations sur la conception de la bibliothèque s’applique spécifiquement à F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-136">There are a variety of library-design recommendations applicable specifically to F#.</span></span> <span data-ttu-id="3395e-137">En l’absence de recommandations spécifiques qui suivent, les règles de conception de bibliothèque .NET sont les conseils de secours.</span><span class="sxs-lookup"><span data-stu-id="3395e-137">In the absence of the specific recommendations that follow, the .NET Library Design Guidelines are the fallback guidance.</span></span>

### <a name="naming-conventions"></a><span data-ttu-id="3395e-138">Conventions d'attribution d'un nom</span><span class="sxs-lookup"><span data-stu-id="3395e-138">Naming conventions</span></span>

#### <a name="use-net-naming-and-capitalization-conventions"></a><span data-ttu-id="3395e-139">Utilisez les conventions d’affectation de noms et de mise en majuscules de .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-139">Use .NET naming and capitalization conventions</span></span>

<span data-ttu-id="3395e-140">Le tableau suivant suit les conventions d’affectation de noms et de mise en majuscules de .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-140">The following table follows .NET naming and capitalization conventions.</span></span> <span data-ttu-id="3395e-141">Il existe des petites ajouts d’inclure également les constructions F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-141">There are small additions to also include F# constructs.</span></span>

| <span data-ttu-id="3395e-142">Construction</span><span class="sxs-lookup"><span data-stu-id="3395e-142">Construct</span></span> | <span data-ttu-id="3395e-143">Case</span><span class="sxs-lookup"><span data-stu-id="3395e-143">Case</span></span> | <span data-ttu-id="3395e-144">Élément</span><span class="sxs-lookup"><span data-stu-id="3395e-144">Part</span></span> | <span data-ttu-id="3395e-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="3395e-145">Examples</span></span> | <span data-ttu-id="3395e-146">Notes</span><span class="sxs-lookup"><span data-stu-id="3395e-146">Notes</span></span> |
|-----------|------|------|----------|-------|
| <span data-ttu-id="3395e-147">Types concrets</span><span class="sxs-lookup"><span data-stu-id="3395e-147">Concrete types</span></span> | <span data-ttu-id="3395e-148">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-148">PascalCase</span></span> | <span data-ttu-id="3395e-149">Nom / adjectivale</span><span class="sxs-lookup"><span data-stu-id="3395e-149">Noun/ adjective</span></span> | <span data-ttu-id="3395e-150">La liste, Double, complexe</span><span class="sxs-lookup"><span data-stu-id="3395e-150">List, Double, Complex</span></span> | <span data-ttu-id="3395e-151">Types concrets sont des structs, des classes, des énumérations, des délégués, des enregistrements et des unions.</span><span class="sxs-lookup"><span data-stu-id="3395e-151">Concrete types are structs, classes, enumerations, delegates, records, and unions.</span></span> <span data-ttu-id="3395e-152">Bien que les noms de types sont généralement en minuscules dans OCaml, F # a arrêté le schéma d’affectation de noms .NET pour les types.</span><span class="sxs-lookup"><span data-stu-id="3395e-152">Though type names are traditionally lowercase in OCaml, F# has adopted the .NET naming scheme for types.</span></span>
| <span data-ttu-id="3395e-153">DLL</span><span class="sxs-lookup"><span data-stu-id="3395e-153">DLLs</span></span>           | <span data-ttu-id="3395e-154">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-154">PascalCase</span></span> |                 | <span data-ttu-id="3395e-155">Fabrikam.Core.dll</span><span class="sxs-lookup"><span data-stu-id="3395e-155">Fabrikam.Core.dll</span></span> |  |
| <span data-ttu-id="3395e-156">Balises d’union</span><span class="sxs-lookup"><span data-stu-id="3395e-156">Union tags</span></span>     | <span data-ttu-id="3395e-157">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-157">PascalCase</span></span> | <span data-ttu-id="3395e-158">nom</span><span class="sxs-lookup"><span data-stu-id="3395e-158">Noun</span></span> | <span data-ttu-id="3395e-159">Certains, ajouter, réussite</span><span class="sxs-lookup"><span data-stu-id="3395e-159">Some, Add, Success</span></span> | <span data-ttu-id="3395e-160">N’utilisez pas de préfixe dans les API publiques.</span><span class="sxs-lookup"><span data-stu-id="3395e-160">Do not use a prefix in public APIs.</span></span> <span data-ttu-id="3395e-161">Éventuellement utiliser un préfixe lorsque internes, tels que ''' les équipes de type = TAlpha</span><span class="sxs-lookup"><span data-stu-id="3395e-161">Optionally use a prefix when internal, such as \`\`\`type Teams = TAlpha</span></span> | <span data-ttu-id="3395e-162">TBeta</span><span class="sxs-lookup"><span data-stu-id="3395e-162">TBeta</span></span> | <span data-ttu-id="3395e-163">TDelta. » »</span><span class="sxs-lookup"><span data-stu-id="3395e-163">TDelta.\`\`\`</span></span> |
| <span data-ttu-id="3395e-164">événement</span><span class="sxs-lookup"><span data-stu-id="3395e-164">Event</span></span>          | <span data-ttu-id="3395e-165">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-165">PascalCase</span></span> | <span data-ttu-id="3395e-166">Verbe</span><span class="sxs-lookup"><span data-stu-id="3395e-166">Verb</span></span> | <span data-ttu-id="3395e-167">ValueChanged / ValueChanging</span><span class="sxs-lookup"><span data-stu-id="3395e-167">ValueChanged / ValueChanging</span></span> |  |
| <span data-ttu-id="3395e-168">Exceptions</span><span class="sxs-lookup"><span data-stu-id="3395e-168">Exceptions</span></span>     | <span data-ttu-id="3395e-169">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-169">PascalCase</span></span> |      | <span data-ttu-id="3395e-170">WebException</span><span class="sxs-lookup"><span data-stu-id="3395e-170">WebException</span></span> | <span data-ttu-id="3395e-171">Nom doit se terminer par « Exception ».</span><span class="sxs-lookup"><span data-stu-id="3395e-171">Name should end with “Exception”.</span></span> |
| <span data-ttu-id="3395e-172">Champ</span><span class="sxs-lookup"><span data-stu-id="3395e-172">Field</span></span>          | <span data-ttu-id="3395e-173">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-173">PascalCase</span></span> | <span data-ttu-id="3395e-174">nom</span><span class="sxs-lookup"><span data-stu-id="3395e-174">Noun</span></span> | <span data-ttu-id="3395e-175">CurrentName</span><span class="sxs-lookup"><span data-stu-id="3395e-175">CurrentName</span></span>  | |
| <span data-ttu-id="3395e-176">Types interface</span><span class="sxs-lookup"><span data-stu-id="3395e-176">Interface types</span></span> |  <span data-ttu-id="3395e-177">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-177">PascalCase</span></span> | <span data-ttu-id="3395e-178">Nom / adjectivale</span><span class="sxs-lookup"><span data-stu-id="3395e-178">Noun/ adjective</span></span> | <span data-ttu-id="3395e-179">IDisposable</span><span class="sxs-lookup"><span data-stu-id="3395e-179">IDisposable</span></span> | <span data-ttu-id="3395e-180">Nom doit commencer par « I ».</span><span class="sxs-lookup"><span data-stu-id="3395e-180">Name should start with “I”.</span></span> |
| <span data-ttu-id="3395e-181">Méthode</span><span class="sxs-lookup"><span data-stu-id="3395e-181">Method</span></span> |  <span data-ttu-id="3395e-182">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-182">PascalCase</span></span> |  <span data-ttu-id="3395e-183">Verbe</span><span class="sxs-lookup"><span data-stu-id="3395e-183">Verb</span></span> | <span data-ttu-id="3395e-184">ToString</span><span class="sxs-lookup"><span data-stu-id="3395e-184">ToString</span></span> | |
| <span data-ttu-id="3395e-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3395e-185">Namespace</span></span> | <span data-ttu-id="3395e-186">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-186">PascalCase</span></span> | | <span data-ttu-id="3395e-187">Microsoft.FSharp.Core</span><span class="sxs-lookup"><span data-stu-id="3395e-187">Microsoft.FSharp.Core</span></span> | <span data-ttu-id="3395e-188">En général utiliser `<Organization>.<Technology>[.<Subnamespace>]`, bien que de supprimer l’organisation si la technologie est indépendante de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3395e-188">Generally use `<Organization>.<Technology>[.<Subnamespace>]`, though drop the organization if the technology is independent of organization.</span></span> |
| <span data-ttu-id="3395e-189">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3395e-189">Parameters</span></span> | <span data-ttu-id="3395e-190">camelCase</span><span class="sxs-lookup"><span data-stu-id="3395e-190">camelCase</span></span> | <span data-ttu-id="3395e-191">nom</span><span class="sxs-lookup"><span data-stu-id="3395e-191">Noun</span></span> |  <span data-ttu-id="3395e-192">typeName, transformation, d’une plage</span><span class="sxs-lookup"><span data-stu-id="3395e-192">typeName, transform, range</span></span> | |
| <span data-ttu-id="3395e-193">permettent de valeurs (internes)</span><span class="sxs-lookup"><span data-stu-id="3395e-193">let values (internal)</span></span> | <span data-ttu-id="3395e-194">camelCase ou PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-194">camelCase or PascalCase</span></span> | <span data-ttu-id="3395e-195">Nom / verbe</span><span class="sxs-lookup"><span data-stu-id="3395e-195">Noun/ verb</span></span> |  <span data-ttu-id="3395e-196">getValue, myTable</span><span class="sxs-lookup"><span data-stu-id="3395e-196">getValue, myTable</span></span> |
| <span data-ttu-id="3395e-197">permettent de valeurs (externe)</span><span class="sxs-lookup"><span data-stu-id="3395e-197">let values (external)</span></span> | <span data-ttu-id="3395e-198">camelCase ou PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-198">camelCase or PascalCase</span></span> | <span data-ttu-id="3395e-199">Nom/verbe</span><span class="sxs-lookup"><span data-stu-id="3395e-199">Noun/verb</span></span>  | <span data-ttu-id="3395e-200">List.Map, Dates.Today</span><span class="sxs-lookup"><span data-stu-id="3395e-200">List.map, Dates.Today</span></span> | <span data-ttu-id="3395e-201">les valeurs liées à Let sont souvent publiques lorsqu’ils suivent les modèles de design fonctionnels traditionnel.</span><span class="sxs-lookup"><span data-stu-id="3395e-201">let-bound values are often public when following traditional functional design patterns.</span></span> <span data-ttu-id="3395e-202">Toutefois, en général utiliser PascalCase lorsque l’identificateur peut être utilisé à partir d’autres langages .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-202">However, generally use PascalCase when the identifier can be used from other .NET languages.</span></span> |
| <span data-ttu-id="3395e-203">Propriété</span><span class="sxs-lookup"><span data-stu-id="3395e-203">Property</span></span>  | <span data-ttu-id="3395e-204">PascalCase</span><span class="sxs-lookup"><span data-stu-id="3395e-204">PascalCase</span></span>  | <span data-ttu-id="3395e-205">Nom / adjectivale</span><span class="sxs-lookup"><span data-stu-id="3395e-205">Noun/ adjective</span></span>  | <span data-ttu-id="3395e-206">IsEndOfFile, couleur d’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="3395e-206">IsEndOfFile, BackColor</span></span>  | <span data-ttu-id="3395e-207">Propriétés booléennes en général utiliser est et peut et doit être positive, comme dans IsEndOfFile, IsNotEndOfFile pas.</span><span class="sxs-lookup"><span data-stu-id="3395e-207">Boolean properties generally use Is and Can and should be affirmative, as in IsEndOfFile, not IsNotEndOfFile.</span></span>

#### <a name="avoid-abbreviations"></a><span data-ttu-id="3395e-208">Éviter les abréviations</span><span class="sxs-lookup"><span data-stu-id="3395e-208">Avoid abbreviations</span></span>

<span data-ttu-id="3395e-209">Les instructions de .NET déconseillons l’utilisation des abréviations (par exemple, « utiliser `OnButtonClick` plutôt que `OnBtnClick`»).</span><span class="sxs-lookup"><span data-stu-id="3395e-209">The .NET guidelines discourage the use of abbreviations (for example, “use `OnButtonClick` rather than `OnBtnClick`”).</span></span> <span data-ttu-id="3395e-210">Les abréviations courantes, telles que `Async` pour « Asynchrone », sont tolérés.</span><span class="sxs-lookup"><span data-stu-id="3395e-210">Common abbreviations, such as `Async` for “Asynchronous”, are tolerated.</span></span> <span data-ttu-id="3395e-211">Cette règle est parfois ignorée pour la programmation fonctionnelle ; par exemple, `List.iter` utilise une abréviation pour « parcourir ».</span><span class="sxs-lookup"><span data-stu-id="3395e-211">This guideline is sometimes ignored for functional programming; for example, `List.iter` uses an abbreviation for “iterate”.</span></span> <span data-ttu-id="3395e-212">Pour cette raison, à l’aide des abréviations a tendance à être tolérée à un niveau plus élevé en F #-à-programmation F #, mais doit toujours généralement être évitée dans la conception du composant public.</span><span class="sxs-lookup"><span data-stu-id="3395e-212">For this reason, using abbreviations tends to be tolerated to a greater degree in F#-to-F# programming, but should still generally be avoided in public component design.</span></span>

#### <a name="avoid-casing-name-collisions"></a><span data-ttu-id="3395e-213">Éviter les collisions de noms de la casse</span><span class="sxs-lookup"><span data-stu-id="3395e-213">Avoid casing name collisions</span></span>

<span data-ttu-id="3395e-214">Les instructions de .NET dire que casse seul ne peut pas être utilisée pour lever l’ambiguïté des collisions de noms, étant donné que certains langages de client (par exemple, Visual Basic) respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="3395e-214">The .NET guidelines say that casing alone cannot be used to disambiguate name collisions, since some client languages (for example, Visual Basic) are case-insensitive.</span></span>

#### <a name="use-acronyms-where-appropriate"></a><span data-ttu-id="3395e-215">Utiliser des acronymes approprié</span><span class="sxs-lookup"><span data-stu-id="3395e-215">Use acronyms where appropriate</span></span>

<span data-ttu-id="3395e-216">Les acronymes telles que XML ne sont pas des abréviations et sont couramment utilisés dans les bibliothèques .NET dans le formulaire en minuscule (Xml).</span><span class="sxs-lookup"><span data-stu-id="3395e-216">Acronyms such as XML are not abbreviations and are widely used in .NET libraries in uncapitalized form (Xml).</span></span> <span data-ttu-id="3395e-217">Uniquement les acronymes connues, largement reconnues doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="3395e-217">Only well-known, widely recognized acronyms should be used.</span></span>

#### <a name="use-pascalcase-for-generic-parameter-names"></a><span data-ttu-id="3395e-218">Utilisez PascalCase pour les noms de paramètre générique</span><span class="sxs-lookup"><span data-stu-id="3395e-218">Use PascalCase for generic parameter names</span></span>

<span data-ttu-id="3395e-219">Utilisez PascalCase pour les noms de paramètre générique dans les API publiques, y compris pour F #-faisant face à des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="3395e-219">Do use PascalCase for generic parameter names in public APIs, including for F#-facing libraries.</span></span> <span data-ttu-id="3395e-220">En particulier, utilisez des noms tels que `T`, `U`, `T1`, `T2` pour les paramètres génériques arbitraires, et lorsque des noms spécifiques ont un sens, puis pour F #-bibliothèques exposés à utilisent des noms tels que `Key`, `Value`, `Arg`(mais pas par exemple, `TKey`).</span><span class="sxs-lookup"><span data-stu-id="3395e-220">In particular, use names like `T`, `U`, `T1`, `T2` for arbitrary generic parameters, and when specific names make sense, then for F#-facing libraries use names like `Key`, `Value`, `Arg` (but not for example, `TKey`).</span></span>

#### <a name="use-either-pascalcase-or-camelcase-for-public-functions-and-values-in-f-modules"></a><span data-ttu-id="3395e-221">Utilisez PascalCase ou camelCase pour les fonctions publiques et les valeurs dans les modules F #</span><span class="sxs-lookup"><span data-stu-id="3395e-221">Use either PascalCase or camelCase for public functions and values in F# modules</span></span>

<span data-ttu-id="3395e-222">camelCase est utilisé pour les fonctions publiques qui sont conçues pour être utilisées non qualifié (par exemple, `invalidArg`) et pour les fonctions de collection standard « » (par exemple, List.map).</span><span class="sxs-lookup"><span data-stu-id="3395e-222">camelCase is used for public functions that are designed to be used unqualified (for example, `invalidArg`), and for the “standard collection functions” (for example, List.map).</span></span> <span data-ttu-id="3395e-223">Dans ces deux cas, les noms de fonctions fonctionnant un peu comme mots clés du langage.</span><span class="sxs-lookup"><span data-stu-id="3395e-223">In both these cases, the function names act much like keywords in the language.</span></span>

### <a name="object-type-and-module-design"></a><span data-ttu-id="3395e-224">Création d’objet, le Type et le Module</span><span class="sxs-lookup"><span data-stu-id="3395e-224">Object, Type, and Module design</span></span>

#### <a name="use-namespaces-or-modules-to-contain-your-types-and-modules"></a><span data-ttu-id="3395e-225">Utiliser des espaces de noms ou des modules pour contenir vos types et des modules</span><span class="sxs-lookup"><span data-stu-id="3395e-225">Use namespaces or modules to contain your types and modules</span></span>

<span data-ttu-id="3395e-226">Chaque fichier F # dans un composant doit commencer par une déclaration d’espace de noms ou une déclaration de module.</span><span class="sxs-lookup"><span data-stu-id="3395e-226">Each F# file in a component should begin with either a namespace declaration or a module declaration.</span></span>

```fsharp
namespace Fabrikam.BasicOperationsAndTypes

type ObjectType1() =
    ...

type ObjectType2() =
     ...

module CommonOperations =
    ...
```

<span data-ttu-id="3395e-227">ou</span><span class="sxs-lookup"><span data-stu-id="3395e-227">or</span></span>

```fsharp
module Fabrikam.BasicOperationsAndTypes

type ObjectType1() =
    ...

type ObjectType2() =
    ...

module CommonOperations =
    ...
```

<span data-ttu-id="3395e-228">Les différences entre l’utilisation des modules et des espaces de noms pour organiser le code au niveau supérieur sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3395e-228">The differences between using modules and namespaces to organize code at the top level are as follows:</span></span>

* <span data-ttu-id="3395e-229">Espaces de noms peut s’étendre sur plusieurs fichiers</span><span class="sxs-lookup"><span data-stu-id="3395e-229">Namespaces can span multiple files</span></span>
* <span data-ttu-id="3395e-230">Espaces de noms ne peut pas contenir de fonctions F #, sauf si elles sont dans un module interne</span><span class="sxs-lookup"><span data-stu-id="3395e-230">Namespaces cannot contain F# functions unless they are within an inner module</span></span>
* <span data-ttu-id="3395e-231">Le code de n’importe quel module donné doit être contenu dans un seul fichier</span><span class="sxs-lookup"><span data-stu-id="3395e-231">The code for any given module must be contained within a single file</span></span>
* <span data-ttu-id="3395e-232">Modules de niveau supérieur peuvent contenir des fonctions F # sans recourir à un module interne</span><span class="sxs-lookup"><span data-stu-id="3395e-232">Top-level modules can contain F# functions without the need for an inner module</span></span>

<span data-ttu-id="3395e-233">Le choix entre un espace de noms de niveau supérieur ou un module a une incidence sur la forme compilée du code et donc affectera la vue à partir d’autres langages .NET doit votre API être consommée en dehors du code F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-233">The choice between a top-level namespace or module affects the compiled form of the code, and thus will affect the view from other .NET languages should your API eventually be consumed outside of F# code.</span></span>

#### <a name="use-methods-and-properties-for-operations-intrinsic-to-object-types"></a><span data-ttu-id="3395e-234">Utilisez les méthodes et propriétés pour les opérations intrinsèques aux types d’objet</span><span class="sxs-lookup"><span data-stu-id="3395e-234">Use methods and properties for operations intrinsic to object types</span></span>

<span data-ttu-id="3395e-235">Lorsque vous travaillez avec des objets, il est préférable pour vous assurer que les fonctionnalités consommable sont implémentée en tant que les méthodes et propriétés de ce type.</span><span class="sxs-lookup"><span data-stu-id="3395e-235">When working with objects, it is best to ensure that consumable functionality is implemented as methods and properties on that type.</span></span>

```fsharp
type HardwareDevice() =

    member this.ID = ...

    member this.SupportedProtocols = ...

type HashTable<'Key,'Value>(comparer: IEqualityComparer<'Key>) =

    member this.Add(key, value) = ...

    member this.ContainsKey(key) = ...

    member this.ContainsValue(value) = ...
```

<span data-ttu-id="3395e-236">Le bloc de fonctionnalité pour un membre donné ne doive pas nécessairement être implémenté dans ce membre, mais la partie consommable de cette fonctionnalité doit être.</span><span class="sxs-lookup"><span data-stu-id="3395e-236">The bulk of functionality for a given member need not necessarily be implemented in that member, but the consumable piece of that functionality should be.</span></span>

#### <a name="use-classes-to-encapsulate-mutable-state"></a><span data-ttu-id="3395e-237">Utiliser les classes pour encapsuler un état mutable</span><span class="sxs-lookup"><span data-stu-id="3395e-237">Use classes to encapsulate mutable state</span></span>

<span data-ttu-id="3395e-238">En F #, cela ne doit être effectué où qu’état n’est pas déjà encapsulé par une autre construction de langage, tel qu’une fermeture, une expression de séquence ou un calcul asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3395e-238">In F#, this only needs to be done where that state is not already encapsulated by another language construct, such as a closure, sequence expression, or asynchronous computation.</span></span>

```fsharp
type Counter() =
    // let-bound values are private in classes.
    let mutable count = 0

    member this.Next() =
        count <- count + 1
        count
```

#### <a name="use-interfaces-to-group-related-operations"></a><span data-ttu-id="3395e-239">Utiliser des interfaces pour regrouper les opérations connexes</span><span class="sxs-lookup"><span data-stu-id="3395e-239">Use interfaces to group related operations</span></span>

<span data-ttu-id="3395e-240">Utiliser les types d’interfaces pour représenter un ensemble d’opérations.</span><span class="sxs-lookup"><span data-stu-id="3395e-240">Use interface types to represent a set of operations.</span></span> <span data-ttu-id="3395e-241">Cela est préférable aux autres options, telles que des tuples de fonctions ou les enregistrements de fonctions.</span><span class="sxs-lookup"><span data-stu-id="3395e-241">This is preferred to other options, such as tuples of functions or records of functions.</span></span>

```fsharp
type Serializer =
    abstract Serialize<'T> : preserveRefEq: bool -> value: 'T -> string
    abstract Deserialize<'T> : preserveRefEq: bool -> pickle: string -> 'T
```

<span data-ttu-id="3395e-242">De préférence à :</span><span class="sxs-lookup"><span data-stu-id="3395e-242">In preference to:</span></span>

```fsharp
type Serializer<'T> = {
    Serialize : bool -> 'T -> string
    Deserialize : bool -> string -> 'T
}
```

<span data-ttu-id="3395e-243">Les interfaces sont des concepts de première classe dans .NET, ce qui vous permet d’obtenir les Foncteurs normalement vous donnera.</span><span class="sxs-lookup"><span data-stu-id="3395e-243">Interfaces are first-class concepts in .NET, which you can use to achieve what Functors would normally give you.</span></span> <span data-ttu-id="3395e-244">En outre, ils peuvent être utilisés pour encoder des types existentiels dans votre programme, les enregistrements de fonctions ne peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="3395e-244">Additionally, they can be used to encode existential types into your program, which records of functions cannot.</span></span>

#### <a name="use-a-module-to-group-functions-which-act-on-collections"></a><span data-ttu-id="3395e-245">Utiliser un module à des fonctions de groupe qui agissent sur des collections</span><span class="sxs-lookup"><span data-stu-id="3395e-245">Use a module to group functions which act on collections</span></span>

<span data-ttu-id="3395e-246">Lorsque vous définissez un type de collection, envisagez de fournir un ensemble standard d’opérations telles que `CollectionType.map` et `CollectionType.iter`) pour les nouveaux types de collection.</span><span class="sxs-lookup"><span data-stu-id="3395e-246">When you define a collection type, consider providing a standard set of operations like `CollectionType.map` and `CollectionType.iter`) for new collection types.</span></span>

```fsharp
module CollectionType =
    let map f c =
        ...
    let iter f c =
        ...
```

<span data-ttu-id="3395e-247">Si vous incluez un tel module, suivez les conventions d’affectation de noms standards pour les fonctions FSharp.Core.</span><span class="sxs-lookup"><span data-stu-id="3395e-247">If you include such a module, follow the standard naming conventions for functions found in FSharp.Core.</span></span>

#### <a name="use-a-module-to-group-functions-for-common-canonical-functions-especially-in-math-and-dsl-libraries"></a><span data-ttu-id="3395e-248">Utiliser un module à des fonctions de groupe pour les fonctions canoniques communes, en particulier dans les mathématiques et des bibliothèques DSL</span><span class="sxs-lookup"><span data-stu-id="3395e-248">Use a module to group functions for common, canonical functions, especially in math and DSL libraries</span></span>

<span data-ttu-id="3395e-249">Par exemple, `Microsoft.FSharp.Core.Operators` est une collection automatiquement ouverte de fonctions de niveau supérieur (comme `abs` et `sin`) fournies par FSharp.Core.dll.</span><span class="sxs-lookup"><span data-stu-id="3395e-249">For example, `Microsoft.FSharp.Core.Operators` is an automatically opened collection of top-level functions (like `abs` and `sin`) provided by FSharp.Core.dll.</span></span>

<span data-ttu-id="3395e-250">De même, une bibliothèque de statistiques peut inclure un module avec des fonctions `erf` et `erfc`, où ce module est conçu pour être ouvert explicitement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="3395e-250">Likewise, a statistics library might include a module with functions `erf` and `erfc`, where this module is designed to be explicitly or automatically opened.</span></span>

#### <a name="consider-using-requirequalifiedaccess-and-carefully-apply-autoopen-attributes"></a><span data-ttu-id="3395e-251">Envisagez d’utiliser RequireQualifiedAccess et soigneusement appliquer les attributs AutoOpen</span><span class="sxs-lookup"><span data-stu-id="3395e-251">Consider using RequireQualifiedAccess and carefully apply AutoOpen attributes</span></span>

<span data-ttu-id="3395e-252">Ajout de la `[<RequireQualifiedAccess>]` attribut à un module indique que le module ne peut-être pas être ouvertes et des références aux éléments du module doivent explicite qualifié accès.</span><span class="sxs-lookup"><span data-stu-id="3395e-252">Adding the `[<RequireQualifiedAccess>]` attribute to a module indicates that the module may not be opened and that references to the elements of the module require explicit qualified access.</span></span> <span data-ttu-id="3395e-253">Par exemple, le `Microsoft.FSharp.Collections.List` module a cet attribut.</span><span class="sxs-lookup"><span data-stu-id="3395e-253">For example, the `Microsoft.FSharp.Collections.List` module has this attribute.</span></span>

<span data-ttu-id="3395e-254">Cela est utile lorsque les valeurs dans le module et les fonctions ont des noms qui sont susceptibles d’entrer en conflit avec les noms dans d’autres modules.</span><span class="sxs-lookup"><span data-stu-id="3395e-254">This is useful when functions and values in the module have names that are likely to conflict with names in other modules.</span></span> <span data-ttu-id="3395e-255">Nécessitant un accès complet peut considérablement améliorer la facilité de maintenance à long terme et evolvability d’une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3395e-255">Requiring qualified access can greatly increase the long-term maintainability and evolvability of a library.</span></span>

<span data-ttu-id="3395e-256">Ajout de la `[<AutoOpen>]` attribut à un module signifie que le module s’ouvre quand l’espace de noms qui le contient est ouvert.</span><span class="sxs-lookup"><span data-stu-id="3395e-256">Adding the `[<AutoOpen>]` attribute to a module means the module will be opened when the containing namespace is opened.</span></span> <span data-ttu-id="3395e-257">Le `[<AutoOpen>]` attribut peut également être appliqué à un assembly pour indiquer un module qui s’ouvre automatiquement lorsque l’assembly est référencé.</span><span class="sxs-lookup"><span data-stu-id="3395e-257">The `[<AutoOpen>]` attribute may also be applied to an assembly to indicate a module that is automatically opened when the assembly is referenced.</span></span>

<span data-ttu-id="3395e-258">Par exemple, une bibliothèque de statistiques **MathsHeaven.Statistics** peut contenir un `module MathsHeaven.Statistics.Operators` contenant des fonctions `erf` et `erfc`.</span><span class="sxs-lookup"><span data-stu-id="3395e-258">For example, a statistics library **MathsHeaven.Statistics** might contain a `module MathsHeaven.Statistics.Operators` containing functions `erf` and `erfc`.</span></span> <span data-ttu-id="3395e-259">Il est raisonnable de marquer ce module en tant que `[<AutoOpen>]`.</span><span class="sxs-lookup"><span data-stu-id="3395e-259">It is reasonable to mark this module as `[<AutoOpen>]`.</span></span> <span data-ttu-id="3395e-260">Cela signifie que `open MathsHeaven.Statistics` également ouvrir ce module et mettre les noms `erf` et `erfc` dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="3395e-260">This means `open MathsHeaven.Statistics` will also open this module and bring the names `erf` and `erfc` into scope.</span></span> <span data-ttu-id="3395e-261">Utiliser un autre bon `[<AutoOpen>]` est pour les modules contenant des méthodes d’extension.</span><span class="sxs-lookup"><span data-stu-id="3395e-261">Another good use of `[<AutoOpen>]` is for modules containing extension methods.</span></span>

<span data-ttu-id="3395e-262">Une surutilisation de `[<AutoOpen>]` aboutissent à des espaces de noms pollués et de l’attribut doit être utilisée avec précaution.</span><span class="sxs-lookup"><span data-stu-id="3395e-262">Overuse of `[<AutoOpen>]` leads to polluted namespaces, and the attribute should be used with care.</span></span> <span data-ttu-id="3395e-263">Pour les bibliothèques spécifiques dans des domaines spécifiques, utiliser judicieusement des `[<AutoOpen>]` peut entraîner une meilleure facilité d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3395e-263">For specific libraries in specific domains, judicious use of `[<AutoOpen>]` can lead to better usability.</span></span>

#### <a name="consider-defining-operator-members-on-classes-where-using-well-known-operators-is-appropriate"></a><span data-ttu-id="3395e-264">Envisagez de définir des membres de l’opérateur sur les classes, où il est nécessaire de l’utilisation d’opérateurs bien connus</span><span class="sxs-lookup"><span data-stu-id="3395e-264">Consider defining operator members on classes where using well-known operators is appropriate</span></span>

<span data-ttu-id="3395e-265">Parfois, les classes sont utilisées pour modéliser des constructions mathématiques telles que les vecteurs.</span><span class="sxs-lookup"><span data-stu-id="3395e-265">Sometimes classes are used to model mathematical constructs such as Vectors.</span></span> <span data-ttu-id="3395e-266">Quand le domaine en cours de modélisation possède des opérateurs bien connus, il est utile de les définir en tant que membres intrinsèques à la classe.</span><span class="sxs-lookup"><span data-stu-id="3395e-266">When the domain being modeled has well-known operators, defining them as members intrinsic to the class is helpful.</span></span>

```fsharp
type Vector(x:float) =

    member v.X = x

    static member (*) (vector:Vector, scalar:float) = Vector(vector.X * scalar)

    static member (+) (vector1:Vector, vector2:Vector) = Vector(vector1.X + vector2.X)

let v = Vector(5.0)

let u = v * 10.0
```

<span data-ttu-id="3395e-267">Ce guide correspond à des indications générales pour ces types .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-267">This guidance corresponds to general .NET guidance for these types.</span></span> <span data-ttu-id="3395e-268">Toutefois, il peut être plus important dans F # car cela permet à ces types à utiliser dans la liaison avec les fonctions F # et les méthodes avec des contraintes de membres, tels que List.sumBy de codage.</span><span class="sxs-lookup"><span data-stu-id="3395e-268">However, it can be additionally important in F# coding as this allows these types to be used in conjunction with F# functions and methods with member constraints, such as List.sumBy.</span></span>

#### <a name="consider-using-compiledname-to-provide-a-net-friendly-name-for-other-net-language-consumers"></a><span data-ttu-id="3395e-269">Envisagez d’utiliser CompiledName pour fournir une. Nom convivial NET pour les autres consommateurs de langage .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-269">Consider using CompiledName to provide a .NET-friendly name for other .NET language consumers</span></span>

<span data-ttu-id="3395e-270">Vous pouvez parfois souhaiter donnez un nom d’un style pour les consommateurs) (F # (tel qu’un membre statique en minuscules afin qu’il apparaisse comme s’il s’agissait d’une fonction liée au module), mais ont un style différent pour le nom lorsqu’il est compilé dans un assembly.</span><span class="sxs-lookup"><span data-stu-id="3395e-270">Sometimes you may wish to name something in one style for F# consumers (such as a static member in lower case so that it appears as if it were a module-bound function), but have a different style for the name when it is compiled into an assembly.</span></span> <span data-ttu-id="3395e-271">Vous pouvez utiliser la `[<CompiledName>]` attribut pour fournir un style différent pour le code non F # consommation de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3395e-271">You can use the `[<CompiledName>]` attribute to provide a different style for non F# code consuming the assembly.</span></span>

```fsharp
type Vector(x:float, y:float) =

    member v.X = x
    member v.Y = y

    [<CompiledName("Create")>]
    static member create x y = Vector (x, y)

let v = Vector.create 5.0 3.0
```

<span data-ttu-id="3395e-272">À l’aide de `[<CompiledName>]`, vous pouvez utiliser les conventions d’affectation de noms .NET pour les consommateurs non F # de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="3395e-272">By using `[<CompiledName>]`, you can use .NET naming conventions for non F# consumers of the assembly.</span></span>

#### <a name="use-method-overloading-for-member-functions-if-doing-so-provides-a-simpler-api"></a><span data-ttu-id="3395e-273">Utilisez la surcharge de méthode pour les fonctions de membre, si cela fournit une API simple</span><span class="sxs-lookup"><span data-stu-id="3395e-273">Use method overloading for member functions, if doing so provides a simpler API</span></span>

<span data-ttu-id="3395e-274">La surcharge de méthode est un outil puissant permettant de simplifier une API qui devra peut-être effectuer des fonctionnalités similaires, mais avec différentes options ou les arguments.</span><span class="sxs-lookup"><span data-stu-id="3395e-274">Method overloading is a powerful tool for simplifying an API that may need to perform similar functionality, but with different options or arguments.</span></span>

```fsharp
type Logger() =

    member this.Log(message) =
        ...
    member this.Log(message, retryPolicy) =
        ...
```

<span data-ttu-id="3395e-275">En F #, il est plus courant de surcharge sur le nombre d’arguments plutôt que des types d’arguments.</span><span class="sxs-lookup"><span data-stu-id="3395e-275">In F#, it is more common to overload on number of arguments rather than types of arguments.</span></span>

#### <a name="hide-the-representations-of-record-and-union-types-if-the-design-of-these-types-is-likely-to-evolve"></a><span data-ttu-id="3395e-276">Masquer les représentations sous forme d’enregistrement et les types union si la conception de ces types est susceptible d’évoluer</span><span class="sxs-lookup"><span data-stu-id="3395e-276">Hide the representations of record and union types if the design of these types is likely to evolve</span></span>

<span data-ttu-id="3395e-277">Éviter de révéler des représentations concrètes des objets.</span><span class="sxs-lookup"><span data-stu-id="3395e-277">Avoid revealing concrete representations of objects.</span></span> <span data-ttu-id="3395e-278">Par exemple, la représentation concrète de <xref:System.DateTime> valeurs n’est pas révélé par l’API publique externe de la conception de la bibliothèque .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-278">For example, the concrete representation of <xref:System.DateTime> values is not revealed by the external, public API of the .NET library design.</span></span> <span data-ttu-id="3395e-279">Au moment de l’exécution, le Common Language Runtime sait l’implémentation validée qui sera utilisée dans l’ensemble de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3395e-279">At run time, the Common Language Runtime knows the committed implementation that will be used throughout execution.</span></span> <span data-ttu-id="3395e-280">Toutefois, code compilé ne lui-même récupérer de dépendances sur la représentation concrète.</span><span class="sxs-lookup"><span data-stu-id="3395e-280">However, compiled code doesn't itself pick up dependencies on the concrete representation.</span></span>

#### <a name="avoid-the-use-of-implementation-inheritance-for-extensibility"></a><span data-ttu-id="3395e-281">Évitez d’utiliser l’héritage d’implémentation pour l’extensibilité</span><span class="sxs-lookup"><span data-stu-id="3395e-281">Avoid the use of implementation inheritance for extensibility</span></span>

<span data-ttu-id="3395e-282">En F #, l’héritage d’implémentation est rarement utilisée.</span><span class="sxs-lookup"><span data-stu-id="3395e-282">In F#, implementation inheritance is rarely used.</span></span> <span data-ttu-id="3395e-283">En outre, les hiérarchies d’héritage sont souvent complexe et difficile à modifier lors de l’arrivent de nouvelles exigences.</span><span class="sxs-lookup"><span data-stu-id="3395e-283">Furthermore, inheritance hierarchies are often complex and difficult to change when new requirements arrive.</span></span> <span data-ttu-id="3395e-284">Implémentation de l’héritage existe toujours dans F # pour les rares cas où il est la meilleure solution à un problème, mais les autres techniques doivent être recherchées dans vos programmes F # lors de la conception pour le polymorphisme, telles que l’implémentation d’interface et de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="3395e-284">Inheritance implementation still exists in F# for compatibility and rare cases where it is the best solution to a problem, but alternative techniques should be sought in your F# programs when designing for polymorphism, such as interface implementation.</span></span>

### <a name="function-and-member-signatures"></a><span data-ttu-id="3395e-285">Signatures de fonction et de membre</span><span class="sxs-lookup"><span data-stu-id="3395e-285">Function and member signatures</span></span>

#### <a name="use-tuples-for-return-values-when-returning-a-small-number-of-multiple-unrelated-values"></a><span data-ttu-id="3395e-286">Utiliser des tuples pour les valeurs retournées lors du retour d’un petit nombre de plusieurs valeurs non liées</span><span class="sxs-lookup"><span data-stu-id="3395e-286">Use tuples for return values when returning a small number of multiple unrelated values</span></span>

<span data-ttu-id="3395e-287">Voici un bon exemple d’utilisation d’un tuple dans un type de retour :</span><span class="sxs-lookup"><span data-stu-id="3395e-287">Here is a good example of using a tuple in a return type:</span></span>

```fsharp
val divrem : BigInteger -> BigInteger -> BigInteger * BigInteger
```

<span data-ttu-id="3395e-288">Pour retourner les types contenant de nombreux composants ou où les composants sont associés à une seule entité identifiable, envisagez d’utiliser un type nommé à la place d’un tuple.</span><span class="sxs-lookup"><span data-stu-id="3395e-288">For return types containing many components, or where the components are related to a single identifiable entity, consider using a named type instead of a tuple.</span></span>

#### <a name="use-asynct-for-async-programming-at-f-api-boundaries"></a><span data-ttu-id="3395e-289">Utilisez `Async<T>` pour la programmation asynchrone au niveau des limites d’API F #</span><span class="sxs-lookup"><span data-stu-id="3395e-289">Use `Async<T>` for async programming at F# API boundaries</span></span>

<span data-ttu-id="3395e-290">S’il existe une opération synchrone correspondante nommée `Operation` qui retourne un `T`, l’opération asynchrone doit être nommé `AsyncOperation` si elle retourne `Async<T>` ou `OperationAsync` si elle retourne `Task<T>`.</span><span class="sxs-lookup"><span data-stu-id="3395e-290">If there is a corresponding synchronous operation named `Operation` that returns a `T`, then the async operation should be named `AsyncOperation` if it returns `Async<T>` or `OperationAsync` if it returns `Task<T>`.</span></span> <span data-ttu-id="3395e-291">Pour les types .NET couramment utilisés qui exposent des méthodes Begin/End, envisagez d’utiliser `Async.FromBeginEnd` pour écrire des méthodes d’extension comme une façade pour fournir le F # async modèle de programmation à l’API .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-291">For commonly used .NET types that expose Begin/End methods, consider using `Async.FromBeginEnd` to write extension methods as a façade to provide the F# async programming model to those .NET APIs.</span></span>

```fsharp
type SomeType =
    member this.Compute(x:int) : int =
        ...
    member this.AsyncCompute(x:int) : Async<int> =
        ...

type System.ServiceModel.Channels.IInputChannel with
    member this.AsyncReceive() =
        ...
```

### <a name="exceptions"></a><span data-ttu-id="3395e-292">Exceptions</span><span class="sxs-lookup"><span data-stu-id="3395e-292">Exceptions</span></span>

<span data-ttu-id="3395e-293">Les exceptions sont exceptionnelles dans .NET ; Autrement dit, ils ne doivent pas se produire fréquemment lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="3395e-293">Exceptions are exceptional in .NET; that is, they should not occur frequently at runtime.</span></span> <span data-ttu-id="3395e-294">Dans ce cas, les informations qu’ils contiennent sont précieuses.</span><span class="sxs-lookup"><span data-stu-id="3395e-294">When they do, the information they contain is valuable.</span></span> <span data-ttu-id="3395e-295">Les exceptions sont un cœur de première classe concept de .NET ; informatique donc approprié à l’application des Exceptions qui suit doit être utilisé dans le cadre de la conception de l’interface d’un composant.</span><span class="sxs-lookup"><span data-stu-id="3395e-295">Exceptions are a core first class concept of .NET; it hence follows that appropriate application of the Exceptions should be used as part of the design of the interface of a component.</span></span>

#### <a name="follow-the-net-guidelines-for-exceptions"></a><span data-ttu-id="3395e-296">Suivez les instructions de .NET pour les exceptions</span><span class="sxs-lookup"><span data-stu-id="3395e-296">Follow the .NET guidelines for exceptions</span></span>

<span data-ttu-id="3395e-297">Le [la conception de bibliothèque .NET](../../standard/design-guidelines/exceptions.md) conseils excellente sur l’utilisation d’exceptions dans le contexte de toute programmation .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-297">The [.NET Library Design Guidelines](../../standard/design-guidelines/exceptions.md) give excellent advice on the use of exceptions in the context of all .NET programming.</span></span> <span data-ttu-id="3395e-298">Certaines de ces indications sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3395e-298">Some of these guidelines are as follows:</span></span>

* <span data-ttu-id="3395e-299">N’utilisez pas d’exceptions pour le flux de contrôle normal.</span><span class="sxs-lookup"><span data-stu-id="3395e-299">Do not use exceptions for normal flow of control.</span></span> <span data-ttu-id="3395e-300">Bien que cette technique est souvent utilisée dans des langages tels que OCaml, il est susceptible d’engendrer des bogues et peut être inefficace sur .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-300">Although this technique is often used in languages such as OCaml, it is bug-prone and can be inefficient on .NET.</span></span> <span data-ttu-id="3395e-301">Au lieu de cela, envisagez de retourner un `None` valeur pour indiquer un échec qui est une occurrence courantes ou attendue de l’option.</span><span class="sxs-lookup"><span data-stu-id="3395e-301">Instead, consider returning a `None` option value to indicate a failure that is a common or expected occurrence.</span></span>

* <span data-ttu-id="3395e-302">Documentez les exceptions levées par vos composants lorsqu’une fonction est utilisée de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="3395e-302">Document exceptions thrown by your components when a function is used incorrectly.</span></span>

* <span data-ttu-id="3395e-303">Si possible, utiliser des exceptions existantes des espaces de noms système.</span><span class="sxs-lookup"><span data-stu-id="3395e-303">Where possible, employ existing exceptions from the System namespaces.</span></span> <span data-ttu-id="3395e-304">Éviter <xref:System.ApplicationException>, même si.</span><span class="sxs-lookup"><span data-stu-id="3395e-304">Avoid <xref:System.ApplicationException>, though.</span></span>

* <span data-ttu-id="3395e-305">Ne levez pas <xref:System.Exception> lorsqu’il échappe au code utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3395e-305">Do not throw <xref:System.Exception> when it will escape to user code.</span></span> <span data-ttu-id="3395e-306">Cela inclut les éviter l’utilisation de `failwith`, `failwithf`, qui sont des fonctions très pratiques pour une utilisation dans les scripts et le code en cours de développement, mais doit être supprimé à partir de code de la bibliothèque F # en faveur de la levée d’un type d’exception plus spécifique.</span><span class="sxs-lookup"><span data-stu-id="3395e-306">This includes avoiding the use of `failwith`, `failwithf`, which are handy functions for use in scripting and for code under development, but should be removed from F# library code in favor of throwing a more specific exception type.</span></span>

* <span data-ttu-id="3395e-307">Utilisez `nullArg`, `invalidArg`, et `invalidOp` comme mécanisme de lever <xref:System.ArgumentNullException>, <xref:System.ArgumentException>, et <xref:System.InvalidOperationException> quand cela est approprié.</span><span class="sxs-lookup"><span data-stu-id="3395e-307">Use `nullArg`, `invalidArg`, and `invalidOp` as the mechanism to throw <xref:System.ArgumentNullException>, <xref:System.ArgumentException>, and <xref:System.InvalidOperationException> when appropriate.</span></span>

#### <a name="consider-using-option-values-for-return-types-when-failure-is-not-an-exceptional-scenario"></a><span data-ttu-id="3395e-308">Envisagez d’utiliser des valeurs d’option pour les types de retournés lors de l’échec n’est pas un scénario exceptionnel</span><span class="sxs-lookup"><span data-stu-id="3395e-308">Consider using option values for return types when failure is not an exceptional scenario</span></span>

<span data-ttu-id="3395e-309">L’approche de .NET pour les exceptions est qu’ils doivent être « exceptionnelles » ; Autrement dit, ils doivent peu fréquentes.</span><span class="sxs-lookup"><span data-stu-id="3395e-309">The .NET approach to exceptions is that they should be “exceptional”; that is, they should occur relatively infrequently.</span></span> <span data-ttu-id="3395e-310">Toutefois, certaines opérations (par exemple, rechercher une table) peuvent échouer fréquemment.</span><span class="sxs-lookup"><span data-stu-id="3395e-310">However, some operations (for example, searching a table) may fail frequently.</span></span> <span data-ttu-id="3395e-311">Les valeurs d’option F # sont un excellent moyen de représenter les types de retour de ces opérations.</span><span class="sxs-lookup"><span data-stu-id="3395e-311">F# option values are an excellent way to represent the return types of these operations.</span></span> <span data-ttu-id="3395e-312">Ces opérations sont traditionnellement démarrer avec le préfixe de nom « try » :</span><span class="sxs-lookup"><span data-stu-id="3395e-312">These operations conventionally start with the name prefix “try”:</span></span>

```fsharp
// bad: throws exception if no element meets criteria
member this.FindFirstIndex(pred : 'T -> bool) : int =
    ...

// bad: returns -1 if no element meets criteria
member this.FindFirstIndex(pred : 'T -> bool) : int =
    ...

// good: returns None if no element meets criteria
member this.TryFindFirstIndex(pred : 'T -> bool) : int option =
    ...
```

### <a name="extension-members"></a><span data-ttu-id="3395e-313">Membres d’extension</span><span class="sxs-lookup"><span data-stu-id="3395e-313">Extension Members</span></span>

#### <a name="carefully-apply-f-extension-members-in-f-to-f-components"></a><span data-ttu-id="3395e-314">Appliquer attentivement les membres d’extension F # en F #-à-composants F #</span><span class="sxs-lookup"><span data-stu-id="3395e-314">Carefully apply F# extension members in F#-to-F# components</span></span>

<span data-ttu-id="3395e-315">Membres d’extension F # doivent uniquement être utilisées pour les opérations qui se trouvent dans la clôture des intrinsèques opérations associées à un type dans la plupart de ses modes d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3395e-315">F# extension members should generally only be used for operations that are in the closure of intrinsic operations associated with a type in the majority of its modes of use.</span></span> <span data-ttu-id="3395e-316">Une utilisation courante consiste à fournir des API qui est plus IDIOMATIQUE à F # pour différents types .NET :</span><span class="sxs-lookup"><span data-stu-id="3395e-316">One common use is to provide APIs that are more idiomatic to F# for various .NET types:</span></span>

```fsharp
type System.ServiceModel.Channels.IInputChannel with
    member this.AsyncReceive() =
        Async.FromBeginEnd(this.BeginReceive, this.EndReceive)

type System.Collections.Generic.IDictionary<'Key,'Value> with
    member this.TryGet key =
        let ok, v = this.TryGetValue key
        if ok then Some v else None
```

### <a name="union-types"></a><span data-ttu-id="3395e-317">Types d’union</span><span class="sxs-lookup"><span data-stu-id="3395e-317">Union Types</span></span>

#### <a name="use-discriminated-unions-instead-of-class-hierarchies-for-tree-structured-data"></a><span data-ttu-id="3395e-318">Utilisez les unions discriminées au lieu de hiérarchies de classes pour l’arborescence de la structure de données</span><span class="sxs-lookup"><span data-stu-id="3395e-318">Use discriminated unions instead of class hierarchies for tree-structured data</span></span>

<span data-ttu-id="3395e-319">Structures d’arborescence sont définies de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="3395e-319">Tree-like structures are recursively defined.</span></span> <span data-ttu-id="3395e-320">Il s’agit maladroite avec héritage mais élégante avec les Unions discriminées.</span><span class="sxs-lookup"><span data-stu-id="3395e-320">This is awkward with inheritance, but elegant with Discriminated Unions.</span></span>

```fsharp
type BST<'T> =
    | Empty
    | Node of 'T * BST<'T> * BST<'T>
```

<span data-ttu-id="3395e-321">Représentant les données sous forme d’arborescence avec les Unions discriminées vous permet également de bénéficier d’exhaustivité dans les critères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="3395e-321">Representing tree-like data with Discriminated Unions also allows you to benefit from exhaustiveness in pattern matching.</span></span>

#### <a name="use-requirequalifiedaccess-on-union-types-whose-case-names-are-not-sufficiently-unique"></a><span data-ttu-id="3395e-322">Utilisez `[<RequireQualifiedAccess>]` sur les types d’union dont les noms cas ne sont pas suffisamment uniques</span><span class="sxs-lookup"><span data-stu-id="3395e-322">Use `[<RequireQualifiedAccess>]` on union types whose case names are not sufficiently unique</span></span>

<span data-ttu-id="3395e-323">Vous pouvez trouver vous-même dans un domaine où le même nom est le meilleur nom pour différents éléments, tels que des cas discriminée Union.</span><span class="sxs-lookup"><span data-stu-id="3395e-323">You may find yourself in a domain where the same name is the best name for different things, such as Discriminated Union cases.</span></span> <span data-ttu-id="3395e-324">Vous pouvez utiliser `[<RequireQualifiedAccess>]` pour lever l’ambiguïté des noms d’incidents pour éviter de déclencher des erreurs à confusion en raison d’une occultation dépendantes de l’ordre de `open` instructions</span><span class="sxs-lookup"><span data-stu-id="3395e-324">You can use `[<RequireQualifiedAccess>]` to disambiguate case names in order to avoid triggering confusing errors due to shadowing dependent on the ordering of `open` statements</span></span>

#### <a name="hide-the-representations-of-discriminated-unions-for-binary-compatible-apis-if-the-design-of-these-types-is-likely-to-evolve"></a><span data-ttu-id="3395e-325">Masquer les représentations sous forme d’unions discriminées pour les API compatible binaire si la conception de ces types est susceptible d’évoluer</span><span class="sxs-lookup"><span data-stu-id="3395e-325">Hide the representations of discriminated unions for binary compatible APIs if the design of these types is likely to evolve</span></span>

<span data-ttu-id="3395e-326">Types d’unions s’appuient sur F # correspondance formulaires pour un modèle de programmation concis.</span><span class="sxs-lookup"><span data-stu-id="3395e-326">Unions types rely on F# pattern-matching forms for a succinct programming model.</span></span> <span data-ttu-id="3395e-327">Comme mentionné précédemment, vous devez éviter de révéler les représentations sous forme de données concrètes si la conception de ces types est susceptible d’évoluer.</span><span class="sxs-lookup"><span data-stu-id="3395e-327">As mentioned previously, you should avoid revealing concrete data representations if the design of these types is likely to evolve.</span></span>

<span data-ttu-id="3395e-328">Par exemple, la représentation sous forme d’une union discriminée peut être masquée à l’aide d’une déclaration privée ou interne, ou à l’aide d’un fichier de signature.</span><span class="sxs-lookup"><span data-stu-id="3395e-328">For example, the representation of a discriminated union can be hidden using a private or internal declaration, or by using a signature file.</span></span>

```fsharp
type Union =
    private
    | CaseA of int
    | CaseB of string
```

<span data-ttu-id="3395e-329">Si vous révéler les unions discriminées sans discrimination, il peut s’avérer difficiles à la version de votre bibliothèque sans rupture du code de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3395e-329">If you reveal discriminated unions indiscriminately, you may find it hard to version your library without breaking user code.</span></span> <span data-ttu-id="3395e-330">Envisagez plutôt de révéler un ou plusieurs modèles actifs pour permettre la mise en correspondance sur les valeurs de ce type.</span><span class="sxs-lookup"><span data-stu-id="3395e-330">Instead, consider revealing one or more active patterns to permit pattern matching over values of your type.</span></span>

<span data-ttu-id="3395e-331">Modèles actifs fournissent une autre façon de fournir aux consommateurs) (F # en correspondance tout en évitant d’exposer directement les Types d’Union F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-331">Active patterns provide an alternate way to provide F# consumers with pattern matching while avoiding exposing F# Union Types directly.</span></span>

### <a name="inline-functions-and-member-constraints"></a><span data-ttu-id="3395e-332">Les fonctions inline et les contraintes de membre</span><span class="sxs-lookup"><span data-stu-id="3395e-332">Inline Functions and Member Constraints</span></span>

#### <a name="define-generic-numeric-algorithms-using-inline-functions-with-implied-member-constraints-and-statically-resolved-generic-types"></a><span data-ttu-id="3395e-333">Définir les algorithmes génériques de numériques à l’aide des fonctions inline avec les contraintes de membre implicite et les types génériques résolus statiquement</span><span class="sxs-lookup"><span data-stu-id="3395e-333">Define generic numeric algorithms using inline functions with implied member constraints and statically resolved generic types</span></span>

<span data-ttu-id="3395e-334">Membre arithmétique contraintes et F # comparaison sont une norme pour la programmation F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-334">Arithmetic member constraints and F# comparison constraints are a standard for F# programming.</span></span> <span data-ttu-id="3395e-335">Considérons par exemple le code suivant :</span><span class="sxs-lookup"><span data-stu-id="3395e-335">For example, consider the following code:</span></span>

```fsharp
let inline highestCommonFactor a b =
    let rec loop a b =
        if a = LanguagePrimitives.GenericZero<_> then b
        elif a < b then loop a (b - a)
        else loop (a - b) b
    loop a b
```

<span data-ttu-id="3395e-336">Le type de cette fonction est comme suit :</span><span class="sxs-lookup"><span data-stu-id="3395e-336">The type of this function is as follows:</span></span>

```fsharp
val inline highestCommonFactor : ^T -> ^T -> ^T
                when ^T : (static member Zero : ^T)
                and ^T : (static member ( - ) : ^T * ^T -> ^T)
                and ^T : equality
                and ^T : comparison
```

<span data-ttu-id="3395e-337">Il s’agit d’une fonction appropriée pour une API publique dans une bibliothèque mathématique.</span><span class="sxs-lookup"><span data-stu-id="3395e-337">This is a suitable function for a public API in a mathematical library.</span></span>

#### <a name="avoid-using-member-constraints-to-simulate-type-classes-and-duck-typing"></a><span data-ttu-id="3395e-338">Évitez d’utiliser des contraintes de membre pour simuler des classes de type et canard en tapant</span><span class="sxs-lookup"><span data-stu-id="3395e-338">Avoid using member constraints to simulate type classes and duck typing</span></span>

<span data-ttu-id="3395e-339">Il est possible de simuler « volante en tapant » à l’aide des contraintes de membre) (F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-339">It is possible to simulate “duck typing” using F# member constraints.</span></span> <span data-ttu-id="3395e-340">Toutefois, les membres qui rendent utiliser de ce pas en général de données doit être utilisé en F #-à-conceptions de bibliothèque F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-340">However, members that make use of this should not in general be used in F#-to-F# library designs.</span></span> <span data-ttu-id="3395e-341">Il s’agit, car les conceptions de bibliothèque selon les contraintes implicites inconnus ou non standard ont tendance à provoquer le code utilisateur deviennent fixes et liée au modèle d’une infrastructure particulière.</span><span class="sxs-lookup"><span data-stu-id="3395e-341">This is because library designs based on unfamiliar or non-standard implicit constraints tend to cause user code to become inflexible and tied to one particular framework pattern.</span></span>

<span data-ttu-id="3395e-342">En outre, il est probable que les délais de compilation très longue peut entraîner une utilisation intensive de contraintes de membre de cette manière.</span><span class="sxs-lookup"><span data-stu-id="3395e-342">Additionally, there is a good chance that heavy use of member constraints in this manner can result in very long compile times.</span></span>

### <a name="operator-definitions"></a><span data-ttu-id="3395e-343">Définitions d’opérateur</span><span class="sxs-lookup"><span data-stu-id="3395e-343">Operator Definitions</span></span>

#### <a name="avoid-defining-custom-symbolic-operators"></a><span data-ttu-id="3395e-344">Évitez de définir des opérateurs symboliques personnalisés</span><span class="sxs-lookup"><span data-stu-id="3395e-344">Avoid defining custom symbolic operators</span></span>

<span data-ttu-id="3395e-345">Opérateurs personnalisés sont essentiels dans certaines situations et appareils de notation très utiles au sein d’un grand nombre de code d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="3395e-345">Custom operators are essential in some situations and are highly useful notational devices within a large body of implementation code.</span></span> <span data-ttu-id="3395e-346">Pour les nouveaux utilisateurs d’une bibliothèque, les fonctions nommées sont souvent plus faciles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3395e-346">For new users of a library, named functions are often easier to use.</span></span> <span data-ttu-id="3395e-347">En outre, opérateurs symboliques personnalisés peuvent être difficiles de document et les utilisateurs s’avérer plus difficile de rechercher de l’aide sur les opérateurs, en raison des limitations existantes dans les moteurs de l’IDE et de recherche.</span><span class="sxs-lookup"><span data-stu-id="3395e-347">In addition, custom symbolic operators can be hard to document, and users find it more difficult to look up help on operators, due to existing limitations in IDE and search engines.</span></span>

<span data-ttu-id="3395e-348">Par conséquent, il est préférable de publier vos fonctionnalités en tant que fonctions nommées et les membres et plus exposer les opérateurs pour cette fonctionnalité que si les notation avantages l’emportent sur la documentation et les coûts cognitifs les.</span><span class="sxs-lookup"><span data-stu-id="3395e-348">As a result, it is best to publish your functionality as named functions and members, and additionally expose operators for this functionality only if the notational benefits outweigh the documentation and cognitive cost of having them.</span></span>

### <a name="units-of-measure"></a><span data-ttu-id="3395e-349">Unités de mesure</span><span class="sxs-lookup"><span data-stu-id="3395e-349">Units of Measure</span></span>

#### <a name="carefully-use-units-of-measure-for-added-type-safety-in-f-code"></a><span data-ttu-id="3395e-350">Avec soin les unités de mesure pour la sécurité de l’ajout d’un type dans le code F #</span><span class="sxs-lookup"><span data-stu-id="3395e-350">Carefully use units of measure for added type safety in F# code</span></span>

<span data-ttu-id="3395e-351">Information de type supplémentaire pour les unités de mesure est effacée lorsqu’ils sont affichés par d’autres langages .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-351">Additional typing information for units of measure is erased when viewed by other .NET languages.</span></span> <span data-ttu-id="3395e-352">N’oubliez pas que réflexion, des outils et composants .NET seront affiche sans unités de types.</span><span class="sxs-lookup"><span data-stu-id="3395e-352">Be aware that .NET components, tools, and reflection will see types-sans-units.</span></span> <span data-ttu-id="3395e-353">Par exemple, C# consommateurs verront `float` plutôt que `float<kg>`.</span><span class="sxs-lookup"><span data-stu-id="3395e-353">For example, C# consumers will see `float` rather than `float<kg>`.</span></span>

### <a name="type-abbreviations"></a><span data-ttu-id="3395e-354">Abréviations de types</span><span class="sxs-lookup"><span data-stu-id="3395e-354">Type Abbreviations</span></span>

#### <a name="carefully-use-type-abbreviations-to-simplify-f-code"></a><span data-ttu-id="3395e-355">Utiliser avec soin les abréviations de type pour simplifier le code F #</span><span class="sxs-lookup"><span data-stu-id="3395e-355">Carefully use type abbreviations to simplify F# code</span></span>

<span data-ttu-id="3395e-356">Réflexion, des outils et composants .NET ne verront pas les noms abrégés pour les types.</span><span class="sxs-lookup"><span data-stu-id="3395e-356">.NET components, tools, and reflection will not see abbreviated names for types.</span></span> <span data-ttu-id="3395e-357">Utilisation intensive des abréviations de type peut également afficher un domaine plus complexe qu’il est en fait, ce qui peut induire en erreur les consommateurs.</span><span class="sxs-lookup"><span data-stu-id="3395e-357">Significant usage of type abbreviations can also make a domain appear more complex than it actually is, which could confuse consumers.</span></span>

#### <a name="avoid-type-abbreviations-for-public-types-whose-members-and-properties-should-be-intrinsically-different-to-those-available-on-the-type-being-abbreviated"></a><span data-ttu-id="3395e-358">Éviter les abréviations de type pour les types publics dont les membres et les propriétés doivent être intrinsèquement différentes de celles qui sont disponibles sur le type abrégé</span><span class="sxs-lookup"><span data-stu-id="3395e-358">Avoid type abbreviations for public types whose members and properties should be intrinsically different to those available on the type being abbreviated</span></span>

<span data-ttu-id="3395e-359">Dans ce cas, le type abrégé révèle trop sur la représentation sous forme de type réel qui est défini.</span><span class="sxs-lookup"><span data-stu-id="3395e-359">In this case, the type being abbreviated reveals too much about the representation of the actual type being defined.</span></span> <span data-ttu-id="3395e-360">Au lieu de cela, envisagez d’encapsuler l’abréviation dans un type de classe ou d’une union discriminée seul cas (ou, lorsque les performances sont essentielles, envisagez d’utiliser un type struct pour encapsuler l’abréviation).</span><span class="sxs-lookup"><span data-stu-id="3395e-360">Instead, consider wrapping the abbreviation in a class type or a single-case discriminated union (or, when performance is essential, consider using a struct type to wrap the abbreviation).</span></span>

<span data-ttu-id="3395e-361">Par exemple, il est tentant de définir un mappage multi comme un cas spécial d’une F # interactive, par exemple :</span><span class="sxs-lookup"><span data-stu-id="3395e-361">For example, it is tempting to define a multi-map as a special case of an F# map, for example:</span></span>

```fsharp
type MultiMap<'Key,'Value> = Map<'Key,'Value list>
```

<span data-ttu-id="3395e-362">Toutefois, les opérations logiques-notation par points sur ce type ne sont pas le même que les opérations sur une carte : par exemple, il est raisonnable que l’opérateur de recherche sont mappés. [clé] Retourne la liste vide si la clé n’est pas dans le dictionnaire, au lieu de lever une exception.</span><span class="sxs-lookup"><span data-stu-id="3395e-362">However, the logical dot-notation operations on this type are not the same as the operations on a Map – for example, it is reasonable that the lookup operator map.[key] return the empty list if the key is not in the dictionary, rather than raising an exception.</span></span>

## <a name="guidelines-for-libraries-for-use-from-other-net-languages"></a><span data-ttu-id="3395e-363">Recommandations pour les bibliothèques à utiliser à partir d’autres langages .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-363">Guidelines for libraries for Use from other .NET Languages</span></span>

<span data-ttu-id="3395e-364">Lorsque vous concevez des bibliothèques pour une utilisation à partir d’autres langages .NET, il est important de respecter le [la conception de bibliothèque .NET](../../standard/design-guidelines/index.md).</span><span class="sxs-lookup"><span data-stu-id="3395e-364">When designing libraries for use from other .NET languages, it is important to adhere to the [.NET Library Design Guidelines](../../standard/design-guidelines/index.md).</span></span> <span data-ttu-id="3395e-365">Dans ce document, ces bibliothèques sont étiquetés vanille bibliothèques .NET, par opposition à F #-faisant face à des bibliothèques qui utilisent F # construit sans restriction.</span><span class="sxs-lookup"><span data-stu-id="3395e-365">In this document, these libraries are labeled as vanilla .NET libraries, as opposed to F#-facing libraries that use F# constructs without restriction.</span></span> <span data-ttu-id="3395e-366">Conception des bibliothèques .NET vanille signifie fournissant des API familière et idiomatiques cohérents avec le reste du .NET Framework en réduisant l’utilisation de F #-des constructions spécifiques dans l’API publique.</span><span class="sxs-lookup"><span data-stu-id="3395e-366">Designing vanilla .NET libraries means providing familiar and idiomatic APIs consistent with the rest of the .NET Framework by minimizing the use of F#-specific constructs in the public API.</span></span> <span data-ttu-id="3395e-367">Les règles sont expliquées dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3395e-367">The rules are explained in the following sections.</span></span>

### <a name="namespace-and-type-design-for-libraries-for-use-from-other-net-languages"></a><span data-ttu-id="3395e-368">Conception Namespace et Type (pour les bibliothèques à utiliser à partir d’autres langages .NET)</span><span class="sxs-lookup"><span data-stu-id="3395e-368">Namespace and Type design (for libraries for use from other .NET Languages)</span></span>

#### <a name="apply-the-net-naming-conventions-to-the-public-api-of-your-components"></a><span data-ttu-id="3395e-369">Appliquer les conventions d’affectation de noms .NET à l’API publique de vos composants</span><span class="sxs-lookup"><span data-stu-id="3395e-369">Apply the .NET naming conventions to the public API of your components</span></span>

<span data-ttu-id="3395e-370">Faites particulièrement attention à l’utilisation de noms abrégés et les instructions de mise en majuscules de .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-370">Pay special attention to the use of abbreviated names and the .NET capitalization guidelines.</span></span>

```fsharp
type pCoord = ...
    member this.theta = ...

type PolarCoordinate = ...
    member this.Theta = ...
```

#### <a name="use-namespaces-types-and-members-as-the-primary-organizational-structure-for-your-components"></a><span data-ttu-id="3395e-371">Utilisez des espaces de noms, types et membres en tant que la structure organisationnelle principale pour vos composants</span><span class="sxs-lookup"><span data-stu-id="3395e-371">Use namespaces, types, and members as the primary organizational structure for your components</span></span>

<span data-ttu-id="3395e-372">Tous les fichiers contenant les fonctionnalités publiques doivent commencer par un `namespace` déclaration, les seules entités publics dans les espaces de noms doivent être des types.</span><span class="sxs-lookup"><span data-stu-id="3395e-372">All files containing public functionality should begin with a `namespace` declaration, and the only public-facing entities in namespaces should be types.</span></span> <span data-ttu-id="3395e-373">N’utilisez pas de modules F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-373">Do not use F# modules.</span></span>

<span data-ttu-id="3395e-374">Utilisez les modules non publics pour contenir le code d’implémentation, les types d’utilitaire et les fonctions d’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="3395e-374">Use non-public modules to hold implementation code, utility types, and utility functions.</span></span>

<span data-ttu-id="3395e-375">Les types static doivent être préférés sur les modules, car elles permettent une évolution ultérieure de l’API à utiliser la surcharge et d’autres concepts de conception de l’API .NET qui ne peuvent pas être utilisées dans des modules F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-375">Static types should be preferred over modules, as they allow for future evolution of the API to use overloading and other .NET API design concepts that may not be used within F# modules.</span></span>

<span data-ttu-id="3395e-376">Par exemple, à la place de l’API publique suivante :</span><span class="sxs-lookup"><span data-stu-id="3395e-376">For example, in place of the following public API:</span></span>

```fsharp
module Fabrikam

module Utilities =
    let Name = "Bob"
    let Add2 x y = x + y
    let Add3 x y z = x + y + z
```

<span data-ttu-id="3395e-377">Pensez à la place :</span><span class="sxs-lookup"><span data-stu-id="3395e-377">Consider instead:</span></span>

```fsharp
namespace Fabrikam

[<AbstractClass; Sealed>]
type Utilities =
    static member Name = "Bob"
    static member Add(x,y) = x + y
    static member Add(x,y,z) = x + y + z
```

#### <a name="use-f-record-types-in-vanilla-net-apis-if-the-design-of-the-types-wont-evolve"></a><span data-ttu-id="3395e-378">Utiliser des types d’enregistrement F # dans vanille API .NET si la conception de types ne sont pas évoluer.</span><span class="sxs-lookup"><span data-stu-id="3395e-378">Use F# record types in vanilla .NET APIs if the design of the types won't evolve</span></span>

<span data-ttu-id="3395e-379">Types d’enregistrement F # compilées en une classe .NET simple.</span><span class="sxs-lookup"><span data-stu-id="3395e-379">F# record types compile to a simple .NET class.</span></span> <span data-ttu-id="3395e-380">Ils ne conviennent pas pour certains types simples, stables dans les API.</span><span class="sxs-lookup"><span data-stu-id="3395e-380">These are suitable for some simple, stable types in APIs.</span></span> <span data-ttu-id="3395e-381">Vous devez envisager d’utiliser le `[<NoEquality>]` et `[<NoComparison>]` attributs à supprimer la génération automatique des interfaces.</span><span class="sxs-lookup"><span data-stu-id="3395e-381">You should consider using the `[<NoEquality>]` and `[<NoComparison>]` attributes to suppress the automatic generation of interfaces.</span></span> <span data-ttu-id="3395e-382">Évitez également à l’aide des champs d’enregistrement mutable dans vanille API .NET en tant que ces expose un champ public.</span><span class="sxs-lookup"><span data-stu-id="3395e-382">Also avoid using mutable record fields in vanilla .NET APIs as these exposes a public field.</span></span> <span data-ttu-id="3395e-383">Envisagez toujours si une classe fournirait une option plus souple pour l’évolution ultérieure de l’API.</span><span class="sxs-lookup"><span data-stu-id="3395e-383">Always consider whether a class would provide a more flexible option for future evolution of the API.</span></span>

<span data-ttu-id="3395e-384">Par exemple, le code F # suivant expose l’API publique à un consommateur c# :</span><span class="sxs-lookup"><span data-stu-id="3395e-384">For example, the following F# code exposes the public API to a C# consumer:</span></span>

<span data-ttu-id="3395e-385">F #:</span><span class="sxs-lookup"><span data-stu-id="3395e-385">F#:</span></span>

```fsharp
[<NoEquality; NoComparison>]
type MyRecord =
    { FirstThing : int
        SecondThing : string }
```

<span data-ttu-id="3395e-386">C# :</span><span class="sxs-lookup"><span data-stu-id="3395e-386">C#:</span></span>

```csharp
public sealed class MyRecord
{
    public MyRecord(int firstThing, string secondThing);
    public int FirstThing { get; }
    public string SecondThing { get; }
}
```

#### <a name="hide-the-representation-of-f-union-types-in-vanilla-net-apis"></a><span data-ttu-id="3395e-387">Masquer la représentation sous forme de types union F # dans vanille API .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-387">Hide the representation of F# union types in vanilla .NET APIs</span></span>

<span data-ttu-id="3395e-388">Types d’union F # ne sont pas utilisés au-delà des limites de composant, même dans F #-à-F # de codage.</span><span class="sxs-lookup"><span data-stu-id="3395e-388">F# union types are not commonly used across component boundaries, even for F#-to-F# coding.</span></span> <span data-ttu-id="3395e-389">Il s’agit d’un appareil de l’implémentation d’un excellent lorsqu’il est utilisé en interne au sein des composants et des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="3395e-389">They are an excellent implementation device when used internally within components and libraries.</span></span>

<span data-ttu-id="3395e-390">Lorsque vous concevez une API .NET vanille, envisagez de le masquer la représentation sous forme d’un type union à l’aide d’une déclaration privée ou un fichier de signature.</span><span class="sxs-lookup"><span data-stu-id="3395e-390">When designing a vanilla .NET API, consider hiding the representation of a union type by using either a private declaration or a signature file.</span></span>

```fsharp
type PropLogic =
    private
    | And of PropLogic * PropLogic
    | Not of PropLogic
    | True
```

<span data-ttu-id="3395e-391">Vous pouvez également augmenter les types qui utilisent une représentation sous forme d’union en interne avec les membres pour fournir un souhaitée. NET avec accès via l’API.</span><span class="sxs-lookup"><span data-stu-id="3395e-391">You may also augment types that use a union representation internally with members to provide a desired .NET-facing API.</span></span>

```fsharp
type PropLogic =
    private
    | And of PropLogic * PropLogic
    | Not of PropLogic
    | True

    /// A public member for use from C#
    member x.Evaluate =
        match x with
        | And(a,b) -> a.Evaluate && b.Evaluate
        | Not a -> not a.Evaluate
        | True -> true

    /// A public member for use from C#
    static member CreateAnd(a,b) = And(a,b)
```

#### <a name="design-gui-and-other-components-using-the-design-patterns-of-the-framework"></a><span data-ttu-id="3395e-392">Conception de l’interface graphique utilisateur et d’autres composants à l’aide de l’infrastructure, les modèles de conception</span><span class="sxs-lookup"><span data-stu-id="3395e-392">Design GUI and other components using the design patterns of the framework</span></span>

<span data-ttu-id="3395e-393">Plusieurs infrastructures de différents sont disponibles dans .NET, tels que Windows Forms, WPF et ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-393">There are many different frameworks available within .NET, such as WinForms, WPF, and ASP.NET.</span></span> <span data-ttu-id="3395e-394">Conventions d’affectation de noms et de conception pour chaque doivent être utilisées si vous concevez des composants pour une utilisation dans ces infrastructures.</span><span class="sxs-lookup"><span data-stu-id="3395e-394">Naming and design conventions for each should be used if you are designing components for use in these frameworks.</span></span> <span data-ttu-id="3395e-395">Par exemple, pour la programmation WPF, adopter les modèles de conception WPF pour les classes que vous créez.</span><span class="sxs-lookup"><span data-stu-id="3395e-395">For example, for WPF programming, adopt WPF design patterns for the classes you are designing.</span></span> <span data-ttu-id="3395e-396">Pour les modèles de programmation de l’interface utilisateur, utilisez les modèles de conception tels que des événements et les collections basées sur les notifications, tels que ceux trouvent dans <xref:System.Collections.ObjectModel>.</span><span class="sxs-lookup"><span data-stu-id="3395e-396">For models in user interface programming, use design patterns such as events and notification-based collections such as those found in <xref:System.Collections.ObjectModel>.</span></span>

### <a name="object-and-member-design-for-libraries-for-use-from-other-net-languages"></a><span data-ttu-id="3395e-397">Conception de membre et d’objet (pour les bibliothèques à utiliser à partir d’autres langages .NET)</span><span class="sxs-lookup"><span data-stu-id="3395e-397">Object and Member design (for libraries for use from other .NET Languages)</span></span>

#### <a name="use-the-clievent-attribute-to-expose-net-events"></a><span data-ttu-id="3395e-398">Utilisez l’attribut CLIEvent pour exposer des événements .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-398">Use the CLIEvent attribute to expose .NET events</span></span>

<span data-ttu-id="3395e-399">Construire un `DelegateEvent` avec .NET spécifique le type qui prend un objet de délégué et `EventArgs` (plutôt qu’une `Event`, qui utilise uniquement la `FSharpHandler` type par défaut) afin que les événements sont publiées dans la façon familier à d’autres langages .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-399">Construct a `DelegateEvent` with a specific .NET delegate type that takes an object and `EventArgs` (rather than an `Event`, which just uses the `FSharpHandler` type by default) so that the events are published in the familiar way to other .NET languages.</span></span>

```fsharp
type MyBadType() =
    let myEv = new Event<int>()

    [<CLIEvent>]
    member this.MyEvent = myEv.Publish

type MyEventArgs(x:int) =
    inherit System.EventArgs()
    member this.X = x

    /// A type in a component designed for use from other .NET languages
type MyGoodType() =
    let myEv = new DelegateEvent<EventHandler<MyEventArgs>>()

    [<CLIEvent>]
    member this.MyEvent = myEv.Publish
```

#### <a name="expose-asynchronous-operations-as-methods-which-return-net-tasks"></a><span data-ttu-id="3395e-400">Exposer des opérations asynchrones en tant que méthodes qui retournent des tâches de .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-400">Expose asynchronous operations as methods which return .NET tasks</span></span>

<span data-ttu-id="3395e-401">Tâches permettent de représenter les calculs asynchrones dans .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-401">Tasks are used in .NET to represent active asynchronous computations.</span></span> <span data-ttu-id="3395e-402">Les tâches sont en général moins composition que F # `Async<T>` car ils représentent les tâches « exécute déjà » et ne peut pas être un ensemble composés de façon qui effectuer une composition parallèle, ou qui masquer la propagation des signaux d’annulation et d’autres objets paramètres contextuelles.</span><span class="sxs-lookup"><span data-stu-id="3395e-402">Tasks are in general less compositional than F# `Async<T>` objects, since they represent “already executing” tasks and can’t be composed together in ways that perform parallel composition, or which hide the propagation of cancellation signals and other contextual parameters.</span></span>

<span data-ttu-id="3395e-403">Toutefois, en dépit de cela, les méthodes qui retournent des tâches sont la représentation standard de la programmation asynchrone sur .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-403">However, despite this, methods which return Tasks are the standard representation of asynchronous programming on .NET.</span></span>

```fsharp
/// A type in a component designed for use from other .NET languages
type MyType() =

    let compute (x: int) : Async<int> = async { ... }

    member this.ComputeAsync(x) = compute x |> Async.StartAsTask
```

<span data-ttu-id="3395e-404">Vous allez souvent que vous souhaitez également accepter un jeton d’annulation explicite :</span><span class="sxs-lookup"><span data-stu-id="3395e-404">You will frequently also want to accept an explicit cancellation token:</span></span>

```fsharp
/// A type in a component designed for use from other .NET languages
type MyType() =
    let compute(x:int) : Async<int> = async { ... }
    member this.ComputeAsTask(x, cancellationToken) = Async.StartAsTask(compute x, cancellationToken)
```

#### <a name="use-net-delegate-types-instead-of-f-function-types"></a><span data-ttu-id="3395e-405">Utiliser des types de délégués de .NET au lieu de types de fonction) (F #</span><span class="sxs-lookup"><span data-stu-id="3395e-405">Use .NET delegate types instead of F# function types</span></span>

<span data-ttu-id="3395e-406">Ici « types de fonction) (F # » signifie que les types « direction » comme `int -> int`.</span><span class="sxs-lookup"><span data-stu-id="3395e-406">Here “F# function types” mean “arrow” types like `int -> int`.</span></span>

<span data-ttu-id="3395e-407">Au lieu de cela :</span><span class="sxs-lookup"><span data-stu-id="3395e-407">Instead of this:</span></span>

```fsharp
member this.Transform(f:int->int) =
    ...
```

<span data-ttu-id="3395e-408">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3395e-408">Do this:</span></span>

```fsharp
member this.Transform(f:Func<int,int>) =
    ...
```

<span data-ttu-id="3395e-409">Le type de fonction F # apparaît sous la forme `class FSharpFunc<T,U>` à d’autres langages .NET et est moins adapté pour les fonctionnalités de langage et les outils qui comprennent les types délégués.</span><span class="sxs-lookup"><span data-stu-id="3395e-409">The F# function type appears as `class FSharpFunc<T,U>` to other .NET languages, and is less suitable for language features and tooling that understand delegate types.</span></span> <span data-ttu-id="3395e-410">Lors de la création d’une méthode d’ordre supérieur ciblant .NET Framework 3.5 ou version ultérieure, le `System.Func` et `System.Action` les délégués sont les API de droite à publier pour permettre aux développeurs de .NET utiliser ces API selon des problèmes.</span><span class="sxs-lookup"><span data-stu-id="3395e-410">When authoring a higher-order method targeting .NET Framework 3.5 or higher, the `System.Func` and `System.Action` delegates are the right APIs to publish to enable .NET developers to consume these APIs in a low-friction manner.</span></span> <span data-ttu-id="3395e-411">(Lorsque vous ciblez .NET Framework 2.0, les types définis par le système de délégués sont plus limitées, envisagez d’utiliser des types de délégué prédéfinis, tels que `System.Converter<T,U>` ou de la définition d’un type délégué spécifique.)</span><span class="sxs-lookup"><span data-stu-id="3395e-411">(When targeting .NET Framework 2.0, the system-defined delegate types are more limited; consider using predefined delegate types such as `System.Converter<T,U>` or defining a specific delegate type.)</span></span>

<span data-ttu-id="3395e-412">Sur l’autre côté, les délégués .NET ne sont pas naturelles pour F #-faisant face à des bibliothèques (consultez la Section suivante sur F #-faisant face à des bibliothèques).</span><span class="sxs-lookup"><span data-stu-id="3395e-412">On the flip side, .NET delegates are not natural for F#-facing libraries (see the next Section on F#-facing libraries).</span></span> <span data-ttu-id="3395e-413">Par conséquent, une stratégie de mise en œuvre courants lors du développement des méthodes d’ordre supérieur pour les bibliothèques .NET vanille va créer toutes l’implémentation à l’aide des types de fonction) (F # et puis créer l’API publique de l’utilisation de délégués comme façade dynamique au-dessus réel F # mise en œuvre.</span><span class="sxs-lookup"><span data-stu-id="3395e-413">As a result, a common implementation strategy when developing higher-order methods for vanilla .NET libraries is to author all the implementation using F# function types, and then create the public API using delegates as a thin façade atop the actual F# implementation.</span></span>

#### <a name="use-the-trygetvalue-pattern-instead-of-returning-f-option-values-and-prefer-method-overloading-to-taking-f-option-values-as-arguments"></a><span data-ttu-id="3395e-414">Utilisez le modèle TryGetValue au lieu de retourner des valeurs d’option F #, préférez la surcharge de méthode à effectuer des valeurs d’option F # en tant qu’arguments</span><span class="sxs-lookup"><span data-stu-id="3395e-414">Use the TryGetValue pattern instead of returning F# option values, and prefer method overloading to taking F# option values as arguments</span></span>

<span data-ttu-id="3395e-415">Modèles courants d’utilisation pour le type d’option F # dans les API sont mieux implémenté dans vanille techniques de création des API .NET à l’aide de .NET standard.</span><span class="sxs-lookup"><span data-stu-id="3395e-415">Common patterns of use for the F# option type in APIs are better implemented in vanilla .NET APIs using standard .NET design techniques.</span></span> <span data-ttu-id="3395e-416">Au lieu de retourner une valeur d’option F #, envisagez d’utiliser le type de retour bool plus un paramètre de sortie comme dans le modèle « TryGetValue ».</span><span class="sxs-lookup"><span data-stu-id="3395e-416">Instead of returning an F# option value, consider using the bool return type plus an out parameter as in the "TryGetValue" pattern.</span></span> <span data-ttu-id="3395e-417">Et plutôt qu’à partir des valeurs d’option F # en tant que paramètres, envisagez d’utiliser la surcharge de méthode ou les arguments facultatifs.</span><span class="sxs-lookup"><span data-stu-id="3395e-417">And instead of taking F# option values as parameters, consider using method overloading or optional arguments.</span></span>

```fsharp
member this.ReturnOption() = Some 3

member this.ReturnBoolAndOut(outVal : byref<int>) =
    outVal <- 3
    true

member this.ParamOption(x : int, y : int option) =
    match y with
    | Some y2 -> x + y2
    | None -> x

member this.ParamOverload(x : int) = x

member this.ParamOverload(x : int, y : int) = x + y
```

#### <a name="use-the-net-collection-interface-types-ienumerablet-and-idictionarykeyvalue-for-parameters-and-return-values"></a><span data-ttu-id="3395e-418">Utilisez l’interface de collection .NET types IEnumerable\<T\> et IDictionary\<de clé, la valeur\> pour les paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3395e-418">Use the .NET collection interface types IEnumerable\<T\> and IDictionary\<Key,Value\> for parameters and return values</span></span>

<span data-ttu-id="3395e-419">Évitez d’utiliser des types de collection concrets tels que les tableaux de .NET `T[]`, types F # `list<T>`, `Map<Key,Value>` et `Set<T>`, et les types de collection concrète .NET tels que `Dictionary<Key,Value>`.</span><span class="sxs-lookup"><span data-stu-id="3395e-419">Avoid the use of concrete collection types such as .NET arrays `T[]`, F# types `list<T>`, `Map<Key,Value>` and `Set<T>`, and .NET concrete collection types such as `Dictionary<Key,Value>`.</span></span> <span data-ttu-id="3395e-420">Les règles de conception de bibliothèque .NET ont bon conseil savoir à quel moment utiliser différents types de collection comme `IEnumerable<T>`.</span><span class="sxs-lookup"><span data-stu-id="3395e-420">The .NET Library Design Guidelines have good advice regarding when to use various collection types like `IEnumerable<T>`.</span></span> <span data-ttu-id="3395e-421">Une utilisation de tableaux (`T[]`) est acceptable dans certains cas, pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="3395e-421">Some use of arrays (`T[]`) is acceptable in some circumstances, on performance grounds.</span></span> <span data-ttu-id="3395e-422">Notez en particulier que `seq<T>` est simplement le F # alias pour `IEnumerable<T>`, et seq est donc souvent un type approprié pour une API .NET vanille.</span><span class="sxs-lookup"><span data-stu-id="3395e-422">Note especially that `seq<T>` is just the F# alias for `IEnumerable<T>`, and thus seq is often an appropriate type for a vanilla .NET API.</span></span>

<span data-ttu-id="3395e-423">À la place de F # répertorie :</span><span class="sxs-lookup"><span data-stu-id="3395e-423">Instead of F# lists:</span></span>

```fsharp
member this.PrintNames(names : string list) =
    ...
```

<span data-ttu-id="3395e-424">Utiliser des séquences de F # :</span><span class="sxs-lookup"><span data-stu-id="3395e-424">Use F# sequences:</span></span>

```fsharp
member this.PrintNames(names : seq<string>) =
    ...
```

#### <a name="use-the-unit-type-as-the-only-input-type-of-a-method-to-define-a-zero-argument-method-or-as-the-only-return-type-to-define-a-void-returning-method"></a><span data-ttu-id="3395e-425">Le type d’unité en tant que le seul type d’entrée d’une méthode pour définir une méthode sans argument, ou en tant que le seul type pour définir une méthode retournant void</span><span class="sxs-lookup"><span data-stu-id="3395e-425">Use the unit type as the only input type of a method to define a zero-argument method, or as the only return type to define a void-returning method</span></span>

<span data-ttu-id="3395e-426">Évitez d’autres utilisations du type d’unité.</span><span class="sxs-lookup"><span data-stu-id="3395e-426">Avoid other uses of the unit type.</span></span> <span data-ttu-id="3395e-427">Voici une bonne :</span><span class="sxs-lookup"><span data-stu-id="3395e-427">These are good:</span></span>

```fsharp
✔ member this.NoArguments() = 3

✔ member this.ReturnVoid(x : int) = ()
```

<span data-ttu-id="3395e-428">Cela est incorrect :</span><span class="sxs-lookup"><span data-stu-id="3395e-428">This is bad:</span></span>

```fsharp
member this.WrongUnit( x:unit, z:int) = ((), ())
```

#### <a name="check-for-null-values-on-vanilla-net-api-boundaries"></a><span data-ttu-id="3395e-429">Vérifier les valeurs null sur les limites de l’API .NET vanille</span><span class="sxs-lookup"><span data-stu-id="3395e-429">Check for null values on vanilla .NET API boundaries</span></span>

<span data-ttu-id="3395e-430">Code d’implémentation F # a tendance à avoir moins de valeurs null, en raison de restrictions sur l’utilisation de littéraux null pour des types F # et les modèles de conception immuable.</span><span class="sxs-lookup"><span data-stu-id="3395e-430">F# implementation code tends to have fewer null values, due to immutable design patterns and restrictions on use of null literals for F# types.</span></span> <span data-ttu-id="3395e-431">Autres langages .NET utilisent souvent null en tant que valeur beaucoup plus fréquemment.</span><span class="sxs-lookup"><span data-stu-id="3395e-431">Other .NET languages often use null as a value much more frequently.</span></span> <span data-ttu-id="3395e-432">Pour cette raison, code F # qui expose une API .NET vanille doit vérifier les paramètres pour la valeur null à la limite de l’API et empêche que ces valeurs transférée plus approfondie dans le code d’implémentation F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-432">Because of this, F# code that is exposing a vanilla .NET API should check parameters for null at the API boundary, and prevent these values from flowing deeper into the F# implementation code.</span></span> <span data-ttu-id="3395e-433">Le `isNull` fonction ou critères spéciaux sur les `null` modèle peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="3395e-433">The `isNull` function or pattern matching on the `null` pattern can be used.</span></span>

```fsharp
let checkNonNull argName (arg: obj) =
    match arg with
    | null -> nullArg argName
    | _ -> ()

let checkNonNull` argName (arg: obj) =
    if isNull arg then nullArg argName
    else ()
```

#### <a name="avoid-using-tuples-as-return-values"></a><span data-ttu-id="3395e-434">Évitez d’utiliser des tuples comme valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3395e-434">Avoid using tuples as return values</span></span>

<span data-ttu-id="3395e-435">Au lieu de cela, préférez retournant un type nommé contenant les données d’agrégation, ou à l’aide des paramètres de sortie pour retourner plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="3395e-435">Instead, prefer returning a named type holding the aggregate data, or using out parameters to return multiple values.</span></span> <span data-ttu-id="3395e-436">Bien que les tuples et les tuples du struct existent dans .NET (y compris c# prise en charge linguistique pour les tuples du struct), ils vont souvent pas fournir l’API idéale et attendu pour les développeurs .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-436">Although tuples and struct tuples exist in .NET (including C# language support for struct tuples), they will most often not provide the ideal and expected API for .NET developers.</span></span>

#### <a name="avoid-the-use-of-currying-of-parameters"></a><span data-ttu-id="3395e-437">Évitez d’utiliser curryfication de paramètres</span><span class="sxs-lookup"><span data-stu-id="3395e-437">Avoid the use of currying of parameters</span></span>

<span data-ttu-id="3395e-438">Au lieu de cela, utilisez les conventions d’appel de .NET ``Method(arg1,arg2,…,argN)``.</span><span class="sxs-lookup"><span data-stu-id="3395e-438">Instead, use .NET calling conventions ``Method(arg1,arg2,…,argN)``.</span></span>

```fsharp
member this.TupledArguments(str, num) = String.replicate num str
```

<span data-ttu-id="3395e-439">Conseil : Si vous concevez des bibliothèques pour une utilisation à partir de n’importe quel langage .NET, puis il est ne remplace en fait certains expérimentale Visual c# et Visual Basic de programmation pour vous assurer que vos bibliothèques « convivialité droite » à partir de ces langues.</span><span class="sxs-lookup"><span data-stu-id="3395e-439">Tip: If you’re designing libraries for use from any .NET language, then there’s no substitute for actually doing some experimental C# and Visual Basic programming to ensure that your libraries "feel right" from these languages.</span></span> <span data-ttu-id="3395e-440">Vous pouvez également utiliser des outils tels que .NET Reflector et l’Explorateur d’objets Visual Studio pour vous assurer que les bibliothèques et leur documentation apparaissent comme prévu pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="3395e-440">You can also use tools such as .NET Reflector and the Visual Studio Object Browser to ensure that libraries and their documentation appear as expected to developers.</span></span>

## <a name="appendix"></a><span data-ttu-id="3395e-441">Annexe</span><span class="sxs-lookup"><span data-stu-id="3395e-441">Appendix</span></span>

### <a name="end-to-end-example-of-designing-f-code-for-use-by-other-net-languages"></a><span data-ttu-id="3395e-442">Exemple de bout en bout de la conception de code F # pour une utilisation par d’autres langages .NET</span><span class="sxs-lookup"><span data-stu-id="3395e-442">End-to-end example of designing F# code for use by other .NET languages</span></span>

<span data-ttu-id="3395e-443">Considérons la classe suivante :</span><span class="sxs-lookup"><span data-stu-id="3395e-443">Consider the following class:</span></span>

```fsharp
open System

type Point1(angle,radius) =
    new() = Point1(angle=0.0, radius=0.0)
    member x.Angle = angle
    member x.Radius = radius
    member x.Stretch(l) = Point1(angle=x.Angle, radius=x.Radius * l)
    member x.Warp(f) = Point1(angle=f(x.Angle), radius=x.Radius)
    static member Circle(n) =
        [ for i in 1..n -> Point1(angle=2.0*Math.PI/float(n), radius=1.0) ]
```

<span data-ttu-id="3395e-444">Le type déduit F # de cette classe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3395e-444">The inferred F# type of this class is as follows:</span></span>

```fsharp
type Point1 =
    new : unit -> Point1
    new : angle:double * radius:double -> Point1
    static member Circle : n:int -> Point1 list
    member Stretch : l:double -> Point1
    member Warp : f:(double -> double) -> Point1
    member Angle : double
    member Radius : double
```

<span data-ttu-id="3395e-445">Jetons un œil à la façon dont ce type) (F # s’affiche pour un programmeur à l’aide d’un autre langage .NET.</span><span class="sxs-lookup"><span data-stu-id="3395e-445">Let’s take a look at how this F# type appears to a programmer using another .NET language.</span></span> <span data-ttu-id="3395e-446">Par exemple, approximatif c# « signature » est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3395e-446">For example, the approximate C# “signature” is as follows:</span></span>

```csharp
// C# signature for the unadjusted Point1 class
public class Point1
{
    public Point1();

    public Point1(double angle, double radius);

    public static Microsoft.FSharp.Collections.List<Point1> Circle(int count);

    public Point1 Stretch(double factor);

    public Point1 Warp(Microsoft.FSharp.Core.FastFunc<double,double> transform);

    public double Angle { get; }

    public double Radius { get; }
}
```

<span data-ttu-id="3395e-447">Il existe quelques points importants à noter sur comment F # représente les constructions ici.</span><span class="sxs-lookup"><span data-stu-id="3395e-447">There are some important points to notice about how F# represents constructs here.</span></span> <span data-ttu-id="3395e-448">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3395e-448">For example:</span></span>

* <span data-ttu-id="3395e-449">Métadonnées telles que les noms d’arguments a été conservée.</span><span class="sxs-lookup"><span data-stu-id="3395e-449">Metadata such as argument names has been preserved.</span></span>

* <span data-ttu-id="3395e-450">Les méthodes F # qui prennent deux arguments sont les méthodes c# qui prennent deux arguments.</span><span class="sxs-lookup"><span data-stu-id="3395e-450">F# methods that take two arguments become C# methods that take two arguments.</span></span>

* <span data-ttu-id="3395e-451">Fonctions et des listes deviennent des références à des types correspondants dans la bibliothèque F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-451">Functions and lists become references to corresponding types in the F# library.</span></span>

<span data-ttu-id="3395e-452">Le code suivant montre comment ajuster le code pour tenir compte de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="3395e-452">The following code shows how to adjust this code to take these things into account.</span></span>

```fsharp
namespace SuperDuperFSharpLibrary.Types

type RadialPoint(angle:double, radius:double) =

    /// Return a point at the origin
    new() = RadialPoint(angle=0.0, radius=0.0)

    /// The angle to the point, from the x-axis
    member x.Angle = angle

    /// The distance to the point, from the origin
    member x.Radius = radius

    /// Return a new point, with radius multiplied by the given factor
    member x.Stretch(factor) =
        RadialPoint(angle=angle, radius=radius * factor)

    /// Return a new point, with angle transformed by the function
    member x.Warp(transform:Func<_,_>) =
        RadialPoint(angle=transform.Invoke angle, radius=radius)

    /// Return a sequence of points describing an approximate circle using
    /// the given count of points
    static member Circle(count) =
        seq { for i in 1..count ->
                RadialPoint(angle=2.0*Math.PI/float(count), radius=1.0) }
```

<span data-ttu-id="3395e-453">Le type) (F # déduit du code est la suivante :</span><span class="sxs-lookup"><span data-stu-id="3395e-453">The inferred F# type of the code is as follows:</span></span>

```fsharp
type RadialPoint =
    new : unit -> RadialPoint
    new : angle:double * radius:double -> RadialPoint
    static member Circle : count:int -> seq<RadialPoint>
    member Stretch : factor:double -> RadialPoint
    member Warp : transform:System.Func<double,double> -> RadialPoint
    member Angle : double
    member Radius : double
```

<span data-ttu-id="3395e-454">La signature c# est désormais comme suit :</span><span class="sxs-lookup"><span data-stu-id="3395e-454">The C# signature is now as follows:</span></span>

```csharp
public class RadialPoint
{
    public RadialPoint();

    public RadialPoint(double angle, double radius);

    public static System.Collections.Generic.IEnumerable<RadialPoint> Circle(int count);

    public RadialPoint Stretch(double factor);

    public RadialPoint Warp(System.Func<double,double> transform);

    public double Angle { get; }

    public double Radius { get; }
}
```

<span data-ttu-id="3395e-455">Les corrections apportées pour préparer ce type à utiliser comme partie d’une bibliothèque .NET vanille sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="3395e-455">The fixes made to prepare this type for use as part of a vanilla .NET library are as follows:</span></span>

* <span data-ttu-id="3395e-456">Ajustée plusieurs noms : `Point1`, `n`, `l`, et `f` est devenu `RadialPoint`, `count`, `factor`, et `transform`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="3395e-456">Adjusted several names: `Point1`, `n`, `l`, and `f` became `RadialPoint`, `count`, `factor`, and `transform`, respectively.</span></span>

* <span data-ttu-id="3395e-457">Utiliser un type de retour de `seq<RadialPoint>` au lieu de `RadialPoint list` en modifiant une construction de la liste à l’aide `[ ... ]` une à l’aide de la construction de séquence `IEnumerable<RadialPoint>`.</span><span class="sxs-lookup"><span data-stu-id="3395e-457">Used a return type of `seq<RadialPoint>` instead of `RadialPoint list` by changing a list construction using `[ ... ]` to a sequence construction using `IEnumerable<RadialPoint>`.</span></span>

* <span data-ttu-id="3395e-458">Utiliser le type de délégué .NET `System.Func` au lieu d’un type de fonction F #.</span><span class="sxs-lookup"><span data-stu-id="3395e-458">Used the .NET delegate type `System.Func` instead of an F# function type.</span></span>

<span data-ttu-id="3395e-459">Il est ainsi beaucoup mieux à utiliser dans le code c#.</span><span class="sxs-lookup"><span data-stu-id="3395e-459">This makes it far nicer to consume in C# code.</span></span>
