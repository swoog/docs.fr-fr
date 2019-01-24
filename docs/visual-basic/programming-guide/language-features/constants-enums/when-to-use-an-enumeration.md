---
title: Quand utiliser une énumération (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- enumerations [Visual Basic]
ms.assetid: e6e47b5b-3ed9-452d-a481-9c3fed88519a
ms.openlocfilehash: 826f8fffedb8c983423fbef0fbf1f4014d93be91
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54535019"
---
# <a name="when-to-use-an-enumeration-visual-basic"></a>Quand utiliser une énumération (Visual Basic)
Les énumérations offrent un moyen simple de travailler avec des ensembles de constantes connexes. Une énumération, ou `Enum`, est un nom symbolique pour un ensemble de valeurs. Énumérations sont traitées comme des types de données, et vous pouvez les utiliser pour créer des ensembles de constantes pour une utilisation avec des variables et propriétés.  
  
## <a name="when-to-use-an-enumeration"></a>Quand utiliser une énumération  
 Chaque fois qu’une procédure accepte un ensemble limité de variables, envisagez d’utiliser une énumération. Énumérations rendent le code plus clair et plus lisible, particulièrement lorsque des noms explicites sont utilisés.  
  
 Avantages de l’utilisation des énumérations :  
  
-   Réduit les erreurs provoquées par transposant ou entrée incorrecte de nombres.  
  
-   Rend plus facile de modifier les valeurs à l’avenir.  
  
-   Rend le code plus facile à lire, ce qui signifie qu’il est moins probable que les erreurs lisibilité dedans.  
  
-   Garantit la compatibilité ascendante. Avec des énumérations, votre code est moins susceptible d’échouer si à l’avenir quelqu'un modifie les valeurs correspondant aux noms de membre.  
  
## <a name="naming-enumerations"></a>Énumérations d’affectation de noms  
 Utiliser une convention d’affectation de noms pour les membres de l’énumération. Lorsque Visual Basic rencontre un nom de membre d’énumération, une exception peut être levée si d’autres bibliothèques de types référencées contiennent le même nom. Utilisez un préfixe unique qui identifie les valeurs à partir de votre application ou composant.  
  
 Lorsque vous faites référence à un membre d’une énumération, vous devez qualifier le nom de membre avec le nom de l’énumération ou bien utiliser la `Imports` instruction. Pour plus d’informations, consultez [énumérations et Qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).  
  
## <a name="predefined-enumerations"></a>Énumérations prédéfinies  
 Visual Basic fournit plusieurs énumérations prédéfinies, telles que `FirstDayOfWeek` et `MsgBoxResult`, afin de faciliter votre code. Pour obtenir la liste de ces consultez [constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md).  
  
## <a name="see-also"></a>Voir aussi
- [Guide pratique pour Déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [Guide pratique pour Faire référence à un membre d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [Énumérations et qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [Guide pratique pour Parcourir une énumération dans Visual Basic](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)
- [Guide pratique pour Déterminer la chaîne associée à une valeur d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [Enum (instruction)](../../../../visual-basic/language-reference/statements/enum-statement.md)
- [Constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md)
