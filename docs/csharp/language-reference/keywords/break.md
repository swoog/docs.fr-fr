---
title: break, instruction (référence C#)
ms.date: 07/20/2015
f1_keywords:
- break
- break_CSharpKeyword
helpviewer_keywords:
- break keyword [C#]
ms.assetid: be2571ed-efb0-4965-b122-81e5b09db0b9
ms.openlocfilehash: 9dc71cce3cc0ca4035df483d2b3a3ab9a3bab9c5
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2018
ms.locfileid: "47215845"
---
# <a name="break-c-reference"></a>break (référence C#)

L’instruction `break` termine la boucle englobante ou l’instruction [switch](../../../csharp/language-reference/keywords/switch.md) la plus proche dans laquelle elle figure. Le contrôle est passé à l’instruction qui suit l’instruction terminée, le cas échéant.

## <a name="example"></a>Exemple

Dans cet exemple, l’instruction conditionnelle contient un compteur qui est supposé compter de 1 à 100. Toutefois, l’instruction `break` termine la boucle après le chiffre 4.

[!code-csharp[csrefKeywordsJump#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#1)]

## <a name="example"></a>Exemple

Dans cet exemple, l’instruction `break` est utilisée pour sortir d’une boucle imbriquée interne et passer le contrôle à la boucle externe.

[!code-csharp[csrefKeywordsJump#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#7)]

## <a name="example"></a>Exemple

Cet exemple illustre l’utilisation de `break` dans une instruction [switch](../../../csharp/language-reference/keywords/switch.md).

[!code-csharp[csrefKeywordsJump#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#2)]

Si vous aviez entré `4`, le résultat serait le suivant :

```console
Enter your selection (1, 2, or 3): 4
Sorry, invalid selection.
```

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [switch](../../../csharp/language-reference/keywords/switch.md)  
- [Instructions de saut](../../../csharp/language-reference/keywords/jump-statements.md)  
- [Instructions d’itération](../../../csharp/language-reference/keywords/iteration-statements.md)
