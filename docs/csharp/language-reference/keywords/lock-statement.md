---
title: lock, instruction (référence C#)
description: Utilisez l’instruction lock en C# pour synchroniser l’accès des threads à une ressource partagée
ms.date: 08/28/2018
f1_keywords:
- lock_CSharpKeyword
- lock
helpviewer_keywords:
- lock keyword [C#]
ms.assetid: 656da1a4-707e-4ef6-9c6e-6d13b646af42
ms.openlocfilehash: 2b6fbfb2f81d7745c4effb9ea0087f34cc872a6c
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43858354"
---
# <a name="lock-statement-c-reference"></a>lock, instruction (référence C#)

L’instruction `lock` obtient le verrou d’exclusion mutuelle d’un objet donné, exécute un bloc d’instructions, puis libère le verrou. Tant qu’un verrou est maintenu, le thread qui contient le verrou peut à nouveau obtenir et libérer le verrou. Tout autre thread se voit bloquer l’obtention du verrou et attend que ce dernier soit libéré.

L’instruction `lock` se présente sous la forme

```csharp
lock (x)
{
    // Your code...
}
```

où `x` est une expression de [type référence](reference-types.md). Elle équivaut précisément à

```csharp
object __lockObj = x;
bool __lockWasTaken = false;
try
{
    System.Threading.Monitor.Enter(__lockObj, ref __lockWasTaken);
    // Your code...
}
finally
{
    if (__lockWasTaken) System.Threading.Monitor.Exit(__lockObj);
}
```

Dans la mesure où le code utilise un bloc [try...finally](try-finally.md), le verrou est libéré même si une exception est levée dans le corps d’une instruction `lock`.

Vous ne pouvez pas utiliser le mot clé [await](await.md) dans le corps d’une instruction `lock`.

## <a name="remarks"></a>Notes

Quand vous synchronisez l’accès des threads à une ressource partagée, verrouillez une instance d’objet dédiée (par exemple `private readonly object balanceLock = new object();`) ou toute autre instance peu susceptible d’être utilisée comme objet de verrouillage par des parties du code non associées. Évitez d’utiliser la même instance d’objet de verrouillage pour différentes ressources partagées, car cela peut entraîner une contention d’interblocage ou de verrouillage. En particulier, évitez

- `this` (peut être utilisé en tant que verrou par les appelants)
- Les instances de <xref:System.Type> (peuvent être obtenues par l’opérateur [typeof](typeof.md) ou par réflexion)
- Les instances de chaîne, notamment les littéraux de chaîne

en tant qu’objets de verrouillage.

## <a name="example"></a>Exemple

L’exemple suivant définit une classe `Account`, qui synchronise l’accès à son champ `balance` privé en verrouillant une instance `balanceLock` dédiée. L’utilisation de la même instance pour le verrouillage permet de garantir que le champ `balance` ne peut pas être mis à jour simultanément par deux threads qui tentent d’appeler les méthodes `Debit` ou `Credit` en même temps.

[!code-csharp[lock-statement-example](~/samples/snippets/csharp/keywords/LockStatementExample.cs)]

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.SpinLock?displayProperty=nameWithType>
- <xref:System.Threading.Interlocked?displayProperty=nameWithType>
- [Référence C#](../index.md)
- [Mots clés C#](index.md)
- [Mots clés d’instructions](statement-keywords.md)
- [Opérations verrouillées](../../../standard/threading/interlocked-operations.md)
- [Vue d’ensemble des primitives de synchronisation](../../../standard/threading/overview-of-synchronization-primitives.md)