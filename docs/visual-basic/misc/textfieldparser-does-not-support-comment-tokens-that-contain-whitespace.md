---
title: TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_WhitespaceInToken
ms.assetid: 55107656-270e-4bbb-841a-478904df8e07
ms.openlocfilehash: af0f09bb7a8afc3b6e63cfab1a7176ba26cf20a6
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64660895"
---
# <a name="textfieldparser-does-not-support-comment-tokens-that-contain-white-space"></a>TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc
Un jeton de commentaire qui contient un espace blanc a été fourni. `TextFieldParser` ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc, sauf si ce dernier se trouve au début du jeton. Un espace blanc situé au début d’un jeton est ignoré.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Fournissez un jeton de commentaire correct.  
  
## <a name="see-also"></a>Voir aussi

- [TextFieldParser.CommentTokens, propriété](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.CommentTokens%2A)
- [Analyse des fichiers texte avec l’objet TextFieldParser](../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)
- [TextFieldParser (objet)](../../visual-basic/language-reference/objects/textfieldparser-object.md)
