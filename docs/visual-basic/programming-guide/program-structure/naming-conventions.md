---
title: Conventions d'affectation de noms Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- names [Visual Basic], Visual Basic rules
- naming conventions
- naming conventions [Visual Basic], Visual Basic
- Visual Basic code, naming conventions
- conventions [Visual Basic], Visual Basic coding
- names [Visual Basic], naming conventions
- naming conventions [Visual Basic], classes
ms.assetid: 164949a4-2a7c-4736-9d82-9c3078e2e56c
ms.openlocfilehash: 46f59403feced4baafef4662065cb7daedbeaa7b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58837076"
---
# <a name="visual-basic-naming-conventions"></a>Conventions d'affectation de noms Visual Basic
Lorsque vous nommez un élément dans votre application Visual Basic, le premier caractère de ce nom doit être un caractère alphabétique ou un trait de soulignement. Notez, cependant, que les noms commençant par un trait de soulignement ne sont pas compatibles avec le [indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md) (CLS).  
  
 Les suggestions suivantes s’appliquent à d’affectation de noms.  
  
-   Commencer chaque mot distinct dans un nom par une lettre majuscule, comme dans `FindLastRecord` et `RedrawMyForm`.  
  
-   Commencer les noms de fonction et de méthode avec un verbe, comme dans `InitNameArray` ou `CloseDialog`.  
  
-   Commencer une classe, structure, module et les noms de propriété par un nom, comme dans `EmployeeName` ou `CarAccessory`.  
  
-   Commencer les noms d’interface avec le préfixe « I », suivi d’un nom ou d’une expression nominale, comme `IComponent`, ou d’un adjectif décrivant le comportement de l’interface, comme `IPersistable`. N’utilisent pas le caractère de soulignement et utilisez les abréviations avec parcimonie, étant donné que les abréviations peuvent entraîner une confusion.  
  
-   Commencer les noms de gestionnaires d’événements par un nom décrivant le type d’événement suivi par la «`EventHandler`« de suffixe, comme dans »`MouseEventHandler`».  
  
-   Dans les noms de classes d’arguments d’événement, ajoutez le «`EventArgs`« suffixe.  
  
-   Si un événement a un concept de « before » ou « after », utilisez un suffixe dans le présent ou passé, comme dans «`ControlAdd`« ou »`ControlAdded`».  
  
-   Pour les termes longs ou fréquemment utilisés, utilisez les abréviations pour limiter la longueur, par exemple, « HTML », au lieu de « Hypertext Markup Language ». En règle générale, les noms de variables de plus de 32 caractères sont difficiles à lire sur un écran avec une faible résolution. En outre, assurez-vous que vos abréviations sont cohérentes dans toute l’application. De manière aléatoire dans un projet entre « HTML » et « Hypertext Markup Language » peut prêter à confusion.  
  
-   Évitez d’utiliser des noms dans une portée interne sont les mêmes que les noms dans une portée externe. Erreurs peuvent entraîner si la variable incorrecte est accessible. En cas de conflit entre une variable et le mot clé du même nom, vous devez identifier le mot clé en le faisant précéder avec la bibliothèque de types appropriés. Par exemple, si vous disposez d’une variable appelée `Date`, vous pouvez utiliser la fonction intrinsèque `Date` fonction uniquement en appelant <xref:System.DateTime.Date%2A?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation des mots clés comme noms d’éléments dans le code](../../../visual-basic/programming-guide/program-structure/keywords-as-element-names-in-code.md)
- [Me, My, MyBase et MyClass](../../../visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass.md)
- [Noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [Informations de référence sur le langage Visual Basic](../../../visual-basic/language-reference/index.md)
