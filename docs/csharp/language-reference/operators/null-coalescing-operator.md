---
title: ?? , opérateur (Informations de référence sur C#)
ms.date: 07/20/2015
f1_keywords:
- ??_CSharpKeyword
helpviewer_keywords:
- coalesce operator [C#]
- ?? operator [C#]
- conditional-AND operator (&&) [C#]
ms.assetid: 088b1f0d-c1af-4fe1-b4b8-196fd5ea9132
ms.openlocfilehash: fbcfda07cc55628aeed82eb7561516f7012bc4fe
ms.sourcegitcommit: b5cd9d5d3b75a5537fc9ad8a3f085f0bb1845ee0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "50980672"
---
# <a name="-operator-c-reference"></a>?? , opérateur (Informations de référence sur C#)
L'opérateur `??` est appelé l'l'opérateur de fusion Null.  Il retourne l’opérande de partie gauche si ce dernier n’est pas Null ; dans le cas contraire, il retourne l’opérande de partie droite.  
  
## <a name="remarks"></a>Notes  
 Un type Nullable peut représenter une valeur à partir du domaine du type, ou la valeur peut être non définie (auquel cas la valeur est Null). Utilisez la simplicité de syntaxe de l’opérateur `??` pour retourner une valeur appropriée (l’opérande de partie droite) si l’opérande de partie gauche a un type Nullable dont la valeur est Null. Si vous essayez d'assigner un type valeur Nullable à un type valeur non Nullable sans utiliser l'opérateur `??`, vous générez une erreur au moment de la compilation. Si vous utilisez un cast et si le type valeur Nullable est actuellement non défini, une exception `InvalidOperationException` est levée.  
  
 Pour plus d’informations, consultez [Types Nullable](../../../csharp/programming-guide/nullable-types/index.md).  
  
 Le résultat d’un opérateur ?? n’est pas considéré comme une constante même si ses deux arguments sont des constantes.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[csRefOperators#53](../../../csharp/language-reference/operators/codesnippet/CSharp/null-conditional-operator_1.cs)]  
  
## <a name="c-language-specification"></a>Spécification du langage C#  

Pour plus d’informations, consultez [Opérateur de fusion de Null](~/_csharplang/spec/expressions.md#the-null-coalescing-operator) dans la [spécification du langage C#](../language-specification/index.md). La spécification du langage est la source de référence pour la syntaxe C# et son utilisation.
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../../../csharp/language-reference/index.md)  
- [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
- [Opérateurs C#](../../../csharp/language-reference/operators/index.md)  
- [Types Nullable](../../../csharp/programming-guide/nullable-types/index.md)  
- [Que signifie réellement « Lifted » ?](https://blogs.msdn.microsoft.com/ericlippert/2007/06/27/what-exactly-does-lifted-mean/)
