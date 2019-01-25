---
title: Énumérations et qualification de noms (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- declarations [Visual Basic], enumerations
- Imports statement [Visual Basic], namespace declarations
- declaring namespaces [Visual Basic], enumerations
- name collisions
- ambiguous names [Visual Basic], enumerations
- enumerations [Visual Basic], name qualification
- names [Visual Basic], avoiding conflicts
- namespaces [Visual Basic], declaring
- naming conflicts, enumerations
- naming conflicts, qualifying names
- declaring enumerations
- references [Visual Basic], enumeration members
- naming conventions [Visual Basic], naming conflicts
- declarations [Visual Basic], namespaces
ms.assetid: 08ba2738-df52-4140-bc55-f57c871c9b73
ms.openlocfilehash: 0336ac54c6a0dadeb9758bcb15477fe96dbfcc65
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513696"
---
# <a name="enumerations-and-name-qualification-visual-basic"></a>Énumérations et qualification de noms (Visual Basic)
Normalement, lorsque vous faites référence à un membre d’une énumération, vous devez qualifier le nom du membre avec le nom de l’énumération. Par exemple, pour faire référence à la `Sunday` membre de votre `Days` énumération, vous utiliseriez la syntaxe suivante :  
  
 [!code-vb[VbEnumsTask#18](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/enumerations-and-name-qualification_1.vb)]  
  
## <a name="using-the-imports-statement"></a>À l’aide de l’instruction Imports  
 Vous pouvez éviter d’utiliser des noms qualifiés complets en ajoutant un `Imports` instruction à la section de déclarations d’espace de noms de votre code, comme dans l’exemple suivant :  
  
 [!code-vb[VbEnumsTask#22](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/enumerations-and-name-qualification_2.vb)]  
  
 Un `Imports` instruction importe des noms d’espace de noms de projets référencés et d’assemblys et depuis le même projet que le module dans lequel apparaît l’instruction. Une fois que cette instruction est ajoutée, vous pouvez faire référence aux membres de l’énumération sans qualification, comme dans l’exemple suivant :  
  
 [!code-vb[VbEnumsTask#24](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/enumerations-and-name-qualification_3.vb)]  
  
 En organisant des ensembles de constantes connexes dans les énumérations, vous pouvez utiliser les mêmes noms de constantes dans des contextes différents. Par exemple, vous pouvez utiliser les mêmes noms pour les constantes de jour de la semaine dans le `Days` et `WorkDays` énumérations. Si vous utilisez la `Imports` instruction avec vos énumérations, vous devez être prudent afin d’éviter les références ambiguës. Prenons l'exemple suivant :  
  
 [!code-vb[VbEnumsTask#22](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/enumerations-and-name-qualification_2.vb)]  
  
 [!code-vb[VbEnumsTask#25](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/enumerations-and-name-qualification_4.vb)]  
  
 En supposant que `Monday` est membre des groupes le `Days` énumération et la `Workdays` énumération, ce code génère une erreur du compilateur. Pour éviter les références ambiguës lorsque vous faites référence à une constante individuelle, qualifiez le nom de constante par son énumération. Le code suivant fait référence à la `Saturday` constantes dans le `Days` et `WorkDays` énumérations.  
  
 [!code-vb[VbEnumsTask#32](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/enumerations-and-name-qualification_5.vb)]  
  
## <a name="see-also"></a>Voir aussi
- [Constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md)
- [Guide pratique pour Déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [Guide pratique pour Faire référence à un membre d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [Guide pratique pour Parcourir une énumération dans Visual Basic](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)
- [Guide pratique pour Déterminer la chaîne associée à une valeur d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [Quand utiliser une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
- [Constantes et types de données littérales](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)
- [Enum (instruction)](../../../../visual-basic/language-reference/statements/enum-statement.md)
- [Imports (instruction) (espace de noms et type .NET)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md)
- [Types de données](../../../../visual-basic/language-reference/data-types/index.md)
