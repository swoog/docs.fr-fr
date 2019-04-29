---
title: Instructions dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], declaring
- colons (:) [Visual Basic]
- constants [Visual Basic], defining
- underlines
- constants [Visual Basic], statements
- blue underline [Visual Basic]
- procedures [Visual Basic], statements
- variables [Visual Basic], assigning
- line breaks [Visual Basic], in code
- executable statements [Visual Basic]
- variables [Visual Basic], defining
- statements [Visual Basic], about statements
ms.assetid: fcfdee1a-82b7-4846-98f7-9ca3f5160089
ms.openlocfilehash: e66acae5e98d561883f4ad59853dfd862c8ebfee
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61946456"
---
# <a name="statements-in-visual-basic"></a>Instructions dans Visual Basic

Une instruction en Visual Basic est une instruction complète. Il peut contenir des mots clés, des opérateurs, des variables, des constantes et des expressions. Chaque instruction appartient à une des catégories suivantes :

- **Les instructions de déclaration**, qui nommer une variable, une constante ou une procédure et que vous pouvez également spécifier un type de données.

- **Instructions exécutables**, initier des actions. Ces instructions peuvent appeler une méthode ou une fonction, et ils peuvent parcourir ou créer des branches de blocs de code. Les instructions exécutables contiennent **instructions d’assignation**, qui affectent une valeur ou une expression à une variable ou constante.

Cette rubrique décrit chaque catégorie. En outre, cette rubrique décrit comment combiner plusieurs instructions sur une seule ligne et comment continuer une instruction sur plusieurs lignes.

## <a name="declaration-statements"></a>Instructions de déclaration

Vous utilisez les instructions de déclaration pour nommer et définir des procédures, des variables, des propriétés, des tableaux et des constantes. Lorsque vous déclarez un élément de programmation, vous pouvez également définir son type de données, le niveau d’accès et l’étendue. Pour plus d’informations, consultez [caractéristiques d’éléments déclarés](./declared-elements/declared-element-characteristics.md).

L’exemple suivant contient trois déclarations.

[!code-vb[VbVbalrStatements#80](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#80)]

La première déclaration est la `Sub` instruction. Avec sa mise en correspondance `End Sub` instruction, elle déclare une procédure nommée `applyFormat`. Il spécifie également que `applyFormat` est `Public`, ce qui signifie que tout code qui peut faire référence à ce dernier peut l’appeler.

La seconde déclaration est la `Const` instruction qui déclare la constante `limit`, en spécifiant le `Integer` type de données et la valeur 33.

La troisième déclaration est la `Dim` instruction qui déclare la variable `thisWidget`. Le type de données est un objet spécifique, à savoir un objet créé à partir de la `Widget` classe. Vous pouvez déclarer une variable de n’importe quel type de données élémentaire ou de tout type d’objet qui est exposé dans l’application que vous utilisez.

### <a name="initial-values"></a>Valeurs initiales

Lorsque le code contenant une instruction de déclaration s’exécute, Visual Basic réserve la mémoire requise pour l’élément déclaré. Si l’élément contient une valeur, Visual Basic l’initialise à la valeur par défaut pour son type de données. Pour plus d’informations, consultez « Comportement » dans [instruction Dim](../../language-reference/statements/dim-statement.md).

Vous pouvez affecter une valeur initiale à une variable dans le cadre de sa déclaration, comme l’illustre l’exemple suivant.

[!code-vb[VbVbalrStatements#81](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#81)]

Si une variable est une variable objet, vous pouvez créer explicitement une instance de sa classe lorsque vous la déclarez à l’aide de la [nouvel opérateur](../../../visual-basic/language-reference/operators/new-operator.md) mot clé, comme dans l’exemple suivant illustre.

[!code-vb[VbVbalrStatements#82](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#82)]

Notez que la valeur initiale que vous spécifiez dans une instruction de déclaration ne possède pas à une variable jusqu'à ce que l’exécution atteint son instruction de déclaration. En attendant, la variable contient la valeur par défaut pour son type de données.

## <a name="executable-statements"></a>Instructions exécutables

Une instruction exécutable effectue une action. Il peut appeler une procédure, la branche vers un autre emplacement dans le code, parcourir plusieurs instructions, ou évaluer une expression. Une instruction d’assignation est un cas spécial d’une instruction exécutable.

L’exemple suivant utilise un `If...Then...Else` structure pour exécuter différents blocs de code selon la valeur d’une variable de contrôle. Dans chaque bloc de code, un `For...Next` boucle s’exécute un nombre de fois spécifié.

[!code-vb[VbVbalrStatements#83](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#83)]

Le `If` instruction dans l’exemple précédent vérifie la valeur du paramètre `clockwise`. Si la valeur est `True`, il appelle le `spinClockwise` méthode de `aWidget`. Si la valeur est `False`, il appelle le `spinCounterClockwise` méthode de `aWidget`. Le `If...Then...Else` structure de contrôle se termine par `End If`.

Le `For...Next` boucle au sein de chaque bloc appelle la méthode appropriée un nombre de fois égal à la valeur de la `revolutions` paramètre.

## <a name="assignment-statements"></a>Instructions d’assignation

Instructions d’assignation exécutent des opérations d’assignation, qui consistent en prenant la valeur sur le côté droit de l’opérateur d’assignation (`=`) et en le stockant dans l’élément sur la gauche, comme dans l’exemple suivant.

[!code-vb[VbVbalrStatements#73](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#73)]

Dans l’exemple précédent, l’instruction d’assignation stocke la valeur littérale 42 dans la variable `v`.

### <a name="eligible-programming-elements"></a>Éléments de programmation éligibles

L’élément de programmation sur le côté gauche de l’opérateur d’assignation doit être en mesure d’accepter et de stocker une valeur. Cela signifie qu’il doit être une variable ou une propriété qui n’est pas [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md), ou il doit être un élément de tableau. Dans le contexte d’une instruction d’assignation, un tel élément est parfois appelé un *lvalue*, pour « left value ».

La valeur sur le côté droit de l’opérateur d’assignation est générée par une expression qui peut être constitué de n’importe quelle combinaison de littéraux, de constantes, variables, propriétés, éléments de tableau, autres expressions ou des appels de fonction. L'exemple suivant illustre ce comportement.

[!code-vb[VbVbalrStatements#74](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#74)]

L’exemple précédent ajoute la valeur contenue dans la variable `y` à la valeur contenue dans la variable `z`, puis ajoute la valeur retournée par l’appel de fonction `findResult`. La valeur totale de cette expression est ensuite stockée dans la variable `x`.

### <a name="data-types-in-assignment-statements"></a>Types de données dans les instructions d’assignation

Outre les valeurs numériques, l’opérateur d’assignation peut également affecter `String` valeurs, comme l’illustre l’exemple suivant.

[!code-vb[VbVbalrStatements#75](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#75)]

Vous pouvez également affecter `Boolean` des valeurs, en utilisant soit un `Boolean` littéral ou un `Boolean` expression, comme dans l’exemple suivant illustre.

[!code-vb[VbVbalrStatements#76](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#76)]

De même, vous pouvez affecter des valeurs appropriées aux éléments de programmation de la `Char`, `Date`, ou `Object` type de données. Vous pouvez également affecter une instance d’objet à un élément déclaré comme étant de la classe à partir de laquelle cette instance est créée.

### <a name="compound-assignment-statements"></a>Instructions d’assignation composée

*Instructions d’assignation composée* tout d’abord effectuer une opération sur une expression avant de l’assigner à un élément de programmation. L’exemple suivant illustre l’une de ces opérateurs, `+=`, ce qui incrémente la valeur de la variable sur le côté gauche de l’opérateur par la valeur de l’expression à droite.

[!code-vb[VbVbalrStatements#77](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#77)]

L’exemple précédent ajoute 1 à la valeur de `n`, puis stocke cette nouvelle valeur dans `n`. Il est une propriété raccourcie équivalente de l’instruction suivante :

[!code-vb[VbVbalrStatements#78](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#78)]

Un ensemble d’opérations d’assignation composée peut être effectué à l’aide des opérateurs de ce type. Pour obtenir la liste de ces opérateurs et plus d’informations à leur sujet, consultez [opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md).

L’opérateur d’assignation de concaténation (`&=`) est utile pour l’ajout d’une chaîne à la fin d’existant déjà des chaînes, comme l’illustre l’exemple suivant.

[!code-vb[VbVbalrStatements#79](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#79)]

### <a name="type-conversions-in-assignment-statements"></a>Conversions de types dans les instructions d’assignation

La valeur que vous assignez à une variable, une propriété ou un élément de tableau doit être un type de données approprié pour cet élément de destination. En règle générale, vous devez tenter de générer une valeur du même type de données que celui de l’élément de destination. Toutefois, certains types peuvent être convertis en d’autres types lors de l’attribution.

Pour plus d’informations sur la conversion entre types de données, consultez [des Conversions de Type dans Visual Basic](./data-types/type-conversions.md). En bref, Visual Basic convertit automatiquement une valeur d’un type donné en un autre type auquel elle s’étend. Un *conversion étendue* est un dans qui réussit au moment de l’exécution toujours et que vous ne perdiez aucune donnée. Par exemple, Visual Basic convertit une `Integer` valeur `Double` quand cela est approprié, car `Integer` s’étend à `Double`. Pour plus d’informations, consultez [Widening and Narrowing Conversions](./data-types/widening-and-narrowing-conversions.md).

*Les conversions restrictives* (ceux qui ne sont pas étendues) comportent un risque de défaillance en cours d’exécution ou de perte de données. Vous pouvez effectuer une conversion restrictive explicitement à l’aide d’une fonction de conversion de type, ou vous pouvez demander au compilateur d’effectuer toutes les conversions implicitement en définissant `Option Strict Off`. Pour plus d’informations, consultez [Conversions implicites et explicites](./data-types/implicit-and-explicit-conversions.md).

## <a name="putting-multiple-statements-on-one-line"></a>Placement de plusieurs instructions sur une seule ligne

Vous pouvez avoir plusieurs instructions sur une seule ligne, séparés par le signe deux-points (`:`) caractères. L'exemple suivant illustre ce comportement.

[!code-vb[VbVbalrStatements#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#70)]

Souvent, cette forme de syntaxe rend votre code difficile à lire et à gérer. Par conséquent, il est recommandé de conserver une seule instruction sur une ligne.

## <a name="continuing-a-statement-over-multiple-lines"></a>Suite d’une instruction sur plusieurs lignes

Une instruction tient généralement sur une seule ligne, mais lorsqu’il est trop long, vous pouvez la continuer sur la ligne suivante à l’aide d’une séquence de continuation de ligne, qui se compose d’un espace suivi par un caractère de soulignement (`_`) suivie d’un retour chariot. Dans l’exemple suivant, la `MsgBox` instruction exécutable se poursuit sur deux lignes.

[!code-vb[VbVbalrStatements#71](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#71)]

### <a name="implicit-line-continuation"></a>Continuation de ligne implicite

Dans de nombreux cas, vous pouvez continuer une instruction sur la ligne consécutive suivante sans utiliser le caractère de soulignement (`_`). Les éléments syntaxiques suivants continuent implicitement l’instruction sur la ligne de code suivante.

- Après une virgule (`,`). Exemple :

   [!code-vb[VbVbalrLineContinuation#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#1)]

- Après une parenthèse ouvrante (`(`) ou avant une parenthèse fermante (`)`). Exemple :

   [!code-vb[VbVbalrLineContinuation#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#2)]

- Après une accolade ouvrante (`{`) ou avant une accolade fermante (`}`). Exemple :

    [!code-vb[VbVbalrLineContinuation#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#3)]

    Pour plus d’informations, consultez [initialiseurs d’objets : Types nommés et anonymes](./objects-and-classes/object-initializers-named-and-anonymous-types.md) ou [initialiseurs de collections](./collection-initializers/index.md).

- Après avoir ouvert expression incorporée (`<%=`) ou avant la fermeture d’une expression incorporée (`%>`) dans un littéral XML. Exemple :

   [!code-vb[VbVbalrLineContinuation#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#4)]

   Pour plus d’informations, consultez [Expressions incorporées en XML](./xml/embedded-expressions-in-xml.md).

- Après l’opérateur de concaténation (`&`). Exemple :

   [!code-vb[VbVbcnConventions#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/vb/Class1.vb#9)]

   Pour plus d’informations, consultez [opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md).

- Après les opérateurs d’assignation (`=`, `&=`, `:=`, `+=`, `-=`, `*=`, `/=`, `\=`, `^=`, `<<=`, `>>=`). Exemple :

   [!code-vb[VbVbalrLineContinuation#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#5)]

   Pour plus d’informations, consultez [opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md).

- Après les opérateurs binaires (`+`, `-`, `/`, `*`, `Mod`, `<>`, `<`, `>`, `<=`, `>=`, `^`, `>>`, `<<`, `And`, `AndAlso`, `Or`, `OrElse`, `Like`, `Xor`) au sein d’une expression. Exemple :

   [!code-vb[VbVbalrLineContinuation#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#7)]

   Pour plus d’informations, consultez [opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md).

- Après le `Is` et `IsNot` opérateurs. Exemple :

   [!code-vb[VbVbalrLineContinuation#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#8)]

   Pour plus d’informations, consultez [opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md).

- Après un caractère de qualificateur de nom de membre (`.`) et avant le nom du membre. Exemple :

   [!code-vb[VbVbalrLineContinuation#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#5)]

   Toutefois, vous devez inclure un caractère de continuation de ligne (`_`) après un caractère de qualificateur de membre lorsque vous utilisez la `With` instruction ou indiquez des valeurs dans la liste d’initialisation pour un type. Arrêtez la ligne après l’opérateur d’assignation (par exemple, `=`) lorsque vous utilisez `With` instructions ou des listes d’initialisation d’objets. Exemple :

   [!code-vb[VbVbalrLineContinuation#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#14)]

   Pour plus d’informations, consultez [avec... End With, instruction](../../../visual-basic/language-reference/statements/with-end-with-statement.md) ou [initialiseurs d’objets : Types nommés et anonymes](./objects-and-classes/object-initializers-named-and-anonymous-types.md).

- Après un qualificateur de propriété d’axe XML (`.` ou `.@` ou `...`). Toutefois, vous devez inclure un caractère de continuation de ligne (`_`) lorsque vous spécifiez un qualificateur de membre lorsque vous utilisez le `With` mot clé. Exemple :

   [!code-vb[VbVbalrLineContinuation#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#9)]

   Pour plus d’informations, consultez [propriétés d’axe XML](../../../visual-basic/language-reference/xml-axis/index.md).

- Après un inférieur-signe (<) ou avant un signe supérieur-signe supérieur (`>`) lorsque vous spécifiez un attribut. Également après un signe supérieur-signe supérieur (`>`) lorsque vous spécifiez un attribut. Toutefois, vous devez inclure un caractère de continuation de ligne (`_`) lorsque vous spécifiez les attributs de niveau assembly ou au niveau du module. Exemple :

   [!code-vb[VbVbalrLineContinuation#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#10)]

   Pour plus d’informations, consultez [vue d’ensemble des attributs](../../../visual-basic/programming-guide/concepts/attributes/index.md).

- Avant et après les opérateurs de requête (`Aggregate`, `Distinct`, `From`, `Group By`, `Group Join`, `Join`, `Let`, `Order By`, `Select`, `Skip`, `Skip While`, `Take`, `Take While`, `Where`, `In`, `Into`, `On`, `Ascending`, et `Descending`). Vous ne pouvez pas de saut de ligne entre les mots clés des opérateurs de requête qui sont composés de plusieurs mots clés (`Order By`, `Group Join`, `Take While`, et `Skip While`). Exemple :

   [!code-vb[VbVbalrLineContinuation#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#11)]

   Pour plus d’informations, consultez [requêtes](../../../visual-basic/language-reference/queries/index.md).

- Après le `In` mot clé dans un `For Each` instruction. Exemple :

   [!code-vb[VbVbalrLineContinuation#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#12)]

   Pour plus d’informations, consultez [For Each... L’instruction suivante](../../../visual-basic/language-reference/statements/for-each-next-statement.md).

- Après le `From` mot clé dans un initialiseur de collection. Exemple :

   [!code-vb[VbVbalrLineContinuation#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrlinecontinuation/vb/module1.vb#13)]

   Pour plus d’informations, consultez [Initialiseurs de collection](../../../visual-basic/programming-guide/language-features/collection-initializers/index.md).

## <a name="adding-comments"></a>Ajout de commentaires

Code source n’est pas toujours explicatif, même pour le programmeur qui l’a écrit. Pour aider à documenter leur code, par conséquent, la plupart des programmeurs utilisent libéral commentaires incorporés. Commentaires dans le code peuvent expliquer une procédure ou une instruction particulière à tout le monde lecture ou l’utilisation de la version ultérieure. Visual Basic ignore les commentaires pendant la compilation, et elles n’affectent pas le code compilé.

Lignes de commentaire commencent par une apostrophe (`'`) ou `REM` suivi d’un espace. Ils peuvent être ajoutés n’importe où dans le code, sauf dans une chaîne. Pour ajouter un commentaire à une instruction, insérez une apostrophe ou `REM` après l’instruction, suivie du commentaire. Commentaires peuvent également figurer sur leur propre ligne distincte. L’exemple suivant illustre ces possibilités.

[!code-vb[VbVbalrStatements#72](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#72)]

## <a name="checking-compilation-errors"></a>Vérification des erreurs de compilation

Si, après avoir tapé une ligne de code, la ligne est affichée avec une ligne bleue ondulée (un message d’erreur peut également apparaître), il existe une erreur de syntaxe dans l’instruction. Vous devez savoir quel est le problème avec l’instruction (en recherchant dans la liste des tâches, ou vous placez le curseur sur l’erreur avec le pointeur de la souris et lire le message d’erreur) et corrigez-le. Jusqu'à ce que vous avez résolu toutes les erreurs de syntaxe dans votre code, votre programme échoue pour une compilation correcte.

## <a name="related-sections"></a>Rubriques connexes

|Terme|Définition|
|---|---|
|[Opérateurs d’assignation](../../../visual-basic/language-reference/operators/assignment-operators.md)|Fournit des liens vers les pages de référence du langage couvrant les opérateurs d’assignation comme `=`, `*=`, et `&=`.|
|[Opérateurs et expressions](./operators-and-expressions/index.md)|Montre comment combiner des éléments avec des opérateurs pour obtenir de nouvelles valeurs.|
|[Guide pratique pour diviser et combiner des instructions dans le code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)|Montre comment diviser une instruction unique en plusieurs lignes et comment placer plusieurs instructions sur la même ligne.|
|[Guide pratique pour étiqueter des instructions](../../../visual-basic/programming-guide/program-structure/how-to-label-statements.md)|Montre comment étiqueter une ligne de code.|
