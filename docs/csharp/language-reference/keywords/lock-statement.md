---
title: lock, instruction (référence C#)
description: 'Le mot-clé lock est utilisé dans le threading '
ms.date: 07/20/2015
f1_keywords:
- lock_CSharpKeyword
- lock
helpviewer_keywords:
- lock keyword [C#]
ms.assetid: 656da1a4-707e-4ef6-9c6e-6d13b646af42
ms.openlocfilehash: 6ed46837482642dfd7e1a96cd120fc18023c5e9f
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42931191"
---
# <a name="lock-statement-c-reference"></a>lock, instruction (référence C#)

Le mot clé `lock` marque un bloc d’instructions comme étant une section critique en obtenant le verrou d’exclusion mutuelle pour un objet donné, en exécutant une instruction, puis en libérant le verrou. L’exemple suivant inclut une instruction `lock`.

```csharp
class Account
{
    decimal balance;
    private Object thisLock = new Object();

    public void Withdraw(decimal amount)
    {
        lock (thisLock)
        {
            if (amount > balance)
            {
                throw new Exception("Insufficient funds");
            }
            balance -= amount;
        }
    }
}
```

Pour plus d’informations, consultez [Synchronisation des threads](../../programming-guide/concepts/threading/thread-synchronization.md).

## <a name="remarks"></a>Notes

Le mot clé `lock` garantit qu’un thread n’entre pas dans une section critique de code alors qu’un autre thread est dans cette section critique. Si un autre thread tente d’entrer dans un code verrouillé, il attend, en restant bloqué jusqu’à ce que l’objet soit libéré.

La section [Threading](../../programming-guide/concepts/threading/index.md) présente le threading.

Le mot clé `lock` appelle <xref:System.Threading.Monitor.Enter%2A> au début du bloc et <xref:System.Threading.Monitor.Exit%2A> à la fin du bloc. Une exception <xref:System.Threading.ThreadInterruptedException> est levée si <xref:System.Threading.Thread.Interrupt%2A> interrompt un thread qui attend de passer une instruction `lock`.

D’une façon générale, évitez de verrouiller sur un type `public` ou sur des instances qui sont au-delà du contrôle de votre code. Les constructions courantes `lock (this)`, `lock (typeof (MyType))` et `lock ("myLock")` enfreignent cette directive :

- `lock (this)` est un problème si l’instance est accessible publiquement.

- `lock (typeof (MyType))` est un problème si `MyType` est accessible publiquement.

- `lock("myLock")` est un problème, car tout autre code dans le processus utilisant la même chaîne partagera le même verrou.

La bonne pratique consiste à définir un objet `private` à verrouiller, ou une variable objet `private static` pour protéger les données communes à toutes les instances.

Vous ne pouvez pas utiliser le mot clé [await](await.md) dans le corps d’une instruction `lock`.

## <a name="example---threads-without-locking"></a>Exemple - Threads sans verrouillage

L’exemple suivant montre une utilisation simple des threads sans verrouillage en C# :

[!code-csharp[csrefKeywordsFixedLock#5](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsFixedLock/CS/csrefKeywordsFixedLock.cs#5)]

## <a name="example---threads-using-locking"></a>Exemple : Threads utilisant le verrouillage

L’exemple suivant utilise des threads et `lock`. Tant que l’instruction `lock` est présente, le bloc d’instructions est une section critique et `balance` ne devient jamais un nombre négatif :

[!code-csharp[csrefKeywordsFixedLock#6](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsFixedLock/CS/csrefKeywordsFixedLock.cs#6)]

## <a name="c-language-specification"></a>spécification du langage C#

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi

- <xref:System.Reflection.MethodImplAttributes>
- <xref:System.Threading.Mutex>
- <xref:System.Threading.Monitor>
- [Référence C#](../../language-reference/index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Thread](../../programming-guide/concepts/threading/index.md)
- [Mots clés C#](index.md)
- [Mots clés d’instructions](statement-keywords.md)
- [Opérations verrouillées](../../../standard/threading/interlocked-operations.md)
- [AutoResetEvent](../../../standard/threading/autoresetevent.md)
- [Synchronisation des threads](../../programming-guide/concepts/threading/thread-synchronization.md)