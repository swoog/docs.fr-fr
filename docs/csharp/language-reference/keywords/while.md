---
title: while (référence C#)
ms.date: 05/28/2018
f1_keywords:
- while_CSharpKeyword
- while
helpviewer_keywords:
- while keyword [C#]
ms.assetid: 72a0765c-6852-4aca-b327-4a11cb7f5c59
ms.openlocfilehash: c082107472ac53d05b3b43dd4d9d8afc508a16cb
ms.sourcegitcommit: bbf70abe6b46073148f78cbf0619de6092b5800c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2018
ms.locfileid: "34565863"
---
# <a name="while-c-reference"></a>while (référence C#)

L’instruction `while` exécute une instruction ou un bloc d’instructions jusqu’à ce qu’une expression booléenne spécifique corresponde à la valeur `true`. Dans la mesure où cette expression est évaluée avant chaque exécution de la boucle, une boucle `while` s’exécute plusieurs fois ou pas du tout. Cela diffère de la boucle [do](do.md), qui s’exécute une ou plusieurs fois.

À tout moment dans le bloc d’instructions `while`, vous pouvez sortir de la boucle à l’aide de l’instruction [break](break.md).

Vous pouvez passer directement à l’évaluation de l’expression `while` à l’aide de l’instruction [continue](continue.md). Si l’expression correspond à `true`, l’exécution passe à la première instruction de la boucle. Sinon, l’exécution passe à la première instruction après la boucle.

Vous pouvez également quitter une boucle `while` en utilisant les instructions [goto](goto.md), [return](return.md) ou [throw](throw.md).

## <a name="example"></a>Exemple

L’exemple suivant illustre l’utilisation de l’instruction `while`. Sélectionnez **Exécuter** pour exécuter l’exemple de code. Après cela, vous pourrez modifier le code et le réexécuter.

[!code-csharp-interactive[while loop example](~/samples/snippets/csharp/keywords/IterationKeywordsExamples.cs#3)]

## <a name="c-language-specification"></a>spécification du langage C#

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

 [Référence C#](../index.md)  
 [Guide de programmation C#](../../programming-guide/index.md)  
 [Mots clés C#](index.md)  
 [while, instruction (C++)](/cpp/cpp/while-statement-cpp)  
 [Instructions d’itération](iteration-statements.md)  
 [Instruction do](do.md)  
