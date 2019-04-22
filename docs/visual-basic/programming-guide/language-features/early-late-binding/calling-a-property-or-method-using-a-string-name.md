---
title: Appel d'une propriété ou méthode à l'aide d'un nom de chaîne (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- passing operators [Visual Basic]
- strings [Visual Basic], passing new operators as
- objects [Visual Basic], setting properties
- setting properties, object properties at run time
- method calls [Visual Basic], strings
- methods [Visual Basic], calling with string names
- calling methods [Visual Basic], string names
- properties [Visual Basic], setting at run time
- CallByName function
ms.assetid: 79a7b8b4-b8c7-4ad8-aca8-12a9a2b32f03
ms.openlocfilehash: e267c0c4d1d3e8f986348863d933c984f686b33b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58842640"
---
# <a name="calling-a-property-or-method-using-a-string-name-visual-basic"></a>Appel d'une propriété ou méthode à l'aide d'un nom de chaîne (Visual Basic)
Dans la plupart des cas, vous pouvez découvrir les propriétés et méthodes d’un objet au moment du design et écrire du code pour les gérer. Toutefois, dans certains cas vous ne pouvez pas savoir sur les propriétés et les méthodes d’un objet à l’avance, ou vous pouvez également la flexibilité de l’utilisateur spécifier les propriétés ou méthodes d’exécution en cours d’exécution.  
  
## <a name="callbyname-function"></a>CallByName (fonction)  
 Considérons, par exemple, une application cliente qui évalue des expressions entrées par l’utilisateur en passant un opérateur à un composant COM. Supposons que vous sont constamment ajouter de nouvelles fonctions pour le composant qui nécessitent de nouveaux opérateurs. Lorsque vous utilisez des techniques d’accès standard, vous devez recompiler et redistribuer l’application cliente avant qu’il puisse utiliser les nouveaux opérateurs. Pour éviter ce problème, vous pouvez utiliser le `CallByName` (fonction) pour passer les nouveaux opérateurs en tant que chaînes, sans modification de l’application.  
  
 Le `CallByName` fonction vous permet d’utiliser une chaîne pour spécifier une propriété ou méthode en cours d’exécution. La signature pour le `CallByName` fonction ressemble à ceci :  
  
 *Result* = `CallByName`(*Object*, *ProcedureName*, *CallType*, *Arguments*())  
  
 Le premier argument, *objet*, prend le nom de l’objet que vous voulez agir. Le *Nom_procédure* argument accepte une chaîne qui contient le nom de la procédure de propriété ou méthode à appeler. Le *CallType* argument accepte une constante qui représente le type de procédure à appeler : une méthode (`Microsoft.VisualBasic.CallType.Method`), une lecture de propriété (`Microsoft.VisualBasic.CallType.Get`), ou un jeu de propriétés (`Microsoft.VisualBasic.CallType.Set`). Le *Arguments* argument, qui est facultatif, accepte un tableau de type `Object` qui contient les arguments à la procédure.  
  
 Vous pouvez utiliser `CallByName` avec les classes de votre solution actuelle, mais il est plus souvent utilisé pour accéder aux objets COM ou des objets à partir de [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] assemblys.  
  
 Supposons que vous ajoutez une référence à un assembly qui contient une classe nommée `MathClass`, qui a une nouvelle fonction nommée `SquareRoot`, comme illustré dans le code suivant :  
  
 [!code-vb[VbVbalrOOP#53](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#53)]  
  
 Votre application peut utiliser des contrôles de zone de texte au contrôle quelle méthode sera appelée et de ses arguments. Par exemple, si `TextBox1` contient l’expression à évaluer, et `TextBox2` est utilisé pour entrer le nom de la fonction, vous pouvez utiliser le code suivant pour appeler le `SquareRoot` fonction sur l’expression dans `TextBox1`:  
  
 [!code-vb[VbVbalrOOP#54](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOOP/VB/OOP.vb#54)]  
  
 Si vous entrez « 64 » dans `TextBox1`, « SquareRoot » dans `TextBox2`, puis appelez le `CallMath` procédure, la racine carrée du nombre figurant dans `TextBox1` est évaluée. Le code dans l’exemple appelle la `SquareRoot` fonction (qui prend une chaîne qui contient l’expression soit évaluée comme un argument obligatoire) et retourne « 8 » dans `TextBox1` (la racine carrée de 64). Bien sûr, si l’utilisateur entre une chaîne non valide dans `TextBox2`si la chaîne contient le nom d’une propriété plutôt qu’une méthode, ou si la méthode possède un argument obligatoire supplémentaire, une erreur d’exécution se produit. Vous devez ajouter le code robuste de gestion des erreurs lorsque vous utilisez `CallByName` afin d’anticiper les autres erreurs.  
  
> [!NOTE]
>  Bien que le `CallByName` fonction peut être utile dans certains cas, vous devez également considérer son utilité contre les implications en matière de performances, à l’aide de `CallByName` pour appeler une procédure est légèrement plus lent qu’un appel à liaison tardive. Si vous appelez une fonction qui est appelée à plusieurs reprises, par exemple comme dans une boucle, `CallByName` peut avoir un impact négatif sur les performances.  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Interaction.CallByName%2A>
- [Détermination du type Object](../../../../visual-basic/programming-guide/language-features/early-late-binding/determining-object-type.md)
