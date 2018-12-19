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
ms.openlocfilehash: 87ccc3a18f0956ffe800ae97598e621e5ca72480
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53238375"
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
