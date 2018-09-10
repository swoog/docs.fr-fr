---
title: "Comment : effectuer sans risque un cast à l'aide des opérateurs as et is (Guide de programmation C#)"
ms.date: 07/20/2015
helpviewer_keywords:
- cast operators [C#], as and is operators
- as operator [C#]
- is operator [C#]
ms.assetid: c1176cea-1426-4a44-8570-3eadafa58863
ms.openlocfilehash: 8e0b17122bd23a7de82ca1c210a559fe09ad7fee
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43508116"
---
# <a name="how-to-safely-cast-by-using-as-and-is-operators-c-programming-guide"></a>Comment : effectuer sans risque un cast à l'aide des opérateurs as et is (Guide de programmation C#)
Les objets étant polymorphes, une variable d’un type de classe de base peut contenir un type dérivé. Pour accéder aux méthodes d’instance du type dérivé, il est nécessaire de recaster la valeur dans le type dérivé. Or, dans ce cas, toute tentative de conversion simple risque de lever une exception <xref:System.InvalidCastException>. C’est pourquoi C# propose les opérateurs [is](../../../csharp/language-reference/keywords/is.md) et [as](../../../csharp/language-reference/keywords/as.md). Vous pouvez utiliser ces opérateurs pour vérifier si une conversion de type (cast) aboutit sans lever d’exception. En règle générale, l’opérateur `as` est plus efficace, car de fait, il ne retourne la valeur de conversion que si cette opération peut aboutir. L’opérateur `is` retourne uniquement une valeur booléenne. Vous pouvez donc vous en servir pour déterminer simplement le type d’un objet sans avoir réellement besoin de le convertir.  
  
## <a name="example"></a>Exemple  
 Les exemples suivants montrent comment utiliser les opérateurs `is` et `as` pour effectuer une conversion d’un type de référence vers un autre sans risquer de lever une exception. L’exemple montre aussi comment utiliser l’opérateur `as` avec les types valeur Nullable.  
  
 [!code-csharp[csProgGuideTypes#40](../../../csharp/programming-guide/nullable-types/codesnippet/CSharp/how-to-safely-cast-by-using-as-and-is-operators_1.cs)]  
  
## <a name="see-also"></a>Voir aussi

- [Types](../../../csharp/programming-guide/types/index.md)  
- [Cast et conversions de types](../../../csharp/programming-guide/types/casting-and-type-conversions.md)  
- [Types Nullable](../../../csharp/programming-guide/nullable-types/index.md)
