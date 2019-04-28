---
title: Types valeur Nullable - Visual Basic
ms.date: 07/20/2015
f1_keywords:
- vb.Nullable
helpviewer_keywords:
- nullable types [Visual Basic]
- '? [Visual Basic]'
- types [Visual Basic], nullable
- nullable types [Visual Basic]
- data types [Visual Basic], nullable
ms.assetid: 9ac3b602-6f96-4e6d-96f7-cd4e81c468a6
ms.openlocfilehash: d17d2ad3fd99c6d563c21ddd646396ccb1c1ca48
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62008226"
---
# <a name="nullable-value-types-visual-basic"></a>Types valeur Nullable (Visual Basic)

Parfois, vous travaillez avec un type valeur qui n’a pas une valeur définie dans certaines circonstances. Par exemple, un champ dans une base de données peut devoir faire la distinction entre une valeur assignée est significative et n’ayant ne pas une valeur assignée. Types de valeur peuvent être étendues pour prendre leurs valeurs normales ou une valeur null. Cette extension est appelée un *type nullable*.

Chaque type nullable est construit à partir de générique <xref:System.Nullable%601> structure. Considérons une base de données qui assure le suivi des activités liées à leur travail. L’exemple suivant construit un nullable `Boolean` tapez et déclare une variable de ce type. Vous pouvez écrire la déclaration de trois façons :

[!code-vb[VbVbalrNullableValue#1](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#1)]

La variable `ridesBusToWork` peut contenir une valeur de `True`, une valeur de `False`, ou aucune valeur. Sa valeur initiale par défaut n’est aucune valeur, qui dans ce cas signifie que les informations n’ont pas encore été obtenues pour cette personne. En revanche, `False` peut signifier que les informations ont été obtenues et que la personne ne puisse pas surfer sur le bus fonctionne.

Vous pouvez déclarer des variables et des propriétés avec des types nullables, et vous pouvez déclarer un tableau avec des éléments d’un type nullable. Vous pouvez déclarer des procédures avec des types nullable en tant que paramètres, et vous pouvez retourner un type nullable à partir d’un `Function` procédure.

Vous ne pouvez pas construire un type nullable sur un type référence tel qu’un tableau, un `String`, ou une classe. Le type sous-jacent doit être un type valeur. Pour plus d'informations, consultez [Value Types and Reference Types](value-types-and-reference-types.md).

## <a name="using-a-nullable-type-variable"></a>À l’aide d’une Variable de Type Nullable

Les membres les plus importants d’un type nullable sont ses <xref:System.Nullable%601.HasValue%2A> et <xref:System.Nullable%601.Value%2A> propriétés. Pour une variable de type nullable, <xref:System.Nullable%601.HasValue%2A> vous indique si la variable contient une valeur définie. Si <xref:System.Nullable%601.HasValue%2A> est `True`, vous pouvez lire la valeur à partir de <xref:System.Nullable%601.Value%2A>. Notez que les deux <xref:System.Nullable%601.HasValue%2A> et <xref:System.Nullable%601.Value%2A> sont `ReadOnly` propriétés.

### <a name="default-values"></a>Valeurs par défaut

Lorsque vous déclarez une variable avec un type nullable, sa <xref:System.Nullable%601.HasValue%2A> propriété a la valeur par défaut `False`. Cela signifie que, par défaut, la variable n’a aucune valeur définie, au lieu de la valeur par défaut de son type valeur sous-jacent. Dans l’exemple suivant, la variable `numberOfChildren` a d’initialement aucune valeur définie, même si la valeur par défaut de la `Integer` type a la valeur 0.

[!code-vb[VbVbalrNullableValue#2](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#2)]

Une valeur null est utile pour indiquer une valeur inconnue ou non définie. Si `numberOfChildren` avait été déclaré comme `Integer`, il n’y aurait aucun valeur qui peut indiquer que les informations ne sont pas disponibles actuellement.

### <a name="storing-values"></a>Stockage de valeurs

Vous stocker une valeur dans une variable ou une propriété d’un type nullable de la façon habituelle. L’exemple suivant assigne une valeur à la variable `numberOfChildren` déclaré dans l’exemple précédent.

[!code-vb[VbVbalrNullableValue#3](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#3)]

Si une variable ou une propriété d’un type nullable contient une valeur définie, vous pouvez le rendre revenir à son état initial de ne pas avoir une valeur assignée. Pour cela en définissant la variable ou la propriété `Nothing`, comme illustré dans l’exemple suivant.

[!code-vb[VbVbalrNullableValue#4](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#4)]

> [!NOTE]
> Bien que vous puissiez attribuer `Nothing` à une variable d’un type nullable, vous ne pouvez pas tester pour `Nothing` à l’aide du signe égal. Comparaison qui utilise le signe égal, `someVar = Nothing`, a toujours la valeur `Nothing`. Vous pouvez tester la variable <xref:System.Nullable%601.HasValue%2A> propriété pour `False`, ou de test à l’aide de la `Is` ou `IsNot` opérateur.

### <a name="retrieving-values"></a>Récupération de valeurs

Pour récupérer la valeur d’une variable d’un type nullable, vous devez tout d’abord tester son <xref:System.Nullable%601.HasValue%2A> propriété pour confirmer qu’il a une valeur. Si vous essayez de lire la valeur lorsque <xref:System.Nullable%601.HasValue%2A> est `False`, Visual Basic lève une <xref:System.InvalidOperationException> exception. L’exemple suivant montre la méthode recommandée pour lire la variable `numberOfChildren` des exemples précédents.

[!code-vb[VbVbalrNullableValue#5](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#5)]

## <a name="comparing-nullable-types"></a>Comparaison de Types Nullable

Lorsque nullable `Boolean` variables sont utilisées dans les expressions booléennes, le résultat peut être `True`, `False`, ou `Nothing`. Voici la table de vérité pour `And` et `Or`. Étant donné que `b1` et `b2` ont maintenant des trois valeurs possibles, il existe neuf combinaisons à évaluer.

|b1|b2|B1 et b2|B1 ou b2|
|--------|--------|---------------|--------------|
|`Nothing`|`Nothing`|`Nothing`|`Nothing`|
|`Nothing`|`True`|`Nothing`|`True`|
|`Nothing`|`False`|`False`|`Nothing`|
|`True`|`Nothing`|`Nothing`|`True`|
|`True`|`True`|`True`|`True`|
|`True`|`False`|`False`|`True`|
|`False`|`Nothing`|`False`|`Nothing`|
|`False`|`True`|`False`|`True`|
|`False`|`False`|`False`|`False`|

Lorsque la valeur d’une variable ou expression booléenne est `Nothing`, il n’est ni `true` ni `false`. Prenons l'exemple suivant.

[!code-vb[VbVbalrNullableValue#6](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#6)]

Dans cet exemple, `b1 And b2` prend la valeur `Nothing`. Par conséquent, le `Else` clause est exécutée dans chaque `If` instruction et la sortie est comme suit :

`Expression is not true`

`Expression is not false`

> [!NOTE]
> `AndAlso` et `OrElse`, qui utilisent l’évaluation de court-circuit doivent évaluer leurs opérandes deuxième lorsque le premier prend la valeur `Nothing`.

## <a name="propagation"></a>Propagation

Si une ou les deux opérandes d’une arithmétique, comparaison, MAJ ou une opération de type est nullable, le résultat de l’opération est également nullable. Si les deux opérandes ont des valeurs qui ne sont pas `Nothing`, l’opération est effectuée sur les valeurs sous-jacentes des opérandes, comme si aucune n’était un type nullable. Dans l’exemple suivant, les variables `compare1` et `sum1` sont implicitement typées. Si vous placez le pointeur de la souris au-dessus d’eux, vous verrez que le compilateur déduit les types nullable pour les deux.

[!code-vb[VbVbalrNullableValue#7](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#7)]

Si un ou deux opérandes ont la valeur `Nothing`, le résultat sera `Nothing`.

[!code-vb[VbVbalrNullableValue#8](../../../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrNullableValue/VB/Class1.vb#8)]

## <a name="using-nullable-types-with-data"></a>Utilisation de Types Nullable avec des données

Une base de données est un des emplacements plus importants pour utiliser des types nullables. Pas tous les objets de base de données prend actuellement en charge les types nullable, mais que faire les adaptateurs de table généré par le concepteur. Consultez [prise en charge du TableAdapter pour les types nullables](/visualstudio/data-tools/fill-datasets-by-using-tableadapters#tableadapter-support-for-nullable-types).

## <a name="see-also"></a>Voir aussi

- <xref:System.InvalidOperationException>
- <xref:System.Nullable%601.HasValue%2A>
- [Utilisation de types Nullable](../../../../csharp/programming-guide/nullable-types/using-nullable-types.md)
- [Types de données](index.md)
- [Value Types and Reference Types](value-types-and-reference-types.md)
- [Dépannage des types de données](troubleshooting-data-types.md)
- [Remplir des datasets à l’aide de TableAdapters](/visualstudio/data-tools/fill-datasets-by-using-tableadapters)
- [If (opérateur)](../../../language-reference/operators/if-operator.md)
- [Inférence de type local](../variables/local-type-inference.md)
- [Is (opérateur)](../../../language-reference/operators/is-operator.md)
- [IsNot (opérateur)](../../../language-reference/operators/isnot-operator.md)