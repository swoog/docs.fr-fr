---
title: stackalloc, mot clé (référence C#)
ms.date: 04/12/2018
f1_keywords:
- stackalloc_CSharpKeyword
- stackalloc
helpviewer_keywords:
- stackalloc keyword [C#]
ms.openlocfilehash: 16b2933423599e985ce57257595d67026dba93ca
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50184521"
---
# <a name="stackalloc-c-reference"></a>stackalloc (référence C#)

Le mot clé `stackalloc` est utilisé dans un contexte de code unsafe pour allouer un bloc de mémoire sur la pile.

```csharp
int* block = stackalloc int[100];
```

## <a name="remarks"></a>Notes

Le mot clé est valide uniquement dans les initialiseurs de variable locale. Le code suivant génère des erreurs de compilation.

```csharp
int* block;
// The following assignment statement causes compiler errors. You
// can use stackalloc only when declaring and initializing a local
// variable.
block = stackalloc int[100];
```

Dans C# 7.3 et les versions ultérieures, vous pouvez utiliser la syntaxe d’initialiseur de tableau pour les tableaux `stackalloc`. Toutes les déclarations suivantes déclarent un tableau de trois éléments ayant pour valeurs les entiers `1`, `2` et `3` :

```csharp
// Valid starting with C# 7.3
int* first = stackalloc int[3] { 1, 2, 3 };
int* second = stackalloc int[] { 1, 2, 3 };
int* third = stackalloc[] { 1, 2, 3 };
```

Des types pointeur étant impliqués, `stackalloc` requiert un contexte [unsafe](unsafe.md). Pour plus d’informations, consultez [Pointeurs et code unsafe](../../programming-guide/unsafe-code-pointers/index.md).

`stackalloc` est similaire à [_alloca](/cpp/c-runtime-library/reference/alloca) dans la bibliothèque Runtime C.

## <a name="examples"></a>Exemples

L’exemple suivant calcule et affiche les 20 premiers nombres de la suite de Fibonacci. Chaque nombre est la somme des deux nombres précédents. Dans le code, un bloc de mémoire de taille suffisante pour contenir 20 éléments de type `int` est alloué sur la pile, et non sur le tas. L’adresse du bloc est stockée dans le pointeur `fib`. Cette mémoire n’est pas soumise au garbage collection et n’est donc pas tenue d’être épinglée (en utilisant [fixed](fixed-statement.md)). La durée de vie du bloc de mémoire est limitée à la durée de vie de la méthode qui le définit. Vous ne pouvez pas libérer la mémoire avant le retour de la méthode.

[!code-csharp[csrefKeywordsOperator#15](~/samples/snippets/csharp/keywords/StackAllocExamples.cs#1)]

L’exemple suivant initialise un tableau `stackalloc` d’entiers sur un masque de bits où un bit est défini dans chaque élément. Cela illustre la nouvelle syntaxe d’initialiseur disponible à partir de C# 7.3 :

[!code-csharp[csrefKeywordsOperator#15](~/samples/snippets/csharp/keywords/StackAllocExamples.cs#2)]

## <a name="security"></a>Sécurité

Le code unsafe est moins sûr que les alternatives safe. Toutefois, l’utilisation de `stackalloc` active automatiquement les fonctionnalités de détection des dépassements de mémoire tampon dans le Common Language Runtime (CLR). Si un dépassement de mémoire tampon est détecté, le processus est terminé aussi rapidement que possible pour réduire les risques d’exécution de code malveillant.

## <a name="c-language-specification"></a>spécification du langage C#

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)
- [Mots clés des opérateurs](../../../csharp/language-reference/keywords/operator-keywords.md)
- [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md)