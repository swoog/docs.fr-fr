---
title: TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un blanc
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_WhitespaceInToken
ms.assetid: 55107656-270e-4bbb-841a-478904df8e07
ms.openlocfilehash: ed22ac435a5cd46288f9854ae711b7fad354f624
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33641221"
---
# <a name="textfieldparser-does-not-support-comment-tokens-that-contain-whitespace"></a>TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un blanc
Un jeton de commentaire qui contient un espace blanc a été fourni. `TextFieldParser` ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc, sauf si ce dernier se trouve au début du jeton. Un espace blanc situé au début d’un jeton est ignoré.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Fournissez un jeton de commentaire correct.  
  
## <a name="see-also"></a>Voir aussi  
 [TextFieldParser.CommentTokens, propriété](http://msdn.microsoft.com/library/2e6b6435-4bee-4c14-a353-e8f2c82e2d61)  
 [Analyse des fichiers texte avec l’objet TextFieldParser](../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)  
 [TextFieldParser (objet)](../../visual-basic/language-reference/objects/textfieldparser-object.md)
