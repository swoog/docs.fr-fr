---
title: Const, instruction (Visual Basic)
ms.date: 05/12/2018
f1_keywords:
- vb.Const
helpviewer_keywords:
- Const statement [Visual Basic]
ms.assetid: 495b318d-b7c5-4198-94f8-0790a541b07a
ms.openlocfilehash: 089c2dca99373f379e1eff319cf8c41242e5f135
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58835308"
---
# <a name="const-statement-visual-basic"></a>Const, instruction (Visual Basic)
Déclare et définit une ou plusieurs constantes.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
[ <attributelist> ] [ accessmodifier ] [ Shadows ]   
Const constantlist  
```  
  
## <a name="parts"></a>Composants  
 `attributelist`  
 Optionnel. Liste des attributs qui s’appliquent à toutes les constantes sont déclarées dans cette instruction. Consultez [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md) figurant entre crochets («`<`« et »`>`»).  
  
 `accessmodifier`  
 Optionnel. Utilisez-le pour spécifier le code peut accéder à ces constantes. Peut être [Public](../../../visual-basic/language-reference/modifiers/public.md), [protégé](../../../visual-basic/language-reference/modifiers/protected.md), [Friend](../../../visual-basic/language-reference/modifiers/friend.md), [Protected Friend](../modifiers/protected-friend.md), [privé](../../../visual-basic/language-reference/modifiers/private.md), ou [Private protégé](../../language-reference/modifiers/private-protected.md).
  
 `Shadows`  
 Optionnel. Utilisez-le pour redéclarer et masquer un élément de programmation dans une classe de base. Consultez [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).  
  
 `constantlist`  
 Obligatoire. Liste des constantes qui sont déclarées dans cette instruction.  
  
 `constant` `[ ,` `constant` `... ]`  
  
 Chaque `constant` emploie la syntaxe et les éléments suivants :  
  
 `constantname` `[ As` `datatype` `] =` `initializer`  
  
|Élément|Description|  
|----------|-----------------|  
|`constantname`|Obligatoire. Nom de la constante. Consultez [Declared Element Names](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).|  
|`datatype`|Obligatoire si `Option Strict` est `On`. Type de données de la constante.|  
|`initializer`|Obligatoire. Expression qui est évaluée au moment de la compilation et assignée à la constante.|  
  
## <a name="remarks"></a>Notes  
 Si vous avez une valeur qui ne change jamais dans votre application, vous pouvez définir une constante nommée et l’utiliser à la place d’une valeur littérale. Un nom est plus facile à retenir qu’une valeur. Vous pouvez définir la constante qu’une seule fois et l’utiliser dans de nombreux endroits dans votre code. Si dans une version ultérieure, vous devez redéfinir la valeur, la `Const` instruction est le seul endroit où vous souhaitez apporter une modification.  
  
 Vous pouvez utiliser `Const` uniquement au niveau du module ou de la procédure. Cela signifie que le *contexte de déclaration* pour une variable doit être une classe, structure, module, procédure ou un bloc et ne peut pas être un fichier source, un espace de noms ou une interface. Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).  
  
 Par défaut des constantes locales (à l’intérieur d’une procédure) à accès public et que vous ne pouvez pas utiliser les modificateurs d’accès sur ces derniers. Classe et le module membre constantes (en dehors de toute procédure) par défaut d’un accès privé et structure membre constantes par défaut d’un accès public. Vous pouvez ajuster leurs niveaux d’accès avec les modificateurs d’accès.  
  
## <a name="rules"></a>Règles  
  
-   **Contexte de déclaration.** Une constante déclarée au niveau du module, en dehors de toute procédure, est un *constante membre*; il est membre de la classe, structure, ou le module qui la déclare.  
  
     Une constante déclarée au niveau de la procédure est un *constante locale*; elle est locale à la procédure ou du bloc qui le déclare.  
  
-   **Attributs.** Vous pouvez appliquer des attributs qu’aux constantes membres, pas aux constantes locales. Un attribut fournit des informations aux métadonnées de l’assembly qui n’est pas significatif pour le stockage temporaire tel que les constantes locales.  
  
-   **Modificateurs.** Par défaut, toutes les constantes sont `Shared`, `Static`, et `ReadOnly`. Vous ne pouvez pas utiliser un de ces mots clés lorsque vous déclarez une constante.  
  
     Au niveau de la procédure, vous ne pouvez pas utiliser `Shadows` ou un modificateur d’accès pour déclarer des constantes locales.  
  
-   **Plusieurs constantes.** Vous pouvez déclarer plusieurs constantes dans la même instruction de déclaration, en spécifiant le `constantname` partie pour chacun d'entre eux. Plusieurs constantes sont séparés par des virgules.  
  
## <a name="data-type-rules"></a>Règles de Type de données  
  
-   **Types de données.** La `Const` instruction peut déclarer le type de données d’une variable. Vous pouvez spécifier n’importe quel type de données ou le nom d’une énumération.  
  
-   **Type par défaut.** Si vous ne spécifiez pas `datatype`, la constante prend le type de données `initializer`. Si vous spécifiez à la fois `datatype` et `initializer`, le type de données de `initializer` doit être convertible en `datatype`. Si ni `datatype` ni `initializer` est présent, le type de données par défaut, `Object`.  
  
-   **Différents Types.** Vous pouvez spécifier différents types de données pour les constantes à l’aide d’un distinct `As` pour chaque variable que vous déclarez. Toutefois, vous ne pouvez pas déclarer plusieurs constantes comme étant du même type à l’aide d’un commun `As` clause.  
  
-   **Initialisation.** Vous devez initialiser la valeur de chaque constante dans `constantlist`. Vous utilisez `initializer` pour fournir une expression à assigner à la constante. L’expression peut être n’importe quelle combinaison de littéraux, les autres constantes qui sont déjà définies et les membres de l’énumération qui sont déjà définis. Vous pouvez utiliser des opérateurs arithmétiques et logiques pour combiner ces éléments.  
  
     Vous ne pouvez pas utiliser des variables ou des fonctions dans `initializer`. Toutefois, vous pouvez utiliser des mots clés de conversion comme `CByte` et `CShort`. Vous pouvez également utiliser `AscW` si vous l’appelez avec une constante `String` ou `Char` argument, étant donné que qui peut être évaluée au moment de la compilation.  
  
## <a name="behavior"></a>Comportement  
  
-   **Étendue.** Constantes locales sont accessibles uniquement à partir de leur procédure ou un bloc. Constantes de membre sont accessibles à partir de n’importe où leur classe, une structure ou un module.  
  
-   **Qualification.** Code en dehors d’une classe, structure ou module doit qualifier le nom d’une constante membre avec le nom de cette classe, une structure ou un module. Code en dehors de qu'une procédure ou un bloc ne peut pas faire référence aux constantes locales de cette procédure ou un bloc.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise la `Const` instruction pour déclarer des constantes à utiliser à la place de valeurs littérales.  
  
 [!code-vb[VbVbalrStatements#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#13)]  
  
## <a name="example"></a>Exemple  
 Si vous définissez une constante avec le type de données `Object`, le compilateur Visual Basic lui donne le type de `initializer`, au lieu de `Object`. Dans l’exemple suivant, la constante `naturalLogBase` a le type au moment de l’exécution `Decimal`.  
  
 [!code-vb[VbVbalrStatements#87](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#87)]  
  
 L’exemple précédent utilise le <xref:System.Type.ToString%2A> méthode sur le <xref:System.Type> objet retourné par la [opérateur GetType](../../../visual-basic/language-reference/operators/gettype-operator.md), car <xref:System.Type> ne peut pas être converti en `String` à l’aide de `CStr`.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Strings.Asc%2A>
- <xref:Microsoft.VisualBasic.Strings.AscW%2A>
- [Enum (instruction)](../../../visual-basic/language-reference/statements/enum-statement.md)
- [#Const (directive)](../../../visual-basic/language-reference/directives/const-directive.md)
- [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)
- [ReDim (instruction)](../../../visual-basic/language-reference/statements/redim-statement.md)
- [Conversions implicites et explicites](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [Constantes et énumérations](../../../visual-basic/programming-guide/language-features/constants-enums/index.md)
- [Constantes et énumérations](../../../visual-basic/language-reference/constants-and-enumerations.md)
- [Fonctions de conversion de types](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
