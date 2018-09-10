---
title: Exécution de tests unitaires sélectifs
description: Vous montre comment utiliser une expression de filtre pour exécuter des tests unitaires sélectifs avec la commande de test dotnet.
author: smadala
ms.author: mairaw
ms.date: 03/22/2017
ms.openlocfilehash: 428e31014f5d8d487deb7c4b4317ebcef13c294d
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43517218"
---
# <a name="running-selective-unit-tests"></a><span data-ttu-id="8621f-103">Exécution de tests unitaires sélectifs</span><span class="sxs-lookup"><span data-stu-id="8621f-103">Running selective unit tests</span></span>

<span data-ttu-id="8621f-104">Les exemples suivants utilisent `dotnet test`.</span><span class="sxs-lookup"><span data-stu-id="8621f-104">The following examples use `dotnet test`.</span></span> <span data-ttu-id="8621f-105">Si vous utilisez `vstest.console.exe`, remplacez `--filter ` par `--testcasefilter:`.</span><span class="sxs-lookup"><span data-stu-id="8621f-105">If you're using `vstest.console.exe`, replace `--filter ` with `--testcasefilter:`.</span></span>

## <a name="mstest"></a><span data-ttu-id="8621f-106">MSTest</span><span class="sxs-lookup"><span data-stu-id="8621f-106">MSTest</span></span>

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

| <span data-ttu-id="8621f-107">Expression</span><span class="sxs-lookup"><span data-stu-id="8621f-107">Expression</span></span> | <span data-ttu-id="8621f-108">Résultat</span><span class="sxs-lookup"><span data-stu-id="8621f-108">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="8621f-109">Exécute les tests dont `FullyQualifiedName` contient `Method`.</span><span class="sxs-lookup"><span data-stu-id="8621f-109">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="8621f-110">Disponible dans `vstest 15.1+`.</span><span class="sxs-lookup"><span data-stu-id="8621f-110">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="8621f-111">Exécute les tests dont le nom contient `TestMethod1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-111">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter ClassName=MSTestNamespace.UnitTest1` | <span data-ttu-id="8621f-112">Exécute les tests qui sont dans la classe `MSTestNamespace.UnitTest1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-112">Runs tests which are in class `MSTestNamespace.UnitTest1`.</span></span><br><span data-ttu-id="8621f-113">**Remarque :** La valeur `ClassName` doit avoir un espace de noms, donc `ClassName=UnitTest1` ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="8621f-113">**Note:** The `ClassName` value should have a namespace, so `ClassName=UnitTest1` won't work.</span></span> |
| `dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="8621f-114">Exécute tous les tests sauf `MSTestNamespace.UnitTest1.TestMethod1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-114">Runs all tests except `MSTestNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="8621f-115">Exécute les tests qui sont annotés avec `[TestCategory("CategoryA")]`.</span><span class="sxs-lookup"><span data-stu-id="8621f-115">Runs tests which are annotated with `[TestCategory("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="8621f-116">Exécute les tests qui sont annotés avec `[Priority(2)]`.</span><span class="sxs-lookup"><span data-stu-id="8621f-116">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="8621f-117">**Utilisation des opérateurs conditionnels | et &amp;**</span><span class="sxs-lookup"><span data-stu-id="8621f-117">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="8621f-118">Expression</span><span class="sxs-lookup"><span data-stu-id="8621f-118">Expression</span></span> | <span data-ttu-id="8621f-119">Résultat</span><span class="sxs-lookup"><span data-stu-id="8621f-119">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="8621f-120">Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **ou** `TestCategory` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="8621f-120">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="8621f-121">Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **et** `TestCategory` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="8621f-121">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="8621f-122">Exécute les tests qui ont un `FullyQualifiedName` contenant `UnitTest1` **et** `TestCategory` est `CategoryA` **ou** `Priority` est 1.</span><span class="sxs-lookup"><span data-stu-id="8621f-122">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="xunit"></a><span data-ttu-id="8621f-123">xUnit</span><span class="sxs-lookup"><span data-stu-id="8621f-123">xUnit</span></span>

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

| <span data-ttu-id="8621f-124">Expression</span><span class="sxs-lookup"><span data-stu-id="8621f-124">Expression</span></span> | <span data-ttu-id="8621f-125">Résultat</span><span class="sxs-lookup"><span data-stu-id="8621f-125">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter DisplayName=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="8621f-126">Exécute uniquement un test, `XUnitNamespace.TestClass1.Test1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-126">Runs only one test, `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter FullyQualifiedName!=XUnitNamespace.TestClass1.Test1` | <span data-ttu-id="8621f-127">Exécute tous les tests sauf `XUnitNamespace.TestClass1.Test1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-127">Runs all tests except `XUnitNamespace.TestClass1.Test1`.</span></span> |
| `dotnet test --filter DisplayName~TestClass1` | <span data-ttu-id="8621f-128">Exécute les tests dont le nom d’affichage contient `TestClass1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-128">Runs tests whose display name contains `TestClass1`.</span></span> |

<span data-ttu-id="8621f-129">Dans l’exemple de code, les caractéristiques définies avec les clés `Category` et `Priority` peuvent être utilisées pour filtrer.</span><span class="sxs-lookup"><span data-stu-id="8621f-129">In the code example, the defined traits with keys `Category` and `Priority` can be used for filtering.</span></span>

| <span data-ttu-id="8621f-130">Expression</span><span class="sxs-lookup"><span data-stu-id="8621f-130">Expression</span></span> | <span data-ttu-id="8621f-131">Résultat</span><span class="sxs-lookup"><span data-stu-id="8621f-131">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter XUnit` | <span data-ttu-id="8621f-132">Exécute les tests dont `FullyQualifiedName` contient `XUnit`.</span><span class="sxs-lookup"><span data-stu-id="8621f-132">Runs tests whose `FullyQualifiedName` contains `XUnit`.</span></span>  <span data-ttu-id="8621f-133">Disponible dans `vstest 15.1+`.</span><span class="sxs-lookup"><span data-stu-id="8621f-133">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Category=CategoryA` | <span data-ttu-id="8621f-134">Exécute les tests qui ont `[Trait("Category", "CategoryA")]`.</span><span class="sxs-lookup"><span data-stu-id="8621f-134">Runs tests which have `[Trait("Category", "CategoryA")]`.</span></span> |

<span data-ttu-id="8621f-135">**Utilisation des opérateurs conditionnels | et &amp;**</span><span class="sxs-lookup"><span data-stu-id="8621f-135">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="8621f-136">Expression</span><span class="sxs-lookup"><span data-stu-id="8621f-136">Expression</span></span> | <span data-ttu-id="8621f-137">Résultat</span><span class="sxs-lookup"><span data-stu-id="8621f-137">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~TestClass1&#124;Category=CategoryA"</code> | <span data-ttu-id="8621f-138">Exécute les tests qui ont `TestClass1` dans `FullyQualifiedName` **ou** `Category` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="8621f-138">Runs tests which has `TestClass1` in `FullyQualifiedName` **or** `Category` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~TestClass1&Category=CategoryA"` | <span data-ttu-id="8621f-139">Exécute les tests qui ont `TestClass1` dans `FullyQualifiedName` **et** `Category` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="8621f-139">Runs tests which has `TestClass1` in `FullyQualifiedName` **and** `Category` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~TestClass1&Category=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="8621f-140">Exécute les tests qui ont un `FullyQualifiedName` contenant `TestClass1` **et** `Category` est `CategoryA` **ou** `Priority` est 1.</span><span class="sxs-lookup"><span data-stu-id="8621f-140">Runs tests which have either `FullyQualifiedName` containing `TestClass1` **and** `Category` is `CategoryA` **or** `Priority` is 1.</span></span> |

## <a name="nunit"></a><span data-ttu-id="8621f-141">NUnit</span><span class="sxs-lookup"><span data-stu-id="8621f-141">NUnit</span></span>

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

| <span data-ttu-id="8621f-142">Expression</span><span class="sxs-lookup"><span data-stu-id="8621f-142">Expression</span></span> | <span data-ttu-id="8621f-143">Résultat</span><span class="sxs-lookup"><span data-stu-id="8621f-143">Result</span></span> |
| ---------- | ------ |
| `dotnet test --filter Method` | <span data-ttu-id="8621f-144">Exécute les tests dont `FullyQualifiedName` contient `Method`.</span><span class="sxs-lookup"><span data-stu-id="8621f-144">Runs tests whose `FullyQualifiedName` contains `Method`.</span></span> <span data-ttu-id="8621f-145">Disponible dans `vstest 15.1+`.</span><span class="sxs-lookup"><span data-stu-id="8621f-145">Available in `vstest 15.1+`.</span></span> |
| `dotnet test --filter Name~TestMethod1` | <span data-ttu-id="8621f-146">Exécute les tests dont le nom contient `TestMethod1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-146">Runs tests whose name contains `TestMethod1`.</span></span> |
| `dotnet test --filter FullyQualifiedName~NUnitNamespace.UnitTest1` | <span data-ttu-id="8621f-147">Exécute les tests qui sont dans la classe `NUnitNamespace.UnitTest1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-147">Runs tests which are in class `NUnitNamespace.UnitTest1`.</span></span><br>
| `dotnet test --filter FullyQualifiedName!=NUnitNamespace.UnitTest1.TestMethod1` | <span data-ttu-id="8621f-148">Exécute tous les tests sauf `NUnitNamespace.UnitTest1.TestMethod1`.</span><span class="sxs-lookup"><span data-stu-id="8621f-148">Runs all tests except `NUnitNamespace.UnitTest1.TestMethod1`.</span></span> |
| `dotnet test --filter TestCategory=CategoryA` | <span data-ttu-id="8621f-149">Exécute les tests qui sont annotés avec `[Category("CategoryA")]`.</span><span class="sxs-lookup"><span data-stu-id="8621f-149">Runs tests which are annotated with `[Category("CategoryA")]`.</span></span> |
| `dotnet test --filter Priority=2` | <span data-ttu-id="8621f-150">Exécute les tests qui sont annotés avec `[Priority(2)]`.</span><span class="sxs-lookup"><span data-stu-id="8621f-150">Runs tests which are annotated with `[Priority(2)]`.</span></span><br>

<span data-ttu-id="8621f-151">**Utilisation des opérateurs conditionnels | et &amp;**</span><span class="sxs-lookup"><span data-stu-id="8621f-151">**Using conditional operators | and &amp;**</span></span>

| <span data-ttu-id="8621f-152">Expression</span><span class="sxs-lookup"><span data-stu-id="8621f-152">Expression</span></span> | <span data-ttu-id="8621f-153">Résultat</span><span class="sxs-lookup"><span data-stu-id="8621f-153">Result</span></span> |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | <span data-ttu-id="8621f-154">Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **ou** `TestCategory` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="8621f-154">Runs tests which have `UnitTest1` in `FullyQualifiedName` **or** `TestCategory` is `CategoryA`.</span></span> |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | <span data-ttu-id="8621f-155">Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **et** `TestCategory` est `CategoryA`.</span><span class="sxs-lookup"><span data-stu-id="8621f-155">Runs tests which have `UnitTest1` in `FullyQualifiedName` **and** `TestCategory` is `CategoryA`.</span></span> |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | <span data-ttu-id="8621f-156">Exécute les tests qui ont un `FullyQualifiedName` contenant `UnitTest1` **et** `TestCategory` est `CategoryA` **ou** `Priority` est 1.</span><span class="sxs-lookup"><span data-stu-id="8621f-156">Runs tests which have either `FullyQualifiedName` containing `UnitTest1` **and** `TestCategory` is `CategoryA` **or** `Priority` is 1.</span></span> |
