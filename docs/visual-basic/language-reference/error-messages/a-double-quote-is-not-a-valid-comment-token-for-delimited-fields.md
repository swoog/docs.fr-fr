---
title: Les guillemets doubles ne constituent pas un jeton de commentaire valide pour les champs délimités quand EscapeQuote a la valeur True
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_InvalidComment
ms.assetid: 636d4b81-00ba-4cfd-98f7-4d57036f494d
ms.openlocfilehash: 5838ef168523e8ba31fe5db93781bc409690e7ce
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33584137"
---
# <a name="a-double-quote-is-not-a-valid-comment-token-for-delimited-fields-where-escapequote-is-set-to-true"></a>Les guillemets doubles ne constituent pas un jeton de commentaire valide pour les champs délimités quand EscapeQuote a la valeur True
Un guillemet a été fourni comme délimiteur pour `TextFieldParser`, mais `EscapeQuotes` a la valeur `True`.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Affectez la valeur `EscapeQuotes` à `False`.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetDelimiters%2A>  
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser.Delimiters%2A>  
 <xref:Microsoft.VisualBasic.FileIO.TextFieldParser>  
 [Guide pratique : lire des fichiers texte délimités par des virgules](../../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)
