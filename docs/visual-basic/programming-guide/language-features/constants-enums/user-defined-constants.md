---
title: Constantes définies par l'utilisateur (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- constants [Visual Basic], circular references
- Const statement [Visual Basic], user-defined constants
- user-defined constants [Visual Basic]
- scope [Visual Basic], constants
- constants [Visual Basic], user-defined
- circular references between constants [Visual Basic]
ms.assetid: a1206d5c-c45e-4ac2-970a-4a0be6a05fdd
ms.openlocfilehash: f0196457235ad77df545a367573f62b43209269d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61906982"
---
# <a name="user-defined-constants-visual-basic"></a>Constantes définies par l'utilisateur (Visual Basic)
Une constante est un nom significatif qui prend la place d’un nombre ou une chaîne qui ne change pas. Les constantes stockent des valeurs qui, comme leur nom l’indique, demeurent constantes tout au long de l’exécution d’une application. Vous pouvez utiliser des constantes qui sont définies par les contrôles ou les composants que vous utilisez, ou vous pouvez créer vos propres. Les constantes que vous créez vous-même sont décrites en tant que *défini par l’utilisateur*.  
  
 Vous déclarez une constante avec la `Const` instruction, en utilisant les mêmes instructions que vous le feriez pour la création d’un nom de variable. Si `Option Strict` est `On`, vous devez déclarer explicitement le type de constante.  
  
## <a name="const-statement-usage"></a>Utilisation de l’instruction const  
 Un `Const` instruction peut représenter une valeur mathématique ou date/heure :  
  
 [!code-vb[VbEnumsTask#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#10)]  
  
 Elle peut également définir `String` constantes :  
  
 [!code-vb[VbEnumsTask#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#13)]  
  
 L’expression située à droite du signe égal ( `=` ) est souvent un nombre ou une chaîne littérale, mais elle peut également être une expression qui aboutit à un nombre ou une chaîne (bien que cette expression ne peut pas contenir des appels aux fonctions). Vous pouvez même définir des constantes en termes de constantes définies précédemment :  
  
 [!code-vb[VbEnumsTask#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#15)]  
  
## <a name="scope-of-user-defined-constants"></a>Portée des constantes définies par l’utilisateur  
 Un `Const` étendue de l’instruction est identique à celui d’une variable déclarée dans le même emplacement. Vous pouvez spécifier l’étendue dans une des manières suivantes :  
  
- Pour créer une constante qui existe uniquement dans une procédure, vous devez le déclarer dans celle-ci.  
  
- Pour créer une constante disponible pour toutes les procédures dans une classe, mais pas pour le code en dehors de ce module, vous devez le déclarer dans la section des déclarations de la classe.  
  
- Pour créer une constante qui est disponible pour tous les membres d’un assembly, mais pas pour les clients en dehors de l’assembly, déclarez-le à l’aide de la `Friend` mot clé dans la section des déclarations de la classe.  
  
- Pour créer une constante disponible tout au long de l’application, déclarez-le à l’aide de la `Public` mot clé dans les déclarations de section de la classe.  
  
 Pour plus d'informations, voir [Procédure : Déclarez une constante](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-a-constant.md).  
  
### <a name="avoiding-circular-references"></a>Éviter les références circulaires  
 Étant donné que les constantes peuvent être définies en termes d’autres constantes, il est possible de créer par inadvertance un *cycle*, ou une référence circulaire entre deux ou plusieurs constantes. Un cycle se produit lorsque vous avez deux ou plusieurs constantes publiques, chacun d’eux est défini en termes de l’autre, comme dans l’exemple suivant :  
  
 [!code-vb[VbEnumsTask#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#16)]  
[!code-vb[VbEnumsTask#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbEnumsTask/VB/Class2.vb#17)]  
  
 Si un cycle se produit, Visual Basic génère une erreur du compilateur.  
  
## <a name="see-also"></a>Voir aussi

- [Const (instruction)](../../../../visual-basic/language-reference/statements/const-statement.md)
- [Constantes et types de données littérales](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)
- [Constantes et énumérations](../../../../visual-basic/programming-guide/language-features/constants-enums/index.md)
- [Constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md)
- [Vue d’ensemble des énumérations](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)
- [Vue d’ensemble des constantes](../../../../visual-basic/programming-guide/language-features/constants-enums/constants-overview.md)
- [Guide pratique pour Déclarer une énumération](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)
- [Énumérations et qualification de noms](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)
- [Option Strict (instruction)](../../../../visual-basic/language-reference/statements/option-strict-statement.md)
