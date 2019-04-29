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
# <a name="textfieldparser-does-not-support-comment-tokens-that-contain-white-space"></a><span data-ttu-id="8c18a-102">TextFieldParser ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc</span><span class="sxs-lookup"><span data-stu-id="8c18a-102">TextFieldParser does not support comment tokens that contain white space</span></span>
<span data-ttu-id="8c18a-103">Un jeton de commentaire qui contient un espace blanc a été fourni.</span><span class="sxs-lookup"><span data-stu-id="8c18a-103">A comment token that contains white space has been supplied.</span></span> <span data-ttu-id="8c18a-104">`TextFieldParser` ne prend pas en charge les jetons de commentaires qui contiennent un espace blanc, sauf si ce dernier se trouve au début du jeton.</span><span class="sxs-lookup"><span data-stu-id="8c18a-104">The `TextFieldParser` does not support comment tokens that contain white space unless the white space occurs at the beginning of the token.</span></span> <span data-ttu-id="8c18a-105">Un espace blanc situé au début d’un jeton est ignoré.</span><span class="sxs-lookup"><span data-stu-id="8c18a-105">White space occurring at the beginning of a token is ignored.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="8c18a-106">Pour corriger cette erreur</span><span class="sxs-lookup"><span data-stu-id="8c18a-106">To correct this error</span></span>  
  
- <span data-ttu-id="8c18a-107">Fournissez un jeton de commentaire correct.</span><span class="sxs-lookup"><span data-stu-id="8c18a-107">Supply a correct comment token.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8c18a-108">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c18a-108">See also</span></span>

- [<span data-ttu-id="8c18a-109">TextFieldParser.CommentTokens, propriété</span><span class="sxs-lookup"><span data-stu-id="8c18a-109">TextFieldParser.CommentTokens Property</span></span>](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.CommentTokens%2A)
- [<span data-ttu-id="8c18a-110">Analyse des fichiers texte avec l’objet TextFieldParser</span><span class="sxs-lookup"><span data-stu-id="8c18a-110">Parsing Text Files with the TextFieldParser Object</span></span>](../../visual-basic/developing-apps/programming/drives-directories-files/parsing-text-files-with-the-textfieldparser-object.md)
- [<span data-ttu-id="8c18a-111">TextFieldParser (objet)</span><span class="sxs-lookup"><span data-stu-id="8c18a-111">TextFieldParser Object</span></span>](../../visual-basic/language-reference/objects/textfieldparser-object.md)
