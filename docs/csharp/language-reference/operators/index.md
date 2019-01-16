---
title: Opérateurs C#
ms.date: 04/04/2018
f1_keywords:
- cs.operators
helpviewer_keywords:
- boolean operators [C#]
- expressions [C#], operators
- logical operators [C#]
- operators [C#]
- Visual C#, operators
- indirection operators [C#]
- assignment operators [C#]
- shift operators [C#]
- relational operators [C#]
- bitwise operators [C#]
- address operators [C#]
- keywords [C#], operators
- arithmetic operators [C#]
ms.assetid: 0301e31f-22ad-49af-ac3c-d5eae7f0ac43
ms.openlocfilehash: 6380fa4ec99f598be0d01db1061900520e94d5f1
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333406"
---
# <a name="c-operators"></a>Opérateurs C#

C# fournit de nombreux opérateurs, qui sont des symboles spécifiant quelles opérations (mathématiques, indexation, appel de fonction, etc.) effectuer dans une expression. Vous pouvez [surcharger](../../programming-guide/statements-expressions-operators/overloadable-operators.md) de nombreux opérateurs pour modifier leur signification quand ils sont appliqués à un type défini par l’utilisateur.

Les opérations sur les types intégraux (comme `==`, `!=`, `<`, `>`, `&` ou `|`) sont en général autorisées sur les types énumération (`enum`).

Les sections ci-dessous listent les opérateurs C# de la priorité la plus élevée à la plus basse. Les opérateurs inclus dans chaque section partagent le même niveau de priorité.

## <a name="primary-operators"></a>Opérateurs principaux

Ce sont les opérateurs dont la priorité est la plus élevée.

[x.y](member-access-operator.md) : accès au membre.

[x?.y](null-conditional-operators.md) : accès au membre conditionnel Null. Retourne `null` si l’opérande de gauche prend la valeur `null`.

[x?[y]](null-conditional-operators.md) : accès à l’index conditionnel Null. Retourne `null` si l’opérande de gauche prend la valeur `null`.

[f(x)](invocation-operator.md) : appel de fonction.

[a&#91;x&#93;](index-operator.md) : indexation de l’objet d’agrégation.

[x++](increment-operator.md) : incrément suffixé. Retourne la valeur de x et met à jour l'emplacement de stockage avec la valeur de x augmentée de un (ajoute généralement l'entier 1).

[x--](decrement-operator.md) : décrément suffixé. Retourne la valeur de x et met à jour l'emplacement de stockage avec la valeur de x diminuée de un (soustrait généralement l'entier 1).

[new](../keywords/new-operator.md) : instanciation de type.

[typeof](../keywords/typeof.md) : retourne l’objet <xref:System.Type> qui représente l’opérande.

[checked](../keywords/checked.md) : active le contrôle de dépassement de capacité pour les opérations sur les entiers.

[unchecked](../keywords/unchecked.md) : désactive le contrôle de dépassement de capacité pour les opérations sur les entiers. Il s'agit du comportement de compilateur par défaut.

[default(T)](../../programming-guide/statements-expressions-operators/default-value-expressions.md) – produit la valeur par défaut du type T.

[delegate](../../programming-guide/statements-expressions-operators/anonymous-methods.md) : déclare et retourne une instance de délégué.

[sizeof](../keywords/sizeof.md) : retourne la taille en octets de l’opérande du type.

[->](dereference-operator.md) : déréférencement de pointeur associé à l’accès au membre.

## <a name="unary-operators"></a>Les opérateurs unaires.

Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[+x](addition-operator.md) : retourne la valeur de x.

[-x](subtraction-operator.md) : négation numérique.

[\!x](logical-negation-operator.md) : négation logique.

[~x](bitwise-complement-operator.md) : complément au niveau du bit.

[++x](increment-operator.md) : incrément préfixé. Retourne la valeur de x après avoir mis à jour l'emplacement de stockage avec la valeur de x augmentée de un (ajoute généralement l'entier 1).

[--x](decrement-operator.md) : décrément préfixé. Retourne la valeur de x après avoir mis à jour l’emplacement de stockage avec la valeur de x diminuée d’une unité (soustrait généralement l’entier 1).

[(T)x](invocation-operator.md) : cast de type.

[await](../keywords/await.md) : attend un `Task`.

[&x](and-operator.md) : adresse de.

[*x](multiplication-operator.md) : déréférencement.

## <a name="multiplicative-operators"></a>Opérateurs multiplicatifs

Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x * y](multiplication-operator.md) : multiplication.

[x / y](division-operator.md) : division. Si les opérandes sont des entiers, le résultat est un entier tronqué vers zéro (par exemple, `-7 / 2 is -3`).

[x % y](remainder-operator.md) : reste. Si les opérandes sont des entiers, cet opérateur renvoie le reste de la division de x par y.  Si `q = x / y` et `r = x % y`, alors `x = q * y + r`.

## <a name="additive-operators"></a>Opérateurs additifs

Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x + y](addition-operator.md) : addition.

[x – y](subtraction-operator.md) : soustraction.

## <a name="shift-operators"></a>Opérateurs de décalage

Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x <\<  y](left-shift-operator.md) : décalage des bits vers la gauche et remplissage avec zéro à droite.

[x >> y](right-shift-operator.md) : décalage des bits vers la droite. Si l'opérande de gauche est `int` ou `long`, alors les bits de gauche sont remplis avec le bit de signe. Si l'opérande de gauche est `uint` ou `ulong`, alors les bits de gauche sont remplis avec zéro.

## <a name="relational-and-type-testing-operators"></a>Opérateurs relationnels et de test de type

Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x \< y](less-than-operator.md) : inférieur à (true si x est inférieur à y).

[x > y](greater-than-operator.md) : supérieur à (true si x est supérieur à y).

[x \<= y](less-than-equal-operator.md) : supérieur ou égal à.

[x >= y](greater-than-equal-operator.md) : supérieur ou égal à.

[is](../keywords/is.md) : compatibilité du type. Retourne true si l’opérande de gauche évalué peut être converti en type spécifié dans l’opérande de droite (type statique).

[as](../keywords/as.md) : conversion de type. Retourne l'opérande de gauche converti en type spécifié par l'opérande de droite (type statique), mais `as` retourne `null` où `(T)x` lèverait une exception.

## <a name="equality-operators"></a>Opérateurs d'égalité

Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x == y](equality-comparison-operator.md) : égalité. Par défaut, pour les types de référence autres que `string`, cet opérateur retourne l'égalité de référence (test d'identité). Toutefois, des types peuvent surcharger `==`, donc si votre objectif est de tester l'identité, il est préférable d'utiliser la méthode `ReferenceEquals` sur `object`.

[x != y](not-equal-operator.md) : différent. Consultez le commentaire sur `==`. Si un type surcharge `==`, alors il doit surcharger `!=`.

## <a name="logical-and-operator"></a>Opérateur AND logique

Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x & y](and-operator.md) : ET logique ou au niveau du bit. Vous pouvez l'utiliser généralement avec des types entiers et des types `enum`.

## <a name="logical-xor-operator"></a>Opérateur XOR logique

Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x ^ y](xor-operator.md) : XOR logique ou au niveau du bit. Vous pouvez l'utiliser généralement avec des types entiers et des types `enum`.

## <a name="logical-or-operator"></a>Opérateur OU logique

Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x &#124; y](or-operator.md) : OU logique ou au niveau du bit. Vous pouvez l'utiliser généralement avec des types entiers et des types `enum`.

## <a name="conditional-and-operator"></a>Opérateur AND conditionnel

Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x && y](conditional-and-operator.md) : ET logique. Si le premier opérande prend la valeur false, C# n’évalue pas le second opérande.

## <a name="conditional-or-operator"></a>Opérateur OR conditionnel

Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x &#124;&#124; y](conditional-or-operator.md) : OU logique. Si le premier opérande prend la valeur true, C# n’évalue pas le second opérande.

## <a name="null-coalescing-operator"></a>Opérateur de fusion de Null

Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x ?? y](null-coalescing-operator.md) : retourne `x` si non `null` ; dans le cas contraire, retourne `y`.

## <a name="conditional-operator"></a>Opérateur conditionnel

Cet opérateur a une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[t ? x : y](conditional-operator.md) : si le test `t` prend la valeur true, alors évalue et retourne `x` ; sinon, évalue et retourne `y`.

## <a name="assignment-and-lambda-operators"></a>Opérateurs d'assignation et lambda

Ces opérateurs ont une priorité supérieure à celle de la section suivante et une priorité inférieure à celle de la section précédente.

[x = y](assignment-operator.md) : affectation.

[x += y](addition-assignment-operator.md) : incrément. Additionne la valeur de `y` à la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur. Si `x` désigne un `event`, alors `y` doit être une fonction appropriée que C# ajoute en tant que gestionnaire d'événements.

[x -= y](subtraction-assignment-operator.md) : décrément. Soustrait la valeur de `y` de la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur. Si `x` désigne un `event`, alors `y` doit être une fonction appropriée que C# supprime en tant que gestionnaire d'événements.

[x *= y](multiplication-assignment-operator.md) : affectation de multiplication. Multiplie la valeur de `y` par la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.

[x /= y](division-assignment-operator.md) : affectation de division. Divise la valeur de `x` par la valeur de `y`, stocke le résultat dans `x` et retourne la nouvelle valeur.

[x %= y](remainder-assignment-operator.md) : assignation de reste. Divise la valeur de `x` par la valeur de `y`, stocke le reste dans `x` et retourne la nouvelle valeur.

[x &= y](and-assignment-operator.md) : affectation ET. Assigne l'opérateur AND à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.

[x &#124;= y](or-assignment-operator.md) : affectation OU. Assigne l'opérateur OR à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.

[x ^= y](xor-assignment-operator.md) : affectation XOR. Assigne l'opérateur XOR à la valeur de `y` et la valeur de `x`, stocke le résultat dans `x` et retourne la nouvelle valeur.

[x <<= y](left-shift-assignment-operator.md) : affectation de décalage vers la gauche. Décale la valeur de `x` vers la gauche de `y` places, stocke le résultat dans `x` et retourne la nouvelle valeur.

[x >>= y](right-shift-assignment-operator.md) : affectation de décalage vers la droite. Décale la valeur de `x` vers la droite de `y` places, stocke le résultat dans `x` et retourne la nouvelle valeur.

[=>](lambda-operator.md) : déclaration lambda.

## <a name="arithmetic-overflow"></a>Dépassement arithmétique

Les opérateurs arithmétiques ([+](addition-operator.md), [-](subtraction-operator.md), [*](multiplication-operator.md) et [/](division-operator.md)) peuvent produire des résultats qui sont en dehors de la plage de valeurs possibles pour le type numérique concerné. Reportez-vous à la section d'un opérateur particulier pour obtenir plus d'informations, mais en règle générale, les points suivants s'appliquent :

- Le dépassement arithmétique d'un entier lève soit une exception <xref:System.OverflowException> ou ignore les bits les plus significatifs du résultat. La division d'un entier par zéro lève toujours une exception <xref:System.DivideByZeroException>.

   En cas de dépassement d’un entier, ce qui se produit dépend du contexte d’exécution, lequel peut être [checked ou unchecked](../keywords/checked-and-unchecked.md). Dans un contexte checked, une exception <xref:System.OverflowException> est levée. Dans un contexte unchecked, les bits les plus significatifs du résultat sont ignorés et l'exécution se poursuit. Ainsi, C# vous donne la possibilité de traiter ou d'ignorer le dépassement. Par défaut, les opérations arithmétiques se produisent dans un contexte *unchecked*.

   En plus des opérations arithmétiques, des casts entre types intégraux peuvent générer un dépassement (par exemple en cas de conversion de type de [long](../keywords/long.md) en [int](../keywords/int.md)). Ils sont sujets à une exécution checked ou unchecked. En revanche, les opérateurs de bits et les opérateurs de décalage ne génèrent jamais de dépassement.

- Le dépassement arithmétique ou la division par zéro d'une virgule flottante ne lèvent jamais d'exception, car les types à virgule flottante se basent sur IEEE 754 et peuvent représenter l'infini et NaN (n'est pas un nombre).

- Le dépassement arithmétique d’un nombre [décimal](../keywords/decimal.md) lève toujours une exception <xref:System.OverflowException>. La division d'un nombre décimal par zéro lève toujours une exception <xref:System.DivideByZeroException>.

## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [C#](../../index.md)
- [Opérateurs surchargeables](../../programming-guide/statements-expressions-operators/overloadable-operators.md)
- [Mots clés C#](../keywords/index.md)