---
title: Effectuer des tests unitaires sur Visual Basic dans .NET Core avec dotnet test et NUnit
description: Apprenez les concepts des tests unitaires dans .NET Core de manière interactive en créant un exemple de solution Visual Basic pas à pas à l’aide de NUnit.
author: rprouse
ms.date: 10/04/2018
dev_langs:
- vb
ms.custom: seodec18
ms.openlocfilehash: 2c8a6b86dd66b13faa242f94cf11cb940986fbd0
ms.sourcegitcommit: 8f95d3a37e591963ebbb9af6e90686fd5f3b8707
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2019
ms.locfileid: "56746874"
---
# <a name="unit-testing-visual-basic-net-core-libraries-using-dotnet-test-and-nunit"></a>Effectuer des tests unitaires sur les bibliothèques .NET Core Visual Basic à l’aide de dotnet test et de NUnit

Ce didacticiel vous guide pas à pas dans la création d’un exemple de solution pour apprendre les concepts des tests unitaires. Si vous préférez suivre le didacticiel à l’aide d’une solution prédéfinie, [affichez ou téléchargez l’exemple de code](https://github.com/dotnet/samples/tree/master/core/getting-started/unit-testing-vb-nunit/) avant de commencer. Pour obtenir des instructions de téléchargement, consultez [Exemples et didacticiels](../../samples-and-tutorials/index.md#viewing-and-downloading-samples).

## <a name="prerequisites"></a>Prérequis

- [Kit SDK .NET Core 2.1](https://www.microsoft.com/net/download) (ou version ultérieure).
- Un éditeur de texte ou un éditeur de code de votre choix.

## <a name="creating-the-source-project"></a>Création du projet source

Ouvrez une fenêtre d’interpréteur de commandes. Créez un répertoire appelé *unit-testing-vb-nunit* qui contiendra la solution. Dans ce nouveau répertoire, exécutez la commande suivante afin de créer un fichier solution pour la bibliothèque de classes et le projet de test :

```console
dotnet new sln
```

Ensuite, créez un répertoire *PrimeService*. La structure de fichiers est pour le moment la suivante :

```
/unit-testing-vb-nunit
    unit-testing-vb-nunit.sln
    /PrimeService
```

Accédez au répertoire *PrimeService* et exécutez la commande suivante pour créer le projet source :

```console
dotnet new classlib -lang VB
```

Renommez *Class1.VB* en *PrimeService.VB*. Créez une implémentation défaillante de la classe `PrimeService` :

```vb
Imports System

Namespace Prime.Services
    Public Class PrimeService
        Public Function IsPrime(candidate As Integer) As Boolean
            Throw New NotImplementedException("Please create a test first")
        End Function
    End Class
End Namespace
```

Accédez de nouveau au répertoire *unit-testing-vb-using-stest*. Exécutez la commande suivante pour ajouter le projet de la bibliothèque de classes à la solution :

```console
dotnet sln add .\PrimeService\PrimeService.vbproj
```

## <a name="creating-the-test-project"></a>Création du projet de test

Ensuite, créez le répertoire *PrimeService.Tests*. La structure du répertoire est illustrée ci-dessous :

```
/unit-testing-vb-nunit
    unit-testing-vb-nunit.sln
    /PrimeService
        Source Files
        PrimeService.vbproj
    /PrimeService.Tests
```

Accédez au répertoire *PrimeService.Tests* et créez un projet à l’aide de la commande suivante :

```console
dotnet new nunit -lang VB
```

La commande [dotnet new](../tools/dotnet-new.md) crée un projet de test qui utilise NUnit comme bibliothèque de test. Le modèle généré configure Test Runner dans le fichier *PrimeServiceTests.vbproj* :

[!code-xml[Packages](~/samples/core/getting-started/unit-testing-vb-nunit/PrimeService.Tests/PrimeService.Tests.vbproj#Packages)]

Le projet de test a besoin d’autres packages pour créer et exécuter des tests unitaires. `dotnet new` dans l’étape précédente a ajouté NUnit et l’adaptateur de test NUnit. Maintenant, ajoutez la bibliothèque de classes `PrimeService` en tant qu’une autre dépendance au projet. Utilisez la commande [`dotnet add reference`](../tools/dotnet-add-reference.md) :

```console
dotnet add reference ../PrimeService/PrimeService.vbproj
```

Vous pouvez consulter le fichier dans son intégralité dans le [dépôt d’exemples](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-vb-nunit/PrimeService.Tests/PrimeService.Tests.vbproj) sur GitHub.

La solution finale se présente comme suit :

```
/unit-testing-vb-nunit
    unit-testing-vb-nunit.sln
    /PrimeService
        Source Files
        PrimeService.vbproj
    /PrimeService.Tests
        Test Source Files
        PrimeService.Tests.vbproj
```

Exécutez la commande suivante dans le répertoire *unit-testing-vb-nunit* :

```console
dotnet sln add .\PrimeService.Tests\PrimeService.Tests.vbproj
```

## <a name="creating-the-first-test"></a>Création du premier test

Vous allez écrire un test défaillant, le corriger pour qu’il réussisse, puis répéter le processus. Dans le répertoire *PrimeService.Tests*, renommez le fichier *UnitTest1.vb* en *PrimeService_IsPrimeShould.VB*, puis remplacez tout son contenu par le code suivant :

```vb
Imports NUnit.Framework

Namespace PrimeService.Tests
    <TestFixture>
    Public Class PrimeService_IsPrimeShould
        Private _primeService As Prime.Services.PrimeService = New Prime.Services.PrimeService()

        <Test>
        Sub ReturnFalseGivenValueOf1()
            Dim result As Boolean = _primeService.IsPrime(1)

            Assert.False(result, "1 should not be prime")
        End Sub

    End Class
End Namespace
```

L’attribut `<TestFixture>` désigne une classe qui contient des tests. L’attribut `<Test>` désigne une méthode qui est exécutée par le Test Runner. À partir de *unit-testing-vb-nunit*, exécutez [`dotnet test`](../tools/dotnet-test.md) pour générer les tests et la bibliothèque de classes, puis exécutez les tests. Le Test Runner NUnit contient le point d’entrée de programme qui permet d’exécuter vos tests. `dotnet test` démarre le Test Runner à l’aide du projet de test unitaire que vous avez créé.

Votre test échoue. Vous n’avez pas encore créé l’implémentation. Effectuez ce test en écrivant le code le plus simple dans la classe `PrimeService` qui fonctionne :

```vb
Public Function IsPrime(candidate As Integer) As Boolean
    If candidate = 1 Then
        Return False
    End If
    Throw New NotImplementedException("Please create a test first")
End Function
```

Dans le répertoire *unit-testing-vb-nunit*, réexécutez `dotnet test`. La commande `dotnet test` exécute une build pour le projet `PrimeService` puis pour le projet `PrimeService.Tests`. Après la création des deux projets, il exécute ce test unique. Le test réussit.

## <a name="adding-more-features"></a>Ajout de fonctionnalités supplémentaires

Maintenant que vous avez fait réussir un test, le moment est venu d’écrire plus de code. Il existe quelques autres cas simples pour des nombres premiers : 0, -1. Vous pouvez ajouter ces cas en tant que nouveaux tests, avec l’attribut `<Test>`, mais cela devient vite fastidieux. D’autres attributs xUnit vous permettent d’écrire une suite de tests similaires.  L’attribut `<TestCase>` représente une suite de tests qui exécutent le même code, mais qui ont des arguments d’entrée différents. Vous pouvez utiliser l’attribut `<TestCase>` pour spécifier des valeurs pour ces entrées.

Au lieu de créer des tests, appliquez ces deux attributs pour créer une série de tests qui teste plusieurs valeurs inférieures à deux, qui est le plus petit nombre premier :

[!code-vb[Sample_TestCode](../../../samples/core/getting-started/unit-testing-vb-nunit/PrimeService.Tests/PrimeService_IsPrimeShould.vb?name=Sample_TestCode)]

Exécutez `dotnet test`, et deux de ces tests échouent. Pour que tous les tests réussissent, changez la clause `if` au début de la méthode `Main` dans le fichier *PrimeServices.cs* :

```vb
if candidate < 2
```

Poursuivez l’itération en ajoutant plus de tests, plus de théories et plus de code dans la bibliothèque principale. Vous disposez de la [version finale des tests](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-vb-nunit/PrimeService.Tests/PrimeService_IsPrimeShould.vb) et de [l’implémentation complète de la bibliothèque](https://github.com/dotnet/samples/blob/master/core/getting-started/unit-testing-vb-nunit/PrimeService/PrimeService.vb).

Vous avez créé une petite bibliothèque et un ensemble de tests unitaires pour cette bibliothèque. Vous avez structuré la solution afin que l’ajout de nouveaux packages et tests fasse partie du flux de travail normal. Vous avez concentré la plupart de votre temps et de vos efforts sur la résolution des objectifs de l’application.
