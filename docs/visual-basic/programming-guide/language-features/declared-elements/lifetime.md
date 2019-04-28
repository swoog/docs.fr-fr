---
title: Durée de vie dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- static variables [Visual Basic], lifetime
- static variables [Visual Basic], Visual Basic
- declared elements [Visual Basic], lifetime
- Shared variable lifetime [Visual Basic]
- lifetime [Visual Basic], declared elements
- lifetime [Visual Basic], Visual Basic
- lifetime [Visual Basic]
ms.assetid: bd91e390-690a-469a-9946-8dca70bc14e7
ms.openlocfilehash: 7a8730834c5241ddb1271d689cdda8942741f15f
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61917928"
---
# <a name="lifetime-in-visual-basic"></a>Durée de vie dans Visual Basic
Le *durée de vie* d’un élément déclaré est la période de temps pendant laquelle il est disponible pour utilisation. Les variables sont les seuls éléments qui ont la durée de vie. À cet effet, le compilateur traite les paramètres de procédure et retours de fonction comme des cas spéciaux de variables. La durée de vie d’une variable représente la période de temps pendant lequel il peut contenir une valeur. Sa valeur peut évoluer au fil de sa durée de vie, mais elle contient toujours une valeur.  
  
## <a name="different-lifetimes"></a>Différentes durées de vie  
 Un *variable membre* (déclarée au niveau du module, en dehors de toute procédure) a généralement la même durée de vie que l’élément dans lequel elle est déclarée. Il existe une variable non partagée déclarée dans une classe ou structure comme une copie distincte pour chaque instance de la classe ou structure dans laquelle elle est déclarée. Chaque variable de ce type a la même durée de vie que son instance. Toutefois, un `Shared` variable a uniquement une seule durée de vie, qui dure pendant toute la durée de votre application est en cours d’exécution.  
  
 Un *variable locale* (déclaré à l’intérieur d’une procédure) existe uniquement pendant l’exécution de la procédure dans laquelle elle est déclarée. Cela s’applique également aux paramètres de cette procédure et de tout retour de fonction. Toutefois, si cette procédure appelle d’autres procédures, les variables locales conservent leurs valeurs pendant l’exécutant de procédures appelées.  
  
## <a name="beginning-of-lifetime"></a>Début de la durée de vie  
 Durée de vie d’une variable locale commence lorsque le contrôle pénètre dans la procédure dans laquelle elle est déclarée. Chaque variable locale est initialisée à la valeur par défaut pour son type de données dès que commence la procédure en cours d’exécution. Lorsque la procédure rencontre un `Dim` instruction qui spécifie les valeurs initiales, elle définit ces variables à ces valeurs, même si votre code a déjà affecté des autres valeurs y.  
  
 Chaque membre d’une variable de structure est initialisé comme s’il s’agissait d’une variable distincte. De même, chaque élément d’une variable tableau est initialisé individuellement.  
  
 Les variables déclarées dans un bloc à l’intérieur d’une procédure (comme un `For` boucle) sont initialisées sur ENTRÉE pour la procédure. Ces initialisations prennent effet que votre code n’exécute le bloc ou non.  
  
## <a name="end-of-lifetime"></a>Fin de la durée de vie  
 Lorsqu’une procédure se termine, les valeurs de ses variables locales ne sont pas conservées, et Visual Basic permet de récupérer leur mémoire. La prochaine fois que vous appelez la procédure, toutes ses variables locales sont recréés et réinitialisés.  
  
 Lorsqu’une instance d’une classe ou une structure prend fin, ses variables non partagées perdent leur mémoire et leurs valeurs. Chaque nouvelle instance de la classe ou structure crée et réinitialise ses variables non partagées. Toutefois, `Shared` variables sont conservées jusqu'à ce que votre application cesse de s’exécuter.  
  
## <a name="extension-of-lifetime"></a>Extension de durée de vie  
 Si vous déclarez une variable locale avec le `Static` mot clé, sa durée de vie est plus longue que la durée d’exécution de sa procédure. Le tableau suivant montre comment la déclaration de procédure détermine la durée pendant laquelle un `Static` variable existe.  
  
|Emplacement de la procédure et le partage|Durée de vie de variable statique commence|Fin de la durée de vie de variable statique|  
|------------------------------------|-------------------------------------|-----------------------------------|  
|Dans un module (partagé par défaut)|La première fois que la procédure est appelée.|Lorsque votre application s’arrête en cours d’exécution|  
|Dans une classe, `Shared` (la procédure n’est pas un membre d’instance)|La première fois que la procédure est appelée sur une instance spécifique ou sur le nom de classe ou structure lui-même|Lorsque votre application s’arrête en cours d’exécution|  
|Dans une instance d’une classe, pas `Shared` (la procédure est un membre d’instance)|La première fois que la procédure est appelée sur une instance spécifique|Lorsque l’instance est libérée pour le garbage collection (GC)|  
  
## <a name="static-variables-of-the-same-name"></a>Variables statiques du même nom  
 Vous pouvez déclarer des variables statiques avec le même nom dans plusieurs procédures. Si vous procédez ainsi, le compilateur Visual Basic considère chacune des variables comme un élément distinct. L’initialisation d’un de ces variables n’affecte pas les valeurs des autres. Va de même si vous définissez une procédure avec un ensemble de surcharges et que vous déclarez une variable statique avec le même nom dans chaque surcharge.  
  
## <a name="containing-elements-for-static-variables"></a>Contenant les éléments pour les Variables statiques  
 Vous pouvez déclarer une variable locale statique dans une classe, autrement dit, à l’intérieur d’une procédure dans cette classe. Toutefois, vous ne pouvez pas déclarer une variable locale statique dans une structure, comme un membre de structure ou comme une variable locale d’une procédure dans cette structure.  
  
## <a name="example"></a>Exemple  
  
### <a name="description"></a>Description  
 L’exemple suivant déclare une variable avec le [statique](../../../../visual-basic/language-reference/modifiers/static.md) mot clé. (Notez que vous n’avez pas besoin du `Dim` mot clé lors de la [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md) utilise un modificateur, telles que `Static`.)  
  
### <a name="code"></a>Code  
 [!code-vb[VbVbalrKeywords#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/class7.vb#13)]  
  
### <a name="comments"></a>Commentaires  
 Dans l’exemple précédent, la variable `applesSold` continue d’exister après la procédure `runningTotal` retourne au code appelant. La prochaine fois `runningTotal` est appelée, `applesSold` conserve sa valeur précédemment calculée.  
  
 Si `applesSold` avait été déclaré sans utiliser `Static`, les valeurs précédemment accumulées ne seraient pas conservés entre les appels à `runningTotal`. La prochaine fois `runningTotal` a été appelée, `applesSold` auraient été recréé et initialisé à 0, et `runningTotal` aurait simplement retourné la même valeur avec laquelle elle a été appelée.  
  
### <a name="compiling-the-code"></a>Compilation du code  
 Vous pouvez initialiser la valeur d’une variable locale statique dans le cadre de sa déclaration. Si vous déclarez un tableau comme étant `Static`, vous pouvez initialiser son rang (nombre de dimensions), la longueur de chaque dimension et les valeurs des éléments individuels.  
  
### <a name="security"></a>Sécurité  
 Dans l’exemple précédent, vous pouvez obtenir la même durée de vie en déclarant `applesSold` au niveau du module. Si vous avez modifié la portée d’une variable de cette façon, toutefois, la procédure n’aient plus un accès exclusif à celui-ci. Étant donné que les autres procédures peuvent accéder `applesSold` et changer sa valeur, le total cumulé n’est plus fiable et le code peut être plus difficile à gérer.  
  
## <a name="see-also"></a>Voir aussi

- [Shared](../../../../visual-basic/language-reference/modifiers/shared.md)
- [Nothing](../../../../visual-basic/language-reference/nothing.md)
- [Noms d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Références aux éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Portée dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
- [Niveaux d’accès dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [Variables](../../../../visual-basic/programming-guide/language-features/variables/index.md)
- [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [Dépannage des types de données](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)
- [Static](../../../../visual-basic/language-reference/modifiers/static.md)
