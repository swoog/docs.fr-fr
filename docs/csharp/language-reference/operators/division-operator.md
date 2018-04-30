---
title: /, opérateur (référence C#)
ms.date: 04/04/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- /_CSharpKeyword
helpviewer_keywords:
- / operator [C#]
- division operator [C#]
ms.assetid: d155e496-678f-4efa-bebe-2bd08da2c5af
caps.latest.revision: 21
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 5b17d122e3e3f75012e084903b6f8975fb53d46c
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2018
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
 [Référence C#](../../../csharp/language-reference/index.md)  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
