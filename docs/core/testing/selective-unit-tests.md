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
# <a name="running-selective-unit-tests"></a>Exécution de tests unitaires sélectifs

Les exemples suivants utilisent `dotnet test`. Si vous utilisez `vstest.console.exe`, remplacez `--filter ` par `--testcasefilter:`.

## <a name="mstest"></a>MSTest

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

| Expression | Résultat |
| ---------- | ------ |
| `dotnet test --filter Method` | Exécute les tests dont `FullyQualifiedName` contient `Method`. Disponible dans `vstest 15.1+`. |
| `dotnet test --filter Name~TestMethod1` | Exécute les tests dont le nom contient `TestMethod1`. |
| `dotnet test --filter ClassName=MSTestNamespace.UnitTest1` | Exécute les tests qui sont dans la classe `MSTestNamespace.UnitTest1`.<br>**Remarque :** La valeur `ClassName` doit avoir un espace de noms, donc `ClassName=UnitTest1` ne fonctionnera pas. |
| `dotnet test --filter FullyQualifiedName!=MSTestNamespace.UnitTest1.TestMethod1` | Exécute tous les tests sauf `MSTestNamespace.UnitTest1.TestMethod1`. |
| `dotnet test --filter TestCategory=CategoryA` | Exécute les tests qui sont annotés avec `[TestCategory("CategoryA")]`. |
| `dotnet test --filter Priority=2` | Exécute les tests qui sont annotés avec `[Priority(2)]`.<br>

**Utilisation des opérateurs conditionnels | et &amp;**

| Expression | Résultat |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **ou** `TestCategory` est `CategoryA`. |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **et** `TestCategory` est `CategoryA`. |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | Exécute les tests qui ont un `FullyQualifiedName` contenant `UnitTest1` **et** `TestCategory` est `CategoryA` **ou** `Priority` est 1. |

## <a name="xunit"></a>xUnit

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

| Expression | Résultat |
| ---------- | ------ |
| `dotnet test --filter DisplayName=XUnitNamespace.TestClass1.Test1` | Exécute uniquement un test, `XUnitNamespace.TestClass1.Test1`. |
| `dotnet test --filter FullyQualifiedName!=XUnitNamespace.TestClass1.Test1` | Exécute tous les tests sauf `XUnitNamespace.TestClass1.Test1`. |
| `dotnet test --filter DisplayName~TestClass1` | Exécute les tests dont le nom d’affichage contient `TestClass1`. |

Dans l’exemple de code, les caractéristiques définies avec les clés `Category` et `Priority` peuvent être utilisées pour filtrer.

| Expression | Résultat |
| ---------- | ------ |
| `dotnet test --filter XUnit` | Exécute les tests dont `FullyQualifiedName` contient `XUnit`.  Disponible dans `vstest 15.1+`. |
| `dotnet test --filter Category=CategoryA` | Exécute les tests qui ont `[Trait("Category", "CategoryA")]`. |

**Utilisation des opérateurs conditionnels | et &amp;**

| Expression | Résultat |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~TestClass1&#124;Category=CategoryA"</code> | Exécute les tests qui ont `TestClass1` dans `FullyQualifiedName` **ou** `Category` est `CategoryA`. |
| `dotnet test --filter "FullyQualifiedName~TestClass1&Category=CategoryA"` | Exécute les tests qui ont `TestClass1` dans `FullyQualifiedName` **et** `Category` est `CategoryA`. |
| <code>dotnet test --filter "(FullyQualifiedName~TestClass1&Category=CategoryA)&#124;Priority=1"</code> | Exécute les tests qui ont un `FullyQualifiedName` contenant `TestClass1` **et** `Category` est `CategoryA` **ou** `Priority` est 1. |

## <a name="nunit"></a>NUnit

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

| Expression | Résultat |
| ---------- | ------ |
| `dotnet test --filter Method` | Exécute les tests dont `FullyQualifiedName` contient `Method`. Disponible dans `vstest 15.1+`. |
| `dotnet test --filter Name~TestMethod1` | Exécute les tests dont le nom contient `TestMethod1`. |
| `dotnet test --filter FullyQualifiedName~NUnitNamespace.UnitTest1` | Exécute les tests qui sont dans la classe `NUnitNamespace.UnitTest1`.<br>
| `dotnet test --filter FullyQualifiedName!=NUnitNamespace.UnitTest1.TestMethod1` | Exécute tous les tests sauf `NUnitNamespace.UnitTest1.TestMethod1`. |
| `dotnet test --filter TestCategory=CategoryA` | Exécute les tests qui sont annotés avec `[Category("CategoryA")]`. |
| `dotnet test --filter Priority=2` | Exécute les tests qui sont annotés avec `[Priority(2)]`.<br>

**Utilisation des opérateurs conditionnels | et &amp;**

| Expression | Résultat |
| ---------- | ------ |
| <code>dotnet test --filter "FullyQualifiedName~UnitTest1&#124;TestCategory=CategoryA"</code> | Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **ou** `TestCategory` est `CategoryA`. |
| `dotnet test --filter "FullyQualifiedName~UnitTest1&TestCategory=CategoryA"` | Exécute les tests qui ont `UnitTest1` dans `FullyQualifiedName` **et** `TestCategory` est `CategoryA`. |
| <code>dotnet test --filter "(FullyQualifiedName~UnitTest1&TestCategory=CategoryA)&#124;Priority=1"</code> | Exécute les tests qui ont un `FullyQualifiedName` contenant `UnitTest1` **et** `TestCategory` est `CategoryA` **ou** `Priority` est 1. |
