---
title: 'Procédure : Déclarer une Structure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- declarations [Visual Basic], structures
- structure statements [Visual Basic]
- statements [Visual Basic], structure
- structures [Visual Basic], declaring
ms.assetid: d5e98381-eb81-47d4-af83-48cc534a2572
ms.openlocfilehash: bfed5c969466cb427e6c94d39bfcc6a6e007c320
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54672043"
---
# <a name="how-to-declare-a-structure-visual-basic"></a>Procédure : Déclarer une Structure (Visual Basic)
Vous commencez une déclaration de structure par le [Structure (instruction)](../../../../visual-basic/language-reference/statements/structure-statement.md), vous vous retrouvez avec la `End` `Structure` instruction. Entre ces deux instructions, vous devez déclarer au moins un *élément*. Les éléments peuvent être de n’importe quel type de données, mais au moins un doit être une variable non partagée ou un événement non partagé.  
  
 Vous ne peut pas initialiser un des éléments de structure dans la déclaration de structure. Lorsque vous déclarez une variable comme étant d’un type structure, vous attribuez des valeurs aux éléments en y accédant via la variable.  
  
 Pour une explication des différences entre les classes et structures, consultez [Structures et Classes](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md).  
  
 À des fins de démonstration, considérez une situation où vous souhaitez effectuer le suivi de nom d’un employé, numéro de poste et salaire. Une structure vous permet de procéder dans une variable unique.  
  
### <a name="to-declare-a-structure"></a>Pour déclarer une structure  
  
1.  Créer le début et fin des instructions pour la structure.  
  
     Vous pouvez spécifier le niveau d’accès d’une structure en utilisant le [Public](../../../../visual-basic/language-reference/modifiers/public.md), [protégé](../../../../visual-basic/language-reference/modifiers/protected.md), [Friend](../../../../visual-basic/language-reference/modifiers/friend.md), ou [privé](../../../../visual-basic/language-reference/modifiers/private.md) mot clé, ou vous pouvez la laisser la valeur par défaut `Public`.  
  
    ```  
    Private Structure employee  
    End Structure  
    ```  
  
2.  Ajouter des éléments au corps de la structure.  
  
     Une structure doit avoir au moins un élément. Vous devez déclarer chaque élément et lui attribuer un niveau d’accès. Si vous utilisez le [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) sans les mots clés, l’accessibilité par défaut est `Public`.  
  
    ```  
    Private Structure employee  
        Public givenName As String  
        Public familyName As String  
        Public phoneExtension As Long  
        Private salary As Decimal  
        Public Sub giveRaise(raise As Double)  
            salary *= raise  
        End Sub  
        Public Event salaryReviewTime()  
    End Structure  
    ```  
  
     Le `salary` champ dans l’exemple précédent est `Private`, ce qui signifie qu’il n’est pas accessible en dehors de la structure, même à partir de la classe conteneur. Toutefois, le `giveRaise` procédure est `Public`, donc elle peut être appelée à partir de l’extérieur de la structure. De même, vous pouvez déclencher la `salaryReviewTime` événement en dehors de la structure de.  
  
     En plus des variables, `Sub` procédures et événements, vous pouvez également définir des constantes, `Function` procédures et des propriétés dans une structure. Vous pouvez désigner au plus une propriété comme le *propriété par défaut*, à condition qu’elle accepte au moins un argument. Vous pouvez gérer un événement avec un [partagé](../../../../visual-basic/language-reference/modifiers/shared.md) `Sub` procédure. Pour plus d'informations, voir [Procédure : Déclarer et appeler une propriété par défaut en Visual Basic](../../../../visual-basic/programming-guide/language-features/procedures/how-to-declare-and-call-a-default-property.md).  
  
## <a name="see-also"></a>Voir aussi
- [Types de données](../../../../visual-basic/programming-guide/language-features/data-types/index.md)
- [Types de données élémentaires](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)
- [Types de données composites](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)
- [Value Types and Reference Types](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)
- [Structures](../../../../visual-basic/programming-guide/language-features/data-types/structures.md)
- [Dépannage des types de données](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [Variables de structure](../../../../visual-basic/programming-guide/language-features/data-types/structure-variables.md)
- [Structures et autres éléments de programmation](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-other-programming-elements.md)
- [Structures et classes](../../../../visual-basic/programming-guide/language-features/data-types/structures-and-classes.md)
- [Type de données défini par l’utilisateur](../../../../visual-basic/language-reference/data-types/user-defined-data-type.md)
