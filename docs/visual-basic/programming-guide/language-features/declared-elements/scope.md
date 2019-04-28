---
title: Portée dans Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- module scope [Visual Basic]
- scope [Visual Basic], levels
- module level
- procedures [Visual Basic], scope
- declared elements [Visual Basic], scope
- namespaces [Visual Basic], scope
- scope [Visual Basic], declared elements
- scope [Visual Basic], about scope
- levels of scope [Visual Basic]
- block scope [Visual Basic]
- scope [Visual Basic], Visual Basic
- procedure scope [Visual Basic]
ms.assetid: 208106fe-79c9-4eec-93c6-55f08548895f
ms.openlocfilehash: 6139af65958cefe43578f436204fa6836a71de0b
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61917837"
---
# <a name="scope-in-visual-basic"></a>Portée dans Visual Basic
Le *étendue* d’un élément déclaré est l’ensemble du code qui peut faire référence à ce dernier sans qualifier son nom ou le rendre disponible via un [instruction Imports (.NET Namespace et Type)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md). Un élément peut avoir la portée à un des niveaux suivants :  
  
|Niveau|Description|  
|-----------|-----------------|  
|Portée de bloc|Disponible uniquement dans le code de bloc dans lequel elle est déclarée|  
|Portée de procédure|Disponible à tout le code au sein de la procédure dans laquelle elle est déclarée|  
|Portée de module|Disponible à tout le code dans le module, une classe ou une structure dans laquelle elle est déclarée|  
|Étendue de Namespace|Disponible à tout le code dans l’espace de noms dans lequel elle est déclarée|  
  
 Ces niveaux de portée plus restreint (bloc) au plus large (espace de noms), où *plus petite portée* signifie que le plus petit ensemble de code qui peut faire référence à l’élément sans qualification. Pour plus d’informations, consultez « Niveaux de portée » sur cette page.  
  
## <a name="specifying-scope-and-defining-variables"></a>Spécifier la portée et la définition de Variables  
 Vous spécifiez l’étendue d’un élément lors de sa déclaration. L’étendue peut dépendre des facteurs suivants :  
  
- La région dans laquelle vous déclarez l’élément (bloc, procédure, module, classe ou structure)  
  
- L’espace de noms contenant la déclaration de l’élément  
  
- Le niveau d’accès que vous déclarez pour l’élément  
  
 Soyez prudent lorsque vous définissez des variables avec le même nom mais une portée différente, car cela peut provoquer des résultats inattendus. Pour plus d'informations, consultez [References to Declared Elements](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md).  
  
## <a name="levels-of-scope"></a>Niveaux de portée  
 Un élément de programmation est disponible dans l’ensemble de la région dans laquelle vous la déclarez. Tout le code dans la même région peut faire référence à l’élément sans qualifier son nom.  
  
### <a name="block-scope"></a>Portée de bloc  
 Un bloc est un ensemble d’instructions placées entre le début et de fin des instructions de déclaration, telles que les éléments suivants :  
  
- `Do` et `Loop`  
  
- `For` [`Each`] et `Next`  
  
- `If` et `End If`  
  
- `Select` et `End Select`  
  
- `SyncLock` et `End SyncLock`  
  
- `Try` et `End Try`  
  
- `While` et `End While`  
  
- `With` et `End With`  
  
 Si vous déclarez une variable dans un bloc, vous pouvez l’utiliser uniquement dans ce bloc. Dans l’exemple suivant, la portée de la variable entière `cube` est le bloc entre `If` et `End If`, et vous pouvez ne font plus référence à `cube` lorsque l’exécution sort du bloc.  
  
```  
If n < 1291 Then  
    Dim cube As Integer  
    cube = n ^ 3  
End If  
```  
  
> [!NOTE]
>  Même si l’étendue d’une variable est limitée à un bloc, sa durée de vie est toujours celui de toute la procédure. Si vous entrez le bloc plusieurs fois pendant la procédure, chaque variable de bloc conserve sa valeur précédente. Pour éviter des résultats inattendus dans ce cas, il est judicieux d’initialiser des variables de bloc au début du bloc.  
  
### <a name="procedure-scope"></a>Portée de procédure  
 Un élément déclaré au sein d’une procédure n’est pas disponible en dehors de cette procédure. Uniquement la procédure qui contient la déclaration peut l’utiliser. Variables à ce niveau sont également appelés *variables locales*. Vous les déclarez avec le [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md), avec ou sans le [statique](../../../../visual-basic/language-reference/modifiers/static.md) mot clé.  
  
 Portée de bloc et de procédure sont étroitement liés. Si vous déclarez une variable à l’intérieur d’une procédure mais en dehors de tout bloc de cette procédure, vous pouvez considérer la variable comme ayant une portée de bloc, où le bloc est toute la procédure.  
  
> [!NOTE]
>  Tous les éléments locaux, même s’ils sont `Static` variables, appartiennent à la procédure dans lequel ils apparaissent. Vous ne pouvez pas déclarer de n’importe quel élément à l’aide de la [Public](../../../../visual-basic/language-reference/modifiers/public.md) mot clé contenu dans une procédure.  
  
### <a name="module-scope"></a>Portée de module  
 Pour plus de commodité, le terme unique *au niveau du module* s’appliquent également aux modules, les classes et structures. Vous pouvez déclarer des éléments à ce niveau en plaçant l’instruction de déclaration en dehors d’une procédure ou un bloc, mais dans le module, une classe ou une structure.  
  
 Lorsque vous effectuez une déclaration au niveau du module, le niveau d’accès que vous choisissez détermine l’étendue. L’espace de noms qui contient le module, la classe ou la structure affecte également la portée.  
  
 Les éléments que vous déclarez [privé](../../../../visual-basic/language-reference/modifiers/private.md) niveau d’accès sont disponibles pour chaque procédure de ce module, mais pas pour le code dans un autre module. Le `Dim` instruction au niveau du module par défaut est `Private` si vous n’utilisez pas de mots clés n’importe quel niveau d’accès. Toutefois, vous pouvez rendre le niveau de portée et d’accès plus évidents en utilisant le `Private` mot clé dans la `Dim` instruction.  
  
 Dans l’exemple suivant, toutes les procédures définies dans le module peuvent faire référence à la variable de chaîne `strMsg`. Lorsque la deuxième procédure est appelée, elle affiche le contenu de la variable chaîne `strMsg` dans une boîte de dialogue.  
  
```  
' Put the following declaration at module level (not in any procedure).  
Private strMsg As String  
' Put the following Sub procedure in the same module.  
Sub initializePrivateVariable()  
    strMsg = "This variable cannot be used outside this module."  
End Sub  
' Put the following Sub procedure in the same module.  
Sub usePrivateVariable()  
    MsgBox(strMsg)  
End Sub  
```  
  
### <a name="namespace-scope"></a>Étendue de Namespace  
 Si vous déclarez un élément au module à l’aide du [Friend](../../../../visual-basic/language-reference/modifiers/friend.md) ou [Public](../../../../visual-basic/language-reference/modifiers/public.md) mot clé, il est accessible à toutes les procédures de l’espace de noms dans lequel l’élément est déclaré. Avec la modification suivante apportée à l’exemple précédent, la variable de chaîne `strMsg` peuvent être référencés par le code n’importe où dans l’espace de noms de sa déclaration.  
  
```  
' Include this declaration at module level (not inside any procedure).  
Public strMsg As String  
```  
  
 Étendue de Namespace inclut des espaces de noms imbriqués. Un élément disponible dans un espace de noms est également disponible à partir de n’importe quel espace de noms imbriqué à l’intérieur de cet espace de noms.  
  
 Si votre projet ne contient aucun [Namespace instruction](../../../../visual-basic/language-reference/statements/namespace-statement.md), tous les éléments dans le projet se trouve dans le même espace de noms. Dans ce cas, la portée espace de noms peut être considérée comme la portée du projet. `Public` éléments dans un module, une classe ou une structure sont également disponibles pour n’importe quel projet qui fait référence à leur projet.  
  
## <a name="choice-of-scope"></a>Choix de la portée  
 Lorsque vous déclarez une variable, vous gardez à l’esprit les points suivants lors du choix de son étendue.  
  
### <a name="advantages-of-local-variables"></a>Avantages des Variables locales  
 Variables locales sont un bon choix pour tout type de calcul temporaire, pour les raisons suivantes :  
  
- **Prévention du conflit de nom.** Noms de variables locales ne sont pas susceptibles d’être en conflit. Par exemple, vous pouvez créer plusieurs procédures différentes qui contiennent une variable appelée `intTemp`. Tant que chaque `intTemp` est déclarée comme une variable locale, chaque procédure ne reconnaît que sa propre version de `intTemp`. Toute procédure peut modifier la valeur dans sa local `intTemp` sans affecter `intTemp` variables dans d’autres procédures.  
  
- **Consommation de mémoire.** Variables locales solliciter la mémoire uniquement pendant l’exécution de la procédure. Leur mémoire est libérée lorsque la procédure retourne au code appelant. En revanche, [partagé](../../../../visual-basic/language-reference/modifiers/shared.md) et [statique](../../../../visual-basic/language-reference/modifiers/static.md) variables consomment des ressources mémoire jusqu'à ce que votre application cesse de s’exécuter, par conséquent, utilisez-les uniquement lorsque cela est nécessaire. *Variables d’instances* consomment de la mémoire alors que leur instance continue d’exister, ce qui les rend moins efficaces que les variables locales, mais potentiellement plus efficaces que `Shared` ou `Static` variables.  
  
### <a name="minimizing-scope"></a>Réduire la portée  
 En général, lorsque vous déclarez une variable ou une constante, il est conseillé de définir une portée aussi courtes que possible (la portée de bloc est la plus restreinte). Cela permet d’économiser la mémoire et réduit les risques de votre code fasse référence à la variable incorrecte. De même, vous devez déclarer une variable comme étant [statique](../../../../visual-basic/language-reference/modifiers/static.md) uniquement lorsqu’il est nécessaire de conserver sa valeur entre les appels de procédure.  
  
## <a name="see-also"></a>Voir aussi

- [Caractéristiques d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md)
- [Guide pratique pour Contrôler la portée d’une Variable](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-control-the-scope-of-a-variable.md)
- [Durée de vie en Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)
- [Niveaux d’accès dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
- [Références aux éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
