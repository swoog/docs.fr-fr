---
title: fixed, instruction - Référence C#
ms.custom: seodec18
ms.date: 05/10/2018
f1_keywords:
- fixed_CSharpKeyword
- fixed
helpviewer_keywords:
- fixed keyword [C#]
ms.openlocfilehash: 4ef334f6d200e75f29e22a9586f4538309797942
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59095982"
---
# <a name="fixed-statement-c-reference"></a>fixed, instruction (référence C#)

L’instruction `fixed` empêche le récupérateur de mémoire de déplacer une variable mobile. L’instruction `fixed` est uniquement autorisée dans un contexte [unsafe](unsafe.md). `fixed` peut également être utilisé pour créer des [mémoires tampons de taille fixe](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md).

L’instruction `fixed` définit un pointeur vers une variable managée et épingle cette variable pendant l’exécution de l’instruction. Les pointeurs vers des variables managées ne sont utiles que dans un contexte `fixed`. Sans contexte `fixed`, le garbage collection peut déplacer les variables de manière imprévisible. Le compilateur C# permet seulement d’assigner un pointeur à une variable managée dans une instruction `fixed`.

[!code-csharp[Accessing fixed memory](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#1)]

Vous pouvez initialiser un pointeur à l’aide d’un tableau, d’une chaîne, d’un tampon de taille fixe ou de l’adresse d’une variable. L’exemple suivant montre l’utilisation des adresses de variables, des tableaux et des chaînes. Pour plus d’informations sur les mémoires tampons de taille fixe, consultez [Mémoires tampons de taille fixe](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md).

[!code-csharp[Initializing fixed size buffers](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#2)]

À compter de C# 7.3, l’instruction `fixed` s’applique à d’autres types au-delà des tableaux, chaînes, mémoires tampons de taille fixe ou variables non managées. Tout type qui implémente une méthode nommée `GetPinnableReference` peut être épinglé. `GetPinnableReference` doit retourner une variable `ref` d’un type non géré. Consultez la rubrique consacrée aux [types pointeur](../../programming-guide/unsafe-code-pointers/pointer-types.md) pour plus d’informations. Les types .NET <xref:System.Span%601?displayProperty=nameWithType> et <xref:System.ReadOnlySpan%601?displayProperty=nameWithType> introduits dans .NET Core 2.0 utilisent ce modèle et peuvent être épinglés. Ceci est illustré dans l'exemple suivant :

[!code-csharp[Accessing fixed memory](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#FixedSpan)]

Si vous créez des types qui doivent être inclus dans ce modèle, consultez <xref:System.Span%601.GetPinnableReference?displayProperty=nameWithType> pour obtenir un exemple d’implémentation du modèle.

Plusieurs pointeurs peuvent être initialisés dans une instruction s’ils sont tous du même type :

```csharp
fixed (byte* ps = srcarray, pd = dstarray) {...}
```

Pour initialiser des pointeurs de types différents, imbriquez des instructions `fixed`, comme indiqué dans l’exemple suivant.

[!code-csharp[Initializing multiple pointers](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#3)]

Une fois que le code de l’instruction est exécuté, toutes les variables épinglées sont libérées et soumises au garbage collection. Par conséquent, ne pointez pas vers ces variables en dehors de l’instruction `fixed`. La portée des variables déclarées dans l’instruction `fixed` est limitée à cette instruction, ce qui facilite les choses :

```csharp
fixed (byte* ps = srcarray, pd = dstarray)
{
   ...
}
// ps and pd are no longer in scope here.
```

Les pointeurs initialisés dans des instructions `fixed` sont des variables en lecture seule. Pour modifier la valeur du pointeur, vous devez déclarer une deuxième variable de pointeur et la modifier. La variable déclarée dans l’instruction `fixed` ne peut pas être modifiée :

```csharp
fixed (byte* ps = srcarray, pd = dstarray)
{
    byte* pSourceCopy = ps;
    pSourceCopy++; // point to the next element.
    ps++; // invalid: cannot modify ps, as it is declared in the fixed statement.
}
```

En mode unsafe, vous pouvez allouer de la mémoire sur la pile, où elle n’est pas soumise au garbage collection et n’a donc pas besoin d’être épinglée. Pour plus d’informations, consultez [stackalloc](stackalloc.md).

[!code-csharp[Initializing multiple pointers](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#4)]

## <a name="c-language-specification"></a>Spécification du langage C#

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [unsafe](unsafe.md)
- [Mémoires tampons de taille fixe](../../programming-guide/unsafe-code-pointers/fixed-size-buffers.md)
