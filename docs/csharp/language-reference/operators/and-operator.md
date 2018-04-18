---
title: '&amp;, opérateur (référence C#)'
ms.date: 04/04/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '&_CSharpKeyword'
helpviewer_keywords:
- bitwise AND operator [C#]
- ampersand operator (&) [C#]
- '& operator [C#]'
- AND operator (&) [C#]
ms.assetid: afa346d5-90ec-4b1f-a2c8-3881f018741d
caps.latest.revision: 19
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: f26305bfa1e8c9ba45493ad2ab4937d554590911
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
---
# <a name="amp-operator-c-reference"></a>&amp;, opérateur (référence C#)
L’opérateur `&` peut être utilisé comme opérateur unaire ou opérateur binaire.  
  
## <a name="remarks"></a>Notes  
 L’opérateur `&` unaire retourne l’adresse de son opérande (requiert un contexte [unsafe](../../../csharp/language-reference/keywords/unsafe.md)).  
  
 Les opérateurs `&` binaires sont prédéfinis pour les types intégraux et `bool`. Pour les types intégraux, & calcule l’opération logique AND au niveau du bit de ses opérandes. Pour les opérandes `bool`, & calcule l’opération logique AND de ses opérandes ; autrement dit, le résultat est `true` uniquement si ses deux opérandes ont la valeur `true`.  
  
 L’opérateur `&` binaire évalue les deux opérateurs, quelle que soit la valeur du premier, à la différence de [l’opérateur AND conditionnel](../../../csharp/language-reference/operators/conditional-and-operator.md) `&&`. Exemple :  
  
 [!code-csharp[csRefOperators#37](../../../csharp/language-reference/operators/codesnippet/CSharp/and-operator_1.cs)]  
  
 Les types définis par l’utilisateur peuvent surcharger l’opérateur `&` binaire (voir [operator](../../../csharp/language-reference/keywords/operator.md)). Les opérations sur les types intégraux sont en général autorisées sur l’énumération. Quand un opérateur binaire est surchargé, l’opérateur d’assignation correspondant, le cas échéant, est aussi implicitement surchargé.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#38](../../../csharp/language-reference/operators/codesnippet/CSharp/and-operator_2.cs)]  
  
## <a name="see-also"></a>Voir aussi  
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
