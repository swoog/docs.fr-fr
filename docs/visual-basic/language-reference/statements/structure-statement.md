---
title: Structure, instruction (Visual Basic)
ms.date: 05/12/2018
f1_keywords:
- vb.Structure
- Structure
helpviewer_keywords:
- user-defined types [Visual Basic], Structure statement
- compound data types [Visual Basic]
- Structure keyword [Visual Basic]
- Structure statement [Visual Basic]
- UDT (user-defined types)
- types [Visual Basic], user-defined
ms.assetid: 9bd1deea-2a89-4cdc-812c-6dcbb947c391
ms.openlocfilehash: 9377d889f56049720ab10439582300913f5cbb37
ms.sourcegitcommit: ea00c05e0995dae928d48ead99ddab6296097b4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2018
ms.locfileid: "48028398"
---
# <a name="structure-statement"></a>Structure, instruction
Déclare le nom d’une structure et introduit la définition des variables, des propriétés, des événements et des procédures qui comprend la structure.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
[ <attributelist> ] [ accessmodifier ] [ Shadows ] [ Partial ] _  
Structure name [ ( Of typelist ) ]  
    [ Implements interfacenames ]  
    [ datamemberdeclarations ]  
    [ methodmemberdeclarations ]  
End Structure  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`attributelist`|Facultatif. Consultez [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md).|  
|`accessmodifier`|Facultatif. Il peut s'agir d'une des valeurs suivantes :<br /><br /> -   [Public](../../../visual-basic/language-reference/modifiers/public.md)<br />-   [Protégé](../../../visual-basic/language-reference/modifiers/protected.md)<br />-   [Friend](../../../visual-basic/language-reference/modifiers/friend.md)<br />-   [Privé](../../../visual-basic/language-reference/modifiers/private.md)<br />- [Protected Friend](../../language-reference/modifiers/protected-friend.md)<br/>- [Private protégé](../../language-reference/modifiers/private-protected.md) <br /><br /> Consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).|  
|`Shadows`|Facultatif. Consultez [Shadows](../../../visual-basic/language-reference/modifiers/shadows.md).|  
|`Partial`|Facultatif. Indique une définition partielle de la structure. Consultez [partielle](../../../visual-basic/language-reference/modifiers/partial.md).|  
|`name`|Obligatoire. Nom de cette structure. Consultez [noms d’éléments déclarés](../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).|  
|`Of`|Facultatif. Spécifie qu’il s’agit d’une structure générique.|  
|`typelist`|Requis si vous utilisez le [de](../../../visual-basic/language-reference/statements/of-clause.md) mot clé. Liste de paramètres de type pour cette structure. Consultez [tapez liste](../../../visual-basic/language-reference/statements/type-list.md).|  
|`Implements`|Facultatif. Indique que cette structure implémente les membres d’une ou plusieurs interfaces. Consultez [implémente instruction](../../../visual-basic/language-reference/statements/implements-statement.md).|  
|`interfacenames`|Requis si vous utilisez la `Implements` instruction. Les noms des interfaces que cette structure implémente.|  
|`datamemberdeclarations`|Obligatoire. Zéro ou plusieurs `Const`, `Dim`, `Enum`, ou `Event` instructions déclaration *membres de données* de la structure.|  
|`methodmemberdeclarations`|Facultatif. Zéro ou plusieurs déclarations de `Function`, `Operator`, `Property`, ou `Sub` procédures, qui sont utilisées comme *membres de la méthode* de la structure.|  
|`End Structure`|Obligatoire. Met fin à la `Structure` définition.|  
  
## <a name="remarks"></a>Notes  
 La `Structure` instruction définit un type valeur composite que vous pouvez personnaliser. Un *structure* est une généralisation du type défini par l’utilisateur (UDT) des versions antérieures de Visual Basic. Pour plus d’informations, consultez [Structures](../../../visual-basic/programming-guide/language-features/data-types/structures.md).  
  
 Structures prennent en charge la plupart des fonctionnalités mêmes en tant que classes. Par exemple, les structures peuvent avoir des propriétés et des procédures, implémenter des interfaces et ont des constructeurs paramétrés. Toutefois, il existe des différences significatives entre les classes et structures dans des domaines tels que l’héritage, les déclarations et l’utilisation. En outre, les classes sont des types référence et les structures sont des types valeur. Pour plus d’informations, consultez [Structures et Classes](../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md).  
  
 Vous pouvez utiliser `Structure` uniquement au niveau de l’espace de noms ou module. Cela signifie que le *contexte de déclaration* pour une structure doit être un fichier source, espace de noms, classe, structure, module ou interface et ne peut pas être une procédure ou un bloc. Pour plus d’informations, consultez [Contextes de déclaration et niveaux d’accès par défaut](../../../visual-basic/language-reference/statements/declaration-contexts-and-default-access-levels.md).  
  
 Structures de valeur par défaut [Friend](../../../visual-basic/language-reference/modifiers/friend.md) accès. Vous pouvez ajuster leurs niveaux d’accès avec les modificateurs d’accès. Pour plus d’informations, consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
## <a name="rules"></a>Règles  
  
-   **Imbrication.** Vous pouvez définir une structure dans une autre. La structure externe est appelée le *contenant la structure*, et la structure interne est appelée un *imbriquée de structure*. Toutefois, vous ne pouvez pas accéder les membres d’une structure imbriquée via la structure contenante. Au lieu de cela, vous devez déclarer une variable de type de données de la structure imbriquée.  
  
-   **Déclaration de membre.** Vous devez déclarer chaque membre d’une structure. Un membre de structure ne peut pas être [protégé](../../../visual-basic/language-reference/modifiers/protected.md) ou `Protected Friend` , car rien ne peut hériter d’une structure. La structure elle-même, toutefois, peut être `Protected` ou `Protected Friend`.  
  
     Vous pouvez déclarer zéro ou plusieurs variables non partagées ou non partagées, non personnalisés des événements dans une structure. Vous ne pouvez avoir uniquement des constantes, des propriétés et des procédures, même si certains d'entre eux sont non partagées.  
  
-   **Initialisation.** Vous ne pouvez pas initialiser la valeur de n’importe quel membre de données non partagée d’une structure dans le cadre de sa déclaration. Vous devez initialiser ce membre de données au moyen d’un constructeur paramétrable sur la structure, ou assigner une valeur au membre après avoir créé une instance de la structure.  
  
-   **Héritage.** Une structure ne peut pas hériter d’un type autre que <xref:System.ValueType>, à partir de laquelle toutes les structures héritent. En particulier, une structure ne peut pas hériter d’un autre.  
  
     Vous ne pouvez pas utiliser le [Inherits Statement](../../../visual-basic/language-reference/statements/inherits-statement.md) dans une définition de structure, même pour spécifier <xref:System.ValueType>.  
  
-   **Mise en œuvre.** Si la structure utilise la [Implements, instruction](../../../visual-basic/language-reference/statements/implements-statement.md), vous devez implémenter chaque membre défini par chaque interface que vous spécifiez dans `interfacenames`.  
  
-   **Propriété par défaut.** Une structure peut spécifier au plus une propriété en tant que son *propriété par défaut*, en utilisant le [par défaut](../../../visual-basic/language-reference/modifiers/default.md) modificateur. Pour plus d’informations, consultez [par défaut](../../../visual-basic/language-reference/modifiers/default.md).  
  
## <a name="behavior"></a>Comportement  
  
-   **Niveau d’accès.** Dans une structure, vous pouvez déclarer chaque membre avec son propre niveau d’accès. Tous les membres de structure par défaut à [Public](../../../visual-basic/language-reference/modifiers/public.md) accès. Notez que si la structure elle-même a un niveau d’accès plus restreint, cela limite automatiquement l’accès à ses membres, même si vous modifiez leurs niveaux d’accès avec les modificateurs d’accès.  
  
-   **Étendue.** Une structure est dans l’étendue tout au long de son espace de noms, classe, structure ou module conteneur.  
  
     La portée de chaque membre de structure est la structure entière.  
  
-   **Durée de vie.** Une structure ne pas lui-même a une durée de vie. Au lieu de cela, chaque instance de cette structure a une durée de vie indépendante de toutes les autres instances.  
  
     La durée de vie d’une instance commence lorsqu’elle est créée par un [nouvel opérateur](../../../visual-basic/language-reference/operators/new-operator.md) clause. Elle se termine lorsque la durée de vie de la variable qui contient elle se termine.  
  
     Vous ne pouvez pas étendre la durée de vie d’une instance de la structure. Une approximation aux fonctionnalités de la structure statique est fournie par un module. Pour plus d’informations, consultez [instruction Module](../../../visual-basic/language-reference/statements/module-statement.md).  
  
     Les membres de structure ont des durées de vie en fonction de comment et où ils sont déclarés. Pour plus d’informations, consultez « Durée de vie » dans [Class, instruction](../../../visual-basic/language-reference/statements/class-statement.md).  
  
-   **Qualification.** Le code en dehors d’une structure doit qualifier le nom d’un membre avec le nom de cette structure.  
  
     Si le code à l’intérieur d’une structure imbriquée établit une référence non qualifiée à un élément de programmation, Visual Basic commence ses recherches pour l’élément dans la structure imbriquée, puis dans sa structure de conteneur, et ainsi de suite à l’élément conteneur extérieur. Pour plus d’informations, consultez [References to Declared Elements](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).  
  
-   **Consommation de mémoire.** Comme avec tous les types de données composites, vous ne peut pas calculer en toute sécurité la consommation totale de la mémoire d’une structure en additionnant les allocations de stockage nominal de ses membres. En outre, vous ne pouvez pas raisonnablement supposer que l’ordre de stockage en mémoire est identique à l’ordre de déclaration. Si vous avez besoin contrôler la disposition de stockage d’une structure, vous pouvez appliquer le <xref:System.Runtime.InteropServices.StructLayoutAttribute> attribut le `Structure` instruction.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise la `Structure` instruction pour définir un jeu de données associées pour un employé. Il illustre l’utilisation de `Public`, `Friend`, et `Private` membres pour refléter la sensibilité des éléments de données. Il montre également la procédure, propriétés et événements membres.  
  
 [!code-vb[VbVbalrStatements#57](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/structure-statement_1.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Class (instruction)](../../../visual-basic/language-reference/statements/class-statement.md)  
 [Interface (instruction)](../../../visual-basic/language-reference/statements/interface-statement.md)  
 [Module (instruction)](../../../visual-basic/language-reference/statements/module-statement.md)  
 [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)  
 [Const (instruction)](../../../visual-basic/language-reference/statements/const-statement.md)  
 [Enum (instruction)](../../../visual-basic/language-reference/statements/enum-statement.md)  
 [Event (instruction)](../../../visual-basic/language-reference/statements/event-statement.md)  
 [Operator (instruction)](../../../visual-basic/language-reference/statements/operator-statement.md)  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
 [Structures et classes](../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md)
