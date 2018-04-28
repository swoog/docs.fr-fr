---
title: Effectuer des tests unitaires de C# avec NUnit et .NET Core
description: Apprenez les concepts des tests unitaires dans C# et .NET Core de manière interactive en créant un exemple de solution pas à pas à l’aide de dotnet test et de NUnit.
author: rprouse
ms.date: 12/01/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.devlang: dotnet
ms.workload:
- dotnetcore
ms.openlocfilehash: db11adf265b2a08456a1bd42bc8a6847ba70a2ce
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="unit-testing-c-with-nunit-and-net-core"></a><span data-ttu-id="7deb8-103">Effectuer des tests unitaires de C# avec NUnit et .NET Core</span><span class="sxs-lookup"><span data-stu-id="7deb8-103">Unit testing C# with NUnit and .NET Core</span></span>

<span data-ttu-id="7deb8-104">Ce didacticiel vous guide pas à pas dans la création d’un exemple de solution pour apprendre les concepts des tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="7deb8-104">This tutorial takes you through an interactive experience building a sample solution step-by-step to learn unit testing concepts.</span></span> <span data-ttu-id="7deb8-105">Si vous préférez suivre le didacticiel à l’aide d’une solution prédéfinie, [affichez ou téléchargez l’exemple de code](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-using-nunit/) avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="7deb8-105">If you prefer to follow the tutorial using a pre-built solution, [view or download the sample code](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-using-nunit/) before you begin.</span></span> <span data-ttu-id="7deb8-106">Pour obtenir des instructions de téléchargement, consultez [Exemples et didacticiels](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span><span class="sxs-lookup"><span data-stu-id="7deb8-106">For download instructions, see [Samples and Tutorials](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).</span></span>

## <a name="creating-the-source-project"></a><span data-ttu-id="7deb8-107">Création du projet source</span><span class="sxs-lookup"><span data-stu-id="7deb8-107">Creating the source project</span></span>

<span data-ttu-id="7deb8-108">Ouvrez une fenêtre d’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="7deb8-108">Open a shell window.</span></span> <span data-ttu-id="7deb8-109">Créez un répertoire appelé *unit-testing-using-nunit* qui contiendra la solution.</span><span class="sxs-lookup"><span data-stu-id="7deb8-109">Create a directory called *unit-testing-using-nunit* to hold the solution.</span></span> <span data-ttu-id="7deb8-110">Dans ce nouveau répertoire, exécutez [`dotnet new sln`](../tools/dotnet-new.md) pour créer un fichier de solution pour la bibliothèque de classes et le projet de test.</span><span class="sxs-lookup"><span data-stu-id="7deb8-110">Inside this new directory, run [`dotnet new sln`](../tools/dotnet-new.md) to create a new solution file for the class library and the test project.</span></span> <span data-ttu-id="7deb8-111">Ensuite, créez un répertoire *PrimeService*.</span><span class="sxs-lookup"><span data-stu-id="7deb8-111">Next, create a *PrimeService* directory.</span></span> <span data-ttu-id="7deb8-112">Vous disposez de la structure de répertoire et de fichiers suivante :</span><span class="sxs-lookup"><span data-stu-id="7deb8-112">The following outline shows the directory and file structure thus far:</span></span>

```
/unit-testing-using-nunit
    unit-testing-using-nunit.sln
    /PrimeService
```

<span data-ttu-id="7deb8-113">Accédez au répertoire *PrimeService* et exécutez [`dotnet new classlib`](../tools/dotnet-new.md) pour créer le projet source.</span><span class="sxs-lookup"><span data-stu-id="7deb8-113">Make *PrimeService* the current directory and run [`dotnet new classlib`](../tools/dotnet-new.md) to create the source project.</span></span> <span data-ttu-id="7deb8-114">Renommez *Class1.cs* en *PrimeService.cs*.</span><span class="sxs-lookup"><span data-stu-id="7deb8-114">Rename *Class1.cs* to *PrimeService.cs*.</span></span> <span data-ttu-id="7deb8-115">Pour utiliser le développement piloté par les tests (TDD), vous créez une implémentation défaillante de la classe `PrimeService` :</span><span class="sxs-lookup"><span data-stu-id="7deb8-115">To use test-driven development (TDD), you create a failing implementation of the `PrimeService` class:</span></span>

```csharp
using System;

namespace Prime.Services
{
    public class PrimeService
    {
        public bool IsPrime(int candidate)
        {
            throw new NotImplementedException("Please create a test first");
        }
    }
}
```

<span data-ttu-id="7deb8-116">Accédez de nouveau au répertoire *unit-testing-using-nunit*.</span><span class="sxs-lookup"><span data-stu-id="7deb8-116">Change the directory back to the *unit-testing-using-nunit* directory.</span></span> <span data-ttu-id="7deb8-117">Exécutez [`dotnet sln add PrimeService/PrimeService.csproj`](../tools/dotnet-sln.md) pour ajouter le projet de la bibliothèque de classes à la solution.</span><span class="sxs-lookup"><span data-stu-id="7deb8-117">Run [`dotnet sln add PrimeService/PrimeService.csproj`](../tools/dotnet-sln.md) to add the class library project to the solution.</span></span>

## <a name="install-the-nunit-project-template"></a><span data-ttu-id="7deb8-118">Installer le modèle de projet NUnit</span><span class="sxs-lookup"><span data-stu-id="7deb8-118">Install the NUnit project template</span></span>

<span data-ttu-id="7deb8-119">Les modèles de projet de test NUnit doivent être installés avant de créer un projet de test.</span><span class="sxs-lookup"><span data-stu-id="7deb8-119">The NUnit test project templates need to be installed before creating a test project.</span></span> <span data-ttu-id="7deb8-120">Cette opération ne doit être effectuée qu’une fois sur chaque ordinateur de développeur où vous allez créer des projets NUnit.</span><span class="sxs-lookup"><span data-stu-id="7deb8-120">This only needs to be done once on each developer machine where you'll create new NUnit projects.</span></span> <span data-ttu-id="7deb8-121">Exécutez [`dotnet new -i NUnit3.DotNetNew.Template`](../tools/dotnet-new.md) pour installer les modèles NUnit.</span><span class="sxs-lookup"><span data-stu-id="7deb8-121">Run [`dotnet new -i NUnit3.DotNetNew.Template`](../tools/dotnet-new.md) to install the NUnit templates.</span></span>

```
dotnet new -i NUnit3.DotNetNew.Template
```

### <a name="creating-the-test-project"></a><span data-ttu-id="7deb8-122">Création du projet de test</span><span class="sxs-lookup"><span data-stu-id="7deb8-122">Creating the test project</span></span>

<span data-ttu-id="7deb8-123">Ensuite, créez le répertoire *PrimeService.Tests*.</span><span class="sxs-lookup"><span data-stu-id="7deb8-123">Next, create the *PrimeService.Tests* directory.</span></span> <span data-ttu-id="7deb8-124">La structure du répertoire est illustrée ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="7deb8-124">The following outline shows the directory structure:</span></span>

```
/unit-testing-using-nunit
    unit-testing-using-nunit.sln
    /PrimeService
        Source Files
        PrimeService.csproj
    /PrimeService.Tests
```

<span data-ttu-id="7deb8-125">Accédez au répertoire *PrimeService.Tests* et créez un projet à l’aide de [`dotnet new nunit`](../tools/dotnet-new.md).</span><span class="sxs-lookup"><span data-stu-id="7deb8-125">Make the *PrimeService.Tests* directory the current directory and create a new project using [`dotnet new nunit`](../tools/dotnet-new.md).</span></span> <span data-ttu-id="7deb8-126">La commande dotnet new crée un projet de test qui utilise NUnit comme bibliothèque de test.</span><span class="sxs-lookup"><span data-stu-id="7deb8-126">The dotnet new command creates a test project that uses NUnit as the test library.</span></span> <span data-ttu-id="7deb8-127">Le modèle généré configure Test Runner dans le fichier *PrimeServiceTests.csproj* :</span><span class="sxs-lookup"><span data-stu-id="7deb8-127">The generated template configures the test runner in the *PrimeServiceTests.csproj* file:</span></span>

```xml
<ItemGroup>
  <PackageReference Include="Microsoft.NET.Test.Sdk" Version="15.5.0" />
  <PackageReference Include="NUnit" Version="3.9.0" />
  <PackageReference Include="NUnit3TestAdapter" Version="3.9.0" />
</ItemGroup>
```

<span data-ttu-id="7deb8-128">Le projet de test a besoin d’autres packages pour créer et exécuter des tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="7deb8-128">The test project requires other packages to create and run unit tests.</span></span> <span data-ttu-id="7deb8-129">`dotnet new` dans l’étape précédente a ajouté le kit SDK de test Microsoft, le framework de test NUnit et l’adaptateur de test NUnit.</span><span class="sxs-lookup"><span data-stu-id="7deb8-129">`dotnet new` in the previous step added the Microsoft test SDK, the NUnit test framework, and the NUnit test adapter.</span></span> <span data-ttu-id="7deb8-130">Maintenant, ajoutez la bibliothèque de classes `PrimeService` en tant qu’une autre dépendance au projet.</span><span class="sxs-lookup"><span data-stu-id="7deb8-130">Now, add the `PrimeService` class library as another dependency to the project.</span></span> <span data-ttu-id="7deb8-131">Utilisez la commande [`dotnet add reference`](../tools/dotnet-add-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="7deb8-131">Use the [`dotnet add reference`](../tools/dotnet-add-reference.md) command:</span></span>

```
dotnet add reference ../PrimeService/PrimeService.csproj
```

<span data-ttu-id="7deb8-132">Vous pouvez consulter le fichier dans son intégralité dans le [dépôt d’exemples](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-using-nunit/PrimeService.Tests/PrimeService.Tests.csproj) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="7deb8-132">You can see the entire file in the [samples repository](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-using-nunit/PrimeService.Tests/PrimeService.Tests.csproj) on GitHub.</span></span>

<span data-ttu-id="7deb8-133">La solution finale se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="7deb8-133">The following outline shows the final solution layout:</span></span>

```
/unit-testing-using-nunit
    unit-testing-using-nunit.sln
    /PrimeService
        Source Files
        PrimeService.csproj
    /PrimeService.Tests
        Test Source Files
        PrimeServiceTests.csproj
```

<span data-ttu-id="7deb8-134">Exécutez [`dotnet sln add .\PrimeService.Tests\PrimeService.Tests.csproj`](../tools/dotnet-sln.md) dans le répertoire *unit-testing-using-dotnet-test*.</span><span class="sxs-lookup"><span data-stu-id="7deb8-134">Execute [`dotnet sln add .\PrimeService.Tests\PrimeService.Tests.csproj`](../tools/dotnet-sln.md) in the *unit-testing-using-dotnet-test* directory.</span></span>

## <a name="creating-the-first-test"></a><span data-ttu-id="7deb8-135">Création du premier test</span><span class="sxs-lookup"><span data-stu-id="7deb8-135">Creating the first test</span></span>

<span data-ttu-id="7deb8-136">L’approche TDD impose d’écrire un test défaillant, de le corriger pour qu’il réussisse, puis de répéter le processus.</span><span class="sxs-lookup"><span data-stu-id="7deb8-136">The TDD approach calls for writing one failing test, making it pass, then repeating the process.</span></span> <span data-ttu-id="7deb8-137">Supprimez *UnitTest1.cs* du répertoire *PrimeService.Tests* et créez un fichier C# nommé *PrimeService_IsPrimeShould.cs* avec le contenu suivant :</span><span class="sxs-lookup"><span data-stu-id="7deb8-137">Remove *UnitTest1.cs* from the *PrimeService.Tests* directory and create a new C# file named *PrimeService_IsPrimeShould.cs* with the following content:</span></span>

```csharp
using NUnit.Framework;
using Prime.Services;

namespace Prime.UnitTests.Services
{
    [TestFixture]
    public class PrimeService_IsPrimeShould
    {
        private readonly PrimeService _primeService;

        public PrimeService_IsPrimeShould()
        {
            _primeService = new PrimeService();
        }

        [Test]
        public void ReturnFalseGivenValueOf1()
        {
            var result = _primeService.IsPrime(1);

            Assert.IsFalse(result, "1 should not be prime");
        }
    }
}
```

<span data-ttu-id="7deb8-138">L’attribut `[TestFixture]` désigne une classe qui contient des tests unitaires.</span><span class="sxs-lookup"><span data-stu-id="7deb8-138">The `[TestFixture]` attribute denotes a class that contains unit tests.</span></span> <span data-ttu-id="7deb8-139">L’attribut `[Test]` indique une méthode qui est une méthode de test.</span><span class="sxs-lookup"><span data-stu-id="7deb8-139">The `[Test]` attribute indicates a method is a test method.</span></span>

<span data-ttu-id="7deb8-140">Enregistrez ce fichier et exécutez [`dotnet test`](../tools/dotnet-test.md) pour générer les tests et la bibliothèque de classes, puis exécutez les tests.</span><span class="sxs-lookup"><span data-stu-id="7deb8-140">Save this file and execute [`dotnet test`](../tools/dotnet-test.md) to build the tests and the class library and then run the tests.</span></span> <span data-ttu-id="7deb8-141">Le Test Runner NUnit contient le point d’entrée de programme qui permet d’exécuter vos tests.</span><span class="sxs-lookup"><span data-stu-id="7deb8-141">The NUnit test runner contains the program entry point to run your tests.</span></span> <span data-ttu-id="7deb8-142">`dotnet test` démarre le Test Runner à l’aide du projet de test unitaire que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="7deb8-142">`dotnet test` starts the test runner using the unit test project you've created.</span></span>

<span data-ttu-id="7deb8-143">Votre test échoue.</span><span class="sxs-lookup"><span data-stu-id="7deb8-143">Your test fails.</span></span> <span data-ttu-id="7deb8-144">Vous n’avez pas encore créé l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="7deb8-144">You haven't created the implementation yet.</span></span> <span data-ttu-id="7deb8-145">Pour que ce test réussisse, écrivez le code le plus simple dans la classe `PrimeService` qui fonctionne :</span><span class="sxs-lookup"><span data-stu-id="7deb8-145">Make this test pass by writing the simplest code in the `PrimeService` class that works:</span></span>

```csharp
public bool IsPrime(int candidate)
{
    if (candidate == 1)
    {
        return false;
    }
    throw new NotImplementedException("Please create a test first");
}
```

<span data-ttu-id="7deb8-146">Dans le répertoire *unit-testing-using-nunit*, réexécutez `dotnet test`.</span><span class="sxs-lookup"><span data-stu-id="7deb8-146">In the *unit-testing-using-nunit* directory, run `dotnet test` again.</span></span> <span data-ttu-id="7deb8-147">La commande `dotnet test` exécute une build pour le projet `PrimeService` puis pour le projet `PrimeService.Tests`.</span><span class="sxs-lookup"><span data-stu-id="7deb8-147">The `dotnet test` command runs a build for the `PrimeService` project and then for the `PrimeService.Tests` project.</span></span> <span data-ttu-id="7deb8-148">Après la création des deux projets, il exécute ce test unique.</span><span class="sxs-lookup"><span data-stu-id="7deb8-148">After building both projects, it runs this single test.</span></span> <span data-ttu-id="7deb8-149">Le test réussit.</span><span class="sxs-lookup"><span data-stu-id="7deb8-149">It passes.</span></span>

## <a name="adding-more-features"></a><span data-ttu-id="7deb8-150">Ajout de fonctionnalités supplémentaires</span><span class="sxs-lookup"><span data-stu-id="7deb8-150">Adding more features</span></span>

<span data-ttu-id="7deb8-151">Maintenant que vous avez fait réussir un test, le moment est venu d’écrire plus de code.</span><span class="sxs-lookup"><span data-stu-id="7deb8-151">Now that you've made one test pass, it's time to write more.</span></span> <span data-ttu-id="7deb8-152">Il existe quelques autres cas simples pour des nombres premiers : 0, -1.</span><span class="sxs-lookup"><span data-stu-id="7deb8-152">There are a few other simple cases for prime numbers: 0, -1.</span></span> <span data-ttu-id="7deb8-153">Vous pouvez ajouter de nouveaux tests avec l’attribut `[Test]`, mais cela devient vite fastidieux.</span><span class="sxs-lookup"><span data-stu-id="7deb8-153">You could add new tests with the `[Test]` attribute, but that quickly becomes tedious.</span></span> <span data-ttu-id="7deb8-154">D’autres attributs NUnit vous permettent d’écrire une suite de tests similaires.</span><span class="sxs-lookup"><span data-stu-id="7deb8-154">There are other NUnit attributes that enable you to write a suite of similar tests.</span></span>  <span data-ttu-id="7deb8-155">Un attribut `[TestCase]` permet de créer une suite de tests qui exécutent le même code, mais qui ont des arguments d’entrée différents.</span><span class="sxs-lookup"><span data-stu-id="7deb8-155">A `[TestCase]` attribute is used to create a suite of tests that execute the same code but have different input arguments.</span></span> <span data-ttu-id="7deb8-156">Vous pouvez utiliser l’attribut `[TestCase]` pour spécifier des valeurs pour ces entrées.</span><span class="sxs-lookup"><span data-stu-id="7deb8-156">You can use the `[TestCase]` attribute to specify values for those inputs.</span></span>

<span data-ttu-id="7deb8-157">Au lieu de créer des tests, appliquez cet attribut pour créer un test unique piloté par les données.</span><span class="sxs-lookup"><span data-stu-id="7deb8-157">Instead of creating new tests, apply this attribute to create a single data driven test.</span></span> <span data-ttu-id="7deb8-158">Le test piloté par les données est une méthode qui teste plusieurs valeurs inférieures à deux, qui est le plus petit nombre premier :</span><span class="sxs-lookup"><span data-stu-id="7deb8-158">The data driven test is a method that tests several values less than two, which is the lowest prime number:</span></span>

[!code-csharp[Sample_TestCode](../../../samples/core/getting-started/unit-testing-using-nunit/PrimeService.Tests/PrimeService_IsPrimeShould.cs?name=Sample_TestCode)]

<span data-ttu-id="7deb8-159">Exécutez `dotnet test`, et deux de ces tests échouent.</span><span class="sxs-lookup"><span data-stu-id="7deb8-159">Run `dotnet test`, and two of these tests fail.</span></span> <span data-ttu-id="7deb8-160">Pour que tous les tests réussissent, modifiez la clause `if` au début de la méthode :</span><span class="sxs-lookup"><span data-stu-id="7deb8-160">To make all of the tests pass, change the `if` clause at the beginning of the method:</span></span>

```csharp
if (candidate < 2)
```

<span data-ttu-id="7deb8-161">Poursuivez l’itération en ajoutant plus de tests, plus de théories et plus de code dans la bibliothèque principale.</span><span class="sxs-lookup"><span data-stu-id="7deb8-161">Continue to iterate by adding more tests, more theories, and more code in the main library.</span></span> <span data-ttu-id="7deb8-162">Vous disposez de la [version finale des tests](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-using-nunit/PrimeService.Tests/PrimeService_IsPrimeShould.cs) et de [l’implémentation complète de la bibliothèque](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-using-nunit/PrimeService/PrimeService.cs).</span><span class="sxs-lookup"><span data-stu-id="7deb8-162">You have the [finished version of the tests](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-using-nunit/PrimeService.Tests/PrimeService_IsPrimeShould.cs) and the [complete implementation of the library](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-using-nunit/PrimeService/PrimeService.cs).</span></span>

<span data-ttu-id="7deb8-163">Vous avez créé une petite bibliothèque et un ensemble de tests unitaires pour cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="7deb8-163">You've built a small library and a set of unit tests for that library.</span></span> <span data-ttu-id="7deb8-164">Vous avez structuré la solution afin que l’ajout de nouveaux packages et tests fasse partie du flux de travail normal.</span><span class="sxs-lookup"><span data-stu-id="7deb8-164">You've structured the solution so that adding new packages and tests is part of the normal workflow.</span></span> <span data-ttu-id="7deb8-165">Vous avez concentré la plupart de votre temps et de vos efforts sur la résolution des objectifs de l’application.</span><span class="sxs-lookup"><span data-stu-id="7deb8-165">You've concentrated most of your time and effort on solving the goals of the application.</span></span>
