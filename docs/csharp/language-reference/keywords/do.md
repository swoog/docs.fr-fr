---
title: do (référence C#)
ms.date: 05/28/2018
f1_keywords:
- do_CSharpKeyword
- do
helpviewer_keywords:
- do keyword [C#]
ms.assetid: 50725f79-9ba6-4898-aa78-6e331568a1bb
ms.openlocfilehash: b918b378623a239803fb4e0a65fcf82fd677b21f
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34566083"
---
# <a name="do-c-reference"></a>do (référence C#)

L’instruction `do` exécute une instruction ou un bloc d’instructions jusqu’à ce qu’une expression booléenne spécifique corresponde à la valeur `true`. Dans la mesure où cette expression est évaluée après chaque exécution de la boucle, une boucle `do-while` s’exécute une ou plusieurs fois. Cela diffère de la boucle [while](while.md), qui s’exécute zéro ou plusieurs fois.

À tout moment dans le bloc d’instructions `do`, vous pouvez sortir de la boucle à l’aide de l’instruction [break](break.md).

Vous pouvez passer directement à l’évaluation de l’expression `while` à l’aide de l’instruction [continue](continue.md). Si l’expression correspond à `true`, l’exécution passe à la première instruction de la boucle. Sinon, l’exécution passe à la première instruction après la boucle.

Vous pouvez également quitter une boucle `do-while` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).

## <a name="example"></a>Exemple

L’exemple suivant illustre l’utilisation de l’instruction `do`. Sélectionnez **Exécuter** pour exécuter l’exemple de code. Après cela, vous pourrez modifier le code et le réexécuter.

[!code-csharp-interactive[do loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#4)]

## <a name="c-language-specification"></a>spécification du langage C#

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

 [Référence C#](../index.md)  
 [Guide de programmation C#](../../programming-guide/index.md)  
 [Mots clés C#](index.md)  
 [do-while, instruction (C++)](/cpp/cpp/do-while-statement-cpp)  
 [Instructions d’itération](iteration-statements.md)  
 [instruction while](while.md)  
