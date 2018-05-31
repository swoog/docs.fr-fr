---
title: foreach, in (référence C#)
ms.date: 05/24/2018
f1_keywords:
- foreach
- foreach_CSharpKeyword
helpviewer_keywords:
- foreach keyword [C#]
- foreach statement [C#]
- in keyword [C#]
ms.assetid: 5a9c5ddc-5fd3-457a-9bb6-9abffcd874ec
ms.openlocfilehash: b6b7dc0a4d3970ddfbbb6635ccebbbd5b75671e4
ms.sourcegitcommit: 54231aa56fca059e9297888a96fbca1d4cf3746c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2018
ms.locfileid: "34549374"
---
# <a name="foreach-in-c-reference"></a>foreach, in (référence C#)

L’instruction `foreach` exécute une instruction ou un bloc d’instructions pour chaque élément d’une instance du type qui implémente l’interface <xref:System.Collections.IEnumerable?displayProperty=nameWithType> ou <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>. L’instruction `foreach` n’est pas limitée à ces types et peut être appliquée à une instance de n’importe quel type répondant aux conditions suivantes :

- comporte la méthode `GetEnumerator` sans paramètre publique dont le retour est de type classe, struct ou interface,
- le type de retour de la méthode `GetEnumerator` contient la propriété publique `Current` et la méthode sans paramètre publique `MoveNext`, dont le type de retour est <xref:System.Boolean>.

Vous pouvez quitter la boucle à n’importe quel endroit du bloc d’instruction `foreach` à l’aide du mot clé [break](break.md), ou passer à l’itération suivante de la boucle à l’aide du mot clé [continue](continue.md). Vous pouvez également quitter une boucle `foreach` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).

## <a name="examples"></a>Exemples

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

L’exemple suivant montre l’utilisation de l’instruction `foreach` avec une instance de type <xref:System.Collections.Generic.List%601> qui implémente l’interface <xref:System.Collections.Generic.IEnumerable%601> :

[!code-csharp-interactive[list example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#1)]

L’exemple suivant utilise l’instruction `foreach` avec une instance de type <xref:System.Span%601?displayProperty=nameWithType> qui n’implémente aucune interface :

[!code-csharp-interactive[span example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#2)]

## <a name="c-language-specification"></a>Spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

[L’instruction foreach (spécification du langage C#)](/dotnet/csharp/language-reference/language-specification/statements#the-foreach-statement)  
[Utilisation de foreach avec des tableaux](../../programming-guide/arrays/using-foreach-with-arrays.md)  
[for](for.md)  
[Instructions d’itération](iteration-statements.md)  
[Mots clés C#](index.md)  
[Référence C#](../index.md)  
[Guide de programmation C#](../../programming-guide/index.md)  