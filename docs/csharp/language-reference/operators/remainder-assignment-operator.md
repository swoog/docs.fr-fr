---
title: '%=, opérateur (référence C#)'
ms.date: 04/04/2018
f1_keywords:
- '%=_CSharpKeyword'
helpviewer_keywords:
- remainder assignment operator (%=) [C#]
- '%= assignment operator (remainder assignment) [C#]'
ms.assetid: 47e5f068-1d97-4010-bd3b-e21b5d3a77f5
ms.openlocfilehash: aadcb5ef969ff408cc1e738fc0f5b67152fdc78b
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2018
ms.locfileid: "34171965"
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
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
