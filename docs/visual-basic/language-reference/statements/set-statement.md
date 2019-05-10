---
title: Set, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Set
helpviewer_keywords:
- property procedures [Visual Basic], Set statements
- Set statement [Visual Basic]
- Set statement [Visual Basic], syntax
- write-only properties
- properties [Visual Basic], write-only
ms.assetid: 9ecc27b4-df84-420d-9075-db25455fb3cd
ms.openlocfilehash: fb51dfbae4d9c4ef205e67ac15c5027e62a9a938
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64663194"
---
# <a name="set-statement-visual-basic"></a>Set, instruction (Visual Basic)
Déclare un `Set` procédure de propriété utilisée pour affecter une valeur à une propriété.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
[ <attributelist> ] [ accessmodifier ] Set (ByVal value [ As datatype ])  
    [ statements ]  
End Set  
```  
  
## <a name="parts"></a>Composants  
 `attributelist`  
 Facultatif. Consultez [liste d’attributs](../../../visual-basic/language-reference/statements/attribute-list.md).  
  
 `accessmodifier`  
 Facultatif sur un de la `Get` et `Set` instructions dans cette propriété. Il peut s'agir d'une des valeurs suivantes :  
  
- [Protected](../../../visual-basic/language-reference/modifiers/protected.md)  
  
- [Friend](../../../visual-basic/language-reference/modifiers/friend.md)  
  
- [Private](../../../visual-basic/language-reference/modifiers/private.md)  
  
- `Protected Friend`  
  
 Consultez [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).  
  
 `value`  
 Obligatoire. Paramètre qui contient la nouvelle valeur pour la propriété.  
  
 `datatype`  
 Obligatoire si `Option Strict` est `On`. Type de données de la `value` paramètre. Le type de données spécifié doit être le même que le type de données de la propriété où cette `Set` instruction est déclarée.  
  
 `statements`  
 Facultatif. Une ou plusieurs instructions qui s’exécutent lorsque le `Set` procédure de propriété est appelée.  
  
 `End Set`  
 Obligatoire. Termine la définition de la `Set` procédure de propriété.  
  
## <a name="remarks"></a>Notes  
 Chaque propriété doit avoir un `Set` procédure de propriété, sauf si la propriété est marquée `ReadOnly`. Le `Set` procédure est utilisée pour définir la valeur de la propriété.  
  
 Visual Basic appelle automatiquement d’une propriété `Set` procédure lors d’une instruction d’assignation fournit une valeur à stocker dans la propriété.  
  
 Visual Basic passe un paramètre à la `Set` procédure pendant les assignations de propriété. Si vous ne fournissez pas un paramètre pour `Set`, l’environnement de développement intégré (IDE) utilise un paramètre implicit nommé `value`. Le paramètre conserve la valeur à assigner à la propriété. Vous en général de stocker cette valeur dans une variable locale privée et renvoyez-le à chaque fois que le `Get` procédure est appelée.  
  
 Le corps de la déclaration de propriété peut contenir uniquement de la propriété `Get` et `Set` procédures entre le [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md) et `End Property` instruction. Il ne peut pas stocker quoi que ce soit d’autre que ces procédures. En particulier, il ne peut pas stocker la valeur actuelle de la propriété. Vous devez stocker cette valeur en dehors de la propriété, car si vous le stockez à l’intérieur d’une des procédures de propriété, les autres procédures de propriété ne peut pas y accéder. L’approche habituelle consiste à stocker la valeur dans un [privé](../../../visual-basic/language-reference/modifiers/private.md) variable déclarée au même niveau que la propriété. Vous devez définir un `Set` procédure à l’intérieur de la propriété à laquelle elle s’applique.  
  
 Le `Set` procédure par défaut est le niveau d’accès de sa propriété conteneur, sauf si vous utilisez `accessmodifier` dans le `Set` instruction.  
  
## <a name="rules"></a>Règles  
  
- **Niveaux d’accès mixtes.** Si vous définissez une propriété en lecture-écriture, vous pouvez éventuellement spécifier un niveau d’accès différent pour un le `Get` ou `Set` procédure, mais pas les deux. Si vous procédez ainsi, le niveau d’accès de la procédure doit être plus restrictif que le niveau d’accès de la propriété. Par exemple, si la propriété est déclarée `Friend`, vous pouvez déclarer le `Set` procédure `Private`, mais pas `Public`.  
  
     Si vous définissez un `WriteOnly` propriété, le `Set` procédure représente la propriété entière. Vous ne pouvez pas déclarer un accès différents au niveau de `Set`, parce que seront définis à deux niveaux d’accès pour la propriété.  
  
## <a name="behavior"></a>Comportement  
  
- **Retour d’une procédure de propriété.** Lorsque le `Set` procédure retourne au code appelant, l’exécution se poursuit après l’instruction qui a fourni la valeur à stocker.  
  
     `Set` procédures de propriété peuvent retourner à l’aide du [instruction Return](../../../visual-basic/language-reference/statements/return-statement.md) ou [Exit Statement](../../../visual-basic/language-reference/statements/exit-statement.md).  
  
     Le `Exit Property` et `Return` instructions provoquent la sortie immédiate d’une procédure de propriété. Un nombre quelconque de `Exit Property` et `Return` instructions peuvent apparaître n’importe où dans la procédure, et vous pouvez combiner `Exit Property` et `Return` instructions.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise la `Set` instruction pour définir la valeur d’une propriété.  
  
 [!code-vb[VbVbalrStatements#55](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#55)]  
  
## <a name="see-also"></a>Voir aussi

- [Get (instruction)](../../../visual-basic/language-reference/statements/get-statement.md)
- [Property (instruction)](../../../visual-basic/language-reference/statements/property-statement.md)
- [Sub (instruction)](../../../visual-basic/language-reference/statements/sub-statement.md)
- [Procédures de propriété](../../../visual-basic/programming-guide/language-features/procedures/property-procedures.md)
