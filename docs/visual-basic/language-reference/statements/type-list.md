---
title: Liste de types (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- StructureConstraint
- vb.StructureConstraint
- ClassConstraint
- vb.ClassConstraint
helpviewer_keywords:
- class constraint
- constraints, Visual Basic generic types
- generic parameters
- generics [Visual Basic], constraints
- generics [Visual Basic], type list
- structure constraint
- constraints, in type parameters
- generics [Visual Basic], generic types
- parameters [Visual Basic], type
- constraints, Structure keyword
- type parameters [Visual Basic], constraints
- types [Visual Basic], generic
- parameters [Visual Basic], generic
- generics [Visual Basic], type parameters
- type parameters
- constraints, Class keyword
ms.assetid: 56db947a-2ae8-40f2-a70a-960764e9d0db
ms.openlocfilehash: d071e59d94e51ca55167983d0ee3098bd5c7dd8f
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58843628"
---
# <a name="type-list-visual-basic"></a>Liste de types (Visual Basic)
Spécifie le *paramètres de type* pour un *générique* élément de programmation. Plusieurs paramètres sont séparés par des virgules. Voici la syntaxe pour un paramètre de type.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
[genericmodifier] typename [ As constraintlist ]  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`genericmodifier`|Facultatif. Peut être utilisé uniquement dans les délégués et interfaces génériques. Vous pouvez déclarer un type covariant à l’aide de la [Out](../../../visual-basic/language-reference/modifiers/out-generic-modifier.md) mot clé ou contravariant à l’aide de la [dans](../../../visual-basic/language-reference/modifiers/in-generic-modifier.md) mot clé. Consultez [Covariance et contravariance](../../programming-guide/concepts/covariance-contravariance/index.md).|  
|`typename`|Obligatoire. Nom du paramètre de type. Il s’agit d’un espace réservé, à remplacer par un type défini fourni par l’argument de type correspondant.|  
|`constraintlist`|Optionnel. Liste des conditions requises qui limitent le type de données qui peut être fourni pour `typename`. Si vous avez plusieurs contraintes, placez-les entre accolades (`{ }`) et séparez-les par des virgules. Vous devez introduire la liste des contraintes avec le [comme](../../../visual-basic/language-reference/statements/as-clause.md) mot clé. Vous utilisez `As` une seule fois, au début de la liste.|  
  
## <a name="remarks"></a>Notes  
 Chaque élément de programmation générique doit prendre au moins un paramètre de type. Un paramètre de type est un espace réservé pour un type spécifique (un *élément construit*) que le code client spécifie lorsqu’il crée une instance du type générique. Vous pouvez définir une classe générique, structure, interface, une procédure ou délégué.  
  
 Pour plus d’informations sur le moment de définir un type générique, consultez [des Types génériques en Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md). Pour plus d’informations sur les noms de paramètre de type, consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
## <a name="rules"></a>Règles  
  
-   **Parenthèses.** Si vous fournissez une liste de paramètres de type, vous devez le placer entre parenthèses, et vous devez introduire la liste avec la [de](../../../visual-basic/language-reference/statements/of-clause.md) mot clé. Vous utilisez `Of` une seule fois, au début de la liste.  
  
-   **Contraintes.** Une liste de *contraintes* sur un type de paramètre permettre inclure les éléments suivants dans n’importe quelle combinaison :  
  
    -   Nombre quelconque d’interfaces. Le type fourni doit implémenter chaque interface dans cette liste.  
  
    -   Une classe au plus. Le type fourni doit hériter de cette classe.  
  
    -   Mot clé `New`. Le type fourni doit exposer un constructeur sans paramètre accessible par votre type générique. Cela est utile si vous contraindre un paramètre de type par une ou plusieurs interfaces. Un type qui implémente les interfaces n’expose pas nécessairement un constructeur, et selon le niveau d’accès d’un constructeur, le code dans le type générique ne peut pas être en mesure d’y accéder.  
  
    -   Soit le `Class` mot clé ou le `Structure` mot clé. Le `Class` mot clé contraint un paramètre de type générique à exiger que tout argument de type passé est un type référence, par exemple une chaîne, un tableau ou un délégué, ou un objet créé à partir d’une classe. Le `Structure` mot clé contraint un paramètre de type générique à exiger que tout argument de type lui est passé un type valeur, par exemple un type de structure, d’énumération ou de données élémentaire. Vous ne pouvez pas inclure à la fois `Class` et `Structure` dans le même `constraintlist`.  
  
     Le type fourni doit satisfaire chaque configuration requise que vous incluez dans `constraintlist`.  
  
     Contraintes sur chaque paramètre de type sont indépendantes des contraintes sur les autres paramètres de type.  
  
## <a name="behavior"></a>Comportement  
  
-   **Substitution de la compilation.** Lorsque vous créez un type construit à partir d’un élément de programmation générique, vous fournissez un type défini pour chaque paramètre de type. Le compilateur Visual Basic substitue ce type fourni pour chaque occurrence de `typename` dans l’élément générique.  
  
-   **Absence de contraintes.** Si vous ne spécifiez pas de contraintes sur un paramètre de type, votre code est limité aux opérations et aux membres pris en charge par le [Object Data Type](../../../visual-basic/language-reference/data-types/object-data-type.md) pour ce paramètre de type.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre une définition squelette d’une classe de dictionnaire générique, y compris une fonction squelette pour ajouter une nouvelle entrée au dictionnaire.  
  
 [!code-vb[VbVbalrStatements#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#3)]  
  
## <a name="example"></a>Exemple  
 Étant donné que `dictionary` est générique, le code qui l’utilise peut créer une variété d’objets à partir de celui-ci, chacun disposant des mêmes fonctionnalités, mais agissant sur un autre type de données. L’exemple suivant montre une ligne de code qui crée un `dictionary` avec l’objet `String` entrées et `Integer` clés.  
  
 [!code-vb[VbVbalrStatements#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#4)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre la définition squelette équivalente générée par l’exemple précédent.  
  
 [!code-vb[VbVbalrStatements#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#5)]  
  
## <a name="see-also"></a>Voir aussi

- [Of](../../../visual-basic/language-reference/statements/of-clause.md)
- [New (opérateur)](../../../visual-basic/language-reference/operators/new-operator.md)
- [Niveaux d’accès dans Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [Object (type de données)](../../../visual-basic/language-reference/data-types/object-data-type.md)
- [Function (instruction)](../../../visual-basic/language-reference/statements/function-statement.md)
- [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)
- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Guide pratique pour utiliser une classe générique](../../../visual-basic/programming-guide/language-features/data-types/how-to-use-a-generic-class.md)
- [Covariance et contravariance](../../programming-guide/concepts/covariance-contravariance/index.md)
- [In](../../../visual-basic/language-reference/modifiers/in-generic-modifier.md)
- [Out](../../../visual-basic/language-reference/modifiers/out-generic-modifier.md)
