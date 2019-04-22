---
title: Vue d'ensemble des constantes (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- constants [Visual Basic]
ms.assetid: 29016fe8-78b3-4dc8-90b8-1cfec2fa8ac9
ms.openlocfilehash: 2939110de77718baf32e2a0d8f1aa52dba997cf3
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58841285"
---
# <a name="constants-overview-visual-basic"></a>Vue d'ensemble des constantes (Visual Basic)
Une constante est un nom significatif qui prend la place d’un nombre ou une chaîne qui ne change pas. Les constantes stockent des valeurs qui, comme son nom l’indique, demeurent identiques lors de l’exécution d’une application. Vous pouvez considérablement améliorer la lisibilité de votre code et le rendre plus facile à gérer à l’aide de constantes. Les utiliser dans le code qui contient des valeurs qui réapparaissent ou qui dépend de certains nombres qui sont difficiles à mémoriser ou n’ont aucune signification évidente.  
  
## <a name="how-to-create-and-use-constants"></a>Comment créer et utiliser des constantes  
 Visual Basic contient plusieurs constantes prédéfinies, principalement à l’aide de l’impression et d’affichage. Vous pouvez également créer vos propres constantes avec le `Const` instruction, en utilisant les mêmes instructions que vous le feriez pour la création d’un nom de variable. Si `Option Strict` est `On`, vous devez déclarer explicitement le type de constante.  
  
 La portée d’une constante, qui est l’ensemble du code que vous pouvez vous y référer sans qualifier son nom, est identique à celui d’une variable déclarée dans le même emplacement. Pour créer une constante qui existe dans l’étendue d’une procédure particulière, déclarez-le à l’intérieur de cette procédure. Pour créer une constante qui est disponible dans une application, déclarez-le à l’aide de la `Public` mot clé dans la section des déclarations de la classe.  
  
> [!NOTE]
>  Bien que les constantes ressemblent un peu aux variables, vous ne peut pas modifier ou leur assigner de nouvelles valeurs que possible aux variables.  
  
 Les constantes que vous utilisez dans votre code peuvent être définies par le modèle objet pour les contrôles ou les composants que vous utilisez, ou ils peuvent être définis par l’utilisateur (autrement dit, celles que vous créez vous-même).  
  
## <a name="compile-time-and-run-time-constants"></a>Constantes de compilation et exécution  
 Une constante de compilation est calculée au moment de que la compilation du code, tandis que la constante au moment de l’exécution peut être calculée uniquement pendant l’exécution de l’application. Une constante de compilation aura la même valeur chaque fois qu'une application s’exécute, une constante d’exécution peut être modifié chaque fois. Constantes de compilation sont nécessaires pour les cas tels que les limites du tableau, les expressions case ou les initialiseurs de l’énumérateur.  
  
## <a name="in-this-section"></a>Dans cette section  
  
|Définition|Terme|  
|---|---|  
|[Guide pratique pour Déclarer une constante](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-a-constant.md)|Explique comment utiliser le `Const` instruction pour déclarer une constante et définir sa valeur ; en déclarant une constante, vous affectez un nom explicite à la valeur.|  
|[Constantes définies par l’utilisateur](../../../../visual-basic/programming-guide/language-features/constants-enums/user-defined-constants.md)|Décrit comment créer vos propres constantes, notamment des informations sur l’étendue et comment éviter les références circulaires.|  
|[Constantes et types de données littérales](../../../../visual-basic/programming-guide/language-features/constants-enums/constant-and-literal-data-types.md)|Fournit des informations sur la façon dont le compilateur Visual Basic initialise des constantes lorsque `Option Explicit` est désactivée.|  
|[Guide pratique pour Regrouper les valeurs de constante connexes](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-group-related-constant-values-together.md)|Montre comment regrouper des valeurs constantes qui sont liées.|  
  
## <a name="reference"></a>Référence  
  
|Définition|Terme|  
|---|---|  
|[Constantes et énumérations](../../../../visual-basic/language-reference/constants-and-enumerations.md)|Répertorie les constantes prédéfinies par Visual Basic.|  
|[Const (instruction)](../../../../visual-basic/language-reference/statements/const-statement.md)|Décrit la `Const` instruction et son utilisation.|  
|[Option Strict (instruction)](../../../../visual-basic/language-reference/statements/option-strict-statement.md)|Décrit la `Option Strict` instruction et son utilisation.|  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des énumérations](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-overview.md)
- [Guide pratique pour Initialiser une Variable tableau en Visual Basic](../../../../visual-basic/programming-guide/language-features/arrays/how-to-initialize-an-array-variable.md)
