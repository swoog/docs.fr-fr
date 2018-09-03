---
title: =, opérateur (référence C#)
ms.date: 07/20/2015
f1_keywords:
- =_CSharpKeyword
helpviewer_keywords:
- = operator [C#]
ms.assetid: d802a6d5-32f0-42b8-b180-12f5a081bfc1
ms.openlocfilehash: 9cd1af400a9afdb7942a49dee7e7f7bb78387f2d
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43477930"
---
# <a name="-operator-c-reference"></a>=, opérateur (référence C#)
L’opérateur d’assignation (`=`) stocke la valeur de l’opérande de droite dans l’emplacement de stockage, la propriété ou l’indexeur indiqué par l’opérande de gauche et retourne la valeur comme résultat. Les opérandes doivent être du même type (ou l’opérande de droite doit être implicitement convertible en type de l’opérande de gauche).  
  
## <a name="remarks"></a>Notes  
 L’opérateur d’assignation ne peut pas être surchargé. Toutefois, vous pouvez définir des opérateurs de conversion implicites pour un type, qui vous permettent d’utiliser l’opérateur d’assignation avec ces types. Pour plus d’informations, consultez [Utilisation d’opérateurs de conversion](../../../csharp/programming-guide/statements-expressions-operators/using-conversion-operators.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#49](../../../csharp/language-reference/operators/codesnippet/CSharp/assignment-operator_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)
