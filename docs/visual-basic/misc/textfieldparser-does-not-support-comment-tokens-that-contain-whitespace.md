---
title: TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_WhitespaceInToken
ms.assetid: 55107656-270e-4bbb-841a-478904df8e07
ms.openlocfilehash: 2beda651dba952969593ffc7d64f01fd51ab7919
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43556274"
---
# <a name="textfieldparser-does-not-support-comment-tokens-that-contain-white-space"></a>TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc
Un jeton de commentaire qui contient un espace blanc a été fourni. `TextFieldParser` ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc, sauf si ce dernier se trouve au début du jeton. Un espace blanc situé au début d’un jeton est ignoré.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Fournissez un jeton de commentaire correct.  
  
## <a name="see-also"></a>Voir aussi  
 [TextFieldParser.CommentTokens, propriété](https://msdn.microsoft.com/library/2e6b6435-4bee-4c14-a353-e8f2c82e2d61)  
 [Analyse des fichiers texte avec l’objet TextFieldParser](../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)  
 [TextFieldParser (objet)](../../visual-basic/language-reference/objects/textfieldparser-object.md)
