---
title: Différences entre l'occultation et la substitution (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- shadowing, vs. overriding
- overriding, vs. shadowing
ms.assetid: 2d014a0b-7630-407d-8f4e-24bd87987923
ms.openlocfilehash: b935184f0e4d0378bfea69811aa4e6c068a9776f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61827942"
---
# <a name="differences-between-shadowing-and-overriding-visual-basic"></a>Différences entre l'occultation et la substitution (Visual Basic)
Lorsque vous définissez une classe qui hérite d’une classe de base, il est parfois utile de redéfinir une ou plusieurs des éléments de classe de base dans la classe dérivée. Occultation et substitution sont disponibles à cet effet.  
  
## <a name="comparison"></a>Comparaison  
 Occultation et substitution sont utilisés lorsqu’une classe dérivée hérite d’une classe de base et redéfinissent un élément déclaré par un autre. Mais il existe des différences importantes entre les deux.  
  
 Le tableau suivant compare l’occultation et substitution.  
  
||||  
|---|---|---|  
|Point de comparaison|Copie shadow|Substitution de|  
|Objectif|Protège contre une modification de classe de base suivante qui introduit un membre que vous avez déjà défini dans votre classe dérivée|Atteint le polymorphisme en définissant une implémentation différente d’une procédure ou une propriété avec la même séquence d’appel<sup>1</sup>|  
|Élément redéfini|Un type d’élément déclaré|Seule une procédure (`Function`, `Sub`, ou `Operator`) ou une propriété|  
|Élément redéfinissant|Un type d’élément déclaré|Seulement une procédure ou une propriété avec la séquence d’appel identiques<sup>1</sup>|  
|Niveau d’accès de l’élément redéfinissant|N’importe quel niveau d’accès|Impossible de modifier le niveau d’accès de l’élément substitué|  
|Capacité de lecture et de l’élément redéfinissant|N’importe quelle combinaison|Impossible de changer la lisibilité ou la facilité d’écriture de la propriété substituée|  
|Contrôle sur la redéfinition|Élément de la classe de base ne peut pas appliquer ou interdire l’occultation|Élément de la classe de base peut spécifier `MustOverride`, `NotOverridable`, ou `Overridable`|  
|Utilisation du mot clé|`Shadows` recommandé dans la classe dérivée ; `Shadows` assumé si aucun `Shadows` ni `Overrides` spécifié<sup>2</sup>|`Overridable` ou `MustOverride` requis dans la classe de base ; `Overrides` requis dans la classe dérivée|  
|Héritage de l’élément redéfinissant par des classes dérivées à partir de votre classe dérivée|Élément occultant hérité en plus des classes dérivées ; élément occulté toujours masqué<sup>3</sup>|Élément substituant hérité en plus des classes dérivées ; élément substitué toujours substitué|  
  
 <sup>1</sup> le *séquence d’appel* se compose du type d’élément (`Function`, `Sub`, `Operator`, ou `Property`), nom, la liste de paramètres et le type de retour. Vous ne pouvez pas substituer une procédure avec une propriété ou l’autre sens. Vous ne pouvez pas substituer un genre de procédure (`Function`, `Sub`, ou `Operator`) avec un autre type.  
  
 <sup>2</sup> si vous ne spécifiez pas `Shadows` ou `Overrides`, le compilateur émet un message d’avertissement pour vous aider à vérifier le genre de redéfinition que vous souhaitez utiliser. Si vous ignorez l’avertissement, le mécanisme d’occultation est utilisé.  
  
 <sup>3</sup> si l’élément d’occultation est inaccessible dans une classe la plus dérivée, l’occultation n’est pas hérité. Par exemple, si vous déclarez l’élément d’occultation comme `Private`, une classe dérivant de votre classe dérivée hérite de l’élément d’origine au lieu de l’élément d’occultation.  
  
## <a name="guidelines"></a>Recommandations  
 Vous utilisez normalement la substitution dans les cas suivants :  
  
- Vous définissez des classes dérivées polymorphes.  
  
- Vous souhaitez que la sécurité du fait que le compilateur d’appliquer le type d’élément identique et de la séquence d’appel.  
  
 Vous utilisez normalement l’occultation dans les cas suivants :  
  
- Vous pensez que votre classe de base peut être modifiée et définir un élément à l’aide du même nom que le vôtre.  
  
- Vous souhaitez que la liberté de modifier le type d’élément ou la séquence d’appel.  
  
## <a name="see-also"></a>Voir aussi

- [Références aux éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Occultation dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
- [Guide pratique pour Masquer une Variable portant le même nom que votre Variable](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-a-variable-with-the-same-name-as-your-variable.md)
- [Guide pratique pour Masquer une Variable héritée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-hide-an-inherited-variable.md)
- [Guide pratique pour Accéder à une Variable masquée par une classe dérivée](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-access-a-variable-hidden-by-a-derived-class.md)
- [Shadows](../../../../visual-basic/language-reference/modifiers/shadows.md)
- [Overrides](../../../../visual-basic/language-reference/modifiers/overrides.md)
