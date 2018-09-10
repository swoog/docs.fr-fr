---
title: /, opérateur (référence C#)
ms.date: 04/04/2018
f1_keywords:
- /_CSharpKeyword
helpviewer_keywords:
- / operator [C#]
- division operator [C#]
ms.assetid: d155e496-678f-4efa-bebe-2bd08da2c5af
ms.openlocfilehash: bddf6d234f3536ad64f0cd876cc7ade4494916d9
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43800753"
---
# <a name="-operator-c-reference"></a>/, opérateur (référence C#)
L’opérateur de division (`/`) divise son premier opérande par son deuxième opérande. Tous les types numériques ont des opérateurs de division prédéfinis.
  
## <a name="remarks"></a>Notes  
 Les types définis par l’utilisateur peuvent surcharger l’opérateur `/` (voir [operator](../../../csharp/language-reference/keywords/operator.md)). Une surcharge de l’opérateur `/` surcharge implicitement l’[opérateur /=](division-assignment-operator.md).  
  
 Quand vous divisez deux entiers, le résultat est toujours un entier. Par exemple, le résultat de 7 / 3 est 2. Il ne faut pas confondre avec la division plancher, car l’opérateur `/` arrondit le résultat vers zéro : -7 / 3 donne le résultat -2.  
  
 Pour obtenir un quotient sous forme de nombre rationnel, utilisez les types `float`, `double` ou `decimal`. Il existe de nombreuses façons d’effectuer des conversions entre des [types numériques intégrés](../../../csharp/language-reference/keywords/reference-tables-for-types.md).  
  
 Pour déterminer le reste, utilisez l’[opérateur de reste](../../../csharp/language-reference/operators/remainder-operator.md) `%`.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#42](../../../csharp/language-reference/operators/codesnippet/CSharp/division-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
