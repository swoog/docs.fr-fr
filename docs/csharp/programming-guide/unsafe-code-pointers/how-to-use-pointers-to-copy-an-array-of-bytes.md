---
title: "Comment : utiliser des pointeurs pour copier un tableau d'octets (Guide de programmation C#)"
ms.date: 04/20/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- byte arrays [C#]
- arrays [C#], byte
- pointers [C#], to copy bytes
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 6e87a2ec2c04812ac9b998c4c6d9a18d1b097342
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-use-pointers-to-copy-an-array-of-bytes--c-programming-guide"></a>Comment : utiliser des pointeurs pour copier un tableau d'octets (Guide de programmation C#)

L’exemple suivant utilise des pointeurs pour copier des octets d’un tableau à un autre.

Cet exemple utilise le mot clé [unsafe](../../language-reference/keywords/unsafe.md), qui vous permet d’utiliser des pointeurs dans la méthode `Copy`. L’instruction [fixed](../../language-reference/keywords/fixed-statement.md) permet de déclarer des pointeurs vers les tableaux source et de destination. L’instruction `fixed` *épingle* l’emplacement des tableaux source et de destination en mémoire pour que ceux-ci ne soient pas déplacés par l’opération de garbage collection. Les blocs de mémoire des tableaux sont libérés quand le bloc `fixed` est effectué. Comme la méthode `Copy` dans cet exemple utilise le mot clé `unsafe`, elle doit être compilée avec l’option de compilateur [-unsafe](../../language-reference/compiler-options/unsafe-compiler-option.md).

Cet exemple accède aux éléments des deux tableaux au moyen d’index et non au moyen d’un second pointeur non managé. La déclaration des pointeurs `pSource` et `pTarget` épingle les tableaux. Cette fonctionnalité est disponible à compter de C# 7.3.

## <a name="example"></a>Exemple

[!code-csharp[Struct with embedded inline array](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#8)]

## <a name="see-also"></a>Voir aussi
 [Guide de programmation C#](../index.md)  
 [Pointeurs et code unsafe](index.md)  
 [-unsafe (Options du compilateur C#)](../../language-reference/compiler-options/unsafe-compiler-option.md)  
 [Nettoyage de la mémoire](../../../standard/garbage-collection/index.md)  
