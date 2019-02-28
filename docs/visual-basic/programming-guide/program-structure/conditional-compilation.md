---
title: Compilation conditionnelle en Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- conditional compilation [Visual Basic], about conditional compilation
- compilation [Visual Basic], conditional
ms.assetid: 9c35e55e-7eee-44fb-a586-dad1f1884848
ms.openlocfilehash: 828edf2e5491394f5ac802b5c9babfb3df359e59
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56967847"
---
# <a name="conditional-compilation-in-visual-basic"></a>Compilation conditionnelle en Visual Basic
Dans *compilation conditionnelle*, blocs de code dans un programme spécifiques compiler de façon sélective tandis que d’autres sont ignorés.  
  
 Par exemple, vous souhaiterez écrire des instructions de débogage qui comparent la rapidité de différentes approches pour la même tâche de programmation, ou vous peuvent souhaiter localiser une application pour plusieurs langues. Instructions de compilation conditionnelle sont conçues pour s’exécuter pendant la compilation, pas au moment de l’exécution.  
  
 Vous désignez des blocs de code à compiler de façon conditionnelle avec la `#If...Then...#Else` directive. Par exemple, pour créer le Français et allemand versions de la même application à partir de la même le code source, incorporez des segments de code spécifique à la plateforme dans `#If...Then` instructions à l’aide de l’une des constantes prédéfinies `FrenchVersion` et `GermanVersion`. L’exemple suivant montre comment :  
  
 [!code-vb[VbVbalrConditionalComp#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrConditionalComp/VB/Class1.vb#5)]  
  
 Si vous définissez la valeur de la `FrenchVersion` constante de compilation conditionnelle à `True` au moment de la compilation, le code conditionnel pour la version Français est compilé. Si vous définissez la valeur de la `GermanVersion` constante à `True`, le compilateur utilise la version allemande. Si aucun n’est défini `True`, le code dans la dernière `Else` bloquer s’exécute.  
  
> [!NOTE]
>  La saisie semi-automatique ne fonctionne pas lorsque vous modifiez du code et à l’aide de directives de compilation conditionnelle Si le code ne fait pas partie de la branche active.  
  
## <a name="declaring-conditional-compilation-constants"></a>Déclarer des constantes de Compilation conditionnelle  
 Vous pouvez définir des constantes de compilation conditionnelle dans un des trois façons :  
  
-   Dans le **du Concepteur de projets**  
  
-   Sur la ligne de commande lorsque vous utilisez le compilateur de ligne de commande  
  
-   Dans votre code  
  
 Constantes de compilation conditionnelle ont une portée spéciale et ne sont pas accessibles à partir du code standard. La portée d’une constante de compilation conditionnelle est dépendante de la façon dont elle est définie. Le tableau suivant répertorie la portée des constantes déclarées à l’aide de chacun des trois méthodes mentionnées ci-dessus.  
  
|Configuration (constante)|Étendue de constante|  
|---|---|  
|**Concepteur de projets**|Public, pour tous les fichiers dans le projet|  
|Ligne de commande|Public, pour tous les fichiers passés au compilateur de ligne de commande|  
|`#Const` instruction de code|Privée pour le fichier dans lequel elle est déclarée|  
  
|Pour définir des constantes dans le Concepteur de projets|  
|---|  
|-Avant de créer votre fichier exécutable, définissez des constantes dans le **Concepteur de projets** en suivant les étapes fournies dans [la gestion des propriétés de projet et Solution](/visualstudio/ide/managing-project-and-solution-properties).|  
  
|Pour définir des constantes à la ligne de commande|  
|---|  
|-Utilisez le **/d** commutateur pour entrer des constantes de compilation conditionnelle, comme dans l’exemple suivant :<br />     `vbc MyProj.vb /d:conFrenchVersion=–1:conANSI=0`<br />     Aucun espace n’est nécessaire entre le **/d** commutateur et la première constante. Pour plus d’informations, consultez [/ define (Visual Basic)](../../../visual-basic/reference/command-line-compiler/define.md).<br />     Les déclarations de ligne de commande substituent les déclarations entrées dans le **Concepteur de projet**, mais ne les suppriment pas. Arguments définis **Concepteur de projets** restent en vigueur pour les compilations ultérieures.<br />     Lorsque vous écrivez des constantes dans le code lui-même, ne sont pas des règles strictes quant à leur emplacement, car leur étendue est l’ensemble du module dans lequel ils sont déclarés.|  
  
|Pour définir des constantes dans votre code|  
|---|  
|-Placez les constantes dans le bloc de déclaration du module dans lequel elles sont utilisées. Cela permet de maintenir votre code organisé et plus facile à lire.|  
  
## <a name="related-topics"></a>Rubriques connexes  
  
|Titre|Description|  
|---|---|  
|[Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)|Fournit des suggestions pour rendre votre code facile à lire et à gérer.|  
  
## <a name="reference"></a>Référence  
 [#Const (directive)](../../../visual-basic/language-reference/directives/const-directive.md)  
  
 [#If...Then...#Else, directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md)  
  
 [/define (Visual Basic)](../../../visual-basic/reference/command-line-compiler/define.md)
