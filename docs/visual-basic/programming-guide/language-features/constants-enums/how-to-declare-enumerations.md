---
title: 'Procédure : Déclarer des énumérations (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- declarations [Visual Basic], enumerations
- enumerations [Visual Basic], declaring
- declaring enumerations [Visual Basic]
ms.assetid: db4ca1c3-f429-4c81-ae81-29e0157b29fd
ms.openlocfilehash: 1e6ec63688899533b64a6fc5215f77019b64b49c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58830160"
---
# <a name="how-to-declare-enumerations-visual-basic"></a>Procédure : Déclarer des énumérations (Visual Basic)
Vous créez une énumération avec la `Enum` instruction dans la section des déclarations d’une classe ou un module. Vous ne pouvez pas déclarer une énumération au sein d’une méthode. Pour spécifier le niveau d’accès approprié, utilisez `Private`, `Protected`, `Friend`, ou `Public`.  
  
 Un `Enum` type a un nom, un type sous-jacent et un ensemble de champs, chacun représentant une constante. Le nom doit être un qualificateur de Visual Basic .NET valid. Le type sous-jacent doit être un des types d’entiers :`Byte`, `Short`, `Long` ou `Integer`. `Integer` est la valeur par défaut. Énumérations sont toujours fortement typées et ne sont pas interchangeables avec les types de nombre entier.  
  
 Les énumérations ne peuvent pas avoir de valeurs à virgule flottante. Si une énumération est affectée une valeur à virgule flottante avec `Option Strict On`, résulte d’une erreur du compilateur. Si `Option Strict` est `Off`, la valeur est automatiquement convertie en la `Enum` type.  
  
 Pour plus d’informations sur les noms et comment utiliser le `Imports` instruction pour rendre la qualification de noms inutiles, consultez [énumérations et Qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).  
  
### <a name="to-declare-an-enumeration"></a>Pour déclarer une énumération  
  
1.  Écrivez une déclaration qui inclut un niveau d’accès de code, le `Enum` mot clé et un nom valide, comme dans les exemples suivants, chacun d’eux déclare une autre `Enum`.  
  
     [!code-vb[VbEnumsTask#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#3)]  
  
2.  Définissez les constantes dans l’énumération. Par défaut, la première constante d’énumération est initialisée à `0`, et les constantes suivantes sont initialisées à une valeur de plus que la constante précédente. Par exemple, l’énumération suivante, `Days`, contient une constante nommée `Sunday` avec la valeur `0`, une constante nommée `Monday` avec la valeur `1`, une constante nommée `Tuesday` avec la valeur de `2`, et ainsi de suite.  
  
     [!code-vb[VbEnumsTask#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#4)]  
  
3.  Vous pouvez affecter explicitement des valeurs à des constantes dans une énumération à l’aide d’une instruction d’assignation. Vous pouvez affecter une valeur entière, y compris les nombres négatifs. Par exemple, vous souhaiterez peut-être constantes avec des valeurs inférieures à zéro pour représenter des conditions d’erreur. Dans l’énumération suivante, la constante `Invalid` est explicitement affectée la valeur `–1`et la constante `Sunday` reçoit la valeur `0`. Car il s’agit de la première constante dans l’énumération, `Saturday` est également initialisée à la valeur `0`. La valeur de `Monday` est `1` (plus la valeur d’un `Sunday`) ; la valeur de `Tuesday` est `2`, et ainsi de suite.  
  
     [!code-vb[VbEnumsTask#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#5)]  
  
### <a name="to-declare-an-enumeration-as-an-explicit-type"></a>Pour déclarer une énumération comme un type explicite  
  
-   Spécifiez le type de l’énumération à l’aide de la `As` clause, comme indiqué dans l’exemple suivant.  
  
     [!code-vb[VbEnumsTask#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#6)]  
  
## <a name="see-also"></a>Voir aussi

- [Énumérations et qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [Guide pratique pour Faire référence à un membre d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-refer-to-an-enumeration-member.md)
- [Guide pratique pour Parcourir une énumération dans Visual Basic](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)
- [Guide pratique pour Déterminer la chaîne associée à une valeur d’énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [Quand utiliser une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
- [Vue d’ensemble des constantes](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)
- [Constantes et types de données littérales](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)
- [Constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md)
