---
title: Types pointeur (Guide de programmation C#)
ms.date: 04/20/2018
helpviewer_keywords:
- unsafe code [C#], pointers
- pointers [C#]
ms.openlocfilehash: cbc75a2ec6fe826cb192b1e8bef61c7295f13916
ms.sourcegitcommit: 412bbc2e43c3b6ca25b358cdf394be97336f0c24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/25/2018
ms.locfileid: "42924506"
---
# <a name="pointer-types-c-programming-guide"></a>Types pointeur (Guide de programmation C#)

Dans un contexte unsafe, un type peut être un type pointeur, un type valeur ou un type référence. La déclaration d'un type pointeur peut prendre l'une des formes suivantes :

``` csharp
type* identifier;
void* identifier; //allowed but not recommended
```

Le type spécifié avant le caractère `*` dans un type de pointeur est appelé le **type référent**. Chacun des types suivants peut être un type référent :

- Tout type intégral : [sbyte](../../language-reference/keywords/sbyte.md), [byte](../../language-reference/keywords/byte.md), [short](../../language-reference/keywords/short.md), [ushort](../../language-reference/keywords/ushort.md), [int](../../language-reference/keywords/int.md), [uint](../../language-reference/keywords/uint.md), [long](../../language-reference/keywords/long.md), [ulong](../../language-reference/keywords/ulong.md).
- Tout type à virgule flottante : [float](../../language-reference/keywords/float.md), [double](../../language-reference/keywords/double.md).
- [char](../../language-reference/keywords/char.md).
- [bool](../../language-reference/keywords/bool.md).
- [decimal](../../language-reference/keywords/decimal.md).
- Tout type [enum](../../language-reference/keywords/enum.md).
- Tout type pointeur. Des expressions comme `void**` sont ainsi autorisées.
- Tout type struct défini par l'utilisateur qui contient des champs de types unmanaged uniquement.

Les types pointeur n’héritent pas de [object](../../language-reference/keywords/object.md), et aucune conversion n’est possible entre les types pointeur et `object`. Par ailleurs, le boxing et l'unboxing ne prennent pas en charge les pointeurs. Cependant, vous pouvez effectuer des conversions entre différents types pointeur ainsi qu'entre des types pointeur et des types intégraux.

Lorsque vous déclarez plusieurs pointeurs dans la même déclaration, l'astérisque (*) est écrit conjointement au type sous-jacent uniquement, il n'est pas utilisé en tant que préfixe de chaque nom de pointeur. Exemple :

```csharp
int* p1, p2, p3;   // Ok
int *p1, *p2, *p3;   // Invalid in C#
```

Un pointeur ne peut pas pointer vers une référence ou vers un [struct](../../language-reference/keywords/struct.md) qui contient des références, car une référence d’objet peut être collectée par le récupérateur de mémoire, même si un pointeur pointe vers elle. Le récupérateur de mémoire ne se préoccupe pas de savoir si un objet est pointé par des types pointeur.

La valeur de la variable pointeur de type `myType*` est l'adresse d'une variable de type `myType`. Les éléments suivants sont des exemples de déclarations de type pointeur :

|Exemple|Description|
|-------------|-----------------|
|`int* p`|`p` est un pointeur vers un entier.|
|`int** p`|`p` est un pointeur vers un pointeur vers un entier.|
|`int*[] p`|`p` est un tableau unidimensionnel de pointeurs vers des entiers.|
|`char* p`|`p` est un pointeur vers un caractère.|
|`void* p`|`p` est un pointeur vers un type inconnu.|

L'opérateur d'indirection de pointeur * peut être utilisé pour accéder au contenu à l'emplacement vers lequel pointe la variable pointeur. Observez par exemple la déclaration suivante :

```csharp
int* myVariable;
```

L'expression `*myVariable` désigne la variable `int` trouvée à l'adresse contenue dans `myVariable`.

Plusieurs exemples de pointeurs sont présentés dans les rubriques [fixed, instruction](../../language-reference/keywords/fixed-statement.md) et [Conversions de pointeur](../../programming-guide/unsafe-code-pointers/pointer-conversions.md). L’exemple suivant utilise le mot clé `unsafe` et les instructions `fixed`, et montre comment incrémenter un pointeur intérieur.  Vous pouvez coller ce code dans la fonction Main d'une application console pour l'exécuter. Ces exemples doivent être compilés avec l’ensemble d’options de compilateur [-unsafe](../../language-reference/compiler-options/unsafe-compiler-option.md).

[!code-csharp[Using pointer types](../../../../samples/snippets/csharp/keywords/FixedKeywordExamples.cs#5)]

L'opérateur d'indirection ne peut pas être appliqué à un pointeur de type `void*`. Toutefois, vous pouvez utiliser un cast pour convertir un pointeur void en n'importe quel autre type pointeur, et inversement.

Un pointeur peut être `null`. Le fait d'appliquer un opérateur d'indirection à un pointeur Null donne lieu à un comportement défini par l'implémentation.

Le passage de pointeurs entre méthodes peut engendrer un comportement non défini. Supposons une méthode qui retourne un pointeur à une variable locale par le biais d’un paramètre `in`, `out` ou `ref`, ou comme résultat de fonction. Si le pointeur a été défini dans un bloc fixed, la variable vers laquelle il pointe peut ne plus être fixed.

Le tableau suivant répertorie les opérateurs et les instructions qui peuvent fonctionner sur des pointeurs dans un contexte unsafe :

|Opérateur/Instruction|Utilisez|
|-------------------------|---------|
|*|Exécute l'indirection de pointeur.|
|->|Accède à un membre d'un struct via un pointeur.|
|[]|Indexe un pointeur.|
|`&`|Obtient l'adresse d'une variable.|
|++ et --|Incrémente et décrémente les pointeurs.|
|+ et -|Exécute des opérations arithmétiques sur les pointeurs.|
|==, !=, \<, >, \<= et >=|Compare des pointeurs.|
|`stackalloc`|Alloue de la mémoire sur la pile.|
|Instruction `fixed`|Résout temporairement une variable afin de pouvoir rechercher son adresse.|

## <a name="c-language-specification"></a>Spécification du langage C#

 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a>Voir aussi
 [Guide de programmation C#](../index.md)  
 [Pointeurs et code unsafe](index.md)  
 [Conversions de pointeurs](pointer-conversions.md)  
 [Expressions de pointeur](pointer-expressions.md)  
 [Types](../../language-reference/keywords/types.md)  
 [unsafe](../../language-reference/keywords/unsafe.md)  
 [fixed, instruction](../../language-reference/keywords/fixed-statement.md)  
 [stackalloc](../../language-reference/keywords/stackalloc.md)  
 [Conversion boxing et unboxing](../types/boxing-and-unboxing.md)
