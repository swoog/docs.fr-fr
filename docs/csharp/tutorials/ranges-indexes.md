---
title: Explorer les plages de données à l’aide d’index et de plages
description: Ce tutoriel avancé vous apprend à explorer les données à l’aide d’index et de plages pour examiner les tranches d’un jeu de données séquentiel.
ms.date: 04/19/2019
ms.custom: mvc
ms.openlocfilehash: 64fae4581e265d4f70b8356d5c651b4fdaca3fe9
ms.sourcegitcommit: dd3b897feb5c4ac39732bb165848e37a344b0765
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2019
ms.locfileid: "64431498"
---
# <a name="indices-and-ranges"></a>Index et plages

Les plages et les index fournissent une syntaxe concise pour accéder à des éléments uniques ou des plages dans un <xref:System.Array>, <xref:System.Span%601> ou <xref:System.ReadOnlySpan%601>. Ces fonctionnalités permettent d’utiliser une syntaxe plus concise et claire pour accéder à des éléments uniques ou à des plages d’éléments dans une séquence.

Dans ce tutoriel, vous allez apprendre à :

> [!div class="checklist"]
> * Utiliser la syntaxe pour les plages dans une séquence.
> * Comprendre les décisions de conception pour le début et la fin de chaque séquence.
> * Découvrir des scénarios pour les types <xref:System.Index> et <xref:System.Range>.

## <a name="language-support-for-indices-and-ranges"></a>Prise en charge linguistique pour les index et les plages

Vous pouvez spécifier un index **à partir de la fin** en utilisant le caractère `^` avant l’index. L’indexation à partir de la fin démarre à partir de la règle que `0..^0` spécifie pour la plage entière. Pour énumérer un tableau entier, vous démarrez *au premier élément* et continuez jusqu’à ce que vous soyez *passé par le dernier élément*. Considérez le comportement de la méthode `MoveNext` sur un énumérateur : elle retourne la valeur false quand l’énumération franchit le dernier élément. L’index `^0` signifie « la fin », `array[array.Length]` ou l’index qui suit le dernier élément. Vous connaissez déjà `array[2]`, qui signifie l’élément « 2 à partir du début ». Maintenant, `array[^2]` signifie que l’élément « 2 à partir de la fin ». 

Vous pouvez spécifier une **plage** avec **l’opérateur de plage** : `..`. Par exemple, `0..^0` spécifie la totalité de la plage du tableau : 0 à partir du début jusqu'à 0 à partir de la fin non inclus. Les deux opérandes peuvent utiliser « à partir du début » ou « à partir de la fin ». L’un comme l’autre peuvent être omis. Les valeurs par défaut sont `0` pour l’index de début et `^0` pour l’index de fin.

```csharp-interactive
string[] words = new string[]
{
                // index from start    index from end
    "The",      // 0                   ^9
    "quick",    // 1                   ^8
    "brown",    // 2                   ^7
    "fox",      // 3                   ^6
    "jumped",   // 4                   ^5
    "over",     // 5                   ^4
    "the",      // 6                   ^3
    "lazy",     // 7                   ^2
    "dog"       // 8                   ^1
};              // 9 (or words.Length) ^0
```

L’index de chaque élément renforce le concept « à partir du début » et « à partir de la fin » ; ces plages excluent la fin de la plage. Le « début » de la totalité du tableau est le premier élément. La « fin » de la totalité du tableau se trouve *après* le dernier élément.

Vous pouvez récupérer le dernier mot avec l’index `^1`. Ajoutez le code suivant sous l’initialisation :

[!code-csharp[LastIndex](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_LastIndex)]

Le code suivant crée une sous-plage qui comporte les mots « quick », « brown » et « fox » et va de `words[1]` à `words[3]`. L’élément `words[4]` n’est pas dans la plage. Ajoutez le code suivant à la même méthode. Copiez-le et collez-le en bas de la fenêtre interactive.

[!code-csharp[Range](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_Range)]

Le code suivant crée une sous-plage qui comporte « lazy » et « dog » et comprend `words[^2]` et `words[^1]`. L’index de fin `words[^0]` n’est pas inclus. Ajoutez également le code suivant :

[!code-csharp[LastRange](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_LastRange)]

Les exemples suivants créent des plages ouvertes au début, à la fin ou les deux :

[!code-csharp[PartialRange](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_PartialRanges)]

Vous pouvez également déclarer des plages ou index comme variables. La variable peut ensuite être utilisée à l’intérieur des caractères `[` et `]` :

[!code-csharp[IndexRangeTypes](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_RangeIndexTypes)]

Les exemples précédents montrent deux décisions de conception qui nécessitent des explications supplémentaires :

- Les plages sont *exclusives*, ce qui signifie que l’élément au dernier index n’est pas dans la plage.
- L’index `^0` est *la fin* de la collection, pas *le dernier élément* de la collection.

L’exemple suivant montre un grand nombre des raisons de ces choix. Modifiez `x`, `y` et `z` pour essayer différentes combinaisons. Quand vous effectuez des essais, utilisez des valeurs de telle sorte que `x` soit inférieur à `y` et `y` inférieur à `z` pour avoir des combinaisons valides. Ajoutez le code suivant à une nouvelle méthode. Essayez différentes combinaisons :

[!code-csharp[SemanticsExamples](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_Semantics)]

## <a name="scenarios-for-indices-and-ranges"></a>Scénarios pour les index et les plages

L’utilisation de plages et d’index est fréquente pour effectuer une analyse sur une sous-plage d’une séquence entière. La nouvelle syntaxe permet de mieux lire la sous-plage exactement impliquée. La fonction locale `MovingAverage` prend un <xref:System.Range> comme argument. La méthode énumère ensuite simplement cette plage lors du calcul des valeurs minimale, maximale et moyenne. Essayez le code suivant dans votre projet :

[!code-csharp[MovingAverages](~/samples/csharp/tutorials/RangesIndexes/IndicesAndRanges.cs#IndicesAndRanges_MovingAverage)]

Vous pouvez télécharger le code terminé à partir du dépôt GitHub [dotnet/samples](https://github.com/dotnet/samples/tree/master/csharp/tutorials/RangesIndexes).
