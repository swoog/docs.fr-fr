---
title: Liste de paramètres (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- parameters [Visual Basic], Visual Basic
- parameters [Visual Basic], lists
- parameter lists [Visual Basic]
- Visual Basic code, parameter lists
- arguments [Visual Basic], Visual Basic
- procedures [Visual Basic], parameter lists
ms.assetid: 5d737319-0c34-4df9-a23d-188fc840becd
ms.openlocfilehash: 651f08812032aa1c5aacc04fdb3d7f491f12b607
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58836283"
---
# <a name="parameter-list-visual-basic"></a>Liste de paramètres (Visual Basic)
Spécifie les paramètres de qu'une procédure attend lorsqu’elle est appelée. Plusieurs paramètres sont séparés par des virgules. Voici la syntaxe pour un paramètre.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
[ <attributelist> ] [ Optional ] [{ ByVal | ByRef }] [ ParamArray ]   
parametername[( )] [ As parametertype ] [ = defaultvalue ]  
```  
  
## <a name="parts"></a>Composants  
 `attributelist`  
 Facultatif. Liste des attributs qui s’appliquent à ce paramètre. Vous devez placer le [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md) figurant entre crochets («`<`« et »`>`»).  
  
 `Optional`  
 Optionnel. Spécifie que ce paramètre n’est pas obligatoire lorsque la procédure est appelée.  
  
 `ByVal`  
 Optionnel. Spécifie que la procédure ne peut pas remplacer ou réassigner l’élément de variable sous-jacent de l’argument correspondant dans le code appelant.  
  
 `ByRef`  
 Optionnel. Spécifie que la procédure peut modifier l’élément de variable sous-jacent dans le code appelant la même façon que le code d’appel.  
  
 `ParamArray`  
 Optionnel. Spécifie que le dernier paramètre dans la liste de paramètres est un tableau facultatif d’éléments du type de données spécifié. Cela permet au code appelant de passer un nombre arbitraire d’arguments à la procédure.  
  
 `parametername`  
 Obligatoire. Nom de la variable locale représentant le paramètre.  
  
 `parametertype`  
 Obligatoire si `Option Strict` est `On`. Type de données de la variable locale représentant le paramètre.  
  
 `defaultvalue`  
 Requis pour `Optional` paramètres. Toute constante ou expression constante qui correspond au type de données du paramètre. Si le type est `Object`, ou une classe, interface, tableau ou une structure, la valeur par défaut peut uniquement être `Nothing`.  
  
## <a name="remarks"></a>Notes  
 Paramètres sont placés entre parenthèses et séparés par des virgules. Un paramètre peut être déclaré avec n’importe quel type de données. Si vous ne spécifiez pas `parametertype`, les valeurs par défaut `Object`.  
  
 Lorsque le code appelant appelle la procédure, il transmet un *argument* à chaque paramètre requis. Pour plus d’informations, consultez [différences entre les paramètres et Arguments](../../../visual-basic/programming-guide/language-features/procedures/differences-between-parameters-and-arguments.md).  
  
 L’argument que le code appelant passe à chaque paramètre est un pointeur vers un élément sous-jacent dans le code appelant. Si cet élément est *variable* (une constante, littéral, énumération ou expression), il est impossible pour n’importe quel code pour le modifier. S’il s’agit une *variable* élément (une variable déclarée, champ, propriété, élément de tableau ou élément de structure), le code appelant peut le modifier. Pour plus d’informations, consultez [différences entre modifiables et non modifiables Arguments](../../../visual-basic/programming-guide/language-features/procedures/differences-between-modifiable-and-nonmodifiable-arguments.md).  
  
 Si un élément de variable est passé `ByRef`, la procédure peut également le modifier. Pour plus d’informations, consultez [différences entre passage d’un Argument par valeur et par référence](../../../visual-basic/programming-guide/language-features/procedures/differences-between-passing-an-argument-by-value-and-by-reference.md).  
  
## <a name="rules"></a>Règles  
  
-   **Parenthèses.** Si vous spécifiez une liste de paramètres, vous devez le placer entre parenthèses. S’il n’y a aucun paramètre, vous pouvez toujours utiliser des parenthèses entourant une liste vide. Cela améliore la lisibilité de votre code en clarifiant que l’élément est une procédure.  
  
-   **Paramètres facultatifs.** Si vous utilisez le `Optional` modificateur sur un paramètre, tous les paramètres suivants dans la liste doivent également être facultatifs et être déclarés à l’aide de la `Optional` modificateur.  
  
     Chaque déclaration de paramètre facultatif doit fournir le `defaultvalue` clause.  
  
     Pour plus d’informations, consultez [paramètres facultatifs](../../../visual-basic/programming-guide/language-features/procedures/optional-parameters.md).  
  
-   **Tableaux de paramètres.** Vous devez spécifier `ByVal` pour un `ParamArray` paramètre.  
  
     Vous ne pouvez pas utiliser les deux `Optional` et `ParamArray` dans la même liste de paramètres.  
  
     Pour plus d’informations, consultez [tableaux de paramètres](../../../visual-basic/programming-guide/language-features/procedures/parameter-arrays.md).  
  
-   **Mécanisme de passage.** Le mécanisme par défaut pour chaque argument est `ByVal`, ce qui signifie que la procédure ne peut pas modifier l’élément variable sous-jacent. Toutefois, si l’élément est un type référence, la procédure peut modifier le contenu ou les membres de l’objet sous-jacent, même si elle ne peut pas remplacer ou réassigner l’objet lui-même.  
  
-   **Noms de paramètre.** Si le type de données du paramètre est un tableau, suivez `parametername` immédiatement par des parenthèses. Pour plus d’informations sur les noms de paramètre, consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre un `Function` procédure qui définit deux paramètres.  
  
 [!code-vb[VbVbalrStatements#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.InteropServices.DllImportAttribute>
- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)
- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Declare (instruction)](../../../visual-basic/language-reference/statements/declare-statement.md)
- [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)
- [Option Strict (instruction)](../../../visual-basic/language-reference/statements/option-strict-statement.md)
- [Vue d’ensemble des attributs](../../../visual-basic/programming-guide/concepts/attributes/index.md)
- [Guide pratique pour diviser et combiner des instructions dans le code](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)
