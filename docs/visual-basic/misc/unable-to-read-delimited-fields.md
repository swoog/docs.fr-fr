---
title: Impossible de lire les champs délimités, car un guillemet double ne constitue pas un délimiteur conforme lorsque EscapeQuotes a la valeur True
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_IllegalDelimiter
ms.assetid: ab8a0c3a-b89c-4617-9e31-7e81f5dca433
ms.openlocfilehash: a119bf2592982b87c4bd361f9d125e6e8b7173c1
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44087223"
---
# <a name="unable-to-read-delimited-fields-because-a-double-quote-is-not-a-legal-delimiter-when-escapequotes-is-set-to-true"></a>Impossible de lire les champs délimités, car un guillemet double ne constitue pas un délimiteur conforme lorsque EscapeQuotes a la valeur True
Le `TextFieldParser` ne peut pas lire le fichier, car un guillemet (") a été fourni comme délimiteur et `EscapeQuotes` a la valeur `True`.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Affectez la valeur `EscapeQuotes` à `False`.  
  
## <a name="see-also"></a>Voir aussi

- [TextFieldParser.SetDelimiters, méthode](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.SetDelimiters%2A)  
- [TextFieldParser.Delimiters, propriété](xref:Microsoft.VisualBasic.FileIO.TextFieldParser.Delimiters%2A)  
- [Guide pratique : lire des fichiers texte délimités par des virgules](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)  
- [TextFieldParser (objet)](../../visual-basic/language-reference/objects/textfieldparser-object.md)
