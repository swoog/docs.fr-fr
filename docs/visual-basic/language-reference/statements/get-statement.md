---
title: Get, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Get
helpviewer_keywords:
- Get statement [Visual Basic], syntax
- Get statement [Visual Basic]
- properties [Visual Basic], read-only
- read-only properties
- Get keyword [Visual Basic]
- property procedures [Visual Basic], Get statements
ms.assetid: 56b05cdc-bd64-4dfd-bb12-824eacec6f94
ms.openlocfilehash: 32b89caf56c010f9e6ed7b78309ef30b56b682ea
ms.sourcegitcommit: 869b5832b667915ac4a5dd8c86b1109ed26b6c08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/28/2018
ms.locfileid: "39332894"
---
# <a name="get-statement"></a>Get, instruction
Déclare un `Get` procédure de propriété utilisée pour récupérer la valeur d’une propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
[ <attributelist> ] [ accessmodifier ] Get()  
    [ statements ]  
End Get  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`attributelist`|Facultatif. Consultez [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md).|  
|`accessmodifier`|Facultatif sur un de la `Get` et `Set` instructions dans cette propriété. Il peut s'agir d'une des valeurs suivantes :<br /><br /> -   [Protégé](../../../visual-basic/language-reference/modifiers/protected.md)<br />-   [Friend](../../../visual-basic/language-reference/modifiers/friend.md)<br />-   [Privé](../../../visual-basic/language-reference/modifiers/private.md)<br />-   `Protected Friend`<br /><br /> Consultez [niveaux en Visual Basic d’accès](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).|  
|`statements`|Facultatif. Une ou plusieurs instructions qui s’exécutent lorsque le `Get` procédure de propriété est appelée.|  
|`End Get`|Obligatoire. Termine la définition de la `Get` procédure de propriété.|  
  
## <a name="remarks"></a>Notes  
 Chaque propriété doit avoir un `Get` procédure de propriété, sauf si la propriété est marquée `WriteOnly`. Le `Get` procédure est utilisée pour retourner la valeur actuelle de la propriété.  
  
 Visual Basic appelle automatiquement d’une propriété `Get` procédure lorsqu’une expression demande la valeur de propriété.  
  
 Le corps de la déclaration de propriété peut contenir uniquement de la propriété `Get` et `Set` procédures entre le [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md) et `End Property` instruction. Il ne peut pas stocker quoi que ce soit d’autre que ces procédures. En particulier, il ne peut pas stocker la valeur actuelle de la propriété. Vous devez stocker cette valeur en dehors de la propriété, car si vous le stockez à l’intérieur d’une des procédures de propriété, les autres procédures de propriété ne peut pas y accéder. L’approche habituelle consiste à stocker la valeur dans un [privé](../../../visual-basic/language-reference/modifiers/private.md) variable déclarée au même niveau que la propriété. Vous devez définir un `Get` procédure à l’intérieur de la propriété à laquelle elle s’applique.  
  
 Le `Get` procédure par défaut est le niveau d’accès de sa propriété conteneur, sauf si vous utilisez `accessmodifier` dans le `Get` instruction.  
  
## <a name="rules"></a>Règles  
  
-   **Niveaux d’accès mixtes.** Si vous définissez une propriété en lecture-écriture, vous pouvez éventuellement spécifier un niveau d’accès différent pour un le `Get` ou `Set` procédure, mais pas les deux. Si vous procédez ainsi, le niveau d’accès de la procédure doit être plus restrictif que le niveau d’accès de la propriété. Par exemple, si la propriété est déclarée `Friend`, vous pouvez déclarer le `Get` procédure `Private`, mais pas `Public`.  
  
     Si vous définissez un `ReadOnly` propriété, le `Get` procédure représente la propriété entière. Vous ne pouvez pas déclarer un accès différents au niveau de `Get`, parce que seront définis à deux niveaux d’accès pour la propriété.  
  
-   **Type de retour.** Le [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md) peut déclarer le type de données de la valeur de retour. Le `Get` procédure retourne automatiquement que le type de données. Vous pouvez spécifier n’importe quel type de données ou le nom d’une énumération, une structure, une classe ou une interface.  
  
     Si le `Property` instruction ne spécifie pas `returntype`, la procédure retourne `Object`.  
  
## <a name="behavior"></a>Comportement  
  
-   **Retour d’une procédure.** Lorsque le `Get` procédure retourne au code appelant, l’exécution se poursuit au sein de l’instruction qui a demandé la valeur de propriété.  
  
     `Get` procédures de propriété peuvent retourner une valeur en utilisant le [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md) ou en attribuant la valeur de retour au nom de propriété. Pour plus d’informations, consultez « Valeur de retour » dans [Function, instruction](../../../visual-basic/language-reference/statements/function-statement.md).  
  
     Le `Exit Property` et `Return` instructions provoquent la sortie immédiate d’une procédure de propriété. Un nombre quelconque de `Exit Property` et `Return` instructions peuvent apparaître n’importe où dans la procédure, et vous pouvez combiner `Exit Property` et `Return` instructions.  
  
-   **Valeur de retour.** Pour retourner une valeur à partir d’un `Get` procédure, vous pouvez affecter la valeur au nom de propriété ou l’inclure dans un [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md). Le `Return` instruction assigne simultanément le `Get` procédure retourner de valeur et termine la procédure.  
  
     Si vous utilisez `Exit Property` sans attribuer une valeur au nom de propriété, le `Get` procédure retourne la valeur par défaut type de la propriété de données. Pour plus d’informations, consultez « Valeur de retour » dans [Function, instruction](../../../visual-basic/language-reference/statements/function-statement.md).  
  
     L’exemple suivant illustre deux façons de la propriété en lecture seule `quoteForTheDay` peut retourner la valeur contenue dans la variable privée `quoteValue`.  
  
     [!code-vb[VbVbalrStatements#27](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/get-statement_1.vb)]  
  
     [!code-vb[VbVbalrStatements#28](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/get-statement_2.vb)]  
  
     [!code-vb[VbVbalrStatements#29](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/get-statement_3.vb)]  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise la `Get` instruction pour retourner la valeur d’une propriété.  
  
 [!code-vb[VbVbalrStatements#30](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/get-statement_4.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Set (instruction)](../../../visual-basic/language-reference/statements/set-statement.md)  
 [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)  
 [Exit (instruction)](../../../visual-basic/language-reference/statements/exit-statement.md)  
 [Objets et classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)  
 [Procédure pas à pas : définition de classes](../../../visual-basic/programming-guide/language-features/objects-and-classes/walkthrough-defining-classes.md)
