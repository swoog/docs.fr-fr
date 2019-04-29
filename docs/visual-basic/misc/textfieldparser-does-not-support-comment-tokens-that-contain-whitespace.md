---
title: TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_WhitespaceInToken
ms.assetid: 55107656-270e-4bbb-841a-478904df8e07
ms.openlocfilehash: 9a14bc29ecfa917b6213f32cd170aa83d6f60f58
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61668989"
---
# <a name="textfieldparser-does-not-support-comment-tokens-that-contain-white-space"></a>TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc
Un jeton de commentaire qui contient un espace blanc a été fourni. `TextFieldParser` ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc, sauf si ce dernier se trouve au début du jeton. Un espace blanc situé au début d’un jeton est ignoré.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Fournissez un jeton de commentaire correct.  
  
## <a name="see-also"></a>Voir aussi

- [TextFieldParser.CommentTokens, propriété](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.CommentTokens%2A)
- [Analyse des fichiers texte avec l’objet TextFieldParser](../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)
- [TextFieldParser (objet)](../../visual-basic/language-reference/objects/textfieldparser-object.md)
