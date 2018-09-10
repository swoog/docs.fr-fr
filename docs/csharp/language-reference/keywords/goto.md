---
title: goto, instruction (référence C#)
ms.date: 07/20/2015
f1_keywords:
- goto_CSharpKeyword
- goto
helpviewer_keywords:
- goto keyword [C#]
ms.assetid: 2c03c9c1-8119-44ef-b740-fb3d287a42fe
ms.openlocfilehash: d4fd9f1f26b82b409d704c45e4bcf18cceef8282
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43405814"
---
# <a name="goto-c-reference"></a>goto (référence C#)

L’instruction `goto` transfère le contrôle du programme directement à une instruction étiquetée.

Une utilisation courante de `goto` consiste à transférer le contrôle à une étiquette switch-case ou à l’étiquette par défaut d’une instruction `switch`.

L’instruction `goto` sert aussi à quitter des boucles fortement imbriquées.

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser `goto` dans une instruction [switch](switch.md).

[!code-csharp[csrefKeywordsJump#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#4)]

## <a name="example"></a>Exemple

L’exemple suivant montre comment utiliser `goto` pour quitter des boucles imbriquées.

[!code-csharp[csrefKeywordsJump#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsJump/CS/csrefKeywordsJump.cs#5)]

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)  
- [Guide de programmation C#](../../programming-guide/index.md)  
- [Mots clés C#](index.md)  
- [goto, instruction (C++)](/cpp/cpp/goto-statement-cpp)  
- [Instructions de saut](jump-statements.md)  
