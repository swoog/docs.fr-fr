---
title: 'Procédure : Parcourir une énumération dans Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [Visual Basic], iterating
- enumerations [Visual Basic], iterating
- ListBox control [Windows Forms], populating from an enumeration
ms.assetid: e5aa10eb-cfcd-4a3b-8e76-f06b8f2002be
ms.openlocfilehash: c3fd7e6f7e8e4fcabf279975f7ffc2d848679396
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64645246"
---
# <a name="how-to-iterate-through-an-enumeration-in-visual-basic"></a>Procédure : Parcourir une énumération dans Visual Basic
Les énumérations offrent un moyen pratique de travailler avec des ensembles de constantes connexes et d’associer des valeurs de constantes à des noms. Pour parcourir une énumération, vous pouvez la déplacer dans un tableau à l’aide de la <xref:System.Enum.GetValues%2A> (méthode). Vous pouvez également itérer sur une énumération à l’aide un `For...Each` instruction, à l’aide de la <xref:System.Enum.GetNames%2A> ou <xref:System.Enum.GetValues%2A> méthode pour extraire la valeur de chaîne ou numérique.  
  
### <a name="to-iterate-through-an-enumeration"></a>Pour effectuer une itération dans une énumération  
  
- Déclarez un tableau et convertissez l’énumération avec la <xref:System.Enum.GetValues%2A> méthode avant de passer le tableau en tant que vous aurait de toute autre variable. L’exemple suivant affiche chaque membre de l’énumération <xref:Microsoft.VisualBasic.FirstDayOfWeek> itère l’énumération.  
  
     [!code-vb[VbEnumsTask#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#7)]  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des énumérations](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)
- [Guide pratique pour Déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [Quand utiliser une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
- [Guide pratique pour Déterminer la chaîne associée à une valeur d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [Guide pratique pour Faire référence à un membre d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [Énumérations et qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [Tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
