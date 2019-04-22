---
title: Utilisation des mots clés comme noms d'éléments dans le code (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, naming conventions
- keywords [Visual Basic], in code
- name conflicts [Visual Basic]
- element names [Visual Basic], in code
ms.assetid: 2e4e8e02-23f7-49b9-a1c8-2b0402b6b525
ms.openlocfilehash: c247ada67f6554362f287cf252dd49856c4995da
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58841145"
---
# <a name="keywords-as-element-names-in-code-visual-basic"></a>Utilisation des mots clés comme noms d'éléments dans le code (Visual Basic)
Un élément de programme, tel qu’une variable, une classe ou un membre — peut avoir le même nom qu’un mot clé restreint. Par exemple, vous pouvez créer une variable nommée `Loop`. Toutefois, pour faire référence à votre version de celui-ci, qui a le même nom que restreint `Loop` mot clé, vous devez le faire précéder d’une chaîne de qualification complète ou le placer entre crochets (`[ ]`), comme illustré dans l’exemple suivant.  
  
 [!code-vb[VbVbcnConventions#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#8)]  
  
 Si vous ne le faites pas une de ces, Visual Basic suppose l’utilisation de la fonction intrinsèque `Loop` mot clé et génère une erreur, comme dans l’exemple suivant :  
  
 `' The following statement causes a compiler error.`  
  
 `Loop.Visible = True`  
  
 Vous pouvez utiliser des crochets lorsque vous faites référence aux formulaires et contrôles et lors de la déclaration d’une variable ou la définition d’une procédure portant le même nom qu’un mot clé restreint. Il peut être facile d’oublier de qualifier des noms ou inclure des crochets, par conséquent introduire des erreurs dans votre code et rendre plus difficile à lire. Pour cette raison, nous vous recommandons de pas utiliser de mots clés restreints comme noms d’éléments de programme. Toutefois, si une version ultérieure de Visual Basic définit un nouveau mot clé qui entre en conflit avec un nom de contrôle ou un formulaire existant, puis vous pouvez utiliser cette technique lorsque la mise à jour votre code pour travailler avec la nouvelle version.  
  
> [!NOTE]
>  Votre programme peut également inclure des noms d’éléments fournis par d’autres assemblys référencés. Si ces noms sont en conflit avec les mots clés restreints, puis placer des crochets autour d’elles entraîne Visual Basic pour les interpréter comme vos éléments définis.  
  
## <a name="see-also"></a>Voir aussi

- [Conventions d’affectation de noms de Visual Basic](../../../visual-basic/programming-guide/program-structure/naming-conventions.md)
- [Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [Mots clés](../../../visual-basic/language-reference/keywords/index.md)
