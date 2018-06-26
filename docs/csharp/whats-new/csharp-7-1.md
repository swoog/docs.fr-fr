---
title: Nouveautés de C# 7.1
description: Vue d’ensemble des nouvelles fonctionnalités de C# 7.1.
ms.date: 08/16/2017
ms.openlocfilehash: 565db102284424f9d8f6fa04ec9c74b52c9da0e6
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34728652"
---
# <a name="whats-new-in-c-71"></a><span data-ttu-id="ed9ce-103">Nouveautés de C# 7.1</span><span class="sxs-lookup"><span data-stu-id="ed9ce-103">What's new in C# 7.1</span></span>

<span data-ttu-id="ed9ce-104">C# 7.1 est la première version mineure pour le langage C#.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-104">C# 7.1 is the first point release to the C# language.</span></span> <span data-ttu-id="ed9ce-105">Elle marque une cadence de publication accrue pour le langage.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-105">It marks an increased release cadence for the language.</span></span> <span data-ttu-id="ed9ce-106">Vous pouvez utiliser les nouvelles fonctionnalités plus tôt, dans l’idéal quand chaque nouvelle fonctionnalité est prête.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-106">You can use the new features sooner, ideally when each new feature is ready.</span></span> <span data-ttu-id="ed9ce-107">C# 7.1 ajoute la possibilité de configurer le compilateur pour le faire correspondre à une version spécifiée du langage.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-107">C# 7.1 adds the ability to configure the compiler to match a specified version of the language.</span></span> <span data-ttu-id="ed9ce-108">Ceci vous permet de séparer la décision de mettre à niveau les outils de la décision de mettre à niveau les versions du langage.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-108">That enables you to separate the decision to upgrade tools from the decision to upgrade language versions.</span></span>

<span data-ttu-id="ed9ce-109">C# 7.1 ajoute l’élément de configuration de [sélection de la version du langage](../language-reference/configure-language-version.md), trois nouvelles fonctionnalités du langage et un nouveau comportement du compilateur.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-109">C# 7.1 adds the [language version selection](../language-reference/configure-language-version.md) configuration element, three new language features and new compiler behavior.</span></span>

<span data-ttu-id="ed9ce-110">Les nouvelles fonctionnalités de langage de cette version sont :</span><span class="sxs-lookup"><span data-stu-id="ed9ce-110">The new language features in this release are:</span></span>

* [<span data-ttu-id="ed9ce-111">Méthode `async` `Main`</span><span class="sxs-lookup"><span data-stu-id="ed9ce-111">`async` `Main` method</span></span>](#async-main)
  - <span data-ttu-id="ed9ce-112">Le point d’entrée pour une application peut avoir le modificateur `async`.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-112">The entry point for an application can have the `async` modifier.</span></span>
* [<span data-ttu-id="ed9ce-113">Expressions littérales `default`</span><span class="sxs-lookup"><span data-stu-id="ed9ce-113">`default` literal expressions</span></span>](#default-literal-expressions)
  - <span data-ttu-id="ed9ce-114">Vous pouvez utiliser des expressions littérales default dans les expressions de valeur par défaut quand le type cible peut être inféré.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-114">You can use default literal expressions in default value expressions when the target type can be inferred.</span></span>
* [<span data-ttu-id="ed9ce-115">Noms des éléments de tuple inférés</span><span class="sxs-lookup"><span data-stu-id="ed9ce-115">Inferred tuple element names</span></span>](#inferred-tuple-element-names)
  - <span data-ttu-id="ed9ce-116">Les noms des éléments de tuple peuvent être inférés dans de nombreux cas à partir de l’initialisation du tuple.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-116">The names of tuple elements can be inferred from tuple initialization in many cases.</span></span>

<span data-ttu-id="ed9ce-117">Enfin, le compilateur a deux options, `/refout` et `/refonly`, qui contrôlent la [génération d’assemblys de références](#reference-assembly-generation).</span><span class="sxs-lookup"><span data-stu-id="ed9ce-117">Finally, the compiler has two options `/refout` and `/refonly` that control [reference assembly generation](#reference-assembly-generation).</span></span>

<span data-ttu-id="ed9ce-118">Pour utiliser les fonctionnalités les plus récentes dans une version mineure, vous devez [configurer la version du langage du compilateur](../language-reference/configure-language-version.md) et sélectionner la version.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-118">To use the latest features in a point release, you need to [configure the compiler language version](../language-reference/configure-language-version.md) and select the version.</span></span>

## <a name="async-main"></a><span data-ttu-id="ed9ce-119">Async main</span><span class="sxs-lookup"><span data-stu-id="ed9ce-119">Async main</span></span>

<span data-ttu-id="ed9ce-120">Une méthode *async main* vous permet d’utiliser `await` dans votre méthode `Main`.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-120">An *async main* method enables you to use `await` in your `Main` method.</span></span>
<span data-ttu-id="ed9ce-121">Auparavant, vous deviez écrire :</span><span class="sxs-lookup"><span data-stu-id="ed9ce-121">Previously you would need to write:</span></span>

```csharp
static int Main()
{
    return DoAsyncWork().GetAwaiter().GetResult();
}
```

<span data-ttu-id="ed9ce-122">Vous pouvez désormais écrire :</span><span class="sxs-lookup"><span data-stu-id="ed9ce-122">You can now write:</span></span>

```csharp
static async Task<int> Main()
{
    // This could also be replaced with the body
    // DoAsyncWork, including its await expressions:
    return await DoAsyncWork();
}
```

<span data-ttu-id="ed9ce-123">Si votre programme ne retourne pas de code de sortie, vous pouvez déclarer une méthode `Main` qui retourne une <xref:System.Threading.Tasks.Task> :</span><span class="sxs-lookup"><span data-stu-id="ed9ce-123">If your program doesn't return an exit code, you can declare a `Main` method that returns a <xref:System.Threading.Tasks.Task>:</span></span>

```csharp
static async Task Main()
{
    await SomeAsyncMethod();
}
```

<span data-ttu-id="ed9ce-124">Pour plus d’informations, consultez la rubrique [async main](../programming-guide/main-and-command-args/index.md) dans le Guide de programmation.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-124">You can read more about the details in the [async main](../programming-guide/main-and-command-args/index.md) topic in the programming guide.</span></span>

## <a name="default-literal-expressions"></a><span data-ttu-id="ed9ce-125">Expressions littérales par défaut</span><span class="sxs-lookup"><span data-stu-id="ed9ce-125">Default literal expressions</span></span>

<span data-ttu-id="ed9ce-126">Les expressions littérales par défaut sont une amélioration des expressions de valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-126">Default literal expressions are an enhancement to default value expressions.</span></span>
<span data-ttu-id="ed9ce-127">Ces expressions initialisent une variable à la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-127">These expressions initialize a variable to the default value.</span></span> <span data-ttu-id="ed9ce-128">Vous deviez écrire auparavant :</span><span class="sxs-lookup"><span data-stu-id="ed9ce-128">Where you previously would write:</span></span>

```csharp
Func<string, bool> whereClause = default(Func<string, bool>);
```

<span data-ttu-id="ed9ce-129">Vous pouvez désormais omettre le type du côté droit de l’initialisation :</span><span class="sxs-lookup"><span data-stu-id="ed9ce-129">You can now omit the type on the right-hand side of the initialization:</span></span>

```csharp
Func<string, bool> whereClause = default;
```

<span data-ttu-id="ed9ce-130">Pour plus d’informations sur cette amélioration, consultez la rubrique [Expressions de valeur par défaut](../programming-guide/statements-expressions-operators/default-value-expressions.md) dans le Guide de programmation C# .</span><span class="sxs-lookup"><span data-stu-id="ed9ce-130">You can learn more about this enhancement in the C# Programming Guide topic on [default value expressions](../programming-guide/statements-expressions-operators/default-value-expressions.md).</span></span>

<span data-ttu-id="ed9ce-131">Cette amélioration change également certaines des règles d’analyse pour le [mot clé default](../language-reference/keywords/default.md).</span><span class="sxs-lookup"><span data-stu-id="ed9ce-131">This enhancement also changes some of the parsing rules for the [default keyword](../language-reference/keywords/default.md).</span></span>

## <a name="inferred-tuple-element-names"></a><span data-ttu-id="ed9ce-132">Noms des éléments de tuple inférés</span><span class="sxs-lookup"><span data-stu-id="ed9ce-132">Inferred tuple element names</span></span>

<span data-ttu-id="ed9ce-133">Cette fonctionnalité est une petite amélioration de la fonctionnalité des tuples introduite dans C# 7.0.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-133">This feature is a small enhancement to the tuples feature introduced in C# 7.0.</span></span> <span data-ttu-id="ed9ce-134">Très souvent, quand vous initialisez un tuple, les variables utilisées pour le côté droit de l’affectation sont identiques aux noms que vous souhaitez pour les éléments du tuple :</span><span class="sxs-lookup"><span data-stu-id="ed9ce-134">Many times when you initialize a tuple, the variables used for the right side of the assignment are the same as the names you'd like for the tuple elements:</span></span>

```csharp
int count = 5;
string label = "Colors used in the map";
var pair = (count: count, label: label);
```

<span data-ttu-id="ed9ce-135">Dans C# 7.1, les noms des éléments du tuple peuvent être inférés à partir des variables utilisées pour initialiser le tuple :</span><span class="sxs-lookup"><span data-stu-id="ed9ce-135">The names of tuple elements can be inferred from the variables used to initialize the tuple in C# 7.1:</span></span>

```csharp
int count = 5;
string label = "Colors used in the map";
var pair = (count, label); // element names are "count" and "label"
```

<span data-ttu-id="ed9ce-136">Pour plus d’informations sur cette fonctionnalité, consultez la rubrique [Tuples](../tuples.md).</span><span class="sxs-lookup"><span data-stu-id="ed9ce-136">You can learn more about this feature in the [Tuples](../tuples.md) topic.</span></span>

## <a name="reference-assembly-generation"></a><span data-ttu-id="ed9ce-137">Génération d’assemblys de références</span><span class="sxs-lookup"><span data-stu-id="ed9ce-137">Reference assembly generation</span></span>

<span data-ttu-id="ed9ce-138">Il existe deux nouvelles options du compilateur qui génèrent des *assemblys de références uniquement* : [/refout](../language-reference/compiler-options/refout-compiler-option.md) et [/refonly](../language-reference/compiler-options/refonly-compiler-option.md).</span><span class="sxs-lookup"><span data-stu-id="ed9ce-138">There are two new compiler options that generate *reference-only assemblies*: [/refout](../language-reference/compiler-options/refout-compiler-option.md) and [/refonly](../language-reference/compiler-options/refonly-compiler-option.md).</span></span>
<span data-ttu-id="ed9ce-139">Les rubriques en lien expliquent ces options et les assemblys de références plus en détails.</span><span class="sxs-lookup"><span data-stu-id="ed9ce-139">The linked topics explain these options and reference assemblies in more detail.</span></span>
