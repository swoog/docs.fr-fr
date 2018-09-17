---
title: void (Référence C#)
ms.date: 07/20/2015
f1_keywords:
- void_CSharpKeyword
- void
helpviewer_keywords:
- void keyword [C#]
ms.assetid: 0d2d8a95-fe20-4fbd-bf5d-c1e54bce71d4
ms.openlocfilehash: 223db893dd42181c234d9a07c1a1c00af26f0c30
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45593060"
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

`void` est également utilisé dans un contexte unsafe pour déclarer un pointeur vers un type inconnu. Pour plus d’informations, consultez [Types pointeur](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md).

`void` est un alias du type <xref:System.Void?displayProperty=nameWithType> .NET Framework.

## <a name="c-language-specification"></a>Spécification du langage C#
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Mots clés C#](../../../csharp/language-reference/keywords/index.md)  
- [Types référence](../../../csharp/language-reference/keywords/reference-types.md)  
- [Types valeur](../../../csharp/language-reference/keywords/value-types.md)  
- [Méthodes](../../../csharp/programming-guide/classes-and-structs/methods.md)  
- [Pointeurs et code unsafe](../../../csharp/programming-guide/unsafe-code-pointers/index.md)
