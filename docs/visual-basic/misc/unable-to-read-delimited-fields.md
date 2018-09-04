---
title: Impossible de lire les champs délimités, car un guillemet double ne constitue pas un délimiteur conforme lorsque EscapeQuotes a la valeur True
ms.date: 07/20/2015
f1_keywords:
- vbrTextFieldParser_IllegalDelimiter
ms.assetid: ab8a0c3a-b89c-4617-9e31-7e81f5dca433
ms.openlocfilehash: faa42c2fec5851857496b321dbdb53c16c43e8c1
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43525935"
---
# <a name="unable-to-read-delimited-fields-because-a-double-quote-is-not-a-legal-delimiter-when-escapequotes-is-set-to-true"></a>Impossible de lire les champs délimités, car un guillemet double ne constitue pas un délimiteur conforme lorsque EscapeQuotes a la valeur True
Le `TextFieldParser` ne peut pas lire le fichier, car un guillemet (") a été fourni comme délimiteur et `EscapeQuotes` a la valeur `True`.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Affectez la valeur `EscapeQuotes` à `False`.  
  
## <a name="see-also"></a>Voir aussi  
 [TextFieldParser.SetDelimiters, méthode](https://msdn.microsoft.com/library/21fa40ec-5866-4d0e-9fd9-c708a190dcc9)  
 [TextFieldParser.Delimiters, propriété](https://msdn.microsoft.com/library/4eb18f4d-3011-40a9-b668-be93eed0444f)  
 [Guide pratique : lire des fichiers texte délimités par des virgules](../../visual-basic/developing-apps/programming/drives-directories-files/how-to-read-from-comma-delimited-text-files.md)  
 [TextFieldParser (objet)](../../visual-basic/language-reference/objects/textfieldparser-object.md)
