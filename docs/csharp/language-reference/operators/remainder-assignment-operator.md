---
title: '%=, opérateur - Référence C#'
ms.custom: seodec18
ms.date: 09/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: d0732f9578b64c894ecc1d3bb15cee11a8d5b6a3
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245559"
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
