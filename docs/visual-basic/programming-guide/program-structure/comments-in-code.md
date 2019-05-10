---
title: Commentaires dans le code (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Uncomment button
- REM statement [Visual Basic]
- comments [Visual Basic], in code
- comments [Visual Basic], Visual Basic code
- Comment button
- buttons [Visual Basic], Uncomment
- buttons [Visual Basic], Comment
- code comments [Visual Basic], Visual Basic
- Visual Basic code, comments
- comments
- code comments
ms.assetid: 90136fba-22eb-49f9-ba81-63db629b4a47
ms.openlocfilehash: 2737d9494fb4cd2f0cfaec4da1bca69003c6bad7
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64753744"
---
# <a name="comments-in-code-visual-basic"></a>Commentaires dans le code (Visual Basic)
Lorsque vous lisez les exemples de code, vous rencontrez souvent le symbole de commentaire (`'`). Ce symbole indique au compilateur de Visual Basic d’ignorer le texte suivant, ou le *commentaire*. Les commentaires sont de courtes explications destinées à éclairer ceux qui lisent le code.  
  
 En programmation, il est hautement recommandé de faire précéder toutes les procédures d'un commentaire court qui décrit les caractéristiques fonctionnelles de la procédure (ce qu'elle fait). Ceci est utile tant pour l'auteur du code lui-même que pour toute autre personne amenée à consulter le code. Vous devez séparer les détails relatifs à l'implémentation (comment la procédure fait ce qu'elle doit faire) des commentaires décrivant les caractéristiques fonctionnelles. Si vous fournissez des informations d'implémentation dans la description, n'oubliez pas de les mettre à jour lors de la mise à jour de la fonction.  
  
 Les commentaires peuvent soit suivre une instruction sur la même ligne, soit occuper une ligne entière. Ces deux cas sont illustrés par le code suivant :  
  
 [!code-vb[VbVbcnConventions#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#16)]  
  
 Si votre commentaire doit occuper plusieurs lignes, utilisez le symbole de commentaire sur chacune d'elles, comme l'exemple ci-dessous l'illustre.  
  
 [!code-vb[VbVbcnConventions#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnConventions/VB/Class1.vb#17)]  
  
## <a name="commenting-guidelines"></a>Recommandations sur le commentaire  
 Le tableau suivant fournit des recommandations générales sur les types de commentaires qui peuvent précéder une section de code. Il s’agit de suggestions ; Visual Basic n’applique pas les règles pour l’ajout de commentaires. Procédez de la façon que vous jugez la plus efficace pour vous et toute personne amenée à lire votre code.  
  
|||  
|---|---|  
|Type de commentaire|Description du commentaire|  
|Objectif|Décrit ce que fait la procédure (et non comment elle le fait)|  
|Assumptions (Hypothèses)|Répertorie chaque variable externe, contrôle, fichier ouvert ou autre élément auquel la procédure accède.|  
|Effects (Effets)|Répertorie chaque variable externe, contrôle ou fichier affecté, ainsi que ses effets (uniquement si ce n'est pas évident)|  
|Inputs (Entrées)|Spécifie l’objectif attaché à l’argument|  
|Returns (Retours)|Explique les valeurs retournées par la procédure.|  
  
 N'oubliez pas :  
  
- Pour chaque déclaration de variable importante, faites précéder d'un commentaire décrivant son utilisation.  
  
- Les noms des variables, contrôles et procédures doivent être suffisamment clairs pour que les commentaires servent uniquement à fournir des détails d'implémentation complexes.  
  
- Vous ne pouvez pas faire suivre une séquence de continuation par un commentaire sur la même ligne.  
  
 Vous pouvez ajouter ou supprimer les symboles de commentaires pour un bloc de code en sélectionnant une ou plusieurs lignes de code et en choisissant le **commentaire** (![bouton le commentaire Visual Basic dans Visual Studio.](./media/comments-in-code/visual-basic-comment-button.gif)) et **marques**  (![Bouton de la supprimez les commentaires de Visual Basic dans Visual Studio.](./media/comments-in-code/visual-basic-uncomment-button.gif)) des boutons de la **modifier** barre d’outils.  
  
> [!NOTE]
>  Vous pouvez également ajouter des commentaires à votre code en faisant précéder le texte du mot clé `REM`. Toutefois, le `'` symbole et le **commentaire**/**Uncomment** boutons sont plus faciles à utiliser et nécessitent moins de mémoire et espace.  
  
## <a name="see-also"></a>Voir aussi

- [Instincts primaires : documentation de votre Code avec des commentaires XML](https://msdn.microsoft.com/magazine/dd722812.aspx)
- [Guide pratique pour Créer une Documentation XML](../../../visual-basic/programming-guide/program-structure/how-to-create-xml-documentation.md)
- [Étiquettes XML pour les commentaires](../../../visual-basic/language-reference/xmldoc/index.md)
- [Structure de programme et conventions de codage](../../../visual-basic/programming-guide/program-structure/program-structure-and-code-conventions.md)
- [REM (instruction)](../../../visual-basic/language-reference/statements/rem-statement.md)
