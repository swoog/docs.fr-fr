---
title: Module, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- Module
- vb.Module
helpviewer_keywords:
- modules, classes
- modules
- Module statement [Visual Basic]
- modules, declaring
- standard modules
- classes [Visual Basic], vs. modules
- declarations [Visual Basic], modules
ms.assetid: a1243afc-14a5-45df-95d5-51118aeac362
ms.openlocfilehash: 5628224a08fe5f12cf2a81b179c4998001174354
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43876688"
---
# <a name="module-statement"></a>Module, instruction
Déclare le nom d’un module et introduit la définition des variables, propriétés, événements et procédures contenus dans le module.  
  
## <a name="syntax"></a>Syntaxe  
  
```vb 
[ <attributelist> ] [ accessmodifier ]  Module name  
    [ statements ]  
End Module  
```  
  
## <a name="parts"></a>Composants  
 `attributelist`  
 Facultatif. Consultez [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md).  
  
 `accessmodifier`  
 Facultatif. Il peut s'agir d'une des valeurs suivantes :  
  
-   [Public](../../../visual-basic/language-reference/modifiers/public.md)  
  
-   [Friend](../../../visual-basic/language-reference/modifiers/friend.md)  
  
 Consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
 `name`  
 Obligatoire. Nom de ce module. Consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
 `statements`  
 Facultatif. Instructions qui définissent des variables, propriétés, événements, procédures et les types imbriqués de ce module.  
  
 `End Module`  
 Met fin à la `Module` définition.  
  
## <a name="remarks"></a>Notes  
 Un `Module` instruction définit un type de référence disponible tout au long de son espace de noms. Un *module* (parfois appelé un *module standard*) est similaire à une classe, mais avec certaines des différences importantes. Chaque module possède exactement une instance et pas nécessairement être créées ou assignées à une variable. Les modules ne prennent en charge l’héritage ou implémenter des interfaces. Notez qu’un module n’est pas un *type* en ce sens qu’une classe ou structure est — vous ne pouvez pas déclarer un élément de programmation comme ayant le type de données d’un module.  
  
 Vous pouvez utiliser `Module` uniquement au niveau de l’espace de noms. Cela signifie que le *contexte de déclaration* pour un module doit être un fichier source ou un espace de noms et ne peut pas être une classe, structure, module, interface, procédure ou bloc. Vous ne pouvez pas imbriquer un module dans un autre module, ou dans n’importe quel type. Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).  
  
 Un module a la même durée de vie en tant que votre programme. Étant donné que ses membres sont tous `Shared`, ils ont également des durées de vie égales à celle du programme.  
  
 Modules par défaut à [Friend](../../../visual-basic/language-reference/modifiers/friend.md) accès. Vous pouvez ajuster leurs niveaux d’accès avec les modificateurs d’accès. Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
 Tous les membres d’un module sont implicitement `Shared`.  
  
## <a name="classes-and-modules"></a>Classes et les Modules  
 Ces éléments présentent beaucoup de similitudes, mais il existe également des différences importantes.  
  
-   **Terminologie.** Les versions précédentes de Visual Basic reconnaissent deux types de modules : *modules de classe* (fichiers .cls) et *modules standard* (fichiers .bas). La version actuelle appelle ces *classes* et *modules*, respectivement.  
  
-   **Membres partagés.** Vous pouvez contrôler si un membre d’une classe est une connexion partagée ou membre d’instance.  
  
-   **Orientation de l’objet.** Les classes sont orientés objet, mais les modules ne sont pas. Par conséquent, seules les classes peuvent être instanciés en tant qu’objets. Pour plus d’informations, consultez [objets et Classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md).  
  
## <a name="rules"></a>Règles  
  
-   **Modificateurs.** Tous les membres de module sont implicitement [partagé](../../../visual-basic/language-reference/modifiers/shared.md). Vous ne pouvez pas utiliser le `Shared` mot clé lors de la déclaration d’un membre et vous ne pouvez pas modifier l’état partagé d’un membre.  
  
-   **Héritage.** Un module ne peut pas hériter d’un type autre que <xref:System.Object>, à partir de quels tous les modules hériter. En particulier, un module ne peut pas hériter d’un autre.  
  
     Vous ne pouvez pas utiliser le [Inherits Statement](../../../visual-basic/language-reference/statements/inherits-statement.md) dans une définition de module, même pour spécifier <xref:System.Object>.  
  
-   **Propriété par défaut.** Vous ne pouvez pas définir les propriétés par défaut dans un module. Pour plus d’informations, consultez [par défaut](../../../visual-basic/language-reference/modifiers/default.md).  
  
## <a name="behavior"></a>Comportement  
  
-   **Niveau d’accès.** Dans un module, vous pouvez déclarer chaque membre avec son propre niveau d’accès. Membres de module par défaut à [Public](../../../visual-basic/language-reference/modifiers/public.md) accéder, à l’exception des variables et des constantes, qui par défaut à [privé](../../../visual-basic/language-reference/modifiers/private.md) accès. Lorsqu’un module a accès plus limité qu’un de ses membres, le niveau d’accès de module spécifié est prioritaire.  
  
-   **Étendue.** Un module est dans l’étendue tout au long de son espace de noms.  
  
     La portée de chaque membre de module est l’ensemble du module. Notez que tous les membres subissent *promotion de type*, ce qui entraîne leur étendue de la promotion de l’espace de noms contenant le module. Pour plus d’informations, consultez [Promotion de Type](../../../visual-basic/programming-guide/language-features/declared-elements/type-promotion.md).  
  
-   **Qualification.** Vous pouvez avoir plusieurs modules dans un projet, et vous pouvez déclarer des membres portant le même nom dans deux ou plusieurs modules. Toutefois, vous devez qualifier toute référence à ce membre avec le nom de module approprié si la référence est externe à ce module. Pour plus d’informations, consultez [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrStatements#69](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/module-statement_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)  
 [Namespace (instruction)](../../../visual-basic/language-reference/statements/namespace-statement.md)  
 [Structure (instruction)](../../../visual-basic/language-reference/statements/structure-statement.md)  
 [Interface (instruction)](../../../visual-basic/language-reference/statements/interface-statement.md)  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
 [Promotion de type](../../../visual-basic/programming-guide/language-features/declared-elements/type-promotion.md)
