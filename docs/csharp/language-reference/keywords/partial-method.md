---
title: partial, méthode - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- partialmethod_CSharpKeyword
helpviewer_keywords:
- partial methods [C#]
ms.assetid: 43f40242-17e0-4452-8573-090503ad3137
ms.openlocfilehash: 14bcd3329b6ca8e46f6c180c97174a561108d143
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633360"
---
# <a name="partial-method-c-reference"></a>partial, méthode (référence C#)

La signature d’une méthode partielle est définie dans une partie d’un type partiel, tandis que son implémentation est définie dans une autre partie du type. Les méthodes partielles permettent aux concepteurs de classes de fournir des hooks de méthode, semblables aux gestionnaires d’événements, que les développeurs peuvent décider ou non d’implémenter. Si le développeur ne fournit pas d’implémentation, le compilateur supprime la signature au moment de la compilation. Les méthodes partielles obéissent aux conditions suivantes :

- Les signatures des deux parties du type partiel doivent correspondre.

- La méthode doit retourner void.

- Aucun modificateur d’accès n’est autorisé. Les méthodes partielles sont implicitement privées.

L’exemple suivant illustre une méthode partielle définie dans deux parties d’une classe partielle :

[!code-csharp[csrefKeywordsContextual#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#9)]

Pour plus d’informations, consultez [Classes et méthodes partielles](../../programming-guide/classes-and-structs/partial-classes-and-methods.md).

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [partial, type](partial-type.md)
