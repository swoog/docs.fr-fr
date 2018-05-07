---
title: 'Comment : regrouper les valeurs de constante connexes (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic], constants
- constants [Visual Basic], grouping together
ms.assetid: 09d61da5-c940-4126-a79f-ba93c36653dc
ms.openlocfilehash: 320373116ad4d61293690353fce6b7b152e79a4f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-group-related-constant-values-together-visual-basic"></a>Comment : regrouper les valeurs de constante connexes (Visual Basic)
Une énumération est le meilleur moyen de regrouper les constantes associées. Vous créez une énumération avec la `Enum` instruction dans la section des déclarations d’une classe ou un module. Pour plus d’informations, consultez [Comment : déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md).  
  
### <a name="to-group-related-constant-values"></a>Groupe les valeurs de constantes connexes  
  
1.  Écrivez une déclaration qui inclut un niveau d’accès de code, le `Enum` (mot clé) et un nom valide. Cet exemple crée la `Private` énumération, `temperatureValues`.  
  
     [!code-vb[VbEnumsTask#21](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-group-related-constant-values-together_1.vb)]  
  
2.  Définissez les constantes dans l’énumération. Cet exemple crée la `Public` énumération `temperatureValues` et assigne ses valeurs.  
  
     [!code-vb[VbEnumsTask#1](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-group-related-constant-values-together_2.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Énumérations et qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)  
 [Guide pratique : faire référence à un membre d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)  
 [Quand utiliser une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)  
 [Vue d’ensemble des constantes](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)  
 [Constantes et types de données littérales](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)  
 [Constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md)
