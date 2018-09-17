---
title: Guide pratique pour caster de manière sécurisée avec les critères spéciaux, ainsi que les opérateurs is et as
description: Découvrez les techniques relatives aux critères spéciaux pour caster de manière sécurisée des variables vers un autre type. Vous pouvez utiliser les critères spéciaux, ainsi que les opérateurs is et as pour convertir des types de manière sécurisée.
ms.date: 09/05/2018
helpviewer_keywords:
- cast operators [C#], as and is operators
- as operator [C#]
- is operator [C#]
ms.openlocfilehash: 88289099864293b3b19da62155d58ba4797948bd
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44216172"
---
# <a name="how-to-safely-cast-by-using-pattern-matching-is-and-as-operators"></a>Guide pratique pour caster de manière sécurisée avec les critères spéciaux, ainsi que les opérateurs is et as

Dans la mesure où les objets sont polymorphes, une variable d’un type de classe de base peut contenir un [type](../programming-guide/types/index.md) dérivé. Pour accéder aux membres d’instance du type dérivé, il est nécessaire de réeffectuer un [cast](../programming-guide/types/casting-and-type-conversions.md) de la valeur vers le type dérivé. Toutefois, un cast risque de lever <xref:System.InvalidCastException>. C# fournit des instructions relatives aux [critères spéciaux](../pattern-matching.md), qui effectuent un cast de manière conditionnelle, uniquement en cas de réussite. C# fournit également les opérateurs [is](../language-reference/keywords/is.md) et [as](../language-reference/keywords/as.md) pour tester l’appartenance d’une valeur à un certain type.

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

Le code suivant illustre l’instruction `is` relative aux critères spéciaux. Il contient des méthodes qui testent un argument de méthode pour déterminer s’il s’agit d’un ensemble possible de types dérivés :

[!code-csharp-interactive[Pattern matching is statement](../../../samples/snippets/csharp/how-to/safelycast/patternmatching/Program.cs#PatternMatchingIs)]

L’exemple précédent illustre quelques fonctionnalités de la syntaxe relative aux critères spéciaux. Les instructions `if (a is Mammal m)` et `if (o is Mammal m)` combinent le test à une assignation d’initialisation. L’assignation a lieu uniquement en cas de réussite du test. La variable `m` se trouve uniquement dans l’étendue de l’instruction `if` incorporée, à laquelle elle a été assignée. Vous ne pouvez pas accéder à `m` plus tard dans la même méthode. Faites un essai dans la fenêtre interactive.

Vous pouvez également utiliser la même syntaxe afin de tester l’existence d’une valeur pour un [type Nullable](../programming-guide/nullable-types/index.md), comme indiqué dans l’exemple de code suivant :

[!code-csharp-interactive[Pattern matching with nullable types](../../../samples/snippets/csharp/how-to/safelycast/nullablepatternmatching/Program.cs#PatternMatchingNullable)]

L’exemple précédent illustre d’autres fonctionnalités relatives aux critères spéciaux pour les conversions. Vous pouvez tester le modèle null d’une variable en vérifiant spécifiquement la valeur `null`. Quand la valeur runtime de la variable est `null`, une instruction `is` de vérification de type retourne toujours `false`. L’instruction `is` relative aux critères spéciaux n’autorise aucun type valeur Nullable, par exemple `int?` ou `Nullable<int>`. Toutefois, vous pouvez tester un autre type valeur.

L’exemple précédent montre également comment utiliser l’expression `is` relative aux critères spéciaux dans une instruction `switch`, où la variable peut avoir plusieurs types différents.

Pour déterminer si une variable a un type donné, mais sans l’assigner pour autant à une nouvelle variable, vous pouvez utiliser les opérateurs `is` et `as` pour les types référence et les types Nullable. Le code suivant montre comment utiliser les instructions `is` et `as`, qui faisaient partie du langage C# avant l’introduction des critères spéciaux permettant de déterminer l’existence ou non d’un type donné pour une variable :

[!code-csharp-interactive[testing variable types with the is and as statements](../../../samples/snippets/csharp/how-to/safelycast/asandis/Program.cs#IsAndAs)]

Comme vous pouvez le constater en comparant ce code avec le code utilisant les critères spéciaux, la syntaxe des critères spéciaux fournit des fonctionnalités plus robustes, car elle combine le test et l’assignation dans une seule instruction. Utilisez la syntaxe des critères spéciaux autant que possible.

Vous pouvez essayer ces exemples en examinant le code dans notre [dépôt GitHub](https://github.com/dotnet/samples/tree/master/snippets/csharp/how-to/safelycast). Vous pouvez aussi télécharger les exemples [sous forme de fichier zip](https://github.com/dotnet/samples/raw/master/snippets/csharp/how-to/safelycast.zip).
