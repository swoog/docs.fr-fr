---
title: '%=, opérateur (référence C#)'
ms.date: 04/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: 009c162b13fab05ba349d0535fe8dfae206502f3
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "42998654"
---
# <a name="-operator-c-reference"></a>%=, opérateur (référence C#)
Opérateur d’assignation de reste.  
  
## <a name="remarks"></a>Notes  
 Une expression qui utilise l’opérateur d’assignation `%=`, telle que  
  
```csharp  
x %= y  
```  
  
 est équivalent à  
  
```csharp  
x = x % y  
```  
  
 sauf que `x` n’est évalué qu’une seule fois. L’[opérateur %](../../../csharp/language-reference/operators/remainder-operator.md) est prédéfini pour les types numériques de façon à calculer le reste d’une division.  
  
 L’opérateur `%=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur %](../../../csharp/language-reference/operators/remainder-operator.md) (consultez [operator (informations de référence sur C#)](../../../csharp/language-reference/keywords/operator.md)).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#4](../../../csharp/language-reference/operators/codesnippet/CSharp/modulus-assignment-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
