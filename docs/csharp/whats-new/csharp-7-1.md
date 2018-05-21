---
title: Nouveautés de C# 7.1
description: Vue d’ensemble des nouvelles fonctionnalités de C# 7.1.
ms.date: 08/16/2017
ms.openlocfilehash: 00baec45d7582d3ac12c7b0865241f5cd8159246
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="whats-new-in-c-71"></a><span data-ttu-id="8b5c1-103">Nouveautés de C# 7.1</span><span class="sxs-lookup"><span data-stu-id="8b5c1-103">What's new in C# 7.1</span></span>

<span data-ttu-id="8b5c1-104">C# 7.1 est la première version mineure pour le langage C#.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-104">C# 7.1 is the first point release to the C# language.</span></span> <span data-ttu-id="8b5c1-105">Elle marque une cadence de publication accrue pour le langage.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-105">It marks an increased release cadence for the language.</span></span> <span data-ttu-id="8b5c1-106">Vous pouvez utiliser les nouvelles fonctionnalités plus tôt, dans l’idéal quand chaque nouvelle fonctionnalité est prête.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-106">You can use the new features sooner, ideally when each new feature is ready.</span></span> <span data-ttu-id="8b5c1-107">C# 7.1 ajoute la possibilité de configurer le compilateur pour le faire correspondre à une version spécifiée du langage.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-107">C# 7.1 adds the ability to configure the compiler to match a specified version of the language.</span></span> <span data-ttu-id="8b5c1-108">Ceci vous permet de séparer la décision de mettre à niveau les outils de la décision de mettre à niveau les versions du langage.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-108">That enables you to separate the decision to upgrade tools from the decision to upgrade language versions.</span></span>

<span data-ttu-id="8b5c1-109">C# 7.1 ajoute l’élément de configuration de [sélection de la version du langage](#language-version-selection), trois nouvelles fonctionnalités du langage et un nouveau comportement du compilateur.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-109">C# 7.1 adds the [language version selection](#language-version-selection) configuration element, three new language features and new compiler behavior.</span></span>

<span data-ttu-id="8b5c1-110">Les nouvelles fonctionnalités de langage de cette version sont :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-110">The new language features in this release are:</span></span>

* [<span data-ttu-id="8b5c1-111">Méthode `async` `Main`</span><span class="sxs-lookup"><span data-stu-id="8b5c1-111">`async` `Main` method</span></span>](#async-main)
  - <span data-ttu-id="8b5c1-112">Le point d’entrée pour une application peut avoir le modificateur `async`.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-112">The entry point for an application can have the `async` modifier.</span></span>
* [<span data-ttu-id="8b5c1-113">Expressions littérales `default`</span><span class="sxs-lookup"><span data-stu-id="8b5c1-113">`default` literal expressions</span></span>](#default-literal-expressions)
  - <span data-ttu-id="8b5c1-114">Vous pouvez utiliser des expressions littérales default dans les expressions de valeur par défaut quand le type cible peut être inféré.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-114">You can use default literal expressions in default value expressions when the target type can be inferred.</span></span>
* [<span data-ttu-id="8b5c1-115">Noms des éléments de tuple inférés</span><span class="sxs-lookup"><span data-stu-id="8b5c1-115">Inferred tuple element names</span></span>](#inferred-tuple-element-names)
  - <span data-ttu-id="8b5c1-116">Les noms des éléments de tuple peuvent être inférés dans de nombreux cas à partir de l’initialisation du tuple.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-116">The names of tuple elements can be inferred from tuple initialization in many cases.</span></span>

<span data-ttu-id="8b5c1-117">Enfin, le compilateur a deux options, `/refout` et `/refonly`, qui contrôlent la [génération d’assemblys de références](#reference-assembly-generation).</span><span class="sxs-lookup"><span data-stu-id="8b5c1-117">Finally, the compiler has two options `/refout` and `/refonly` that control [reference assembly generation](#reference-assembly-generation).</span></span>

## <a name="language-version-selection"></a><span data-ttu-id="8b5c1-118">Sélection de la version du langage</span><span class="sxs-lookup"><span data-stu-id="8b5c1-118">Language version selection</span></span>

<span data-ttu-id="8b5c1-119">Le compilateur C# prend en charge C# 7.1 à compter de Visual Studio 2017 version 15.3 ou du SDK .NET Core 2.0.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-119">The C# compiler supports C# 7.1 starting with Visual Studio 2017 version 15.3, or the .NET Core SDK 2.0.</span></span> <span data-ttu-id="8b5c1-120">Cependant, les fonctionnalités 7.1 sont désactivées par défaut.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-120">However, the 7.1 features are turned off by default.</span></span> <span data-ttu-id="8b5c1-121">Pour activer les fonctionnalités 7.1, vous devez modifier le paramètre de version du langage pour votre projet.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-121">To enable the 7.1 features, you need to change the language version setting for your project.</span></span>

<span data-ttu-id="8b5c1-122">Dans Visual Studio, cliquez avec le bouton droit sur le nœud du projet dans l’Explorateur de solutions, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-122">In Visual Studio, right-click on the project node in Solution Explorer and select **Properties**.</span></span> <span data-ttu-id="8b5c1-123">Sélectionnez l’onglet **Build**, puis sélectionnez le bouton **Avancé**.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-123">Select the **Build** tab and select the **Advanced** button.</span></span> <span data-ttu-id="8b5c1-124">Dans la liste déroulante, sélectionnez **Version mineure la plus récente de C# (latest)** ou la version spécifique **C# 7.1**, comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-124">In the dropdown, select **C# latest minor version (latest)**, or the specific version **C# 7.1** as shown in the image following.</span></span> <span data-ttu-id="8b5c1-125">La valeur `latest` signifie que vous voulez utiliser la dernière version mineure sur l’ordinateur actif.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-125">The `latest` value means you want to use the latest minor version on the current machine.</span></span> <span data-ttu-id="8b5c1-126">`C# 7.1` signifie que vous voulez utiliser C# 7.1, même après la publication de versions mineures plus récentes.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-126">The `C# 7.1` means that you want to use C# 7.1, even after newer minor versions are released.</span></span>

![Définition de la version du langage](./media/csharp-7-1/advanced-build-settings.png)

<span data-ttu-id="8b5c1-128">Vous pouvez aussi éditer le fichier « csproj », et ajouter ou modifier les lignes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-128">Alternatively, you can edit the "csproj" file and add or modify the following lines:</span></span>

```xml
<PropertyGroup>
  <LangVersion>latest</LangVersion>
</PropertyGroup>
```

> [!NOTE]
> <span data-ttu-id="8b5c1-129">Si vous utilisez l’IDE Visual Studio pour mettre à jour vos fichiers csproj, il crée des nœuds distincts pour chaque configuration de build.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-129">If you use the Visual Studio IDE to update your csproj files, the IDE creates separate nodes for each build configuration.</span></span> <span data-ttu-id="8b5c1-130">Vous définissez généralement la même valeur dans toutes les configurations de build, mais vous devez la définir explicitement pour chaque configuration de build ou sélectionner « Toutes les configurations » quand vous modifiez ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-130">You'll typically set the value the same in all build configurations, but you need to set it explicitly for each build configuration, or select "All Configurations" when you modify this setting.</span></span> <span data-ttu-id="8b5c1-131">Vous voyez alors ceci dans votre fichier csproj :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-131">You'll see the following in your csproj file:</span></span>

```xml
<PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Release|AnyCPU'">
  <LangVersion>latest</LangVersion>
</PropertyGroup>

<PropertyGroup Condition="'$(Configuration)|$(Platform)'=='Debug|AnyCPU'">
  <LangVersion>latest</LangVersion>
</PropertyGroup>
```

<span data-ttu-id="8b5c1-132">Les valeurs valides pour l’élément `LangVersion` sont :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-132">Valid settings for the `LangVersion` element are:</span></span>

* `ISO-1`
* `ISO-2`
* `3`
* `4`
* `5`
* `6`
* `7`
* `7.1`
* `default`
* `latest`

<span data-ttu-id="8b5c1-133">Les chaînes spéciales `default` et `latest` définissent respectivement la dernière version majeure et la dernière version mineure du langage installées sur l’ordinateur de build.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-133">The special strings `default` and `latest` resolve to the latest major and minor language versions installed on the build machine, respectively.</span></span>

<span data-ttu-id="8b5c1-134">Ce paramètre dissocie l’installation de nouvelles versions du SDK et des outils dans votre environnement de développement du choix d’incorporer les nouvelles fonctionnalités du langage dans un projet.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-134">This setting decouples installing new versions of the SDK and tools in your development environment from choosing to incorporate new language features in a project.</span></span> <span data-ttu-id="8b5c1-135">Vous pouvez installer la dernière version du SDK et des outils sur votre ordinateur de build.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-135">You can install the latest SDK and tools on your build machine.</span></span> <span data-ttu-id="8b5c1-136">Chaque projet peut être configuré pour utiliser une version spécifique du langage pour sa build.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-136">Each project can be configured to use a specific version of the language for its build.</span></span>

## <a name="async-main"></a><span data-ttu-id="8b5c1-137">Async main</span><span class="sxs-lookup"><span data-stu-id="8b5c1-137">Async main</span></span>

<span data-ttu-id="8b5c1-138">Une méthode *async main* vous permet d’utiliser `await` dans votre méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-138">An *async main* method enables you to use `await` in your `Main` method.</span></span>
<span data-ttu-id="8b5c1-139">Auparavant, vous deviez écrire :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-139">Previously you would need to write:</span></span>

```csharp
static int Main()
{
    return DoAsyncWork().GetAwaiter().GetResult();
}
```

<span data-ttu-id="8b5c1-140">Vous pouvez désormais écrire :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-140">You can now write:</span></span>

```csharp
static async Task<int> Main()
{
    // This could also be replaced with the body
    // DoAsyncWork, including its await expressions:
    return await DoAsyncWork();
}
```

<span data-ttu-id="8b5c1-141">Si votre programme ne retourne pas de code de sortie, vous pouvez déclarer une méthode `Main` qui retourne une <xref:System.Threading.Tasks.Task> :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-141">If your program doesn't return an exit code, you can declare a `Main` method that returns a <xref:System.Threading.Tasks.Task>:</span></span>

```csharp
static async Task Main()
{
    await SomeAsyncMethod();
}
```

<span data-ttu-id="8b5c1-142">Pour plus d’informations, consultez la rubrique [async main](../programming-guide/main-and-command-args/index.md) dans le Guide de programmation.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-142">You can read more about the details in the [async main](../programming-guide/main-and-command-args/index.md) topic in the programming guide.</span></span>

## <a name="default-literal-expressions"></a><span data-ttu-id="8b5c1-143">Expressions littérales par défaut</span><span class="sxs-lookup"><span data-stu-id="8b5c1-143">Default literal expressions</span></span>

<span data-ttu-id="8b5c1-144">Les expressions littérales par défaut sont une amélioration des expressions de valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-144">Default literal expressions are an enhancement to default value expressions.</span></span>
<span data-ttu-id="8b5c1-145">Ces expressions initialisent une variable à la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-145">These expressions initialize a variable to the default value.</span></span> <span data-ttu-id="8b5c1-146">Vous deviez écrire auparavant :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-146">Where you previously would write:</span></span>

```csharp
Func<string, bool> whereClause = default(Func<string, bool>);
```

<span data-ttu-id="8b5c1-147">Vous pouvez désormais omettre le type du côté droit de l’initialisation :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-147">You can now omit the type on the right-hand side of the initialization:</span></span>

```csharp
Func<string, bool> whereClause = default;
```

<span data-ttu-id="8b5c1-148">Pour plus d’informations sur cette amélioration, consultez la rubrique [Expressions de valeur par défaut](../programming-guide/statements-expressions-operators/default-value-expressions.md) dans le Guide de programmation C# .</span><span class="sxs-lookup"><span data-stu-id="8b5c1-148">You can learn more about this enhancement in the C# Programming Guide topic on [default value expressions](../programming-guide/statements-expressions-operators/default-value-expressions.md).</span></span>

<span data-ttu-id="8b5c1-149">Cette amélioration change également certaines des règles d’analyse pour le [mot clé default](../language-reference/keywords/default.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c1-149">This enhancement also changes some of the parsing rules for the [default keyword](../language-reference/keywords/default.md).</span></span>

## <a name="inferred-tuple-element-names"></a><span data-ttu-id="8b5c1-150">Noms des éléments de tuple inférés</span><span class="sxs-lookup"><span data-stu-id="8b5c1-150">Inferred tuple element names</span></span>

<span data-ttu-id="8b5c1-151">Cette fonctionnalité est une petite amélioration de la fonctionnalité des tuples introduite dans C# 7.0.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-151">This feature is a small enhancement to the tuples feature introduced in C# 7.0.</span></span> <span data-ttu-id="8b5c1-152">Très souvent, quand vous initialisez un tuple, les variables utilisées pour le côté droit de l’affectation sont identiques aux noms que vous souhaitez pour les éléments du tuple :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-152">Many times when you initialize a tuple, the variables used for the right side of the assignment are the same as the names you'd like for the tuple elements:</span></span>

```csharp
int count = 5;
string label = "Colors used in the map";
var pair = (count: count, label: label);
```

<span data-ttu-id="8b5c1-153">Dans C# 7.1, les noms des éléments du tuple peuvent être inférés à partir des variables utilisées pour initialiser le tuple :</span><span class="sxs-lookup"><span data-stu-id="8b5c1-153">The names of tuple elements can be inferred from the variables used to initialize the tuple in C# 7.1:</span></span>

```csharp
int count = 5;
string label = "Colors used in the map";
var pair = (count, label); // element names are "count" and "label"
```

<span data-ttu-id="8b5c1-154">Pour plus d’informations sur cette fonctionnalité, consultez la rubrique [Tuples](../tuples.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c1-154">You can learn more about this feature in the [Tuples](../tuples.md) topic.</span></span>

## <a name="reference-assembly-generation"></a><span data-ttu-id="8b5c1-155">Génération d’assemblys de références</span><span class="sxs-lookup"><span data-stu-id="8b5c1-155">Reference assembly generation</span></span>

<span data-ttu-id="8b5c1-156">Il existe deux nouvelles options du compilateur qui génèrent des *assemblys de références uniquement* : [/refout](../language-reference/compiler-options/refout-compiler-option.md) et [/refonly](../language-reference/compiler-options/refonly-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="8b5c1-156">There are two new compiler options that generate *reference-only assemblies*: [/refout](../language-reference/compiler-options/refout-compiler-option.md) and [/refonly](../language-reference/compiler-options/refonly-compiler-option.md).</span></span>
<span data-ttu-id="8b5c1-157">Les rubriques en lien expliquent ces options et les assemblys de références plus en détails.</span><span class="sxs-lookup"><span data-stu-id="8b5c1-157">The linked topics explain these options and reference assemblies in more detail.</span></span>
