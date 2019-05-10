---
title: 'Procédure : Déclarer une constante (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- vb.constant
helpviewer_keywords:
- Integer data type [Visual Basic], declaring constants
- Single data type [Visual Basic], declaring constants
- Const statement [Visual Basic], declaring constants
- procedures [Visual Basic], declaration
- data types [Visual Basic], constants
- Long data type [Visual Basic], declaring constants
- Visual Basic code, declaring variables and constants
- Double data type [Visual Basic], declaring constants
- Boolean data type [Visual Basic], declaring constants
- modules, declaring constants
- Byte data type [Visual Basic], declaring constants
- constants [Visual Basic], declaring
- Date data type [Visual Basic], declaring constants
- String data type [Visual Basic], declaring constants
- declaring constants [Visual Basic], const keyword
- Currency data type [Visual Basic], declaring constants and variants
- module-level constants and variables
- Object data type [Visual Basic], declaring constants
ms.assetid: f901b4fa-481f-4621-822e-427060577ad1
ms.openlocfilehash: b84afe4e354d4029bc61ba67bc93bd36a3430de4
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64610598"
---
# <a name="how-to-declare-a-constant-visual-basic"></a>Procédure : Déclarer une constante (Visual Basic)
Vous utilisez la `Const` instruction pour déclarer une constante et définir sa valeur. En déclarant une constante, vous affectez un nom explicite à une valeur. Une fois qu’une constante est déclarée, il ne peut pas être modifié ou attribuer une nouvelle valeur.  
  
 Vous déclarez une constante dans une procédure ou dans la section Déclarations d’un module, une classe ou une structure. Classe ou des constantes au niveau de la structure sont `Private` par défaut, mais peuvent également être déclarées comme `Public`, `Friend`, `Protected`, ou `Protected Friend` pour le niveau d’accès au code approprié.  
  
 La constante doit avoir un nom symbolique valide (les règles sont les mêmes que celles permettant de créer des noms de variables) et une expression composée de numérique ou chaîne constantes et opérateurs (mais aucun appel de fonction).  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-declare-a-constant"></a>Pour déclarer une constante  
  
- Écrivez une déclaration qui inclut un spécificateur d’accès, le `Const` mot clé et une expression, comme dans les exemples suivants :  
  
     [!code-vb[VbEnumsTask#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#8)]  
  
     Lorsque [Option Infer](../../../../visual-basic/language-reference/statements/option-infer-statement.md) est `Off` et [Option Strict](../../../../visual-basic/language-reference/statements/option-strict-statement.md) est `On`, vous devez déclarer explicitement une constante en spécifiant un type de données (`Boolean`, `Byte`, `Char`, `DateTime`, `Decimal`, `Double`, `Integer`, `Long`, `Short`, `Single`, ou `String`).  
  
     Lorsque `Option Infer` est `On` ou `Option Strict` est `Off`, vous pouvez déclarer une constante sans spécifier un type de données avec un `As` clause. Le compilateur détermine le type de la constante à partir du type de l’expression. Pour plus d’informations, consultez [constante et les Types de données littérales](constant-and-literal-data-types.md).  
  
### <a name="to-declare-a-constant-that-has-an-explicitly-stated-data-type"></a>Pour déclarer une constante qui a un type de données indiqué explicitement  
  
- Écrivez une déclaration qui inclut le `As` mot clé et une explicites type de données, comme dans les exemples suivants :  
  
     [!code-vb[VbEnumsTask#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#9)]  
  
     Vous pouvez déclarer plusieurs constantes sur une seule ligne, bien que votre code est plus lisible si vous ne déclarez qu’une seule constante par ligne. Si vous déclarez plusieurs constantes sur une seule ligne, ils doivent tous avoir le même niveau d’accès (`Public`, `Private`, `Friend`, `Protected`, ou `Protected Friend`).  
  
### <a name="to-declare-multiple-constants-on-a-single-line"></a>Pour déclarer plusieurs constantes sur une seule ligne  
  
- Séparez les déclarations par une virgule et un espace, comme dans l’exemple suivant :  
  
    ```  
    Public Const Four As Integer = 4, Five As Integer = 5, Six As Integer = 44  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Const (instruction)](../../../../visual-basic/language-reference/statements/const-statement.md)
- [Constantes et types de données littérales](constant-and-literal-data-types.md)
- [Vue d’ensemble des constantes](constants-overview.md)
- [Guide pratique pour Déclarer une constante](how-to-declare-a-constant.md)
- [Constantes définies par l’utilisateur](user-defined-constants.md)
- [Constantes et types de données littérales](constant-and-literal-data-types.md)
- [Guide pratique pour Regrouper les valeurs de constante connexes](how-to-group-related-constant-values-together.md)
- [Vue d’ensemble des énumérations](enumerations-overview.md)
- [Guide pratique pour Déclarer des énumérations](how-to-declare-enumerations.md)
- [Guide pratique pour Faire référence à un membre d’énumération](how-to-refer-to-an-enumeration-member.md)
- [Énumérations et qualification de noms](enumerations-and-name-qualification.md)
- [Guide pratique pour Parcourir une énumération](how-to-iterate-through-an-enumeration.md)
- [Guide pratique pour Déterminer la chaîne associée à une valeur d’énumération](how-to-determine-the-string-associated-with-an-enumeration-value.md)
- [Quand utiliser une énumération](when-to-use-an-enumeration.md)

- [Vue d’ensemble des énumérations](enumerations-overview.md)
- [Vue d’ensemble des constantes](constants-overview.md)
- [Guide pratique pour Déclarer une énumération](how-to-declare-enumerations.md)
- [Énumérations et qualification de noms](enumerations-and-name-qualification.md)
- [Option Strict (instruction)](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
- [Constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md)
