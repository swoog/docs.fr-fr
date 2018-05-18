---
title: Critères spéciaux - Guide C#
description: En savoir plus sur les expressions de critères spéciaux en langage C#
ms.date: 01/24/2017
ms.assetid: 1e575c32-2e2b-4425-9dca-7d118f3ed15b
ms.openlocfilehash: 0f95ac8b16939173e6cfd7304b9cbe52526b5169
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
---
# <a name="pattern-matching"></a>Critères spéciaux #

Les modèles vérifient qu’une valeur a une certaine *forme* et peuvent *extraire* des informations de la valeur quand celle-ci a la forme correspondante. Les critères spéciaux offrent une syntaxe plus concise pour les algorithmes que vous utilisez déjà aujourd’hui. Vous pouvez déjà créer des algorithmes de critères spéciaux à l’aide de la syntaxe existante. Pour cela, vous écrivez des instructions `if` ou `switch` qui testent une valeur. Ensuite, quand ces instructions correspondent, vous extrayez et utilisez les informations de cette valeur. Les nouveaux éléments de syntaxe étendent les instructions que vous connaissez déjà : `is` et `switch`. Ces nouvelles extensions permettent à la fois de tester une valeur et d’extraire les informations de cette valeur.

Dans cette rubrique, nous allons examiner la nouvelle syntaxe et montrer de quelle manière l’utiliser pour rendre votre code plus lisible et concis. Les critères spéciaux permettent l’utilisation d’idiomes où le code et les données sont séparés, contrairement aux conceptions orientées objet où les données et les méthodes qui les manipulent sont étroitement couplées.

Pour illustrer ces nouveaux idiomes, nous allons manipuler des structures représentant des formes géométriques à l’aide d’instructions de critères spéciaux. Vous savez probablement déjà concevoir des hiérarchies de classes et créer des [méthodes virtuelles et méthodes substituées](methods.md#inherited) pour personnaliser le comportement d’un objet en fonction du type de runtime de l’objet.

Ces techniques ne sont pas possibles avec des données qui ne sont pas structurées dans une hiérarchie de classes. Quand les données et les méthodes sont séparées, vous avez besoin d’autres outils. Les nouvelles constructions de *critères spéciaux* utilisent une syntaxe simplifiée pour examiner les données et manipuler le flux de contrôle en fonction de la condition de ces données. Vous écrivez déjà des instructions `if` et `switch` qui testent la valeur d’une variable. Vous écrivez déjà des instructions `is` qui testent le type d’une variable. Les *critères spéciaux* ajoutent de nouvelles fonctionnalités à ces instructions.

Dans cette rubrique, vous allez créer une méthode qui calcule la surface de différentes formes géométriques. Pour cela, vous n’allez pas utiliser les techniques orientées objet, ni créer une hiérarchie de classes pour les différentes formes, comme vous le faites habituellement.
Vous allez utiliser des *critères spéciaux* à la place. Pour bien illustrer le fait qu’il n’y a pas d’héritage, vous allez définir chaque forme comme un `struct` au lieu d’une classe. Notez que des types de `struct` différents ne peuvent pas spécifier un type de base commun défini par l’utilisateur, ce qui explique pourquoi l’héritage n’est pas une conception possible.
Tout au long de cet exemple, comparez ce code avec le même code structuré comme une hiérarchie d’objets. Quand les données à interroger et à manipuler ne sont pas une hiérarchie de classes, les critères spéciaux permettent des conceptions très élégantes.

Au lieu de commencer avec une définition de forme abstraite et d’ajouter ensuite différentes classes de formes spécifiques, écrivez d’abord les définitions de données simples pour chacune des formes géométriques :

[!code-csharp[ShapeDefinitions](../../samples/csharp/PatternMatching/Shapes.cs#01_ShapeDefinitions "Shape definitions")]

À partir de ces structures, écrivez une méthode qui calcule la surface d’une forme.

## <a name="the-is-type-pattern-expression"></a>Expression du modèle de type `is`

Avant C# 7.0, vous deviez tester chaque type dans une série d’instructions `if` et `is` :

[!code-csharp[ClassicIsExpression](../../samples/csharp/PatternMatching/GeometricUtilities.cs#02_ClassicIsExpression "Classic type pattern using is")]

Le code ci-dessus est une expression standard du *modèle de type* : vous testez une variable pour déterminer son type et vous effectuez une action différente en fonction de ce type.

Vous pouvez simplifier ce code en ajoutant des extensions à l’expression `is` pour assigner une variable si le test réussit :

[!code-csharp[IsPatternExpression](../../samples/csharp/PatternMatching/GeometricUtilities.cs#03_IsPatternExpression "is pattern expression")]

Dans cette version mise à jour, l’expression `is` teste la variable et l’assigne à une nouvelle variable du type approprié. Remarquez également que cette version inclut le type `Rectangle`, qui est un `struct`. La nouvelle expression `is` peut être utilisée avec des types valeur et des types référence.

Les règles de langage des expressions de critères spéciaux vous aident à éviter une utilisation incorrecte des résultats d’une expression de correspondance. Dans l’exemple ci-dessus, les variables `s`, `c` et `r` sont uniquement dans la portée et assignées de manière définitive quand les expressions de critères spéciaux respectives retournent le résultat `true`. Si vous essayez d’utiliser l’une de ces variables à un autre emplacement, votre code génère des erreurs de compilateur.

Examinons ces deux règles en détail, en commençant par la portée. La variable `c` est dans la portée uniquement dans la branche `else` de la première instruction `if`. La variable `s` est dans la portée dans la méthode `ComputeAreaModernIs`. Cela est dû au fait que chaque branche d’une instruction `if` établit une portée distincte pour les variables, ce que ne fait pas l’instruction `if` proprement dite. Cela signifie que les variables déclarées dans l’instruction `if` sont dans la même portée que l’instruction `if` (la méthode, dans le cas présent). Ce comportement n’est pas propre aux critères spéciaux. C’est le comportement défini pour les portées de variables et pour les instructions `if` et `else`.

Les variables `c` et `s` sont assignées quand les instructions `if` respectives ont la valeur true, selon la règle d’assignation définitive quand le résultat est true.

> [!TIP]
> Les exemples de cette rubrique utilisent la construction recommandée où une expression de critères spéciaux `is` assigne de manière définitive la variable de correspondance dans la branche `true` de l’instruction `if`.
> Vous pourriez inverser la logique en écrivant `if (!(shape is Square s))`. La variable `s` serait alors assignée de manière définitive uniquement dans la branche `false`. Cette pratique est possible dans C#, mais elle est déconseillée, car elle repose sur une logique plus compliquée à suivre.

Ces règles limitent le risque d’accéder accidentellement au résultat d’une expression de critères spéciaux dont le test n’a pas réussi.

## <a name="using-pattern-matching-switch-statements"></a>Utilisation des instructions de critères spéciaux `switch`

Au fil du temps, vous aurez peut-être besoin de prendre en charge d’autres types de formes. Si vous avez de plus en plus de conditions à tester, utiliser les expressions de critères spéciaux `is` peut devenir compliqué. En plus de nécessiter des instructions `if` pour chaque type à vérifier, les expressions `is` permettent uniquement de vérifier si l’entrée correspond à un type unique. Dans ce cas, les expressions de critères spéciaux `switch` sont plus adaptées. 

L’instruction `switch` standard était une expression de modèle, qui prenait en charge le modèle de constante.
Vous pouviez comparer une variable à n’importe quelle constante utilisée dans une instruction `case` :

[!code-csharp[ClassicSwitch](../../samples/csharp/PatternMatching/GeometricUtilities.cs#04_ClassicSwitch "Classic switch statement")]

Le seul modèle pris en charge par l’instruction `switch` était le modèle de constante. De plus, il était limité aux types numériques et au type `string`.
Ces restrictions ayant été supprimées, vous pouvez maintenant écrire une instruction `switch` en utilisant le modèle de type :

[!code-csharp[Switch Type Pattern](../../samples/csharp/PatternMatching/GeometricUtilities.cs#05_SwitchTypePattern "Compute with `switch` expression")]

L’instruction de critères spéciaux `switch` utilise une syntaxe qui est familière aux développeurs ayant utilisé l’instruction `switch` de style C standard. Chaque instruction `case` est évaluée, et le code en-dessous de la condition qui correspond à la variable d’entrée est exécuté. L’exécution du code ne continue pas d’une expression case à la suivante, car la syntaxe de l’instruction `case` nécessite que chaque `case` se termine par un `break`, `return` ou `goto`.

> [!NOTE]
> Les instructions `goto` pour accéder à une autre étiquette sont valides uniquement pour le modèle de constante, l’instruction switch standard.

Il y a de nouvelles règles importantes qui régissent l’instruction `switch`. Les restrictions sur le type de la variable dans l’expression `switch` ont été supprimées.
Vous pouvez maintenant utiliser tous les types, comme le type `object` dans cet exemple. Les expressions case ne sont plus limitées à des valeurs de constante. Avec la suppression de cette limitation, la réorganisation des sections `switch` peut changer le comportement d’un programme.

Quand les expressions étaient limitées à des valeurs de constante, une seule étiquette `case` pouvait correspondre à la valeur de l’expression `switch`. La conséquence de cette règle, associée à la règle selon laquelle une section `switch` ne devait pas passer à la section suivante, était que les sections `switch` pouvaient être réorganisées dans n’importe quel ordre sans que cela change le comportement du programme.
Maintenant, avec les expressions `switch` généralisées, l’ordre de chaque section est important. Les expressions `switch` sont évaluées dans l’ordre textuel. L’exécution passe à la première étiquette `switch` qui correspond à l’expression `switch`.  
Notez que l’expression case `default` est exécutée uniquement si aucune autre étiquette case ne correspond. L’expression case `default` est évaluée en dernier, quel que soit son ordre textuel. S’il n’existe aucune expression case `default` et aucune correspondance avec les autres instructions `case`, l’exécution continue à l’instruction qui suit l’instruction `switch`. Aucun code d’étiquettes `case` n’est exécuté.

## <a name="when-clauses-in-case-expressions"></a>Clauses `when` dans les expressions `case`

Vous pouvez créer des expressions case spéciales pour les formes de surface 0 en ajoutant une clause `when` dans l’étiquette `case`. Un carré avec une longueur de côté de 0, ou un cercle de rayon 0, a une surface égale à 0. Vous spécifiez cette condition en ajoutant une clause `when` dans l’étiquette `case` :  

[!code-csharp[ComputeDegenerateShapes](../../samples/csharp/PatternMatching/GeometricUtilities.cs#07_ComputeDegenerateShapes "Compute shapes with 0 area")]

Cette modification illustre quelques points importants relatifs à la nouvelle syntaxe. Tout d’abord, plusieurs étiquettes `case` peuvent être appliquées à une même section `switch`. Le bloc d’instructions est exécuté quand l’une de ces étiquettes est `true`. Dans ce cas, si l’expression `switch` est un cercle ou un carré de surface 0, la méthode retourne la constante 0.

Cet exemple introduit deux variables différentes dans les deux étiquettes `case` du premier bloc `switch`. Notez que les instructions de ce bloc `switch` n’utilisent ni la variable `c` (pour le cercle), ni la variable `s` (pour le carré).
Aucune de ces variables n’est assignée de manière définitive dans ce bloc `switch`.
Si l’une de ces étiquettes case correspond, cela signifie qu’une des variables a été assignée.
Toutefois, il est impossible de déterminer *laquelle* de ces variables a été assignée au moment de la compilation, car les deux étiquettes case peuvent correspondre au moment de l’exécution. Pour cette raison, la plupart du temps quand vous utilisez plusieurs étiquettes `case` dans le même bloc, vous ne devez pas introduire une nouvelle variable dans l’instruction `case`, ou vous devez utiliser uniquement la variable dans la clause `when`.

Après avoir ajouté ces formes de surface 0, ajoutez deux autres types de formes, un rectangle et un triangle :

[!code-csharp[AddRectangleAndTriangle](../../samples/csharp/PatternMatching/GeometricUtilities.cs#09_AddRectangleAndTriangle "Add rectangle and triangle")]

 Avec cet ensemble de modifications, vous avez ajouté des étiquettes `case` pour l’expression case dégénérée, ainsi que des étiquettes et des blocs pour chacune des nouvelles formes. 

Enfin, vous pouvez ajouter une expression case `null` pour garantir que l’argument n’est pas `null` :

[!code-csharp[NullCase](../../samples/csharp/PatternMatching/GeometricUtilities.cs#10_NullCase "Add null case")]

Le comportement spécial pour le modèle `null` est intéressant, car la constante `null` du modèle n’a pas de type, mais elle peut être convertie en un type référence ou un type Nullable. Plutôt que de convertir une valeur `null` en un type quelconque, le langage définit qu’une valeur `null` ne correspond à aucun modèle de type, quel que soit le type de la variable au moment de la compilation. En raison de ce comportement, le nouveau modèle de type basé sur `switch` est cohérent par rapport à l’instruction `is` : les instructions `is` retournent toujours `false` quand la valeur vérifiée est `null`. Il s’avère aussi plus simple : une fois que vous avez vérifié le type, vous n’avez pas besoin d’effectuer de contrôle de valeur null supplémentaire. Vous pouvez le constater par le fait qu’aucun contrôle de valeur null ne figure dans les blocs d’expression case des exemples ci-dessus : ces contrôles ne sont pas nécessaires dans la mesure où la correspondance du modèle de type est l’assurance d’une valeur non null.

## <a name="var-declarations-in-case-expressions"></a>Déclarations `var` dans les expressions `case`

L’introduction de `var` comme l’une des expressions de correspondance fournit de nouvelles règles pour les critères spéciaux.

La première règle est que la déclaration `var` suit les règles standard d’inférence de type, à savoir que le type est supposé être le type statique de l’expression switch. Avec cette règle, il y a toujours correspondance du type.

La deuxième règle est qu’une déclaration `var` n’a pas la vérification de valeur Null que d’autres expressions de modèle de type incluent. La variable peut donc être Null, et une vérification de valeur Null est alors nécessaire.

Ces deux règles signifient que, dans de nombreux cas, une déclaration `var` dans une expression `case` remplit les mêmes conditions qu’une expression `default`.
Étant donné qu’une expression case non définie par défaut est toujours préférée à l’expression case `default`, l’expression case `default` n’est jamais exécutée.

> [!NOTE]
> Le compilateur n’émet pas d’avertissement pour signaler qu’une expression case `default` écrite ne peut pas s’exécuter. Cela est cohérent avec le comportement actuel de l’instruction `switch` où tous les cas possibles ont été répertoriés.

La troisième règle présente les cas où l’utilisation d’une expression case `var` peut être appropriée. Imaginez que vous utilisez des critères spéciaux où l’entrée est une chaîne et que vous recherchez des valeurs de commande connues. Vous pouvez écrire un code similaire à celui-ci :

[!code-csharp[VarCaseExpression](../../samples/csharp/PatternMatching/Program.cs#VarCaseExpression "use a var case expression to filter white space")]

L’instruction case `var` correspond à une valeur `null`, une chaîne vide ou une chaîne composée uniquement d’espaces blancs. Dans le code ci-dessus, l’utilisation de l’opérateur `?.` empêche la levée accidentelle d’une exception <xref:System.NullReferenceException>. L’instruction case `default` gère toutes les autres valeurs de chaîne qui ne sont pas comprises par cet analyseur de commande.

Il s’agit d’un exemple où vous pouvez envisager d’utiliser une expression case `var` différente d’une expression `default`.

## <a name="conclusions"></a>Conclusions

Les *constructions de critères spéciaux* vous permettent de gérer facilement le flux de contrôle entre différents types et variables qui ne sont pas liés par une hiérarchie d’héritage. Vous pouvez également contrôler la logique pour utiliser n’importe quelle condition testée sur la variable. Ces constructions permettent d’utiliser les modèles et les idiomes dont vous aurez davantage besoin à mesure que vous créez d’autres applications distribuées, où les données et les méthodes qui les manipulent sont séparées. Vous remarquerez que les structures de formes utilisées dans cet exemple ne contiennent pas de méthodes, mais uniquement des propriétés en lecture seule.
Les critères spéciaux peuvent être utilisés avec tous les types de données. Vous écrivez des expressions qui examinent l’objet et vous prenez des décisions de flux de contrôle en fonction de ces conditions.

Comparez le code de cet exemple avec la conception qui résulterait de la création d’une hiérarchie de classes pour une `Shape` abstraite et des formes dérivées spécifiques, chacune avec sa propre implémentation d’une méthode virtuelle pour calculer la surface. Les expressions de critères spéciaux vous seront souvent d’une grande utilité quand vous manipulerez des données et souhaiterez gérer les questions de stockage de données de façon distincte des questions de comportement.

