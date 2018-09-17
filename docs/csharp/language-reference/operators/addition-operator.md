---
title: + , opérateur (Informations de référence sur C#)
ms.date: 07/20/2015
f1_keywords:
- +_CSharpKeyword
helpviewer_keywords:
- + operator [C#]
- concatenation operator [C#]
- addition operator [C#]
ms.assetid: 93e56486-bb42-43c1-bd43-60af11e64e67
ms.openlocfilehash: b49694bc8937c58bd295f0f8e57c378802d0dfb9
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45594596"
---
# <a name="-operator-c-reference"></a>+, opérateur (référence C#)
L’opérateur `+` peut être utilisé comme opérateur unaire ou opérateur binaire.  
  
## <a name="remarks"></a>Notes  
 Les opérateurs `+` sont prédéfinis pour tous les types numériques. Le résultat d’une opération `+` unaire sur un type numérique correspond simplement à la valeur de l’opérande.  
  
 Les opérateurs `+` binaires sont prédéfinis pour les types numériques et chaîne. Pour les types numériques, + calcule la somme des deux opérandes. Quand les deux opérandes ou l’un d’entre eux sont de type chaîne, + concatène les représentations sous forme de chaîne des opérandes.  
  
 Les types délégués fournissent aussi un opérateur `+` binaire, qui effectue la concaténation de délégués.  
  
 Les types définis par l’utilisateur peuvent surcharger les opérateurs `+` unaires et `+` binaires. Les opérations sur les types intégraux sont en général autorisées sur l’énumération. Pour plus d’informations, consultez [operator (référence C#)](../../../csharp/language-reference/keywords/operator.md).  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#28](../../../csharp/language-reference/operators/codesnippet/CSharp/addition-operator_1.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)  
- [operator (référence C#)](../../../csharp/language-reference/keywords/operator.md)
