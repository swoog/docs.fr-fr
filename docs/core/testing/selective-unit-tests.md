---
title: Exécution de tests unitaires sélectifs
description: Vous montre comment utiliser une expression de filtre pour exécuter des tests unitaires sélectifs avec la commande de test dotnet.
author: smadala
ms.author: mairaw
ms.date: 03/22/2017
ms.openlocfilehash: 428e31014f5d8d487deb7c4b4317ebcef13c294d
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42935178"
---
# <a name="running-selective-unit-tests"></a><span data-ttu-id="4596d-103">Exécution de tests unitaires sélectifs</span><span class="sxs-lookup"><span data-stu-id="4596d-103">Running selective unit tests</span></span>

<span data-ttu-id="4596d-104">Les exemples suivants utilisent `dotnet test`.</span><span class="sxs-lookup"><span data-stu-id="4596d-104">The following examples use `dotnet test`.</span></span> <span data-ttu-id="4596d-105">Si vous utilisez `vstest.console.exe`, remplacez `--filter ` par `--testcasefilter:`.</span><span class="sxs-lookup"><span data-stu-id="4596d-105">If you're using `vstest.console.exe`, replace `--filter ` with `--testcasefilter:`.</span></span>

## <a name="mstest"></a><span data-ttu-id="4596d-106">MSTest</span><span class="sxs-lookup"><span data-stu-id="4596d-106">MSTest</span></span>

```csharp
using Microsoft.VisualStudio.TestTools.UnitTesting;

namespace MSTestNamespace
{
    [TestClass]
    public class UnitTest1
    {
        [TestCategory("CategoryA")]
        [Priority(1)]
        [TestMethod]
        public void TestMethod1()
        {
        }

        [Priority(2)]
        [TestMethod]
        public void TestMethod2()
        {
        }
    }
}
```

| <span data-ttu-id="4596d-107">Expression</span><span class="sxs-lookup"><span data-stu-id="4596d-107">Expression</span></span> | <span data-ttu-id="4596d-108">Résultat</span><span class="sxs-lookup"><span data-stu-id="4596d-108">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="4596d-109">Exécute les tests dont `FullyQualifiedName` contient `Method`.</span><span class="sxs-lookup"><span data-stu-id="4596d-109">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="4596d-110">Disponible dans `vstest 15.1+`.</span><span class="sxs-lookup"><span data-stu-id="4596d-110">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="4596d-111">Exécute les tests dont le nom contient `TestMethod1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-111">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter ClassName=MSTestNamespace.UnitTest1` | <span data-ttu-id="4596d-112">Exécute les tests qui sont dans la classe `MSTestNamespace.UnitTest1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-112">Runs tests which are in class `MSTestNamespace.UnitTest1`.</span></span><br><span data-ttu-id="4596d-113">**Remarque :** La valeur `ClassName` doit avoir un espace de noms, donc `ClassName=UnitTest1` ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="4596d-113">**Note:** The `ClassName` value should have a namespace, so `ClassName=UnitTest1` won't work.</span></span> |
| `dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="4596d-114">Exécute tous les tests sauf `MSTestNamespace.UnitTest1.TestMethod1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-114">Runs all tests except `MSTestNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="4596d-115">Exécute les tests qui sont annotés avec `[TestCategory("CategoryA")]`.</span><span class="sxs-lookup"><span data-stu-id="4596d-115">Runs tests which are annotated with `[TestCategory("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="4596d-116">Exécute les tests qui sont annotés avec `[Priority(2)]`.</span><span class="sxs-lookup"><span data-stu-id="4596d-116">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="4596d-117">**Utilisation des opérateurs conditionnels | et &amp;**</span><span class="sxs-lookup"><span data-stu-id="4596d-117">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="4596d-118">Expression</span><span class="sxs-lookup"><span data-stu-id="4596d-118">Expression</span></span> | <span data-ttu-id="4596d-119">Résultat</span><span class="sxs-lookup"><span data-stu-id="4596d-119">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="4596d-120">Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **ou** `TestCategory` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="4596d-120">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="4596d-121">Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **et** `TestCategory` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="4596d-121">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="4596d-122">Exécute les tests qui ont un `FullyQualifiedName` contenant `UnitTest1` **et** `TestCategory` est `CategoryA` **ou** `Priority` est 1.</span><span class="sxs-lookup"><span data-stu-id="4596d-122">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="xunit"></a><span data-ttu-id="4596d-123">xUnit</span><span class="sxs-lookup"><span data-stu-id="4596d-123">xUnit</span></span>

```csharp
using Xunit;

namespace XUnitNamespace
{
    public class TestClass1
    {
        [Trait("Category", "CategoryA")]
        [Trait("Priority", "1")]
        [Fact]
        public void Test1()
        {
        }

        [Trait("Priority", "2")]
        [Fact]
        public void Test2()
        {
        }
    }
}
```

| <span data-ttu-id="4596d-124">Expression</span><span class="sxs-lookup"><span data-stu-id="4596d-124">Expression</span></span> | <span data-ttu-id="4596d-125">Résultat</span><span class="sxs-lookup"><span data-stu-id="4596d-125">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter DisplayName=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="4596d-126">Exécute uniquement un test, `XUnitNamespace.TestClass1.Test1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-126">Runs only one test, `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter FullyQualifiedName!=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="4596d-127">Exécute tous les tests sauf `XUnitNamespace.TestClass1.Test1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-127">Runs all tests except `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter DisplayName~TestClass1` | <span data-ttu-id="4596d-128">Exécute les tests dont le nom d’affichage contient `TestClass1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-128">Runs tests whose display name contains `TestClass1`.</span></span> |

<span data-ttu-id="4596d-129">Dans l’exemple de code, les caractéristiques définies avec les clés `Category` et `Priority` peuvent être utilisées pour filtrer.</span><span class="sxs-lookup"><span data-stu-id="4596d-129">In the code example, the defined traits with keys `Category` and `Priority` can be used for filtering.</span></span>

| <span data-ttu-id="4596d-130">Expression</span><span class="sxs-lookup"><span data-stu-id="4596d-130">Expression</span></span> | <span data-ttu-id="4596d-131">Résultat</span><span class="sxs-lookup"><span data-stu-id="4596d-131">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter XUnit` | <span data-ttu-id="4596d-132">Exécute les tests dont `FullyQualifiedName` contient `XUnit`.</span><span class="sxs-lookup"><span data-stu-id="4596d-132">Runs tests whose `FullyQualifiedName` contains `XUnit`.</span></span>  <span data-ttu-id="4596d-133">Disponible dans `vstest 15.1+`.</span><span class="sxs-lookup"><span data-stu-id="4596d-133">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Category=CategoryA` | <span data-ttu-id="4596d-134">Exécute les tests qui ont `[Trait("Category", "CategoryA")]`.</span><span class="sxs-lookup"><span data-stu-id="4596d-134">Runs tests which have `[Trait("Category", "CategoryA")]`.</span></span> |

<span data-ttu-id="4596d-135">**Utilisation des opérateurs conditionnels | et &amp;**</span><span class="sxs-lookup"><span data-stu-id="4596d-135">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="4596d-136">Expression</span><span class="sxs-lookup"><span data-stu-id="4596d-136">Expression</span></span> | <span data-ttu-id="4596d-137">Résultat</span><span class="sxs-lookup"><span data-stu-id="4596d-137">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~TestClass1&#124;Category=CategoryA"</code> | <span data-ttu-id="4596d-138">Exécute les tests qui ont `TestClass1` dans `FullyQualifiedName` **ou** `Category` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="4596d-138">Runs tests which has `TestClass1` in `FullyQualifiedName` **or** `Category` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~TestClass1&Category=CategoryA"` | <span data-ttu-id="4596d-139">Exécute les tests qui ont `TestClass1` dans `FullyQualifiedName` **et** `Category` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="4596d-139">Runs tests which has `TestClass1` in `FullyQualifiedName` **and** `Category` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~TestClass1&Category=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="4596d-140">Exécute les tests qui ont un `FullyQualifiedName` contenant `TestClass1` **et** `Category` est `CategoryA` **ou** `Priority` est 1.</span><span class="sxs-lookup"><span data-stu-id="4596d-140">Runs tests which have either `FullyQualifiedName` containing `TestClass1` **and** `Category` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="nunit"></a><span data-ttu-id="4596d-141">NUnit</span><span class="sxs-lookup"><span data-stu-id="4596d-141">NUnit</span></span>

```csharp
using NUnit.Framework;

namespace NUnitNamespace
{
    public class UnitTest1
    {
        [Category("CategoryA")]
        [Property("Priority", 1)]
        [Test]
        public void TestMethod1()
        {
        }

        [Property("Priority", 2)]
        [Test]
        public void TestMethod2()
        {
        }
    }
}
```

| <span data-ttu-id="4596d-142">Expression</span><span class="sxs-lookup"><span data-stu-id="4596d-142">Expression</span></span> | <span data-ttu-id="4596d-143">Résultat</span><span class="sxs-lookup"><span data-stu-id="4596d-143">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="4596d-144">Exécute les tests dont `FullyQualifiedName` contient `Method`.</span><span class="sxs-lookup"><span data-stu-id="4596d-144">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="4596d-145">Disponible dans `vstest 15.1+`.</span><span class="sxs-lookup"><span data-stu-id="4596d-145">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="4596d-146">Exécute les tests dont le nom contient `TestMethod1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-146">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter FullyQualifiedName~NUnitNamespace.UnitTest1` | <span data-ttu-id="4596d-147">Exécute les tests qui sont dans la classe `NUnitNamespace.UnitTest1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-147">Runs tests which are in class `NUnitNamespace.UnitTest1`.</span></span><br>
| `dotnet test --filter FullyQualifiedName!=NUnitNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="4596d-148">Exécute tous les tests sauf `NUnitNamespace.UnitTest1.TestMethod1`.</span><span class="sxs-lookup"><span data-stu-id="4596d-148">Runs all tests except `NUnitNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="4596d-149">Exécute les tests qui sont annotés avec `[Category("CategoryA")]`.</span><span class="sxs-lookup"><span data-stu-id="4596d-149">Runs tests which are annotated with `[Category("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="4596d-150">Exécute les tests qui sont annotés avec `[Priority(2)]`.</span><span class="sxs-lookup"><span data-stu-id="4596d-150">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="4596d-151">**Utilisation des opérateurs conditionnels | et &amp;**</span><span class="sxs-lookup"><span data-stu-id="4596d-151">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="4596d-152">Expression</span><span class="sxs-lookup"><span data-stu-id="4596d-152">Expression</span></span> | <span data-ttu-id="4596d-153">Résultat</span><span class="sxs-lookup"><span data-stu-id="4596d-153">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="4596d-154">Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **ou** `TestCategory` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="4596d-154">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="4596d-155">Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **et** `TestCategory` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="4596d-155">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="4596d-156">Exécute les tests qui ont un `FullyQualifiedName` contenant `UnitTest1` **et** `TestCategory` est `CategoryA` **ou** `Priority` est 1.</span><span class="sxs-lookup"><span data-stu-id="4596d-156">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |
