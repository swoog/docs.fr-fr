---
title: void - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- void_CSharpKeyword
- void
helpviewer_keywords:
- void keyword [C#]
ms.assetid: 0d2d8a95-fe20-4fbd-bf5d-c1e54bce71d4
ms.openlocfilehash: ce52e4d19335db0e21637b87bbd1589c86c06ae1
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53613126"
---
# <a name="void-c-reference"></a>void (Référence C#)

Quand le mot clé `void` est utilisé en tant que type de retour pour une méthode, il spécifie que cette méthode ne retourne aucune valeur.

`void` n’est pas autorisé dans la liste des paramètres d’une méthode. Une méthode sans paramètres qui ne retourne aucune valeur se déclare comme suit :

```csharp
public void SampleMethod()
{
    // Body of the method.
}
```

`void` est également utilisé dans un contexte unsafe pour déclarer un pointeur vers un type inconnu. Pour plus d’informations, consultez [Types pointeur](../../programming-guide/unsafe-code-pointers/pointer-types.md).

`void` est un alias du type <xref:System.Void?displayProperty=nameWithType> .NET Framework.

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Types référence](reference-types.md)
- [Types valeur](value-types.md)
- [Méthodes](../../programming-guide/classes-and-structs/methods.md)
- [Pointeurs et code unsafe](../../programming-guide/unsafe-code-pointers/index.md)