---
title: '%=, opérateur (référence C#)'
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: ab3a6a8d5cbfeb4d527ca1f9c233ddfaba3d35ff
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188714"
---
# <a name="-operator-c-reference"></a>%=, opérateur (référence C#)

Opérateur d’assignation de reste.

Expression utilisant l’opérateur `%=`, par exemple  

```csharp
x %= y
```  

est équivalent à  

```csharp
x = x % y
```  

sauf que `x` n’est évalué qu’une seule fois.
  
[L’opérateur de reste](remainder-operator.md) `%` calcule le reste après division de ses opérandes. Il est pris en charge par tous les types numériques.

Si un type défini par l’utilisateur [surcharge](../keywords/operator.md) l’[opérateur de reste](remainder-operator.md) `%`, l’opérateur d’assignation de reste `%=` est implicitement surchargé.
  
L’exemple suivant illustre l’utilisation de l’opérateur `%=` :

[!code-csharp-interactive[%= example](~/samples/snippets/csharp/language-reference/operators/RemainderExamples.cs#3)]

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Opérateurs C#](index.md)
