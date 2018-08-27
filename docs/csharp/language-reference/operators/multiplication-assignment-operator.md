---
title: '*=, opérateur (référence C#)'
ms.date: 07/20/2015
f1_keywords:
- '*=_CSharpKeyword'
helpviewer_keywords:
- '*= operator [C#]'
- binary multiplication assignment operator (*=) [C#]
ms.assetid: 2e472155-59db-4dbf-bb94-bcccfa1a794d
ms.openlocfilehash: e47bc5c681c94ac3fc5c345c56b3814350ffa5ec
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932348"
---
# <a name="-operator-c-reference"></a>*=, opérateur (référence C#)
Opérateur d’assignation de multiplication binaire.  
  
## <a name="remarks"></a>Notes  
 Une expression qui utilise l’opérateur d’assignation `*=`, telle que  
  
```csharp  
x *= y  
```  
  
 est équivalent à  
  
```csharp  
x = x * y  
```  
  
 sauf que `x` n’est évalué qu’une seule fois. L’[opérateur *](../../../csharp/language-reference/operators/multiplication-operator.md) est prédéfini pour les types numériques de façon à effectuer une multiplication.  
  
 L’opérateur `*=` ne peut pas être surchargé directement, mais les types définis par l’utilisateur peuvent surcharger l’[opérateur *](../../../csharp/language-reference/operators/multiplication-operator.md) (consultez [operator](../../../csharp/language-reference/keywords/operator.md)).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#13](../../../csharp/language-reference/operators/codesnippet/CSharp/multiplication-assignment-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
