---
title: Déclaration de variable en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], declaring
- member variables [Visual Basic], declarations
- Dim statement [Visual Basic], variable declaration
- declaring variables [Visual Basic]
- variables [Visual Basic], scope
- variables [Visual Basic], data types
- data types [Visual Basic], variable declarations
- lifetime [Visual Basic], variables
- variables [Visual Basic], lifetime
- access levels [Visual Basic], variables
- scope [Visual Basic], declaration statements
- variables [Visual Basic], access level
- local variables [Visual Basic], declarations
- scope [Visual Basic], variables
ms.assetid: d8f10226-92b1-480f-9f53-df377b2d7e15
ms.openlocfilehash: a23d16d4ef4e90041e320c52381fa34b8b33d2d4
ms.sourcegitcommit: facefcacd7ae2e5645e463bc841df213c505ffd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55738745"
---
# <a name="variable-declaration-in-visual-basic"></a>Déclaration de variable en Visual Basic
Vous déclarez une variable pour spécifier son nom et les caractéristiques. L’instruction de déclaration de variables est la [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md). Son emplacement et son contenu déterminent les caractéristiques de la variable.  
  
 Pour les règles d’affectation de noms des variables et des considérations, consultez [noms d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
## <a name="declaration-levels"></a>Niveaux de déclaration  
  
### <a name="local-and-member-variables"></a>Local et les Variables de membre  
 Un *variable locale* est celui qui est déclaré dans une procédure. Un *variable membre* est un membre d’un type Visual Basic ; elle est déclarée au niveau du module, à l’intérieur d’une classe, une structure ou un module, mais pas dans une procédure interne à cette classe, une structure ou un module.  
  
### <a name="shared-and-instance-variables"></a>Instance et Variables partagées  
 Dans une classe ou une structure, la catégorie d’une variable membre dépend ou non, il est partagé. S’il est déclaré avec le [partagé](../../../../visual-basic/language-reference/modifiers/shared.md) mot clé, il est un *variable partagée*, et il existe une seule copie partagée entre toutes les instances de la classe ou structure.  
  
 Sinon, il est un *variable d’instance*, et une copie séparée est créée pour chaque instance de la classe ou structure. Une copie donnée d’une variable d’instance est disponible uniquement à l’instance de la classe ou structure dans lequel il a été créé. Elle est indépendante d’une copie de la variable d’instance dans une autre instance de la classe ou structure.  
  
## <a name="declaring-data-type"></a>Déclaration de Type de données  
 Le [comme](../../../../visual-basic/language-reference/statements/as-clause.md) clause dans l’instruction de déclaration vous permet de définir le type de données ou d’un type d’objet de la variable que vous déclarez. Vous pouvez spécifier un des types suivants d’une variable :  
  
-   Type de données élémentaire, tel que `Boolean`, `Long`, ou `Decimal`  
  
-   Un type de données composite, tel qu’un tableau ou une structure  
  
-   Type d’objet, ou classe, défini dans votre application ou dans une autre application  
  
-   Un [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] classe, telle que <xref:System.Windows.Forms.Label> ou <xref:System.Windows.Forms.TextBox>  
  
-   Type d’interface, tel que <xref:System.IComparable> ou <xref:System.IDisposable>  
  
 Vous pouvez déclarer plusieurs variables dans une instruction sans avoir à répéter le type de données. Dans les instructions suivantes, les variables `i`, `j`, et `k` sont déclarés en tant que type `Integer`, `l` et `m` comme `Long`, et `x` et `y` comme `Single`:  
  
```  
Dim i, j, k As Integer  
' All three variables in the preceding statement are declared as Integer.  
Dim l, m As Long, x, y As Single  
' In the preceding statement, l and m are Long, x and y are Single.  
```  
  
 Pour plus d’informations sur les types de données, consultez [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md). Pour plus d’informations sur les objets, consultez [objets et Classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md) et [programmation avec des composants](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/0ffkdtkf(v=vs.120)).  
  
## <a name="local-type-inference"></a>Inférence de type local  
 *Inférence de type* est utilisé pour déterminer les types de données des variables locales déclarées sans un `As` clause. Le compilateur déduit le type de la variable du type de l’expression d’initialisation. Cela vous permet de déclarer des variables sans déclarer explicitement un type. Dans l’exemple suivant, les deux `num1` et `num2` sont fortement typées en tant qu’entiers.  
  
 [!code-vb[VbVbalrTypeInference#1](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/variable-declaration_1.vb)]  
  
 Si vous souhaitez utiliser l’inférence de type local, `Option Infer` doit être définie sur `On`. Pour plus d’informations, consultez [Inférence de type de variable locale](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md) et [Option Infer, instruction](../../../../visual-basic/language-reference/statements/option-infer-statement.md).  
  
## <a name="characteristics-of-declared-variables"></a>Caractéristiques des Variables déclarées  
 Le *durée de vie* d’une variable est la période de temps pendant laquelle il est disponible pour utilisation. En règle générale, une variable existe tant que l’élément qui le déclare (par exemple, une procédure ou une classe) continue d’exister. Si la variable n’a pas besoin excède la durée de vie de son élément conteneur, il est inutile à rien de spécial dans la déclaration. Si la variable doit continuer d’exister plus longtemps que son élément conteneur, vous pouvez inclure le `Static` ou `Shared` mot clé dans son `Dim` instruction. Pour plus d’informations, consultez [durée de vie dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md).  
  
 Le *étendue* d’une variable est l’ensemble du code que vous pouvez vous y référer sans qualifier son nom. La portée d’une variable est déterminée par l’où elle est déclarée. Code que qui se trouve dans une région donnée peut utiliser les variables définies dans cette région sans devoir qualifier leurs noms. Pour plus d'informations, consultez [Scope in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md).  
  
 D’une variable *niveau d’accès* est l’étendue de code qui a l’autorisation d’y accéder. Cela est déterminé par le modificateur d’accès (tel que [Public](../../../../visual-basic/language-reference/modifiers/public.md) ou [privé](../../../../visual-basic/language-reference/modifiers/private.md)) que vous utilisez dans le `Dim` instruction. Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Créer une Variable](../../../../visual-basic/programming-guide/language-features/variables/how-to-create-a-new-variable.md)
- [Guide pratique pour Déplacer des données dans et hors d’une Variable](../../../../visual-basic/programming-guide/language-features/variables/how-to-move-data-into-and-out-of-a-variable.md)
- [Types de données](../../../../visual-basic/language-reference/data-types/index.md)
- [Protected](../../../../visual-basic/language-reference/modifiers/protected.md)
- [Friend](../../../../visual-basic/language-reference/modifiers/friend.md)
- [Static](../../../../visual-basic/language-reference/modifiers/static.md)
- [Caractéristiques d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md)
- [Inférence de type local](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [Option Infer (instruction)](../../../../visual-basic/language-reference/statements/option-infer-statement.md)
