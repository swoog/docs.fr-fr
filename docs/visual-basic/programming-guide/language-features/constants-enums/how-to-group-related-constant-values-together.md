---
title: 'Procédure : Regrouper des valeurs de constante connexes ensemble (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic], constants
- constants [Visual Basic], grouping together
ms.assetid: 09d61da5-c940-4126-a79f-ba93c36653dc
ms.openlocfilehash: a4f74e48cfdd5c0bc0f745d0f32eb39442f5bd83
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906761"
---
# <a name="how-to-group-related-constant-values-together-visual-basic"></a>Procédure : Regrouper des valeurs de constante connexes ensemble (Visual Basic)
Une énumération est la meilleure façon de regrouper des constantes connexes. Vous créez une énumération avec la `Enum` instruction dans la section des déclarations d’une classe ou un module. Pour plus d'informations, voir [Procédure : Déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md).  
  
### <a name="to-group-related-constant-values"></a>Groupe les valeurs de constante connexes  
  
1. Écrivez une déclaration qui inclut un niveau d’accès de code, le `Enum` mot clé et un nom valide. Cet exemple crée la `Private` énumération, `temperatureValues`.  
  
     [!code-vb[VbEnumsTask#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#21)]  
  
2. Définissez les constantes dans l’énumération. Cet exemple crée la `Public` énumération `temperatureValues` et assigne ses valeurs.  
  
     [!code-vb[VbEnumsTask#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#1)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations et qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [Guide pratique pour Faire référence à un membre d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [Quand utiliser une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
- [Vue d’ensemble des constantes](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)
- [Constantes et types de données littérales](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)
- [Constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md)
