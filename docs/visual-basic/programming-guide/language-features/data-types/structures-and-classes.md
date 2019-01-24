---
title: Structures et classes (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- classes [Visual Basic], vs. structures
- structures [Visual Basic]
- classes [Visual Basic]
- structures [Visual Basic], compared to classes
- structures [Visual Basic], structure variables
- structure variables [Visual Basic]
ms.assetid: a221e74a-ffcf-4bdc-a0f6-a088a9bf26cc
ms.openlocfilehash: 78c1d529053a10fc208ee5499b759623c227cb25
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54681808"
---
# <a name="structures-and-classes-visual-basic"></a>Structures et classes (Visual Basic)
Visual Basic unifie la syntaxe des structures et des classes, avec le résultat que les deux entités prennent en charge les mêmes fonctionnalités. Toutefois, il existe également des différences importantes entre les classes et structures.  
  
 Classes ont l’avantage d’être des types référence, en passant une référence est plus efficace que le passage d’une variable de structure avec toutes ses données. En revanche, les structures ne nécessitent pas d’allocation de mémoire sur le tas global.  
  
 Car il ne peut pas hériter d’une structure, structures doivent être utilisées uniquement pour les objets qui ne doivent pas être étendu. Structures utilisées lors de l’objet que vous souhaitez créer a une taille de petite instance et prendre en compte les caractéristiques de performances des classes et structures.  
  
## <a name="similarities"></a>Similitudes  
 Les classes et les structures sont similaires aux points suivants :  
  
-   Les deux sont *conteneur* types, ce qui signifie qu’ils contiennent d’autres types en tant que membres.  
  
-   Elles ont des membres, ce qui peuvent inclure des constructeurs, méthodes, propriétés, champs, constantes, énumérations, événements et gestionnaires d’événements. Toutefois, ne confondez pas ces membres avec déclaré *éléments* d’une structure.  
  
-   Les membres des deux peuvent avoir individualisée niveaux d’accès. Par exemple, un membre peut être déclaré `Public` et un autre `Private`.  
  
-   Les deux peuvent implémenter des interfaces.  
  
-   À la fois peuvent avoir des constructeurs partagés, avec ou sans paramètres.  
  
-   Elles peuvent exposer une *propriété par défaut*, à condition que la propriété prend au moins un paramètre.  
  
-   Elles peuvent déclarer et déclencher des événements, et déclarer des délégués.  
  
## <a name="differences"></a>Différences  
 Structures et classes diffèrent dans les indications suivantes :  
  
-   Les structures sont *types valeur*; les classes sont *référencent des types*. Une variable d’un type structure contient les données de la structure, plutôt que contenant une référence aux données comme un type de classe.  
  
-   Les structures utilisent l’allocation de pile ; les classes utilisent l’allocation de tas.  
  
-   Tous les éléments de structure sont `Public` par défaut ; classe variables et constantes sont `Private` par défaut, tandis que d’autres membres de classe sont `Public` par défaut. Ce comportement pour les membres de classe assure la compatibilité avec le système de Visual Basic 6.0 de valeurs par défaut.  
  
-   Une structure doit avoir au moins un non non partagée de variable ou non partagé, élément d’événement ; une classe peut être entièrement vide.  
  
-   Éléments de structure ne peuvent pas être déclarés en tant que `Protected`; les membres de classe peuvent.  
  
-   Une procédure de structure peut gérer des événements uniquement s’il est un [partagé](../../../../visual-basic/language-reference/modifiers/shared.md) `Sub` procédure et uniquement par le biais de la [AddHandler, instruction](../../../../visual-basic/language-reference/statements/addhandler-statement.md); toute procédure de classe peut gérer des événements, en utilisant soit le [ Gère](../../../../visual-basic/language-reference/statements/handles-clause.md) mot clé ou le `AddHandler` instruction. Pour plus d’informations, consultez [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md).  
  
-   Les déclarations de variable de structure ne peut pas spécifier initialiseurs ou tailles initiales des tableaux ; les déclarations de variable de classe peuvent.  
  
-   Les structures héritent implicitement de la <xref:System.ValueType?displayProperty=nameWithType> classe et ne peut pas hériter d’un autre type ; les classes peuvent hériter d’une classe ou les classes autres que <xref:System.ValueType?displayProperty=nameWithType>.  
  
-   Structures ne sont pas héritées ; les classes sont.  
  
-   Structures n’étant jamais arrêtées, le common language runtime (CLR) n’appelle jamais la <xref:System.Object.Finalize%2A> méthode sur une structure ; classes sont terminent par le garbage collector (GC), qui appelle <xref:System.Object.Finalize%2A> sur une classe lorsqu’il détecte il n’existe aucune référence active restantes.  
  
-   Une structure ne nécessite pas un constructeur ; fait d’une classe.  
  
-   Les structures peuvent avoir des constructeurs non partagés uniquement si elles acceptent des paramètres ; classes peuvent avoir les avec ou sans paramètres.  
  
 Chaque structure possède un constructeur public implicit sans paramètres. Ce constructeur initialise les éléments de données de tous les de la structure à leurs valeurs par défaut. Vous ne pouvez pas redéfinir ce comportement.  
  
## <a name="instances-and-variables"></a>Instances et Variables  
 Étant donné que les structures sont des types valeur, chaque variable de structure est définitivement lié à une instance de structure individuelle. Mais les classes sont des types référence, et une variable objet peut faire référence à plusieurs instances de classe à des moments différents. Cette distinction affecte votre utilisation de structures et classes de plusieurs manières :  
  
-   **Initialisation.** Une variable de structure comprend implicitement une initialisation des éléments à l’aide du constructeur sans paramètre de la structure. Par conséquent, `Dim s As struct1` équivaut à `Dim s As struct1 = New struct1()`.  
  
-   **Affectation de Variables.** Lorsque vous assignez une variable de structure à un autre, ou que vous passez une instance de structure à un argument de procédure, les valeurs actuelles de tous les éléments de variable sont copiés vers la nouvelle structure. Lorsque vous assignez une variable d’objet à un autre, ou passez une variable objet à une procédure, seul le pointeur de la référence est copié.  
  
-   **Assignation de Nothing.** Vous pouvez affecter la valeur [rien](../../../../visual-basic/language-reference/nothing.md) vers une structure variable, mais l’instance continue à associer à la variable. Vous pouvez toujours appeler ses méthodes et accéder à ses éléments de données, bien que les éléments de variable sont réinitialisés par l’assignation.  
  
     En revanche, si vous définissez une variable objet `Nothing`, vous les assigniez à partir de n’importe quelle instance de classe, et vous ne pouvez pas accéder à tous les membres via la variable jusqu'à ce que vous lui affectez une autre instance.  
  
-   **Plusieurs Instances.** Une variable objet peut avoir diverses instances de classe qui lui est assignées à des moments différents, et plusieurs variables d’objet peuvent faire référence à la même instance de classe en même temps. Les modifications apportées aux valeurs des membres de classe affectent ces membres lorsque pour accéder à une autre variable pointant vers la même instance.  
  
     Toutefois, les éléments de structure, sont isolés dans leur propre instance. Modifications apportées à leurs valeurs ne sont pas répercutées dans toutes les autres variables de structure, même dans d’autres instances du même `Structure` déclaration.  
  
-   **Égalité.** Tester l’égalité de deux structures doit être effectué sur un élément par élément. Deux variables d’objet peuvent être comparées à l’aide de la <xref:System.Object.Equals%2A> (méthode). <xref:System.Object.Equals%2A> Indique si les deux variables pointent vers la même instance.  
  
## <a name="see-also"></a>Voir aussi
- [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [Types de données composites](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)
- [Value Types and Reference Types](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [Structures](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Dépannage des types de données](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [Structures et autres éléments de programmation](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-other-programming-elements.md)
- [Objets et classes](../../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)
