---
title: 'Procédure : Déterminer la chaîne associée à une valeur d’énumération (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic]
- strings [Visual Basic], enumeration values
- values [Visual Basic], enumeration members
ms.assetid: 9253e7c8-579c-49a2-8f26-392b20ea99eb
ms.openlocfilehash: 4fa04fa621347ae961975bfb636734e6c9df39fc
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906800"
---
# <a name="how-to-determine-the-string-associated-with-an-enumeration-value-visual-basic"></a>Procédure : Déterminer la chaîne associée à une valeur d’énumération (Visual Basic)
Le <xref:System.Enum.GetValues%2A> et <xref:System.Enum.GetNames%2A> méthodes permettent de déterminer les chaînes et les valeurs associées aux membres de l’énumération.  
  
### <a name="to-determine-the-string-associated-with-an-enumeration"></a>Pour déterminer la chaîne associée à une énumération  
  
- Utilisez le <xref:System.Enum.GetNames%2A> méthode pour récupérer les chaînes associées aux membres de l’énumération. Cet exemple déclare une énumération, `flavorEnum`, puis utilise le <xref:System.Enum.GetNames%2A> méthode pour afficher les chaînes associées à chaque membre.  
  
     [!code-vb[VbEnumsTask#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#2)]  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Enum.GetValues%2A>
- <xref:System.Enum.GetNames%2A>
- <xref:System.Enum>
- [Guide pratique pour Déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [Guide pratique pour Faire référence à un membre d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [Énumérations et qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [Guide pratique pour Parcourir une énumération dans Visual Basic](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)
- [Quand utiliser une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
- [Enum (instruction)](../../../../visual-basic/language-reference/statements/enum-statement.md)
