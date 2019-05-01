---
title: Caractères spéciaux dans le code (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.)
- vb.(
- vb.colon
- vb.!
- vb..
- 'vb.:'
helpviewer_keywords:
- special characters [Visual Basic], in code
- parentheses [Visual Basic], using in code
- colons (:)
- period character in code
- dot operator (.)
- dictionary access operator [Visual Basic]
- concatenation operators [Visual Basic], special characters in code
- concatenation operators [Visual Basic], vs. addition operator
- '! operator'
- separators [Visual Basic], using in code
- operators [Visual Basic], dictionary access
- ': separator character'
- member access operator [Visual Basic]
- addition operator [Visual Basic]
- operators [Visual Basic], member access
- . operator
- exclamation points
- separators
- exclamation point operator (!)
- Visual Basic code, special characters
ms.assetid: 310dce0c-45b5-4e0d-83e9-32df258d2a3e
ms.openlocfilehash: 65fcd10521742e287c7934080b3352a06668df7a
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61967979"
---
# <a name="special-characters-in-code-visual-basic"></a>Caractères spéciaux dans le code (Visual Basic)
Vous devez parfois utiliser des caractères spéciaux dans votre code, autrement dit, les caractères qui ne sont pas alphabétiques ou numériques. La ponctuation et caractères spéciaux dans le jeu de caractères de Visual Basic ont plusieurs utilisations, de l’organisation du texte de programme à la définition des tâches effectuées par le compilateur ou le programme compilé. Ils ne spécifient pas d'opération à effectuer.  
  
## <a name="parentheses"></a>Parenthèses  
 Utilisez des parenthèses lorsque vous définissez une procédure, comme un `Sub` ou `Function`. Vous devez placer toutes les listes d’arguments de procédure entre parenthèses. Vous également utiliser des parenthèses pour insérer des variables ou arguments en groupes logiques, en particulier pour substituer l’ordre par défaut de priorité des opérateurs dans une expression complexe. L'exemple suivant illustre ce comportement.  
  
 [!code-vb[VbVbcnConventions#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#11)]  
  
 Après l’exécution du code précédent, la valeur de `d` est 8.225 et la valeur de `e` est 3. Le calcul pour `d` utilise la priorité par défaut de `/` sur `+` et équivaut à `d = b + (c / a)`. Les parenthèses dans le calcul pour `e` substituer la priorité par défaut.  
  
## <a name="separators"></a>Séparateurs  
 Séparateurs de faire ce que leur nom suggère : séparent les différentes sections de code. En Visual Basic, le caractère de séparation est le signe deux-points (`:`). Utilisez des séparateurs lorsque vous voulez inclure plusieurs instructions sur une seule ligne au lieu des lignes distinctes. Cela économise de l’espace et améliore la lisibilité de votre code. L’exemple suivant montre les trois instructions séparées par le signe deux-points.  
  
 [!code-vb[VbVbcnConventions#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#12)]  
  
 Pour plus d'informations, voir [Procédure : Diviser et combiner des instructions dans le Code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md).  
  
 Le signe deux-points (`:`) caractère est également utilisé pour identifier une étiquette d’instruction. Pour plus d'informations, voir [Procédure : Étiqueter des instructions](../../../visual-basic/programming-guide/program-structure/how-to-label-statements.md).  
  
## <a name="concatenation"></a>Concaténation  
 Utilisez le `&` opérateur pour *concaténation*, ou lier plusieurs chaînes. Ne confondez pas avec le `+` opérateur, qui additionne les valeurs numériques. Si vous utilisez le `+` pour concaténer lorsque vous travaillez sur des valeurs numériques, vous pouvez obtenir des résultats incorrects. Cela est illustré par l'exemple suivant.  
  
 [!code-vb[VbVbcnConventions#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#13)]  
  
 Après l’exécution du code précédent, la valeur de `resultA` est 21.01 et la valeur de `resultB` est « 10.0111 ».  
  
## <a name="member-access-operators"></a>Opérateurs d’accès au membre  
 Pour accéder à un membre d’un type, utilisez le point (`.`) ou un point d’exclamation (`!`) opérateur entre le nom de type et le nom du membre.  
  
### <a name="dot--operator"></a>Point (.) Opérateur  
 Utilisez le `.` opérateur sur une classe, structure, interface, énumération ou comme un opérateur d’accès au membre. Le membre peut être un champ, une propriété, un événement ou une méthode. L'exemple suivant illustre ce comportement.  
  
 [!code-vb[VbVbcnConventions#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#14)]  
  
### <a name="exclamation-point--operator"></a>Point d’exclamation ( !) Opérateur  
 Utilisez le `!` opérateur uniquement sur une classe ou une interface comme un opérateur d’accès au dictionnaire. La classe ou interface doit avoir une propriété par défaut qui accepte un seul `String` argument. L’identificateur qui suit immédiatement la `!` opérateur devient la valeur d’argument passée à la propriété par défaut sous forme de chaîne. Cela est illustré par l'exemple suivant.  
  
 [!code-vb[VbVbcnConventions#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#15)]  
  
 Les trois lignes de sortie de `MsgBox` affichent tous la valeur `32856`. La première ligne utilise l’accès traditionnel à la propriété `index`, la seconde utilise le fait que `index` est la propriété par défaut de la classe `hasDefault`, et la troisième utilise l’accès au dictionnaire à la classe.  
  
 Notez que le second opérande de le `!` opérateur doit être un identificateur Visual Basic valide ne pas entourée de guillemets doubles (`" "`). En d’autres termes, vous ne pouvez pas utiliser un littéral de chaîne ou une variable de chaîne. La modification ci-dessous à la dernière ligne de la `MsgBox` appel génère une erreur car `"X"` est une chaîne délimitée littéral.  
  
 `"Dictionary access returns " & hD!"X")`  
  
> [!NOTE]
>  Références aux collections par défaut doivent être explicites. En particulier, vous ne pouvez pas utiliser le `!` opérateur sur une variable à liaison tardive.  
  
 Le `!` caractère est également utilisé comme le `Single` caractère de type.  
  
## <a name="see-also"></a>Voir aussi

- [Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [Caractères de type](../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)
