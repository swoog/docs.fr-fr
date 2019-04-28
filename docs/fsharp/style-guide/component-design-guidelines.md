---
title: F#instructions de conception de composant
description: Découvrez les instructions pour l’écriture F# composants destinée à la consommation par les autres appelants.
ms.date: 05/14/2018
ms.openlocfilehash: c61e4cd9098388b356c71c325d66c760fa866cf0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61902159"
---
# <a name="f-component-design-guidelines"></a><span data-ttu-id="23431-103">F#instructions de conception de composant</span><span class="sxs-lookup"><span data-stu-id="23431-103">F# component design guidelines</span></span>

<span data-ttu-id="23431-104">Ce document est un ensemble de règles de conception de composant pour F# de programmation, selon le F# les instructions de conception de composant, v14, Microsoft Research, et [une autre version](https://fsharp.org/specs/component-design-guidelines/) à l’origine organisé et géré par le F# Software Foundation.</span><span class="sxs-lookup"><span data-stu-id="23431-104">This document is a set of component design guidelines for F# programming, based on the F# Component Design Guidelines, v14, Microsoft Research, and [another version](https://fsharp.org/specs/component-design-guidelines/) originally curated and maintained by the F# Software Foundation.</span></span>

<span data-ttu-id="23431-105">Ce document suppose que vous êtes familiarisé avec F# de programmation.</span><span class="sxs-lookup"><span data-stu-id="23431-105">This document assumes you are familiar with F# programming.</span></span> <span data-ttu-id="23431-106">Plusieurs grâce à la F# Communauté pour obtenir des commentaires utiles sur différentes versions de ce guide et leurs contributions.</span><span class="sxs-lookup"><span data-stu-id="23431-106">Many thanks to the F# community for their contributions and helpful feedback on various versions of this guide.</span></span>

## <a name="overview"></a><span data-ttu-id="23431-107">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="23431-107">Overview</span></span>

<span data-ttu-id="23431-108">Ce document présente certains des problèmes liés à F# conception de composant et de codage.</span><span class="sxs-lookup"><span data-stu-id="23431-108">This document looks at some of the issues related to F# component design and coding.</span></span> <span data-ttu-id="23431-109">Un composant peut signifier que les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="23431-109">A component can mean any of the following:</span></span>

* <span data-ttu-id="23431-110">Une couche dans votre F# projet qui a des consommateurs externes dans ce projet.</span><span class="sxs-lookup"><span data-stu-id="23431-110">A layer in your F# project that has external consumers within that project.</span></span>
* <span data-ttu-id="23431-111">Une bibliothèque destinée à la consommation par F# code entre les limites de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="23431-111">A library intended for consumption by F# code across assembly boundaries.</span></span>
* <span data-ttu-id="23431-112">Une bibliothèque destinée à la consommation par n’importe quel langage .NET entre les limites de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="23431-112">A library intended for consumption by any .NET language across assembly boundaries.</span></span>
* <span data-ttu-id="23431-113">Une bibliothèque prévue pour une distribution via un dépôt de packages, tels que [NuGet](https://nuget.org).</span><span class="sxs-lookup"><span data-stu-id="23431-113">A library intended for distribution via a package repository, such as [NuGet](https://nuget.org).</span></span>

<span data-ttu-id="23431-114">Suivent des techniques décrites dans cet article le [cinq principes bonne F# code](index.md#five-principles-of-good-f-code)et par conséquent utiliser à la fois fonctionnels et de l’objet de programmation comme il convient.</span><span class="sxs-lookup"><span data-stu-id="23431-114">Techniques described in this article follow the [Five principles of good F# code](index.md#five-principles-of-good-f-code), and thus utilize both functional and object programming as appropriate.</span></span>

<span data-ttu-id="23431-115">Quelle que soit la méthodologie, le Concepteur de composant et de bibliothèque est confronté à un nombre de problèmes pratiques et prosaïques lorsque vous tentez de créer une API qui n’est plus facilement utilisable par les développeurs.</span><span class="sxs-lookup"><span data-stu-id="23431-115">Regardless of the methodology, the component and library designer faces a number of practical and prosaic issues when trying to craft an API that is most easily usable by developers.</span></span> <span data-ttu-id="23431-116">Consciencieux application de la [directives de conception de bibliothèque .NET](../../standard/design-guidelines/index.md) sera vous diriger vers la création d’un ensemble cohérent d’API qui sont agréables à utiliser.</span><span class="sxs-lookup"><span data-stu-id="23431-116">Conscientious application of the [.NET Library Design Guidelines](../../standard/design-guidelines/index.md) will steer you towards creating a consistent set of APIs that are pleasant to consume.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="23431-117">Indications générales</span><span class="sxs-lookup"><span data-stu-id="23431-117">General guidelines</span></span>

<span data-ttu-id="23431-118">Il existe quelques instructions universelles qui s’appliquent à F# bibliothèques, quel que soit le public concerné par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="23431-118">There are a few universal guidelines that apply to F# libraries, regardless of the intended audience for the library.</span></span>

### <a name="learn-the-net-library-design-guidelines"></a><span data-ttu-id="23431-119">Découvrez les instructions de conception de bibliothèque .NET</span><span class="sxs-lookup"><span data-stu-id="23431-119">Learn the .NET Library Design Guidelines</span></span>

<span data-ttu-id="23431-120">Quel que soit le type de F# codage vous effectuez, il est intéressant d’avoir une connaissance pratique de la [directives de conception de bibliothèque .NET](../../standard/design-guidelines/index.md).</span><span class="sxs-lookup"><span data-stu-id="23431-120">Regardless of the kind of F# coding you are doing, it is valuable to have a working knowledge of the [.NET Library Design Guidelines](../../standard/design-guidelines/index.md).</span></span> <span data-ttu-id="23431-121">La plupart des autres F# et les programmeurs .NET seront connaissance de ces instructions et attendre le code .NET pour y conforment.</span><span class="sxs-lookup"><span data-stu-id="23431-121">Most other F# and .NET programmers will be familiar with these guidelines, and expect .NET code to conform to them.</span></span>

<span data-ttu-id="23431-122">Les règles de conception de bibliothèque .NET fournissent des recommandations générales concernant d’affectation de noms, la conception des classes et interfaces, conception de membres (propriétés, méthodes, événements, etc.) et bien plus encore et sont utile premier point de référence pour un large éventail de guide de conception.</span><span class="sxs-lookup"><span data-stu-id="23431-122">The .NET Library Design Guidelines provide general guidance regarding naming, designing classes and interfaces, member design (properties, methods, events, etc.) and more, and are a useful first point of reference for a variety of design guidance.</span></span>

### <a name="add-xml-documentation-comments-to-your-code"></a><span data-ttu-id="23431-123">Ajouter des commentaires de documentation XML à votre code</span><span class="sxs-lookup"><span data-stu-id="23431-123">Add XML documentation comments to your code</span></span>

<span data-ttu-id="23431-124">Documentation XML sur les API publiques vous assurer que les utilisateurs peuvent obtenir excellent Intellisense et les Infosrapides lors de la bibliothèque à l’aide de ces types et membres et activer génération de documentation de fichiers.</span><span class="sxs-lookup"><span data-stu-id="23431-124">XML documentation on public APIs ensure that users can get great Intellisense and Quickinfo when using these types and members, and enable building documentation files for the library.</span></span> <span data-ttu-id="23431-125">Consultez le [Documentation XML](../language-reference/xml-documentation.md) sur différentes balises xml qui peuvent être utilisées pour le balisage supplémentaire dans les commentaires de xmldoc.</span><span class="sxs-lookup"><span data-stu-id="23431-125">See the [XML Documentation](../language-reference/xml-documentation.md) about various xml tags that can be used for additional markup within xmldoc comments.</span></span>

```fsharp
/// A class for representing (x,y) coordinates
type Point =

    /// Computes the distance between this point and another
    member DistanceTo: otherPoint:Point -> float
```

<span data-ttu-id="23431-126">Vous pouvez utiliser des commentaires XML forme abrégée (`/// comment`), ou des commentaires XML standards (`///<summary>comment</summary>`).</span><span class="sxs-lookup"><span data-stu-id="23431-126">You can use either the short form XML comments (`/// comment`), or standard XML comments (`///<summary>comment</summary>`).</span></span>

### <a name="consider-using-explicit-signature-files-fsi-for-stable-library-and-component-apis"></a><span data-ttu-id="23431-127">Envisagez d’utiliser des fichiers explicite de signature (.fsi) pour la bibliothèque stable et API de composant</span><span class="sxs-lookup"><span data-stu-id="23431-127">Consider using explicit signature files (.fsi) for stable library and component APIs</span></span>

<span data-ttu-id="23431-128">À l’aide de fichiers de signatures explicite dans un F# bibliothèque fournit un résumé succinct des API publique, ce qui les deux permet de se pour assurer que vous connaissez le public complet surface de votre bibliothèque fournit une séparation nette entre la documentation publique et interne détails d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="23431-128">Using explicit signatures files in an F# library provides a succinct summary of public API, which both helps to ensure that you know the full public surface of your library, as well as provides a clean separation between public documentation and internal implementation details.</span></span> <span data-ttu-id="23431-129">Notez que les fichiers de signature ajoutent friction à l’évolution de l’API publique, en demandant des modifications doit être faite dans l’implémentation et la signature des fichiers.</span><span class="sxs-lookup"><span data-stu-id="23431-129">Note that signature files add friction to changing the public API, by requiring changes to be made in both the implementation and signature files.</span></span> <span data-ttu-id="23431-130">Par conséquent, les fichiers de signature doivent généralement uniquement être introduites lorsqu’une API deviennent solidification et est censée ne plus changer de manière significative.</span><span class="sxs-lookup"><span data-stu-id="23431-130">As a result, signature files should typically only be introduced when an API has become solidified and is no longer expected to change significantly.</span></span>

### <a name="always-follow-best-practices-for-using-strings-in-net"></a><span data-ttu-id="23431-131">Suivez toujours les meilleures pratiques pour l’utilisation de chaînes dans .NET</span><span class="sxs-lookup"><span data-stu-id="23431-131">Always follow best practices for using strings in .NET</span></span>

<span data-ttu-id="23431-132">Suivez [meilleures pratiques pour l’utilisation de chaînes dans .NET](../../standard/base-types/best-practices-strings.md) conseils.</span><span class="sxs-lookup"><span data-stu-id="23431-132">Follow [Best Practices for Using Strings in .NET](../../standard/base-types/best-practices-strings.md) guidance.</span></span> <span data-ttu-id="23431-133">En particulier, l’état toujours explicitement *intention culturelle* dans la conversion et la comparaison de chaînes (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="23431-133">In particular, always explicitly state *cultural intent* in the conversion and comparison of strings (where applicable).</span></span>

## <a name="guidelines-for-f-facing-libraries"></a><span data-ttu-id="23431-134">Instructions pour F#-accessible sur les bibliothèques</span><span class="sxs-lookup"><span data-stu-id="23431-134">Guidelines for F#-facing libraries</span></span>

<span data-ttu-id="23431-135">Cette section présente des recommandations pour le développement publique F#-accessible sur les bibliothèques ; Autrement dit, les bibliothèques exposant les API publiques qui sont destinés à être consommés par F# les développeurs.</span><span class="sxs-lookup"><span data-stu-id="23431-135">This section presents recommendations for developing public F#-facing libraries; that is, libraries exposing public APIs that are intended to be consumed by F# developers.</span></span> <span data-ttu-id="23431-136">Il existe une variété de recommandations sur la conception de la bibliothèque s’applique spécifiquement à F#.</span><span class="sxs-lookup"><span data-stu-id="23431-136">There are a variety of library-design recommendations applicable specifically to F#.</span></span> <span data-ttu-id="23431-137">En l’absence des recommandations spécifiques qui suivent, les règles de conception de bibliothèque .NET sont les instructions de secours.</span><span class="sxs-lookup"><span data-stu-id="23431-137">In the absence of the specific recommendations that follow, the .NET Library Design Guidelines are the fallback guidance.</span></span>

### <a name="naming-conventions"></a><span data-ttu-id="23431-138">Conventions d'attribution d'un nom</span><span class="sxs-lookup"><span data-stu-id="23431-138">Naming conventions</span></span>

#### <a name="use-net-naming-and-capitalization-conventions"></a><span data-ttu-id="23431-139">Utiliser les conventions d’affectation de noms et de mise en majuscules de .NET</span><span class="sxs-lookup"><span data-stu-id="23431-139">Use .NET naming and capitalization conventions</span></span>

<span data-ttu-id="23431-140">Le tableau suivant respecte les conventions d’affectation de noms et de mise en majuscules de .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-140">The following table follows .NET naming and capitalization conventions.</span></span> <span data-ttu-id="23431-141">Petite ajouts pour inclure également les F# construit.</span><span class="sxs-lookup"><span data-stu-id="23431-141">There are small additions to also include F# constructs.</span></span>

| <span data-ttu-id="23431-142">Construction</span><span class="sxs-lookup"><span data-stu-id="23431-142">Construct</span></span> | <span data-ttu-id="23431-143">Case</span><span class="sxs-lookup"><span data-stu-id="23431-143">Case</span></span> | <span data-ttu-id="23431-144">Élément</span><span class="sxs-lookup"><span data-stu-id="23431-144">Part</span></span> | <span data-ttu-id="23431-145">Exemples</span><span class="sxs-lookup"><span data-stu-id="23431-145">Examples</span></span> | <span data-ttu-id="23431-146">Notes</span><span class="sxs-lookup"><span data-stu-id="23431-146">Notes</span></span> |
|-----------|------|------|----------|-------|
| <span data-ttu-id="23431-147">Types concrets</span><span class="sxs-lookup"><span data-stu-id="23431-147">Concrete types</span></span> | <span data-ttu-id="23431-148">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-148">PascalCase</span></span> | <span data-ttu-id="23431-149">Nom / adjectif</span><span class="sxs-lookup"><span data-stu-id="23431-149">Noun/ adjective</span></span> | <span data-ttu-id="23431-150">La liste, Double, complexe</span><span class="sxs-lookup"><span data-stu-id="23431-150">List, Double, Complex</span></span> | <span data-ttu-id="23431-151">Types concrets sont des structs, des classes, des énumérations, des délégués, des enregistrements et des unions.</span><span class="sxs-lookup"><span data-stu-id="23431-151">Concrete types are structs, classes, enumerations, delegates, records, and unions.</span></span> <span data-ttu-id="23431-152">Bien que les noms de types sont traditionnellement en minuscules dans OCaml, F# a adopté le schéma d’affectation de noms .NET pour les types.</span><span class="sxs-lookup"><span data-stu-id="23431-152">Though type names are traditionally lowercase in OCaml, F# has adopted the .NET naming scheme for types.</span></span>
| <span data-ttu-id="23431-153">DLL</span><span class="sxs-lookup"><span data-stu-id="23431-153">DLLs</span></span>           | <span data-ttu-id="23431-154">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-154">PascalCase</span></span> |                 | <span data-ttu-id="23431-155">Fabrikam.Core.dll</span><span class="sxs-lookup"><span data-stu-id="23431-155">Fabrikam.Core.dll</span></span> |  |
| <span data-ttu-id="23431-156">Balises Union</span><span class="sxs-lookup"><span data-stu-id="23431-156">Union tags</span></span>     | <span data-ttu-id="23431-157">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-157">PascalCase</span></span> | <span data-ttu-id="23431-158">Nom</span><span class="sxs-lookup"><span data-stu-id="23431-158">Noun</span></span> | <span data-ttu-id="23431-159">Certains, ajouter, réussite</span><span class="sxs-lookup"><span data-stu-id="23431-159">Some, Add, Success</span></span> | <span data-ttu-id="23431-160">N’utilisez pas de préfixe dans les API publiques.</span><span class="sxs-lookup"><span data-stu-id="23431-160">Do not use a prefix in public APIs.</span></span> <span data-ttu-id="23431-161">Si vous le souhaitez utiliser un préfixe lorsque internes, tels que `type Teams = TAlpha | TBeta | TDelta.`</span><span class="sxs-lookup"><span data-stu-id="23431-161">Optionally use a prefix when internal, such as `type Teams = TAlpha | TBeta | TDelta.`</span></span> |
| <span data-ttu-id="23431-162">Événement</span><span class="sxs-lookup"><span data-stu-id="23431-162">Event</span></span>          | <span data-ttu-id="23431-163">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-163">PascalCase</span></span> | <span data-ttu-id="23431-164">Verbe</span><span class="sxs-lookup"><span data-stu-id="23431-164">Verb</span></span> | <span data-ttu-id="23431-165">ValueChanged / ValueChanging</span><span class="sxs-lookup"><span data-stu-id="23431-165">ValueChanged / ValueChanging</span></span> |  |
| <span data-ttu-id="23431-166">Exceptions</span><span class="sxs-lookup"><span data-stu-id="23431-166">Exceptions</span></span>     | <span data-ttu-id="23431-167">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-167">PascalCase</span></span> |      | <span data-ttu-id="23431-168">WebException</span><span class="sxs-lookup"><span data-stu-id="23431-168">WebException</span></span> | <span data-ttu-id="23431-169">Nom doit se terminer avec « Exception ».</span><span class="sxs-lookup"><span data-stu-id="23431-169">Name should end with “Exception”.</span></span> |
| <span data-ttu-id="23431-170">Champ</span><span class="sxs-lookup"><span data-stu-id="23431-170">Field</span></span>          | <span data-ttu-id="23431-171">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-171">PascalCase</span></span> | <span data-ttu-id="23431-172">Nom</span><span class="sxs-lookup"><span data-stu-id="23431-172">Noun</span></span> | <span data-ttu-id="23431-173">CurrentName</span><span class="sxs-lookup"><span data-stu-id="23431-173">CurrentName</span></span>  | |
| <span data-ttu-id="23431-174">Types interface</span><span class="sxs-lookup"><span data-stu-id="23431-174">Interface types</span></span> |  <span data-ttu-id="23431-175">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-175">PascalCase</span></span> | <span data-ttu-id="23431-176">Nom / adjectif</span><span class="sxs-lookup"><span data-stu-id="23431-176">Noun/ adjective</span></span> | <span data-ttu-id="23431-177">IDisposable</span><span class="sxs-lookup"><span data-stu-id="23431-177">IDisposable</span></span> | <span data-ttu-id="23431-178">Nom doit commencer par « I ».</span><span class="sxs-lookup"><span data-stu-id="23431-178">Name should start with “I”.</span></span> |
| <span data-ttu-id="23431-179">Méthode</span><span class="sxs-lookup"><span data-stu-id="23431-179">Method</span></span> |  <span data-ttu-id="23431-180">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-180">PascalCase</span></span> |  <span data-ttu-id="23431-181">Verbe</span><span class="sxs-lookup"><span data-stu-id="23431-181">Verb</span></span> | <span data-ttu-id="23431-182">ToString</span><span class="sxs-lookup"><span data-stu-id="23431-182">ToString</span></span> | |
| <span data-ttu-id="23431-183">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="23431-183">Namespace</span></span> | <span data-ttu-id="23431-184">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-184">PascalCase</span></span> | | <span data-ttu-id="23431-185">Microsoft.FSharp.Core</span><span class="sxs-lookup"><span data-stu-id="23431-185">Microsoft.FSharp.Core</span></span> | <span data-ttu-id="23431-186">En général utiliser `<Organization>.<Technology>[.<Subnamespace>]`, toutefois supprimer l’organisation si la technologie est indépendante de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="23431-186">Generally use `<Organization>.<Technology>[.<Subnamespace>]`, though drop the organization if the technology is independent of organization.</span></span> |
| <span data-ttu-id="23431-187">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23431-187">Parameters</span></span> | <span data-ttu-id="23431-188">camelCase</span><span class="sxs-lookup"><span data-stu-id="23431-188">camelCase</span></span> | <span data-ttu-id="23431-189">Nom</span><span class="sxs-lookup"><span data-stu-id="23431-189">Noun</span></span> |  <span data-ttu-id="23431-190">typeName, transform, range</span><span class="sxs-lookup"><span data-stu-id="23431-190">typeName, transform, range</span></span> | |
| <span data-ttu-id="23431-191">laisser les valeurs (internes)</span><span class="sxs-lookup"><span data-stu-id="23431-191">let values (internal)</span></span> | <span data-ttu-id="23431-192">une casse mixte ou la casse Pascal</span><span class="sxs-lookup"><span data-stu-id="23431-192">camelCase or PascalCase</span></span> | <span data-ttu-id="23431-193">Nom / verbe</span><span class="sxs-lookup"><span data-stu-id="23431-193">Noun/ verb</span></span> |  <span data-ttu-id="23431-194">getValue, myTable</span><span class="sxs-lookup"><span data-stu-id="23431-194">getValue, myTable</span></span> |
| <span data-ttu-id="23431-195">laisser les valeurs (externe)</span><span class="sxs-lookup"><span data-stu-id="23431-195">let values (external)</span></span> | <span data-ttu-id="23431-196">une casse mixte ou la casse Pascal</span><span class="sxs-lookup"><span data-stu-id="23431-196">camelCase or PascalCase</span></span> | <span data-ttu-id="23431-197">Nom/verbe</span><span class="sxs-lookup"><span data-stu-id="23431-197">Noun/verb</span></span>  | <span data-ttu-id="23431-198">List.map, Dates.Today</span><span class="sxs-lookup"><span data-stu-id="23431-198">List.map, Dates.Today</span></span> | <span data-ttu-id="23431-199">Let lié aux valeurs sont souvent publique si l'on suit les modèles de conception fonctionnelle traditionnel.</span><span class="sxs-lookup"><span data-stu-id="23431-199">let-bound values are often public when following traditional functional design patterns.</span></span> <span data-ttu-id="23431-200">Toutefois, généralement utiliser la casse Pascal lors de l’identificateur peut être utilisé à partir d’autres langages .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-200">However, generally use PascalCase when the identifier can be used from other .NET languages.</span></span> |
| <span data-ttu-id="23431-201">Propriété</span><span class="sxs-lookup"><span data-stu-id="23431-201">Property</span></span>  | <span data-ttu-id="23431-202">PascalCase</span><span class="sxs-lookup"><span data-stu-id="23431-202">PascalCase</span></span>  | <span data-ttu-id="23431-203">Nom / adjectif</span><span class="sxs-lookup"><span data-stu-id="23431-203">Noun/ adjective</span></span>  | <span data-ttu-id="23431-204">IsEndOfFile, BackColor</span><span class="sxs-lookup"><span data-stu-id="23431-204">IsEndOfFile, BackColor</span></span>  | <span data-ttu-id="23431-205">Propriétés booléennes généralement l’utilisation est et peut et doit être positive, comme dans IsEndOfFile, IsNotEndOfFile pas.</span><span class="sxs-lookup"><span data-stu-id="23431-205">Boolean properties generally use Is and Can and should be affirmative, as in IsEndOfFile, not IsNotEndOfFile.</span></span>

#### <a name="avoid-abbreviations"></a><span data-ttu-id="23431-206">Éviter les abréviations</span><span class="sxs-lookup"><span data-stu-id="23431-206">Avoid abbreviations</span></span>

<span data-ttu-id="23431-207">Les règles de .NET déconseillons l’utilisation des abréviations (par exemple, « utiliser `OnButtonClick` plutôt que `OnBtnClick`»).</span><span class="sxs-lookup"><span data-stu-id="23431-207">The .NET guidelines discourage the use of abbreviations (for example, “use `OnButtonClick` rather than `OnBtnClick`”).</span></span> <span data-ttu-id="23431-208">Abréviations courantes, telles que `Async` pour « Asynchrone », sont tolérées.</span><span class="sxs-lookup"><span data-stu-id="23431-208">Common abbreviations, such as `Async` for “Asynchronous”, are tolerated.</span></span> <span data-ttu-id="23431-209">Cette recommandation est parfois ignorée pour la programmation fonctionnelle ; par exemple, `List.iter` utilise une abréviation pour « parcourir ».</span><span class="sxs-lookup"><span data-stu-id="23431-209">This guideline is sometimes ignored for functional programming; for example, `List.iter` uses an abbreviation for “iterate”.</span></span> <span data-ttu-id="23431-210">Pour cette raison, à l’aide des abréviations a tendance à être tolérée à un degré supérieur dans F#- au -F# de programmation, mais doit toujours en général être évitées dans la conception du composant public.</span><span class="sxs-lookup"><span data-stu-id="23431-210">For this reason, using abbreviations tends to be tolerated to a greater degree in F#-to-F# programming, but should still generally be avoided in public component design.</span></span>

#### <a name="avoid-casing-name-collisions"></a><span data-ttu-id="23431-211">Éviter les collisions de noms de mise en majuscules</span><span class="sxs-lookup"><span data-stu-id="23431-211">Avoid casing name collisions</span></span>

<span data-ttu-id="23431-212">Les règles de .NET dire que casse seul ne peut pas être utilisée pour lever l’ambiguïté des collisions de noms, dans la mesure où certaines langues du client (par exemple, Visual Basic) respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="23431-212">The .NET guidelines say that casing alone cannot be used to disambiguate name collisions, since some client languages (for example, Visual Basic) are case-insensitive.</span></span>

#### <a name="use-acronyms-where-appropriate"></a><span data-ttu-id="23431-213">Utiliser des acronymes approprié</span><span class="sxs-lookup"><span data-stu-id="23431-213">Use acronyms where appropriate</span></span>

<span data-ttu-id="23431-214">Acronymes tel que XML ne sont pas des abréviations et sont couramment utilisés dans les bibliothèques .NET dans le formulaire en minuscule (Xml).</span><span class="sxs-lookup"><span data-stu-id="23431-214">Acronyms such as XML are not abbreviations and are widely used in .NET libraries in uncapitalized form (Xml).</span></span> <span data-ttu-id="23431-215">Uniquement les acronymes bien connus, largement reconnues doivent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="23431-215">Only well-known, widely recognized acronyms should be used.</span></span>

#### <a name="use-pascalcase-for-generic-parameter-names"></a><span data-ttu-id="23431-216">Utilisez la casse Pascal pour les noms de paramètre générique</span><span class="sxs-lookup"><span data-stu-id="23431-216">Use PascalCase for generic parameter names</span></span>

<span data-ttu-id="23431-217">Utilisez la casse Pascal pour les noms de paramètre générique dans les API publiques, y compris pour F#-accessible sur les bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="23431-217">Do use PascalCase for generic parameter names in public APIs, including for F#-facing libraries.</span></span> <span data-ttu-id="23431-218">En particulier, utilisez des noms comme `T`, `U`, `T1`, `T2` pour les paramètres génériques arbitraires, et lorsque des noms spécifiques sont justifiées, puis pour F#-bibliothèques exposés utilisent des noms tels que `Key`, `Value`, `Arg` (mais pas par exemple, `TKey`).</span><span class="sxs-lookup"><span data-stu-id="23431-218">In particular, use names like `T`, `U`, `T1`, `T2` for arbitrary generic parameters, and when specific names make sense, then for F#-facing libraries use names like `Key`, `Value`, `Arg` (but not for example, `TKey`).</span></span>

#### <a name="use-either-pascalcase-or-camelcase-for-public-functions-and-values-in-f-modules"></a><span data-ttu-id="23431-219">Utilisez la casse Pascal ou la casse mixte pour les fonctions publiques et les valeurs de F# modules</span><span class="sxs-lookup"><span data-stu-id="23431-219">Use either PascalCase or camelCase for public functions and values in F# modules</span></span>

<span data-ttu-id="23431-220">une casse mixte est utilisée pour les fonctions publiques qui sont conçues pour être utilisés non qualifié (par exemple, `invalidArg`) et pour les fonctions de collection standard « » (par exemple, List.map).</span><span class="sxs-lookup"><span data-stu-id="23431-220">camelCase is used for public functions that are designed to be used unqualified (for example, `invalidArg`), and for the “standard collection functions” (for example, List.map).</span></span> <span data-ttu-id="23431-221">Dans ces deux cas, les noms de fonction fonctionnant un peu comme mots clés du langage.</span><span class="sxs-lookup"><span data-stu-id="23431-221">In both these cases, the function names act much like keywords in the language.</span></span>

### <a name="object-type-and-module-design"></a><span data-ttu-id="23431-222">Conception de Type, l’objet et le Module</span><span class="sxs-lookup"><span data-stu-id="23431-222">Object, Type, and Module design</span></span>

#### <a name="use-namespaces-or-modules-to-contain-your-types-and-modules"></a><span data-ttu-id="23431-223">Utilisez des espaces de noms ou des modules pour contenir vos types et les modules</span><span class="sxs-lookup"><span data-stu-id="23431-223">Use namespaces or modules to contain your types and modules</span></span>

<span data-ttu-id="23431-224">Chaque F# fichier dans un composant doit commencer par une déclaration d’espace de noms ou une déclaration de module.</span><span class="sxs-lookup"><span data-stu-id="23431-224">Each F# file in a component should begin with either a namespace declaration or a module declaration.</span></span>

```fsharp
namespace Fabrikam.BasicOperationsAndTypes

type ObjectType1() =
    ...

type ObjectType2() =
     ...

module CommonOperations =
    ...
```

<span data-ttu-id="23431-225">ou</span><span class="sxs-lookup"><span data-stu-id="23431-225">or</span></span>

```fsharp
module Fabrikam.BasicOperationsAndTypes

type ObjectType1() =
    ...

type ObjectType2() =
    ...

module CommonOperations =
    ...
```

<span data-ttu-id="23431-226">Les différences entre l’utilisation des modules et des espaces de noms pour organiser le code au niveau supérieur sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="23431-226">The differences between using modules and namespaces to organize code at the top level are as follows:</span></span>

* <span data-ttu-id="23431-227">Espaces de noms peut s’étendre sur plusieurs fichiers</span><span class="sxs-lookup"><span data-stu-id="23431-227">Namespaces can span multiple files</span></span>
* <span data-ttu-id="23431-228">Espaces de noms ne peut pas contenir F# fonctions, sauf si ces derniers sont dans un module interne</span><span class="sxs-lookup"><span data-stu-id="23431-228">Namespaces cannot contain F# functions unless they are within an inner module</span></span>
* <span data-ttu-id="23431-229">Le code de n’importe quel module donné doit être contenu dans un seul fichier</span><span class="sxs-lookup"><span data-stu-id="23431-229">The code for any given module must be contained within a single file</span></span>
* <span data-ttu-id="23431-230">Modules de niveau supérieur peuvent contenir F# fonctions sans avoir besoin d’un module interne</span><span class="sxs-lookup"><span data-stu-id="23431-230">Top-level modules can contain F# functions without the need for an inner module</span></span>

<span data-ttu-id="23431-231">Le choix entre un espace de noms de niveau supérieur ou un module a une incidence sur la forme compilée du code et par conséquent affecteront la vue à partir d’autres langages .NET devrait votre API être consommée en dehors de F# code.</span><span class="sxs-lookup"><span data-stu-id="23431-231">The choice between a top-level namespace or module affects the compiled form of the code, and thus will affect the view from other .NET languages should your API eventually be consumed outside of F# code.</span></span>

#### <a name="use-methods-and-properties-for-operations-intrinsic-to-object-types"></a><span data-ttu-id="23431-232">Utiliser les méthodes et propriétés pour les opérations intrinsèques aux types d’objets</span><span class="sxs-lookup"><span data-stu-id="23431-232">Use methods and properties for operations intrinsic to object types</span></span>

<span data-ttu-id="23431-233">Lorsque vous travaillez avec des objets, il est préférable pour vous assurer que les fonctionnalité consommable est implémentée en tant que les méthodes et propriétés sur ce type.</span><span class="sxs-lookup"><span data-stu-id="23431-233">When working with objects, it is best to ensure that consumable functionality is implemented as methods and properties on that type.</span></span>

```fsharp
type HardwareDevice() =

    member this.ID = ...

    member this.SupportedProtocols = ...

type HashTable<'Key,'Value>(comparer: IEqualityComparer<'Key>) =

    member this.Add(key, value) = ...

    member this.ContainsKey(key) = ...

    member this.ContainsValue(value) = ...
```

<span data-ttu-id="23431-234">La majeure partie des fonctionnalités pour un membre donné ne doive pas nécessairement implémentée dans ce membre, mais la partie consommable de cette fonctionnalité doit être.</span><span class="sxs-lookup"><span data-stu-id="23431-234">The bulk of functionality for a given member need not necessarily be implemented in that member, but the consumable piece of that functionality should be.</span></span>

#### <a name="use-classes-to-encapsulate-mutable-state"></a><span data-ttu-id="23431-235">Utiliser des classes pour encapsuler un état mutable</span><span class="sxs-lookup"><span data-stu-id="23431-235">Use classes to encapsulate mutable state</span></span>

<span data-ttu-id="23431-236">Dans F#, cela ne doit être effectuée où qu’état n’est pas déjà encapsulé par une autre construction de langage, par exemple une fermeture, une expression de séquence ou un calcul asynchrone.</span><span class="sxs-lookup"><span data-stu-id="23431-236">In F#, this only needs to be done where that state is not already encapsulated by another language construct, such as a closure, sequence expression, or asynchronous computation.</span></span>

```fsharp
type Counter() =
    // let-bound values are private in classes.
    let mutable count = 0

    member this.Next() =
        count <- count + 1
        count
```

#### <a name="use-interfaces-to-group-related-operations"></a><span data-ttu-id="23431-237">Utiliser des interfaces pour regrouper des opérations associées</span><span class="sxs-lookup"><span data-stu-id="23431-237">Use interfaces to group related operations</span></span>

<span data-ttu-id="23431-238">Utiliser des types d’interface pour représenter un ensemble d’opérations.</span><span class="sxs-lookup"><span data-stu-id="23431-238">Use interface types to represent a set of operations.</span></span> <span data-ttu-id="23431-239">Cette option est préférable aux autres options, telles que des tuples de fonctions ou des enregistrements de fonctions.</span><span class="sxs-lookup"><span data-stu-id="23431-239">This is preferred to other options, such as tuples of functions or records of functions.</span></span>

```fsharp
type Serializer =
    abstract Serialize<'T>: preserveRefEq: bool -> value: 'T -> string
    abstract Deserialize<'T>: preserveRefEq: bool -> pickle: string -> 'T
```

<span data-ttu-id="23431-240">De préférence à :</span><span class="sxs-lookup"><span data-stu-id="23431-240">In preference to:</span></span>

```fsharp
type Serializer<'T> = {
    Serialize: bool -> 'T -> string
    Deserialize: bool -> string -> 'T
}
```

<span data-ttu-id="23431-241">Les interfaces sont des concepts de première classe dans .NET, qui vous permettent d’obtenir les Functors normalement vous donnera.</span><span class="sxs-lookup"><span data-stu-id="23431-241">Interfaces are first-class concepts in .NET, which you can use to achieve what Functors would normally give you.</span></span> <span data-ttu-id="23431-242">En outre, elles peuvent servir pour encoder les types existentiels dans votre programme, qui ne peut pas des enregistrements de fonctions.</span><span class="sxs-lookup"><span data-stu-id="23431-242">Additionally, they can be used to encode existential types into your program, which records of functions cannot.</span></span>

#### <a name="use-a-module-to-group-functions-which-act-on-collections"></a><span data-ttu-id="23431-243">Utiliser un module à des fonctions de groupe qui agissent sur des collections</span><span class="sxs-lookup"><span data-stu-id="23431-243">Use a module to group functions which act on collections</span></span>

<span data-ttu-id="23431-244">Lorsque vous définissez un type de collection, envisagez de fournir un ensemble standard d’opérations telles que `CollectionType.map` et `CollectionType.iter`) pour les nouveaux types de collection.</span><span class="sxs-lookup"><span data-stu-id="23431-244">When you define a collection type, consider providing a standard set of operations like `CollectionType.map` and `CollectionType.iter`) for new collection types.</span></span>

```fsharp
module CollectionType =
    let map f c =
        ...
    let iter f c =
        ...
```

<span data-ttu-id="23431-245">Si vous incluez un de ces modules, suivez les conventions d’affectation de noms des fonctions trouvées dans FSharp.Core.</span><span class="sxs-lookup"><span data-stu-id="23431-245">If you include such a module, follow the standard naming conventions for functions found in FSharp.Core.</span></span>

#### <a name="use-a-module-to-group-functions-for-common-canonical-functions-especially-in-math-and-dsl-libraries"></a><span data-ttu-id="23431-246">Utiliser un module à des fonctions de groupe pour les fonctions canoniques courants, en particulier dans les mathématiques et les bibliothèques DSL</span><span class="sxs-lookup"><span data-stu-id="23431-246">Use a module to group functions for common, canonical functions, especially in math and DSL libraries</span></span>

<span data-ttu-id="23431-247">Par exemple, `Microsoft.FSharp.Core.Operators` est une collection automatiquement ouverte de fonctions de niveau supérieur (comme `abs` et `sin`) fourni par FSharp.Core.dll.</span><span class="sxs-lookup"><span data-stu-id="23431-247">For example, `Microsoft.FSharp.Core.Operators` is an automatically opened collection of top-level functions (like `abs` and `sin`) provided by FSharp.Core.dll.</span></span>

<span data-ttu-id="23431-248">De même, une bibliothèque de statistiques peut inclure un module avec des fonctions `erf` et `erfc`, où ce module est conçu pour être ouverte explicitement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="23431-248">Likewise, a statistics library might include a module with functions `erf` and `erfc`, where this module is designed to be explicitly or automatically opened.</span></span>

#### <a name="consider-using-requirequalifiedaccess-and-carefully-apply-autoopen-attributes"></a><span data-ttu-id="23431-249">Envisagez d’utiliser des RequireQualifiedAccess et appliquez soigneusement les attributs de AutoOpen</span><span class="sxs-lookup"><span data-stu-id="23431-249">Consider using RequireQualifiedAccess and carefully apply AutoOpen attributes</span></span>

<span data-ttu-id="23431-250">Ajout de la `[<RequireQualifiedAccess>]` attribut à un module indique que le module ne peut-être pas être ouverts et des références aux éléments du module doivent explicite qualifié d’accès.</span><span class="sxs-lookup"><span data-stu-id="23431-250">Adding the `[<RequireQualifiedAccess>]` attribute to a module indicates that the module may not be opened and that references to the elements of the module require explicit qualified access.</span></span> <span data-ttu-id="23431-251">Par exemple, le `Microsoft.FSharp.Collections.List` module a cet attribut.</span><span class="sxs-lookup"><span data-stu-id="23431-251">For example, the `Microsoft.FSharp.Collections.List` module has this attribute.</span></span>

<span data-ttu-id="23431-252">Cela est utile lorsque les valeurs dans le module et les fonctions ont des noms qui sont susceptibles d’entrer en conflit avec les noms dans d’autres modules.</span><span class="sxs-lookup"><span data-stu-id="23431-252">This is useful when functions and values in the module have names that are likely to conflict with names in other modules.</span></span> <span data-ttu-id="23431-253">Nécessitant un accès complet peut augmenter considérablement la facilité de maintenance à long terme et aspects d’une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="23431-253">Requiring qualified access can greatly increase the long-term maintainability and evolvability of a library.</span></span>

<span data-ttu-id="23431-254">Ajout de la `[<AutoOpen>]` attribut à un module signifie que le module s’ouvre quand l’espace de noms conteneur est ouvert.</span><span class="sxs-lookup"><span data-stu-id="23431-254">Adding the `[<AutoOpen>]` attribute to a module means the module will be opened when the containing namespace is opened.</span></span> <span data-ttu-id="23431-255">Le `[<AutoOpen>]` attribut peut également être appliqué à un assembly pour indiquer un module qui s’ouvre automatiquement quand l’assembly est référencé.</span><span class="sxs-lookup"><span data-stu-id="23431-255">The `[<AutoOpen>]` attribute may also be applied to an assembly to indicate a module that is automatically opened when the assembly is referenced.</span></span>

<span data-ttu-id="23431-256">Par exemple, une bibliothèque de statistiques **MathsHeaven.Statistics** peut contenir un `module MathsHeaven.Statistics.Operators` contenant des fonctions `erf` et `erfc`.</span><span class="sxs-lookup"><span data-stu-id="23431-256">For example, a statistics library **MathsHeaven.Statistics** might contain a `module MathsHeaven.Statistics.Operators` containing functions `erf` and `erfc`.</span></span> <span data-ttu-id="23431-257">Il est raisonnable de marquer ce module en tant que `[<AutoOpen>]`.</span><span class="sxs-lookup"><span data-stu-id="23431-257">It is reasonable to mark this module as `[<AutoOpen>]`.</span></span> <span data-ttu-id="23431-258">Cela signifie que `open MathsHeaven.Statistics` également ouvrir ce module et afficher les noms `erf` et `erfc` dans l’étendue.</span><span class="sxs-lookup"><span data-stu-id="23431-258">This means `open MathsHeaven.Statistics` will also open this module and bring the names `erf` and `erfc` into scope.</span></span> <span data-ttu-id="23431-259">Utiliser une autre bonne `[<AutoOpen>]` est pour les modules contenant les méthodes d’extension.</span><span class="sxs-lookup"><span data-stu-id="23431-259">Another good use of `[<AutoOpen>]` is for modules containing extension methods.</span></span>

<span data-ttu-id="23431-260">Abusez de `[<AutoOpen>]` aboutissent à des espaces de noms polluée et l’attribut doit être utilisée avec précaution.</span><span class="sxs-lookup"><span data-stu-id="23431-260">Overuse of `[<AutoOpen>]` leads to polluted namespaces, and the attribute should be used with care.</span></span> <span data-ttu-id="23431-261">Pour les bibliothèques spécifiques dans des domaines spécifiques, une utilisation judicieuse de `[<AutoOpen>]` peut entraîner une meilleure convivialité.</span><span class="sxs-lookup"><span data-stu-id="23431-261">For specific libraries in specific domains, judicious use of `[<AutoOpen>]` can lead to better usability.</span></span>

#### <a name="consider-defining-operator-members-on-classes-where-using-well-known-operators-is-appropriate"></a><span data-ttu-id="23431-262">Envisagez de définir des membres de l’opérateur sur les classes où à l’aide des opérateurs bien connus est approprié</span><span class="sxs-lookup"><span data-stu-id="23431-262">Consider defining operator members on classes where using well-known operators is appropriate</span></span>

<span data-ttu-id="23431-263">Parfois, les classes sont utilisées pour modéliser des mathématiques constructions telles que les vecteurs.</span><span class="sxs-lookup"><span data-stu-id="23431-263">Sometimes classes are used to model mathematical constructs such as Vectors.</span></span> <span data-ttu-id="23431-264">Quand le domaine en cours de modélisation possède des opérateurs bien connus, il est utile de les définir en tant que membres intrinsèques à la classe.</span><span class="sxs-lookup"><span data-stu-id="23431-264">When the domain being modeled has well-known operators, defining them as members intrinsic to the class is helpful.</span></span>

```fsharp
type Vector(x: float) =

    member v.X = x

    static member (*) (vector: Vector, scalar: float) = Vector(vector.X * scalar)

    static member (+) (vector1: Vector, vector2: Vector) = Vector(vector1.X + vector2.X)

let v = Vector(5.0)

let u = v * 10.0
```

<span data-ttu-id="23431-265">Ce guide correspond aux conseils généraux de .NET pour ces types.</span><span class="sxs-lookup"><span data-stu-id="23431-265">This guidance corresponds to general .NET guidance for these types.</span></span> <span data-ttu-id="23431-266">Toutefois, il peut être plus important dans F# codage car cela permet à ces types à utiliser conjointement avec F# fonctions et méthodes avec des contraintes de membre, telles que List.sumBy.</span><span class="sxs-lookup"><span data-stu-id="23431-266">However, it can be additionally important in F# coding as this allows these types to be used in conjunction with F# functions and methods with member constraints, such as List.sumBy.</span></span>

#### <a name="consider-using-compiledname-to-provide-a-net-friendly-name-for-other-net-language-consumers"></a><span data-ttu-id="23431-267">Envisagez d’utiliser CompiledName pour fournir une. Nom NET conviviale pour les autres consommateurs de langage .NET</span><span class="sxs-lookup"><span data-stu-id="23431-267">Consider using CompiledName to provide a .NET-friendly name for other .NET language consumers</span></span>

<span data-ttu-id="23431-268">Parfois, vous pouvez souhaiter donnez un nom dans un style pour les F# consommateurs (tel qu’un membre statique en minuscules afin qu’il apparaisse comme s’il s’agissait d’une fonction liée au module), mais ont un style différent pour le nom lorsqu’il est compilé dans un assembly.</span><span class="sxs-lookup"><span data-stu-id="23431-268">Sometimes you may wish to name something in one style for F# consumers (such as a static member in lower case so that it appears as if it were a module-bound function), but have a different style for the name when it is compiled into an assembly.</span></span> <span data-ttu-id="23431-269">Vous pouvez utiliser la `[<CompiledName>]` attribut pour fournir un style différent pour non F# code utilisant l’assembly.</span><span class="sxs-lookup"><span data-stu-id="23431-269">You can use the `[<CompiledName>]` attribute to provide a different style for non F# code consuming the assembly.</span></span>

```fsharp
type Vector(x:float, y:float) =

    member v.X = x
    member v.Y = y

    [<CompiledName("Create")>]
    static member create x y = Vector (x, y)

let v = Vector.create 5.0 3.0
```

<span data-ttu-id="23431-270">À l’aide de `[<CompiledName>]`, vous pouvez utiliser les conventions de nommage .NET pour non F# consommateurs de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="23431-270">By using `[<CompiledName>]`, you can use .NET naming conventions for non F# consumers of the assembly.</span></span>

#### <a name="use-method-overloading-for-member-functions-if-doing-so-provides-a-simpler-api"></a><span data-ttu-id="23431-271">Utilisez la surcharge de méthode pour les fonctions de membre, si cela vous permet une API plus simple</span><span class="sxs-lookup"><span data-stu-id="23431-271">Use method overloading for member functions, if doing so provides a simpler API</span></span>

<span data-ttu-id="23431-272">La surcharge de méthode est un outil puissant permettant de simplifier une API qui devra peut-être effectuer une fonctionnalité similaire, mais avec des options ou des arguments.</span><span class="sxs-lookup"><span data-stu-id="23431-272">Method overloading is a powerful tool for simplifying an API that may need to perform similar functionality, but with different options or arguments.</span></span>

```fsharp
type Logger() =

    member this.Log(message) =
        ...
    member this.Log(message, retryPolicy) =
        ...
```

<span data-ttu-id="23431-273">Dans F#, il est plus courant de surcharge sur le nombre d’arguments plutôt que des types d’arguments.</span><span class="sxs-lookup"><span data-stu-id="23431-273">In F#, it is more common to overload on number of arguments rather than types of arguments.</span></span>

#### <a name="hide-the-representations-of-record-and-union-types-if-the-design-of-these-types-is-likely-to-evolve"></a><span data-ttu-id="23431-274">Masquer les représentations sous forme d’enregistrement et de types union si la conception de ces types est susceptible d’évoluer</span><span class="sxs-lookup"><span data-stu-id="23431-274">Hide the representations of record and union types if the design of these types is likely to evolve</span></span>

<span data-ttu-id="23431-275">Éviter de révéler des représentations concrètes des objets.</span><span class="sxs-lookup"><span data-stu-id="23431-275">Avoid revealing concrete representations of objects.</span></span> <span data-ttu-id="23431-276">Par exemple, la représentation concrète de <xref:System.DateTime> valeurs n’est pas révélée par l’API externe, public de la conception de la bibliothèque .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-276">For example, the concrete representation of <xref:System.DateTime> values is not revealed by the external, public API of the .NET library design.</span></span> <span data-ttu-id="23431-277">Au moment de l’exécution, le Common Language Runtime sait l’implémentation validée qui sera utilisée tout au long de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="23431-277">At run time, the Common Language Runtime knows the committed implementation that will be used throughout execution.</span></span> <span data-ttu-id="23431-278">Toutefois, code compilé ne lui-même récupère les dépendances sur la représentation concrète.</span><span class="sxs-lookup"><span data-stu-id="23431-278">However, compiled code doesn't itself pick up dependencies on the concrete representation.</span></span>

#### <a name="avoid-the-use-of-implementation-inheritance-for-extensibility"></a><span data-ttu-id="23431-279">Évitez d’utiliser l’héritage d’implémentation pour l’extensibilité</span><span class="sxs-lookup"><span data-stu-id="23431-279">Avoid the use of implementation inheritance for extensibility</span></span>

<span data-ttu-id="23431-280">Dans F#, mise en œuvre l’héritage est rarement utilisé.</span><span class="sxs-lookup"><span data-stu-id="23431-280">In F#, implementation inheritance is rarely used.</span></span> <span data-ttu-id="23431-281">En outre, les hiérarchies d’héritage sont souvent complexes et difficiles à modifier à l’arrivée de nouvelles exigences.</span><span class="sxs-lookup"><span data-stu-id="23431-281">Furthermore, inheritance hierarchies are often complex and difficult to change when new requirements arrive.</span></span> <span data-ttu-id="23431-282">Implémentation de l’héritage existe toujours dans F# pour la compatibilité et les rares cas où il est la meilleure solution à un problème, mais les autres techniques doivent être recherchées dans votre F# programmes lors de la conception pour le polymorphisme, par exemple d’interface mise en œuvre.</span><span class="sxs-lookup"><span data-stu-id="23431-282">Inheritance implementation still exists in F# for compatibility and rare cases where it is the best solution to a problem, but alternative techniques should be sought in your F# programs when designing for polymorphism, such as interface implementation.</span></span>

### <a name="function-and-member-signatures"></a><span data-ttu-id="23431-283">Signatures de fonction et de membre</span><span class="sxs-lookup"><span data-stu-id="23431-283">Function and member signatures</span></span>

#### <a name="use-tuples-for-return-values-when-returning-a-small-number-of-multiple-unrelated-values"></a><span data-ttu-id="23431-284">Utiliser des tuples pour les valeurs de retour lors du retour d’un petit nombre de plusieurs valeurs non liées</span><span class="sxs-lookup"><span data-stu-id="23431-284">Use tuples for return values when returning a small number of multiple unrelated values</span></span>

<span data-ttu-id="23431-285">Voici un bon exemple d’utilisation d’un tuple dans un type de retour :</span><span class="sxs-lookup"><span data-stu-id="23431-285">Here is a good example of using a tuple in a return type:</span></span>

```fsharp
val divrem: BigInteger -> BigInteger -> BigInteger * BigInteger
```

<span data-ttu-id="23431-286">Pour retourner des types contenant de nombreux composants, ou où les composants sont associés à une seule entité identifiable, envisagez d’utiliser un type nommé au lieu d’un tuple.</span><span class="sxs-lookup"><span data-stu-id="23431-286">For return types containing many components, or where the components are related to a single identifiable entity, consider using a named type instead of a tuple.</span></span>

#### <a name="use-asynct-for-async-programming-at-f-api-boundaries"></a><span data-ttu-id="23431-287">Utilisez `Async<T>` pour la programmation à async F# limites des API</span><span class="sxs-lookup"><span data-stu-id="23431-287">Use `Async<T>` for async programming at F# API boundaries</span></span>

<span data-ttu-id="23431-288">S’il existe une opération synchrone correspondante nommée `Operation` qui retourne un `T`, puis l’opération asynchrone doit être nommée `AsyncOperation` si elle retourne `Async<T>` ou `OperationAsync` si elle retourne `Task<T>`.</span><span class="sxs-lookup"><span data-stu-id="23431-288">If there is a corresponding synchronous operation named `Operation` that returns a `T`, then the async operation should be named `AsyncOperation` if it returns `Async<T>` or `OperationAsync` if it returns `Task<T>`.</span></span> <span data-ttu-id="23431-289">Pour les types .NET couramment utilisés qui exposent des méthodes Begin/End, envisagez d’utiliser `Async.FromBeginEnd` pour écrire des méthodes d’extension comme une façade pour fournir le F# modèle de programmation asynchrone pour les API .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-289">For commonly used .NET types that expose Begin/End methods, consider using `Async.FromBeginEnd` to write extension methods as a façade to provide the F# async programming model to those .NET APIs.</span></span>

```fsharp
type SomeType =
    member this.Compute(x:int): int =
        ...
    member this.AsyncCompute(x:int): Async<int> =
        ...

type System.ServiceModel.Channels.IInputChannel with
    member this.AsyncReceive() =
        ...
```

### <a name="exceptions"></a><span data-ttu-id="23431-290">Exceptions</span><span class="sxs-lookup"><span data-stu-id="23431-290">Exceptions</span></span>

<span data-ttu-id="23431-291">Consultez [gestion des erreurs](conventions.md#error-management) pour en savoir plus sur l’utilisation appropriée des exceptions, les résultats et les options.</span><span class="sxs-lookup"><span data-stu-id="23431-291">See [Error Management](conventions.md#error-management) to learn about appropriate use of exceptions, results, and options.</span></span>

### <a name="extension-members"></a><span data-ttu-id="23431-292">Membres d’extension</span><span class="sxs-lookup"><span data-stu-id="23431-292">Extension Members</span></span>

#### <a name="carefully-apply-f-extension-members-in-f-to-f-components"></a><span data-ttu-id="23431-293">Appliquez soigneusement F# membres d’extension dans F#- au -F# composants</span><span class="sxs-lookup"><span data-stu-id="23431-293">Carefully apply F# extension members in F#-to-F# components</span></span>

<span data-ttu-id="23431-294">F#membres d’extension doivent généralement être utilisées uniquement pour les opérations qui se trouvent dans la clôture d’opérations intrinsèques associées à un type dans la majorité de ses modes d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="23431-294">F# extension members should generally only be used for operations that are in the closure of intrinsic operations associated with a type in the majority of its modes of use.</span></span> <span data-ttu-id="23431-295">Une utilisation courante consiste à fournir des API qui sont plus idiomatiques F# pour différents types de .NET :</span><span class="sxs-lookup"><span data-stu-id="23431-295">One common use is to provide APIs that are more idiomatic to F# for various .NET types:</span></span>

```fsharp
type System.ServiceModel.Channels.IInputChannel with
    member this.AsyncReceive() =
        Async.FromBeginEnd(this.BeginReceive, this.EndReceive)

type System.Collections.Generic.IDictionary<'Key,'Value> with
    member this.TryGet key =
        let ok, v = this.TryGetValue key
        if ok then Some v else None
```

### <a name="union-types"></a><span data-ttu-id="23431-296">Types d’union</span><span class="sxs-lookup"><span data-stu-id="23431-296">Union Types</span></span>

#### <a name="use-discriminated-unions-instead-of-class-hierarchies-for-tree-structured-data"></a><span data-ttu-id="23431-297">Utiliser les unions discriminées au lieu de hiérarchies de classes pour les données structurées en arborescence</span><span class="sxs-lookup"><span data-stu-id="23431-297">Use discriminated unions instead of class hierarchies for tree-structured data</span></span>

<span data-ttu-id="23431-298">Structures en arborescence sont définis de manière récursive.</span><span class="sxs-lookup"><span data-stu-id="23431-298">Tree-like structures are recursively defined.</span></span> <span data-ttu-id="23431-299">C’est délicat avec l’héritage, mais il est élégant avec des Unions discriminées.</span><span class="sxs-lookup"><span data-stu-id="23431-299">This is awkward with inheritance, but elegant with Discriminated Unions.</span></span>

```fsharp
type BST<'T> =
    | Empty
    | Node of 'T * BST<'T> * BST<'T>
```

<span data-ttu-id="23431-300">Représentant les données sous forme d’arborescence avec des Unions discriminées vous permet également de bénéficier d’exhaustivité dans les critères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="23431-300">Representing tree-like data with Discriminated Unions also allows you to benefit from exhaustiveness in pattern matching.</span></span>

#### <a name="use-requirequalifiedaccess-on-union-types-whose-case-names-are-not-sufficiently-unique"></a><span data-ttu-id="23431-301">Utilisez `[<RequireQualifiedAccess>]` sur les types d’union dont les noms cas ne sont pas suffisamment uniques</span><span class="sxs-lookup"><span data-stu-id="23431-301">Use `[<RequireQualifiedAccess>]` on union types whose case names are not sufficiently unique</span></span>

<span data-ttu-id="23431-302">Vous pouvez vous retrouver dans un domaine où le même nom est le meilleur nom pour des choses différentes, telles que des cas d’Union discriminée.</span><span class="sxs-lookup"><span data-stu-id="23431-302">You may find yourself in a domain where the same name is the best name for different things, such as Discriminated Union cases.</span></span> <span data-ttu-id="23431-303">Vous pouvez utiliser `[<RequireQualifiedAccess>]` pour lever l’ambiguïté des noms d’incidents afin d’éviter de déclencher des erreurs à confusion en raison d’une occultation dépendantes de l’ordre des `open` instructions</span><span class="sxs-lookup"><span data-stu-id="23431-303">You can use `[<RequireQualifiedAccess>]` to disambiguate case names in order to avoid triggering confusing errors due to shadowing dependent on the ordering of `open` statements</span></span>

#### <a name="hide-the-representations-of-discriminated-unions-for-binary-compatible-apis-if-the-design-of-these-types-is-likely-to-evolve"></a><span data-ttu-id="23431-304">Masquer les représentations sous forme d’unions discriminées pour les API compatible binaire si la conception de ces types est susceptible d’évoluer</span><span class="sxs-lookup"><span data-stu-id="23431-304">Hide the representations of discriminated unions for binary compatible APIs if the design of these types is likely to evolve</span></span>

<span data-ttu-id="23431-305">Types d’unions s’appuient sur F# correspondance des formulaires pour un modèle de programmation concis.</span><span class="sxs-lookup"><span data-stu-id="23431-305">Unions types rely on F# pattern-matching forms for a succinct programming model.</span></span> <span data-ttu-id="23431-306">Comme mentionné précédemment, vous devez éviter de révéler les représentations sous forme de données concrètes si la conception de ces types est susceptible d’évoluer.</span><span class="sxs-lookup"><span data-stu-id="23431-306">As mentioned previously, you should avoid revealing concrete data representations if the design of these types is likely to evolve.</span></span>

<span data-ttu-id="23431-307">Par exemple, la représentation sous forme d’une union discriminée peut être masquée à l’aide d’une déclaration privée ou interne, ou à l’aide d’un fichier de signature.</span><span class="sxs-lookup"><span data-stu-id="23431-307">For example, the representation of a discriminated union can be hidden using a private or internal declaration, or by using a signature file.</span></span>

```fsharp
type Union =
    private
    | CaseA of int
    | CaseB of string
```

<span data-ttu-id="23431-308">Si vous affichez les unions discriminées sans discrimination, il peut s’avérer difficile de version de votre bibliothèque sans casser le code de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="23431-308">If you reveal discriminated unions indiscriminately, you may find it hard to version your library without breaking user code.</span></span> <span data-ttu-id="23431-309">Envisagez plutôt de révéler un ou plusieurs modèles actifs pour autoriser des critères spéciaux sur les valeurs de votre type.</span><span class="sxs-lookup"><span data-stu-id="23431-309">Instead, consider revealing one or more active patterns to permit pattern matching over values of your type.</span></span>

<span data-ttu-id="23431-310">Modèles actifs fournissent une autre méthode pour fournir F# consommateurs disposant de critères spéciaux tout en évitant l’exposition F# directement les Types d’Union.</span><span class="sxs-lookup"><span data-stu-id="23431-310">Active patterns provide an alternate way to provide F# consumers with pattern matching while avoiding exposing F# Union Types directly.</span></span>

### <a name="inline-functions-and-member-constraints"></a><span data-ttu-id="23431-311">Les fonctions inline et les contraintes de membre</span><span class="sxs-lookup"><span data-stu-id="23431-311">Inline Functions and Member Constraints</span></span>

#### <a name="define-generic-numeric-algorithms-using-inline-functions-with-implied-member-constraints-and-statically-resolved-generic-types"></a><span data-ttu-id="23431-312">Définir les algorithmes numériques génériques à l’aide des fonctions inline avec les contraintes de membre implicite et les types génériques résolus statiquement</span><span class="sxs-lookup"><span data-stu-id="23431-312">Define generic numeric algorithms using inline functions with implied member constraints and statically resolved generic types</span></span>

<span data-ttu-id="23431-313">Contraintes de membre arithmétique et F# contraintes de comparaison sont une norme pour F# de programmation.</span><span class="sxs-lookup"><span data-stu-id="23431-313">Arithmetic member constraints and F# comparison constraints are a standard for F# programming.</span></span> <span data-ttu-id="23431-314">Considérons par exemple le code suivant :</span><span class="sxs-lookup"><span data-stu-id="23431-314">For example, consider the following code:</span></span>

```fsharp
let inline highestCommonFactor a b =
    let rec loop a b =
        if a = LanguagePrimitives.GenericZero<_> then b
        elif a < b then loop a (b - a)
        else loop (a - b) b
    loop a b
```

<span data-ttu-id="23431-315">Le type de cette fonction est comme suit :</span><span class="sxs-lookup"><span data-stu-id="23431-315">The type of this function is as follows:</span></span>

```fsharp
val inline highestCommonFactor : ^T -> ^T -> ^T
                when ^T : (static member Zero : ^T)
                and ^T : (static member ( - ) : ^T * ^T -> ^T)
                and ^T : equality
                and ^T : comparison
```

<span data-ttu-id="23431-316">Il s’agit d’une fonction appropriée pour une API publique dans une bibliothèque mathématique.</span><span class="sxs-lookup"><span data-stu-id="23431-316">This is a suitable function for a public API in a mathematical library.</span></span>

#### <a name="avoid-using-member-constraints-to-simulate-type-classes-and-duck-typing"></a><span data-ttu-id="23431-317">Évitez d’utiliser des contraintes de membre pour simuler des classes de type et canard en tapant</span><span class="sxs-lookup"><span data-stu-id="23431-317">Avoid using member constraints to simulate type classes and duck typing</span></span>

<span data-ttu-id="23431-318">Il est possible de simuler à l’aide de « canard en tapant » F# les contraintes de membre.</span><span class="sxs-lookup"><span data-stu-id="23431-318">It is possible to simulate “duck typing” using F# member constraints.</span></span> <span data-ttu-id="23431-319">Toutefois, les membres qui rendent utilisent ce grand pas en utiliser dans F#- au -F# conceptions de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="23431-319">However, members that make use of this should not in general be used in F#-to-F# library designs.</span></span> <span data-ttu-id="23431-320">Il s’agit, car les conceptions de bibliothèque en fonction des contraintes implicites inconnus ou non standards ont tendance à provoquer le code utilisateur à devenir rigide et liée au modèle un framework particulier.</span><span class="sxs-lookup"><span data-stu-id="23431-320">This is because library designs based on unfamiliar or non-standard implicit constraints tend to cause user code to become inflexible and tied to one particular framework pattern.</span></span>

<span data-ttu-id="23431-321">En outre, il est probable que le temps de compilation très longue peut entraîner une utilisation intensive de contraintes de membre de cette manière.</span><span class="sxs-lookup"><span data-stu-id="23431-321">Additionally, there is a good chance that heavy use of member constraints in this manner can result in very long compile times.</span></span>

### <a name="operator-definitions"></a><span data-ttu-id="23431-322">Définitions d’opérateur</span><span class="sxs-lookup"><span data-stu-id="23431-322">Operator Definitions</span></span>

#### <a name="avoid-defining-custom-symbolic-operators"></a><span data-ttu-id="23431-323">Évitez de définir des opérateurs symboliques personnalisés</span><span class="sxs-lookup"><span data-stu-id="23431-323">Avoid defining custom symbolic operators</span></span>

<span data-ttu-id="23431-324">Opérateurs personnalisés sont essentielles dans certaines situations et des appareils de notation très utiles au sein d’un large corps de code d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="23431-324">Custom operators are essential in some situations and are highly useful notational devices within a large body of implementation code.</span></span> <span data-ttu-id="23431-325">Pour les nouveaux utilisateurs d’une bibliothèque, fonctions nommées sont souvent plus faciles à utiliser.</span><span class="sxs-lookup"><span data-stu-id="23431-325">For new users of a library, named functions are often easier to use.</span></span> <span data-ttu-id="23431-326">En outre, les opérateurs symboliques personnalisés peuvent être difficiles de document, et rend difficile plus à rechercher de l’aide sur les opérateurs, en raison des limitations existantes dans l’IDE et recherche des moteurs.</span><span class="sxs-lookup"><span data-stu-id="23431-326">In addition, custom symbolic operators can be hard to document, and users find it more difficult to look up help on operators, due to existing limitations in IDE and search engines.</span></span>

<span data-ttu-id="23431-327">Par conséquent, il est préférable de publier vos fonctionnalités en tant que fonctions nommées et les membres et exposer en outre les opérateurs pour cette fonctionnalité uniquement si les notation avantages l’emportent sur la documentation et les cognitive coût engendré par les.</span><span class="sxs-lookup"><span data-stu-id="23431-327">As a result, it is best to publish your functionality as named functions and members, and additionally expose operators for this functionality only if the notational benefits outweigh the documentation and cognitive cost of having them.</span></span>

### <a name="units-of-measure"></a><span data-ttu-id="23431-328">Unités de mesure</span><span class="sxs-lookup"><span data-stu-id="23431-328">Units of Measure</span></span>

#### <a name="carefully-use-units-of-measure-for-added-type-safety-in-f-code"></a><span data-ttu-id="23431-329">Avec soin les unités de mesure de la sécurité de type ajouté dans F# code</span><span class="sxs-lookup"><span data-stu-id="23431-329">Carefully use units of measure for added type safety in F# code</span></span>

<span data-ttu-id="23431-330">Information de type supplémentaire pour les unités de mesure est effacée lorsqu’ils sont affichés par d’autres langages .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-330">Additional typing information for units of measure is erased when viewed by other .NET languages.</span></span> <span data-ttu-id="23431-331">N’oubliez pas que la réflexion, des outils et composants .NET verra types sans unités.</span><span class="sxs-lookup"><span data-stu-id="23431-331">Be aware that .NET components, tools, and reflection will see types-sans-units.</span></span> <span data-ttu-id="23431-332">Par exemple, C# consommateurs verrez `float` plutôt que `float<kg>`.</span><span class="sxs-lookup"><span data-stu-id="23431-332">For example, C# consumers will see `float` rather than `float<kg>`.</span></span>

### <a name="type-abbreviations"></a><span data-ttu-id="23431-333">Abréviations de types</span><span class="sxs-lookup"><span data-stu-id="23431-333">Type Abbreviations</span></span>

#### <a name="carefully-use-type-abbreviations-to-simplify-f-code"></a><span data-ttu-id="23431-334">Utiliser avec précaution les abréviations de type pour simplifier F# code</span><span class="sxs-lookup"><span data-stu-id="23431-334">Carefully use type abbreviations to simplify F# code</span></span>

<span data-ttu-id="23431-335">Réflexion, des outils et composants .NET ne verront pas les noms abrégés pour les types.</span><span class="sxs-lookup"><span data-stu-id="23431-335">.NET components, tools, and reflection will not see abbreviated names for types.</span></span> <span data-ttu-id="23431-336">Intensive des abréviations de type peut également afficher un domaine plus complexe qu’il est en fait, ce qui peut perturber de consommateurs.</span><span class="sxs-lookup"><span data-stu-id="23431-336">Significant usage of type abbreviations can also make a domain appear more complex than it actually is, which could confuse consumers.</span></span>

#### <a name="avoid-type-abbreviations-for-public-types-whose-members-and-properties-should-be-intrinsically-different-to-those-available-on-the-type-being-abbreviated"></a><span data-ttu-id="23431-337">Éviter les abréviations de type pour les types publics dont les membres et les propriétés doivent être intrinsèquement différents de ceux disponibles sur le type en cours abrégé</span><span class="sxs-lookup"><span data-stu-id="23431-337">Avoid type abbreviations for public types whose members and properties should be intrinsically different to those available on the type being abbreviated</span></span>

<span data-ttu-id="23431-338">Dans ce cas, le type en cours abrégé révèle trop d’informations sur la représentation du type réel qui est défini.</span><span class="sxs-lookup"><span data-stu-id="23431-338">In this case, the type being abbreviated reveals too much about the representation of the actual type being defined.</span></span> <span data-ttu-id="23431-339">Au lieu de cela, envisagez d’encapsuler l’abréviation dans un type de classe ou une union discriminée cas unique (ou, lorsque les performances sont essentielles, envisagez d’utiliser un type struct pour encapsuler l’abréviation).</span><span class="sxs-lookup"><span data-stu-id="23431-339">Instead, consider wrapping the abbreviation in a class type or a single-case discriminated union (or, when performance is essential, consider using a struct type to wrap the abbreviation).</span></span>

<span data-ttu-id="23431-340">Par exemple, il est tentant de définir un mappage multi comme un cas spécial d’un F# la carte, par exemple :</span><span class="sxs-lookup"><span data-stu-id="23431-340">For example, it is tempting to define a multi-map as a special case of an F# map, for example:</span></span>

```fsharp
type MultiMap<'Key,'Value> = Map<'Key,'Value list>
```

<span data-ttu-id="23431-341">Toutefois, les opérations logiques-notation par points sur ce type ne sont pas le même que les opérations sur une carte – par exemple, il est raisonnable que l’opérateur de recherche sont mappés. la liste vide si la clé n’est pas dans le dictionnaire, au lieu de lever une exception de retour [clé].</span><span class="sxs-lookup"><span data-stu-id="23431-341">However, the logical dot-notation operations on this type are not the same as the operations on a Map – for example, it is reasonable that the lookup operator map.[key] return the empty list if the key is not in the dictionary, rather than raising an exception.</span></span>

## <a name="guidelines-for-libraries-for-use-from-other-net-languages"></a><span data-ttu-id="23431-342">Instructions pour les bibliothèques à utiliser à partir d’autres langages .NET</span><span class="sxs-lookup"><span data-stu-id="23431-342">Guidelines for libraries for Use from other .NET Languages</span></span>

<span data-ttu-id="23431-343">Lorsque vous concevez des bibliothèques à utiliser à partir d’autres langages .NET, il est important de respecter le [directives de conception de bibliothèque .NET](../../standard/design-guidelines/index.md).</span><span class="sxs-lookup"><span data-stu-id="23431-343">When designing libraries for use from other .NET languages, it is important to adhere to the [.NET Library Design Guidelines](../../standard/design-guidelines/index.md).</span></span> <span data-ttu-id="23431-344">Dans ce document, ces bibliothèques sont étiquetés comme des bibliothèques .NET vanille, par opposition à F#-accessible sur les bibliothèques qui utilisent F# construit sans restriction.</span><span class="sxs-lookup"><span data-stu-id="23431-344">In this document, these libraries are labeled as vanilla .NET libraries, as opposed to F#-facing libraries that use F# constructs without restriction.</span></span> <span data-ttu-id="23431-345">Conception des bibliothèques .NET vanille on entend : fournir des API familières et idiomatiques cohérents avec le reste du .NET Framework en réduisant l’utilisation de F#-des constructions spécifiques dans l’API publique.</span><span class="sxs-lookup"><span data-stu-id="23431-345">Designing vanilla .NET libraries means providing familiar and idiomatic APIs consistent with the rest of the .NET Framework by minimizing the use of F#-specific constructs in the public API.</span></span> <span data-ttu-id="23431-346">Les règles sont expliquées dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="23431-346">The rules are explained in the following sections.</span></span>

### <a name="namespace-and-type-design-for-libraries-for-use-from-other-net-languages"></a><span data-ttu-id="23431-347">Conception Namespace et Type (pour les bibliothèques à utiliser à partir d’autres langages .NET)</span><span class="sxs-lookup"><span data-stu-id="23431-347">Namespace and Type design (for libraries for use from other .NET Languages)</span></span>

#### <a name="apply-the-net-naming-conventions-to-the-public-api-of-your-components"></a><span data-ttu-id="23431-348">Appliquer les conventions d’affectation de noms .NET à l’API publique de vos composants</span><span class="sxs-lookup"><span data-stu-id="23431-348">Apply the .NET naming conventions to the public API of your components</span></span>

<span data-ttu-id="23431-349">Faites particulièrement attention à l’utilisation de noms abrégés et les règles de mise en majuscules de .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-349">Pay special attention to the use of abbreviated names and the .NET capitalization guidelines.</span></span>

```fsharp
type pCoord = ...
    member this.theta = ...

type PolarCoordinate = ...
    member this.Theta = ...
```

#### <a name="use-namespaces-types-and-members-as-the-primary-organizational-structure-for-your-components"></a><span data-ttu-id="23431-350">Utilisez des espaces de noms, types et membres en tant que la structure organisationnelle principale pour vos composants</span><span class="sxs-lookup"><span data-stu-id="23431-350">Use namespaces, types, and members as the primary organizational structure for your components</span></span>

<span data-ttu-id="23431-351">Tous les fichiers contenant des fonctionnalités publiques doivent commencer par un `namespace` déclaration et que les seules entités destinées au public dans les espaces de noms doivent être des types.</span><span class="sxs-lookup"><span data-stu-id="23431-351">All files containing public functionality should begin with a `namespace` declaration, and the only public-facing entities in namespaces should be types.</span></span> <span data-ttu-id="23431-352">N’utilisez pas F# modules.</span><span class="sxs-lookup"><span data-stu-id="23431-352">Do not use F# modules.</span></span>

<span data-ttu-id="23431-353">Utilisez les modules non publics pour contenir le code d’implémentation, les types de l’utilitaire et les fonctions utilitaires.</span><span class="sxs-lookup"><span data-stu-id="23431-353">Use non-public modules to hold implementation code, utility types, and utility functions.</span></span>

<span data-ttu-id="23431-354">Les types static doivent avoir priorité sur les modules, car elles permettent une évolution future de l’API à utiliser la surcharge et d’autres principes de conception de l’API .NET qui ne peuvent pas être utilisés au sein de F# modules.</span><span class="sxs-lookup"><span data-stu-id="23431-354">Static types should be preferred over modules, as they allow for future evolution of the API to use overloading and other .NET API design concepts that may not be used within F# modules.</span></span>

<span data-ttu-id="23431-355">Par exemple, à la place de l’API publique suivante :</span><span class="sxs-lookup"><span data-stu-id="23431-355">For example, in place of the following public API:</span></span>

```fsharp
module Fabrikam

module Utilities =
    let Name = "Bob"
    let Add2 x y = x + y
    let Add3 x y z = x + y + z
```

<span data-ttu-id="23431-356">Pensez à la place :</span><span class="sxs-lookup"><span data-stu-id="23431-356">Consider instead:</span></span>

```fsharp
namespace Fabrikam

[<AbstractClass; Sealed>]
type Utilities =
    static member Name = "Bob"
    static member Add(x,y) = x + y
    static member Add(x,y,z) = x + y + z
```

#### <a name="use-f-record-types-in-vanilla-net-apis-if-the-design-of-the-types-wont-evolve"></a><span data-ttu-id="23431-357">Utilisez F# types d’enregistrements dans l’API .NET de vanille si la conception des types ne sont pas évoluer.</span><span class="sxs-lookup"><span data-stu-id="23431-357">Use F# record types in vanilla .NET APIs if the design of the types won't evolve</span></span>

<span data-ttu-id="23431-358">F#types d’enregistrements compilent à une classe .NET simple.</span><span class="sxs-lookup"><span data-stu-id="23431-358">F# record types compile to a simple .NET class.</span></span> <span data-ttu-id="23431-359">Ils ne conviennent pas pour certains types simples, stables dans les API.</span><span class="sxs-lookup"><span data-stu-id="23431-359">These are suitable for some simple, stable types in APIs.</span></span> <span data-ttu-id="23431-360">Vous devez envisager d’utiliser le `[<NoEquality>]` et `[<NoComparison>]` attributs à supprimer la génération automatique des interfaces.</span><span class="sxs-lookup"><span data-stu-id="23431-360">You should consider using the `[<NoEquality>]` and `[<NoComparison>]` attributes to suppress the automatic generation of interfaces.</span></span> <span data-ttu-id="23431-361">Évitez également à l’aide des champs d’enregistrement mutable dans vanille API .NET en tant que ces expose un champ public.</span><span class="sxs-lookup"><span data-stu-id="23431-361">Also avoid using mutable record fields in vanilla .NET APIs as these exposes a public field.</span></span> <span data-ttu-id="23431-362">Toujours envisager si une classe fournirait une option plus flexible pour l’évolution future de l’API.</span><span class="sxs-lookup"><span data-stu-id="23431-362">Always consider whether a class would provide a more flexible option for future evolution of the API.</span></span>

<span data-ttu-id="23431-363">Par exemple, ce qui suit F# code expose l’API publique pour un C# consommateur :</span><span class="sxs-lookup"><span data-stu-id="23431-363">For example, the following F# code exposes the public API to a C# consumer:</span></span>

<span data-ttu-id="23431-364">F# :</span><span class="sxs-lookup"><span data-stu-id="23431-364">F#:</span></span>

```fsharp
[<NoEquality; NoComparison>]
type MyRecord =
    { FirstThing: int
        SecondThing: string }
```

<span data-ttu-id="23431-365">C# :</span><span class="sxs-lookup"><span data-stu-id="23431-365">C#:</span></span>

```csharp
public sealed class MyRecord
{
    public MyRecord(int firstThing, string secondThing);
    public int FirstThing { get; }
    public string SecondThing { get; }
}
```

#### <a name="hide-the-representation-of-f-union-types-in-vanilla-net-apis"></a><span data-ttu-id="23431-366">Masquer la représentation sous forme de F# types union dans vanille API .NET</span><span class="sxs-lookup"><span data-stu-id="23431-366">Hide the representation of F# union types in vanilla .NET APIs</span></span>

<span data-ttu-id="23431-367">F#les types d’union ne sont pas utilisés au-delà des limites de composant, généralement même pour F#- au -F# de codage.</span><span class="sxs-lookup"><span data-stu-id="23431-367">F# union types are not commonly used across component boundaries, even for F#-to-F# coding.</span></span> <span data-ttu-id="23431-368">Il s’agit d’un appareil de mise en œuvre une excellente lorsqu’il est utilisé en interne au sein des composants et des bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="23431-368">They are an excellent implementation device when used internally within components and libraries.</span></span>

<span data-ttu-id="23431-369">Lorsque vous concevez une API .NET vanille, vous pouvez le masquer la représentation sous forme d’un type union en utilisant une déclaration privée ou un fichier de signature.</span><span class="sxs-lookup"><span data-stu-id="23431-369">When designing a vanilla .NET API, consider hiding the representation of a union type by using either a private declaration or a signature file.</span></span>

```fsharp
type PropLogic =
    private
    | And of PropLogic * PropLogic
    | Not of PropLogic
    | True
```

<span data-ttu-id="23431-370">Vous pouvez également augmenter les types qui permettent une représentation union en interne avec les membres de fournir un texte souhaité. API NET orientés.</span><span class="sxs-lookup"><span data-stu-id="23431-370">You may also augment types that use a union representation internally with members to provide a desired .NET-facing API.</span></span>

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

#### <a name="design-gui-and-other-components-using-the-design-patterns-of-the-framework"></a><span data-ttu-id="23431-371">Conception de l’interface graphique utilisateur et d’autres composants à l’aide de modèles de conception de l’infrastructure</span><span class="sxs-lookup"><span data-stu-id="23431-371">Design GUI and other components using the design patterns of the framework</span></span>

<span data-ttu-id="23431-372">Plusieurs environnements différents sont disponibles dans .NET, tels que ASP.NET, WinForms et WPF.</span><span class="sxs-lookup"><span data-stu-id="23431-372">There are many different frameworks available within .NET, such as WinForms, WPF, and ASP.NET.</span></span> <span data-ttu-id="23431-373">Conventions d’affectation de noms et de conception pour chacun doivent être utilisées si vous concevez des composants pour une utilisation dans ces infrastructures.</span><span class="sxs-lookup"><span data-stu-id="23431-373">Naming and design conventions for each should be used if you are designing components for use in these frameworks.</span></span> <span data-ttu-id="23431-374">Par exemple, pour la programmation WPF, adopter les modèles de conception WPF pour les classes que vous concevez.</span><span class="sxs-lookup"><span data-stu-id="23431-374">For example, for WPF programming, adopt WPF design patterns for the classes you are designing.</span></span> <span data-ttu-id="23431-375">Pour les modèles de programmation de l’interface utilisateur, utilisez les modèles de conception tels que des événements et basé sur la notification de collections tels que ceux trouvent dans <xref:System.Collections.ObjectModel>.</span><span class="sxs-lookup"><span data-stu-id="23431-375">For models in user interface programming, use design patterns such as events and notification-based collections such as those found in <xref:System.Collections.ObjectModel>.</span></span>

### <a name="object-and-member-design-for-libraries-for-use-from-other-net-languages"></a><span data-ttu-id="23431-376">Conception de membre et d’objet (pour les bibliothèques à utiliser à partir d’autres langages .NET)</span><span class="sxs-lookup"><span data-stu-id="23431-376">Object and Member design (for libraries for use from other .NET Languages)</span></span>

#### <a name="use-the-clievent-attribute-to-expose-net-events"></a><span data-ttu-id="23431-377">Utilisez l’attribut CLIEvent pour exposer des événements .NET</span><span class="sxs-lookup"><span data-stu-id="23431-377">Use the CLIEvent attribute to expose .NET events</span></span>

<span data-ttu-id="23431-378">Construire un `DelegateEvent` avec .NET spécifique le type qui prend un objet de délégué et `EventArgs` (plutôt qu’un `Event`, qui utilise simplement le `FSharpHandler` type par défaut) afin que les événements sont publiés dans le moyen familier d’autres langages .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-378">Construct a `DelegateEvent` with a specific .NET delegate type that takes an object and `EventArgs` (rather than an `Event`, which just uses the `FSharpHandler` type by default) so that the events are published in the familiar way to other .NET languages.</span></span>

```fsharp
type MyBadType() =
    let myEv = new Event<int>()

    [<CLIEvent>]
    member this.MyEvent = myEv.Publish

type MyEventArgs(x: int) =
    inherit System.EventArgs()
    member this.X = x

    /// A type in a component designed for use from other .NET languages
type MyGoodType() =
    let myEv = new DelegateEvent<EventHandler<MyEventArgs>>()

    [<CLIEvent>]
    member this.MyEvent = myEv.Publish
```

#### <a name="expose-asynchronous-operations-as-methods-which-return-net-tasks"></a><span data-ttu-id="23431-379">Exposer des opérations asynchrones en tant que méthodes qui retournent des tâches de .NET</span><span class="sxs-lookup"><span data-stu-id="23431-379">Expose asynchronous operations as methods which return .NET tasks</span></span>

<span data-ttu-id="23431-380">Tâches sont utilisées dans .NET pour représenter les calculs asynchrones actives.</span><span class="sxs-lookup"><span data-stu-id="23431-380">Tasks are used in .NET to represent active asynchronous computations.</span></span> <span data-ttu-id="23431-381">Les tâches sont en général moins composition que F# `Async<T>` objets, car ils représentent les tâches « en cours d’exécution » et ne peut pas être combinées dans les méthodes qui effectuent la composition parallèle, ou qui masquer la propagation de signaux de l’annulation et d’autres paramètres contextuelles.</span><span class="sxs-lookup"><span data-stu-id="23431-381">Tasks are in general less compositional than F# `Async<T>` objects, since they represent “already executing” tasks and can’t be composed together in ways that perform parallel composition, or which hide the propagation of cancellation signals and other contextual parameters.</span></span>

<span data-ttu-id="23431-382">Toutefois, en dépit de cela, les méthodes qui retournent des tâches sont la représentation de la programmation asynchrone dans .NET standard.</span><span class="sxs-lookup"><span data-stu-id="23431-382">However, despite this, methods which return Tasks are the standard representation of asynchronous programming on .NET.</span></span>

```fsharp
/// A type in a component designed for use from other .NET languages
type MyType() =

    let compute (x: int): Async<int> = async { ... }

    member this.ComputeAsync(x) = compute x |> Async.StartAsTask
```

<span data-ttu-id="23431-383">Vous allez souvent que vous souhaitez également accepter un jeton d’annulation explicite :</span><span class="sxs-lookup"><span data-stu-id="23431-383">You will frequently also want to accept an explicit cancellation token:</span></span>

```fsharp
/// A type in a component designed for use from other .NET languages
type MyType() =
    let compute(x: int): Async<int> = async { ... }
    member this.ComputeAsTask(x, cancellationToken) = Async.StartAsTask(compute x, cancellationToken)
```

#### <a name="use-net-delegate-types-instead-of-f-function-types"></a><span data-ttu-id="23431-384">Utiliser des types de délégués .NET à la place de F# types de fonction</span><span class="sxs-lookup"><span data-stu-id="23431-384">Use .NET delegate types instead of F# function types</span></span>

<span data-ttu-id="23431-385">Ici «F# types de fonction » signifie que les types « flèche » comme `int -> int`.</span><span class="sxs-lookup"><span data-stu-id="23431-385">Here “F# function types” mean “arrow” types like `int -> int`.</span></span>

<span data-ttu-id="23431-386">Au lieu de cela :</span><span class="sxs-lookup"><span data-stu-id="23431-386">Instead of this:</span></span>

```fsharp
member this.Transform(f: int->int) =
    ...
```

<span data-ttu-id="23431-387">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="23431-387">Do this:</span></span>

```fsharp
member this.Transform(f: Func<int,int>) =
    ...
```

<span data-ttu-id="23431-388">Le F# type de fonction apparaît sous la forme `class FSharpFunc<T,U>` à d’autres langages .NET et est moins adaptée pour les fonctionnalités de langage et outils qui comprennent les types délégués.</span><span class="sxs-lookup"><span data-stu-id="23431-388">The F# function type appears as `class FSharpFunc<T,U>` to other .NET languages, and is less suitable for language features and tooling that understand delegate types.</span></span> <span data-ttu-id="23431-389">Lors de la création d’une méthode d’ordre supérieur qui ciblent .NET Framework 3.5 ou version ultérieure, le `System.Func` et `System.Action` les délégués sont les API de droite à publier pour permettre aux développeurs .NET de consommer ces API de manière faible friction.</span><span class="sxs-lookup"><span data-stu-id="23431-389">When authoring a higher-order method targeting .NET Framework 3.5 or higher, the `System.Func` and `System.Action` delegates are the right APIs to publish to enable .NET developers to consume these APIs in a low-friction manner.</span></span> <span data-ttu-id="23431-390">(Si vous ciblez .NET Framework 2.0, les types délégués définis par le système sont plus limités ; envisagez d’utiliser des types de délégué prédéfinis, tels que `System.Converter<T,U>` ou définition d’un type délégué spécifique.)</span><span class="sxs-lookup"><span data-stu-id="23431-390">(When targeting .NET Framework 2.0, the system-defined delegate types are more limited; consider using predefined delegate types such as `System.Converter<T,U>` or defining a specific delegate type.)</span></span>

<span data-ttu-id="23431-391">En revanche, les délégués .NET ne sont pas naturelles pour F#-accessible sur les bibliothèques (consultez la Section suivante sur F#-accessible sur les bibliothèques).</span><span class="sxs-lookup"><span data-stu-id="23431-391">On the flip side, .NET delegates are not natural for F#-facing libraries (see the next Section on F#-facing libraries).</span></span> <span data-ttu-id="23431-392">Par conséquent, une stratégie d’implémentation courantes lors du développement des méthodes d’ordre supérieur pour les bibliothèques .NET vanille consiste à créer tout l’implémentation en utilisant F# types de fonction et puis créer l’API publique à l’aide de délégués comme une façade mince située en haut de la F#implémentation.</span><span class="sxs-lookup"><span data-stu-id="23431-392">As a result, a common implementation strategy when developing higher-order methods for vanilla .NET libraries is to author all the implementation using F# function types, and then create the public API using delegates as a thin façade atop the actual F# implementation.</span></span>

#### <a name="use-the-trygetvalue-pattern-instead-of-returning-f-option-values-and-prefer-method-overloading-to-taking-f-option-values-as-arguments"></a><span data-ttu-id="23431-393">Utiliser le modèle TryGetValue au lieu de retourner F# les valeurs d’option et préférez la surcharge de méthode pour la prise de F# les valeurs en tant qu’arguments d’option</span><span class="sxs-lookup"><span data-stu-id="23431-393">Use the TryGetValue pattern instead of returning F# option values, and prefer method overloading to taking F# option values as arguments</span></span>

<span data-ttu-id="23431-394">Modèles courants d’utilisation pour le F# type d’option dans les API sont préférables implémenté dans vanille techniques de création des API de .NET à l’aide de .NET standard.</span><span class="sxs-lookup"><span data-stu-id="23431-394">Common patterns of use for the F# option type in APIs are better implemented in vanilla .NET APIs using standard .NET design techniques.</span></span> <span data-ttu-id="23431-395">Au lieu de retourner un F# valeur d’option, envisagez d’utiliser le type de retour de bool ainsi qu’un paramètre de sortie, comme dans le modèle « TryGetValue ».</span><span class="sxs-lookup"><span data-stu-id="23431-395">Instead of returning an F# option value, consider using the bool return type plus an out parameter as in the "TryGetValue" pattern.</span></span> <span data-ttu-id="23431-396">Et au lieu de prendre F# les valeurs en tant que paramètres d’option, envisagez d’utiliser des arguments de méthode surcharge ou facultatif.</span><span class="sxs-lookup"><span data-stu-id="23431-396">And instead of taking F# option values as parameters, consider using method overloading or optional arguments.</span></span>

```fsharp
member this.ReturnOption() = Some 3

member this.ReturnBoolAndOut(outVal: byref<int>) =
    outVal <- 3
    true

member this.ParamOption(x: int, y: int option) =
    match y with
    | Some y2 -> x + y2
    | None -> x

member this.ParamOverload(x: int) = x

member this.ParamOverload(x: int, y: int) = x + y
```

#### <a name="use-the-net-collection-interface-types-ienumerablet-and-idictionarykeyvalue-for-parameters-and-return-values"></a><span data-ttu-id="23431-397">Utiliser l’interface de collection .NET des types IEnumerable\<T\> et IDictionary\<clé, valeur\> pour les paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="23431-397">Use the .NET collection interface types IEnumerable\<T\> and IDictionary\<Key,Value\> for parameters and return values</span></span>

<span data-ttu-id="23431-398">Évitez d’utiliser des types de collection concrets tels que les tableaux .NET `T[]`, F# types `list<T>`, `Map<Key,Value>` et `Set<T>`, et les types de collection concrets .NET tels que `Dictionary<Key,Value>`.</span><span class="sxs-lookup"><span data-stu-id="23431-398">Avoid the use of concrete collection types such as .NET arrays `T[]`, F# types `list<T>`, `Map<Key,Value>` and `Set<T>`, and .NET concrete collection types such as `Dictionary<Key,Value>`.</span></span> <span data-ttu-id="23431-399">Les règles de conception de bibliothèque .NET ont bon Conseil concernant quand utiliser les différents types de collection comme `IEnumerable<T>`.</span><span class="sxs-lookup"><span data-stu-id="23431-399">The .NET Library Design Guidelines have good advice regarding when to use various collection types like `IEnumerable<T>`.</span></span> <span data-ttu-id="23431-400">Une utilisation de tableaux (`T[]`) est acceptable dans certains cas, pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="23431-400">Some use of arrays (`T[]`) is acceptable in some circumstances, on performance grounds.</span></span> <span data-ttu-id="23431-401">Notez en particulier que `seq<T>` est simplement le F# alias `IEnumerable<T>`, et seq est donc souvent un type approprié pour une API .NET vanille.</span><span class="sxs-lookup"><span data-stu-id="23431-401">Note especially that `seq<T>` is just the F# alias for `IEnumerable<T>`, and thus seq is often an appropriate type for a vanilla .NET API.</span></span>

<span data-ttu-id="23431-402">Au lieu de F# répertorie :</span><span class="sxs-lookup"><span data-stu-id="23431-402">Instead of F# lists:</span></span>

```fsharp
member this.PrintNames(names: string list) =
    ...
```

<span data-ttu-id="23431-403">Utilisez F# séquences :</span><span class="sxs-lookup"><span data-stu-id="23431-403">Use F# sequences:</span></span>

```fsharp
member this.PrintNames(names: seq<string>) =
    ...
```

#### <a name="use-the-unit-type-as-the-only-input-type-of-a-method-to-define-a-zero-argument-method-or-as-the-only-return-type-to-define-a-void-returning-method"></a><span data-ttu-id="23431-404">Utiliser le type d’unité en tant que le seul type d’entrée d’une méthode pour définir une méthode sans argument, ou en tant que le seul type de retour par définir une méthode retournant void</span><span class="sxs-lookup"><span data-stu-id="23431-404">Use the unit type as the only input type of a method to define a zero-argument method, or as the only return type to define a void-returning method</span></span>

<span data-ttu-id="23431-405">Évitez d’autres utilisations du type d’unité.</span><span class="sxs-lookup"><span data-stu-id="23431-405">Avoid other uses of the unit type.</span></span> <span data-ttu-id="23431-406">Il s’agit bon :</span><span class="sxs-lookup"><span data-stu-id="23431-406">These are good:</span></span>

```fsharp
✔ member this.NoArguments() = 3

✔ member this.ReturnVoid(x: int) = ()
```

<span data-ttu-id="23431-407">Cela est incorrect :</span><span class="sxs-lookup"><span data-stu-id="23431-407">This is bad:</span></span>

```fsharp
member this.WrongUnit( x: unit, z: int) = ((), ())
```

#### <a name="check-for-null-values-on-vanilla-net-api-boundaries"></a><span data-ttu-id="23431-408">Vérifier les valeurs null sur les limites de l’API .NET vanille</span><span class="sxs-lookup"><span data-stu-id="23431-408">Check for null values on vanilla .NET API boundaries</span></span>

<span data-ttu-id="23431-409">F#code d’implémentation a tendance à avoir moins de valeurs null, en raison des modèles de conception immuable et les restrictions sur l’utilisation des littéraux null pour F# types.</span><span class="sxs-lookup"><span data-stu-id="23431-409">F# implementation code tends to have fewer null values, due to immutable design patterns and restrictions on use of null literals for F# types.</span></span> <span data-ttu-id="23431-410">Autres langages .NET utilisent souvent null en tant que valeur beaucoup plus fréquemment.</span><span class="sxs-lookup"><span data-stu-id="23431-410">Other .NET languages often use null as a value much more frequently.</span></span> <span data-ttu-id="23431-411">Pour cette raison, F# code qui expose une API .NET vanille doit vérifier les paramètres pour la valeur null à la limite de l’API et ces valeurs empêcher de passer plus profondément dans le F# code d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="23431-411">Because of this, F# code that is exposing a vanilla .NET API should check parameters for null at the API boundary, and prevent these values from flowing deeper into the F# implementation code.</span></span> <span data-ttu-id="23431-412">Le `isNull` (fonction) ou des critères spéciaux sur les `null` modèle peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="23431-412">The `isNull` function or pattern matching on the `null` pattern can be used.</span></span>

```fsharp
let checkNonNull argName (arg: obj) =
    match arg with
    | null -> nullArg argName
    | _ -> ()

let checkNonNull` argName (arg: obj) =
    if isNull arg then nullArg argName
    else ()
```

#### <a name="avoid-using-tuples-as-return-values"></a><span data-ttu-id="23431-413">Évitez d’utiliser des tuples comme valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="23431-413">Avoid using tuples as return values</span></span>

<span data-ttu-id="23431-414">Au lieu de cela, préférez retournant un type nommé contenant les données d’agrégation ou d’utiliser les paramètres de sortie pour retourner plusieurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="23431-414">Instead, prefer returning a named type holding the aggregate data, or using out parameters to return multiple values.</span></span> <span data-ttu-id="23431-415">Bien que les tuples et les tuples de struct existent dans .NET (notamment C# prise en charge linguistique pour les tuples de struct), ils plus souvent ne fournira pas l’API idéale et attendu pour les développeurs .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-415">Although tuples and struct tuples exist in .NET (including C# language support for struct tuples), they will most often not provide the ideal and expected API for .NET developers.</span></span>

#### <a name="avoid-the-use-of-currying-of-parameters"></a><span data-ttu-id="23431-416">Évitez d’utiliser des curryfication de paramètres</span><span class="sxs-lookup"><span data-stu-id="23431-416">Avoid the use of currying of parameters</span></span>

<span data-ttu-id="23431-417">Au lieu de cela, utilisez les conventions d’appel de .NET `Method(arg1,arg2,…,argN)`.</span><span class="sxs-lookup"><span data-stu-id="23431-417">Instead, use .NET calling conventions `Method(arg1,arg2,…,argN)`.</span></span>

```fsharp
member this.TupledArguments(str, num) = String.replicate num str
```

<span data-ttu-id="23431-418">Conseil : Si vous concevez des bibliothèques à utiliser à partir de n’importe quel langage .NET, rien ne vaut pour faire réellement certaines expérimentale C# et pour vous assurer que vos bibliothèques « la convivialité droite » à partir de ces langages de programmation Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="23431-418">Tip: If you’re designing libraries for use from any .NET language, then there’s no substitute for actually doing some experimental C# and Visual Basic programming to ensure that your libraries "feel right" from these languages.</span></span> <span data-ttu-id="23431-419">Vous pouvez également utiliser des outils tels que .NET Reflector et l’Explorateur d’objets Visual Studio pour vous assurer que les bibliothèques et leur documentation apparaissent comme prévu pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="23431-419">You can also use tools such as .NET Reflector and the Visual Studio Object Browser to ensure that libraries and their documentation appear as expected to developers.</span></span>

## <a name="appendix"></a><span data-ttu-id="23431-420">Annexe</span><span class="sxs-lookup"><span data-stu-id="23431-420">Appendix</span></span>

### <a name="end-to-end-example-of-designing-f-code-for-use-by-other-net-languages"></a><span data-ttu-id="23431-421">Exemple de bout en bout de la conception F# code pour une utilisation par d’autres langages .NET</span><span class="sxs-lookup"><span data-stu-id="23431-421">End-to-end example of designing F# code for use by other .NET languages</span></span>

<span data-ttu-id="23431-422">Considérez la classe suivante :</span><span class="sxs-lookup"><span data-stu-id="23431-422">Consider the following class:</span></span>

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

<span data-ttu-id="23431-423">Le déduit F# est de type de cette classe comme suit :</span><span class="sxs-lookup"><span data-stu-id="23431-423">The inferred F# type of this class is as follows:</span></span>

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

<span data-ttu-id="23431-424">Examinons comment faire cela F# type s’affiche pour un programmeur à l’aide d’un autre langage .NET.</span><span class="sxs-lookup"><span data-stu-id="23431-424">Let’s take a look at how this F# type appears to a programmer using another .NET language.</span></span> <span data-ttu-id="23431-425">Par exemple, approximatif c# « signature » est la suivante :</span><span class="sxs-lookup"><span data-stu-id="23431-425">For example, the approximate C# “signature” is as follows:</span></span>

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

<span data-ttu-id="23431-426">Il existe quelques points importants à noter sur la façon F# représente construit ici.</span><span class="sxs-lookup"><span data-stu-id="23431-426">There are some important points to notice about how F# represents constructs here.</span></span> <span data-ttu-id="23431-427">Exemple :</span><span class="sxs-lookup"><span data-stu-id="23431-427">For example:</span></span>

* <span data-ttu-id="23431-428">Métadonnées telles que les noms d’arguments a été conservée.</span><span class="sxs-lookup"><span data-stu-id="23431-428">Metadata such as argument names has been preserved.</span></span>

* <span data-ttu-id="23431-429">F#les méthodes qui acceptent deux arguments deviennent C# les méthodes qui acceptent deux arguments.</span><span class="sxs-lookup"><span data-stu-id="23431-429">F# methods that take two arguments become C# methods that take two arguments.</span></span>

* <span data-ttu-id="23431-430">Fonctions et les listes deviennent des références à des types correspondants dans le F# bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="23431-430">Functions and lists become references to corresponding types in the F# library.</span></span>

<span data-ttu-id="23431-431">Le code suivant montre comment ajuster ce code pour tenir compte de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="23431-431">The following code shows how to adjust this code to take these things into account.</span></span>

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

<span data-ttu-id="23431-432">Le déduit F# est de type de code comme suit :</span><span class="sxs-lookup"><span data-stu-id="23431-432">The inferred F# type of the code is as follows:</span></span>

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

<span data-ttu-id="23431-433">La signature c# est désormais comme suit :</span><span class="sxs-lookup"><span data-stu-id="23431-433">The C# signature is now as follows:</span></span>

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

<span data-ttu-id="23431-434">Les corrections apportées à préparer ce type à utiliser dans le cadre d’une bibliothèque .NET vanille sont comme suit :</span><span class="sxs-lookup"><span data-stu-id="23431-434">The fixes made to prepare this type for use as part of a vanilla .NET library are as follows:</span></span>

* <span data-ttu-id="23431-435">Ajusté plusieurs noms : `Point1`, `n`, `l`, et `f` est devenu `RadialPoint`, `count`, `factor`, et `transform`, respectivement.</span><span class="sxs-lookup"><span data-stu-id="23431-435">Adjusted several names: `Point1`, `n`, `l`, and `f` became `RadialPoint`, `count`, `factor`, and `transform`, respectively.</span></span>

* <span data-ttu-id="23431-436">Utiliser un type de retour `seq<RadialPoint>` au lieu de `RadialPoint list` en modifiant une construction de la liste à l’aide `[ ... ]` à une construction de séquence à l’aide `IEnumerable<RadialPoint>`.</span><span class="sxs-lookup"><span data-stu-id="23431-436">Used a return type of `seq<RadialPoint>` instead of `RadialPoint list` by changing a list construction using `[ ... ]` to a sequence construction using `IEnumerable<RadialPoint>`.</span></span>

* <span data-ttu-id="23431-437">Utilisé le type de délégué .NET `System.Func` au lieu d’un F# type de fonction.</span><span class="sxs-lookup"><span data-stu-id="23431-437">Used the .NET delegate type `System.Func` instead of an F# function type.</span></span>

<span data-ttu-id="23431-438">Cela facilite beaucoup mieux à consommer en code c#.</span><span class="sxs-lookup"><span data-stu-id="23431-438">This makes it far nicer to consume in C# code.</span></span>
