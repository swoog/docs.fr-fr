---
title: Tester la sortie publiée avec dotnet vstest
description: Découvrez comment exécuter des tests sur une sortie publiée avec la commande dotnet vstest.
author: kendrahavens
ms.author: kehavens
ms.date: 10/18/2017
ms.openlocfilehash: e99000996f5dfa9f9d4f9b823e36ecbe325da835
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43508131"
---
# <a name="test-published-output-with-dotnet-vstest"></a><span data-ttu-id="cb3c8-103">Tester la sortie publiée avec dotnet vstest</span><span class="sxs-lookup"><span data-stu-id="cb3c8-103">Test published output with dotnet vstest</span></span>

<span data-ttu-id="cb3c8-104">Vous pouvez exécuter des tests sur la sortie déjà publiée à l’aide de la commande `dotnet vstest`.</span><span class="sxs-lookup"><span data-stu-id="cb3c8-104">You can run tests on already published output by using the `dotnet vstest` command.</span></span> <span data-ttu-id="cb3c8-105">Cela s’applique aux tests sur xUnit, MSTest et NUnit.</span><span class="sxs-lookup"><span data-stu-id="cb3c8-105">This will work on xUnit, MSTest, and NUnit tests.</span></span> <span data-ttu-id="cb3c8-106">Recherchez simplement le fichier DLL qui faisait partie de votre sortie publiée et exécutez :</span><span class="sxs-lookup"><span data-stu-id="cb3c8-106">Simply locate the DLL file that was part of your published output and run:</span></span>

```
dotnet vstest <MyPublishedTests>.dll
```

<span data-ttu-id="cb3c8-107">où `<MyPublishedTests>` est le nom de votre projet de test publié.</span><span class="sxs-lookup"><span data-stu-id="cb3c8-107">where `<MyPublishedTests>` is the name of your published test project.</span></span>

## <a name="example-of-running-tests-on-a-published-dll"></a><span data-ttu-id="cb3c8-108">Exemple d’exécution de tests sur une DLL publiée</span><span class="sxs-lookup"><span data-stu-id="cb3c8-108">Example of running tests on a published DLL</span></span>

```
dotnet new mstest -o MyProject.Tests
cd MyProject.Tests
dotnet publish -o out
dotnet vstest out/MyProject.Tests.dll
```

> [!NOTE]
> <span data-ttu-id="cb3c8-109">Remarque : si votre application cible une version de .NET Framework autre que `netcoreapp`, vous pouvez toujours exécuter la commande `dotnet vstest` en passant à la version de .NET Framework ciblée avec un indicateur de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="cb3c8-109">Note: If your app is targeting a framework other than `netcoreapp` you can still run the `dotnet vstest` command by passing in the targeted framework with a framework flag.</span></span> <span data-ttu-id="cb3c8-110">Par exemple, `dotnet vstest <MyPublishedTests>.dll  --Framework:".NETFramework,Version=v4.6"`.</span><span class="sxs-lookup"><span data-stu-id="cb3c8-110">For example, `dotnet vstest <MyPublishedTests>.dll  --Framework:".NETFramework,Version=v4.6"`.</span></span> <span data-ttu-id="cb3c8-111">Dans Visual Studio 2017 Update 5, la version souhaitée du .NET framework est automatiquement détectée.</span><span class="sxs-lookup"><span data-stu-id="cb3c8-111">In Visual Studio 2017 Update 5 the desired framework is automatically detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb3c8-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb3c8-112">See also</span></span>
- [<span data-ttu-id="cb3c8-113">Tests unitaires avec dotnet-test et xUnit</span><span class="sxs-lookup"><span data-stu-id="cb3c8-113">Unit Testing with dotnet test and xUnit</span></span>](unit-testing-with-dotnet-test.md)
- [<span data-ttu-id="cb3c8-114">Tests unitaires avec dotnet-test et NUnit</span><span class="sxs-lookup"><span data-stu-id="cb3c8-114">Unit Testing with dotnet test and NUnit</span></span>](unit-testing-with-nunit.md)
- [<span data-ttu-id="cb3c8-115">Tests unitaires avec dotnet-test et MSTest</span><span class="sxs-lookup"><span data-stu-id="cb3c8-115">Unit Testing with dotnet test and MSTest</span></span>](unit-testing-with-mstest.md)
