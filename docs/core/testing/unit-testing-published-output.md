---
title: Tester la sortie publiée avec dotnet vstest
description: Découvrez comment exécuter des tests sur des bibliothèques publiées plutôt que sur le code source avec la commande dotnet vstest.
author: kendrahavens
ms.author: kehavens
ms.date: 10/18/2017
ms.custom: seodec18
ms.openlocfilehash: 9d842f26336d0ddf5375d49676523086bb632684
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53239525"
---
# <a name="test-published-output-with-dotnet-vstest"></a><span data-ttu-id="eedc6-103">Tester la sortie publiée avec dotnet vstest</span><span class="sxs-lookup"><span data-stu-id="eedc6-103">Test published output with dotnet vstest</span></span>

<span data-ttu-id="eedc6-104">Vous pouvez exécuter des tests sur la sortie déjà publiée à l’aide de la commande `dotnet vstest`.</span><span class="sxs-lookup"><span data-stu-id="eedc6-104">You can run tests on already published output by using the `dotnet vstest` command.</span></span> <span data-ttu-id="eedc6-105">Cela s’applique aux tests sur xUnit, MSTest et NUnit.</span><span class="sxs-lookup"><span data-stu-id="eedc6-105">This will work on xUnit, MSTest, and NUnit tests.</span></span> <span data-ttu-id="eedc6-106">Recherchez simplement le fichier DLL qui faisait partie de votre sortie publiée et exécutez :</span><span class="sxs-lookup"><span data-stu-id="eedc6-106">Simply locate the DLL file that was part of your published output and run:</span></span>

```
dotnet vstest <MyPublishedTests>.dll
```

<span data-ttu-id="eedc6-107">où `<MyPublishedTests>` est le nom de votre projet de test publié.</span><span class="sxs-lookup"><span data-stu-id="eedc6-107">Where `<MyPublishedTests>` is the name of your published test project.</span></span>

## <a name="example"></a><span data-ttu-id="eedc6-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="eedc6-108">Example</span></span>

<span data-ttu-id="eedc6-109">Les commandes ci-dessous montrent des tests en cours d’exécution sur une DLL publiée.</span><span class="sxs-lookup"><span data-stu-id="eedc6-109">The commands below demonstrate running tests on a published DLL.</span></span>

```
dotnet new mstest -o MyProject.Tests
cd MyProject.Tests
dotnet publish -o out
dotnet vstest out/MyProject.Tests.dll
```

> [!NOTE]
> <span data-ttu-id="eedc6-110">Remarque : si votre application cible une version de .NET Framework autre que `netcoreapp`, vous pouvez toujours exécuter la commande `dotnet vstest` en passant à la version de .NET Framework ciblée avec un indicateur de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="eedc6-110">Note: If your app is targeting a framework other than `netcoreapp` you can still run the `dotnet vstest` command by passing in the targeted framework with a framework flag.</span></span> <span data-ttu-id="eedc6-111">Par exemple, `dotnet vstest <MyPublishedTests>.dll  --Framework:".NETFramework,Version=v4.6"`.</span><span class="sxs-lookup"><span data-stu-id="eedc6-111">For example, `dotnet vstest <MyPublishedTests>.dll  --Framework:".NETFramework,Version=v4.6"`.</span></span> <span data-ttu-id="eedc6-112">Dans Visual Studio 2017 Update 5, la version souhaitée du .NET framework est automatiquement détectée.</span><span class="sxs-lookup"><span data-stu-id="eedc6-112">In Visual Studio 2017 Update 5 the desired framework is automatically detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="eedc6-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eedc6-113">See also</span></span>
- [<span data-ttu-id="eedc6-114">Tests unitaires avec dotnet-test et xUnit</span><span class="sxs-lookup"><span data-stu-id="eedc6-114">Unit Testing with dotnet test and xUnit</span></span>](unit-testing-with-dotnet-test.md)
- [<span data-ttu-id="eedc6-115">Tests unitaires avec dotnet-test et NUnit</span><span class="sxs-lookup"><span data-stu-id="eedc6-115">Unit Testing with dotnet test and NUnit</span></span>](unit-testing-with-nunit.md)
- [<span data-ttu-id="eedc6-116">Tests unitaires avec dotnet-test et MSTest</span><span class="sxs-lookup"><span data-stu-id="eedc6-116">Unit Testing with dotnet test and MSTest</span></span>](unit-testing-with-mstest.md)
