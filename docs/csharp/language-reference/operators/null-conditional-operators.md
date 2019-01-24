---
title: Opérateurs conditionnels Null - Référence C#
ms.custom: seodec18
ms.date: 04/03/2015
helpviewer_keywords:
- null-conditional operators [C#]
- ?. operator [C#]
- ?[] operator [C#]
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
ms.openlocfilehash: 38298cded904cbfedeaf3c6b66c74d610d714902
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333237"
---
# <a name="-and--null-conditional-operators-c-and-visual-basic"></a>?. et ?[], opérateurs conditionnels Null (C# et Visual Basic)

Teste si l’opérande de gauche a une valeur Null avant d’effectuer une opération d’accès au membre (`?.`) ou d’index (`?[]`) ; retourne `null` si l’opérande de gauche s’évalue à `null`.

Ces opérateurs permettent d’écrire moins de code pour gérer les vérifications Null, notamment pour l’exploration des structures de données.

```csharp
int? length = customers?.Length; // null if customers is null
Customer first = customers?[0];  // null if customers is null
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null
```

Les opérateurs conditionnels Null ont un effet de court-circuit.  Si une opération dans une chaîne d'opérations d'accès au membre et d'indexation conditionnelles retourne une valeur Null, l'exécution du reste de la chaîne s'arrête.  Dans l’exemple ci-dessous, `E` ne s’exécute pas si `A`, `B` ou `C` a une valeur Null.

```csharp
A?.B?.C?.Do(E);
A?.B?.C?[E];
```

L’accès au membre conditionnel Null s’utilise également pour appeler des délégués de façon thread-safe, avec beaucoup moins de code.  Avec l'ancienne méthode, vous deviez utiliser un code similaire au suivant :

```csharp
var handler = this.PropertyChanged;
if (handler != null)
    handler(…);
```

La nouvelle méthode est beaucoup plus simple :

```csharp
PropertyChanged?.Invoke(…)
```

La nouvelle méthode est thread-safe, car le compilateur génère du code qui évalue `PropertyChanged` une seule fois, en conservant le résultat dans une variable temporaire. Vous devez explicitement appeler la méthode `Invoke`, car il n'existe pas de syntaxe d'appel de délégué conditionnel Null `PropertyChanged?(e)`.

## <a name="language-specifications"></a>Spécifications du langage

Pour plus d’informations, consultez [Opérateur de condition Null](~/_csharplang/spec/expressions.md#null-conditional-operator) dans la [spécification du langage C#](../language-specification/index.md). La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.

## <a name="see-also"></a>Voir aussi

- [?? (opérateur de fusion Null)](null-coalescing-operator.md)
- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)