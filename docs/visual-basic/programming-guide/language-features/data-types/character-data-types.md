---
title: Types de données caractères (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- data types [Visual Basic], character
- String data type [Visual Basic], character data types
- character data types [Visual Basic]
- Char data type [Visual Basic], character data types
- data types [Visual Basic], choosing
ms.assetid: 902479ef-1679-47fc-9911-0c1c5008226c
ms.openlocfilehash: 5a6a8dae63f3c0b5e3038304c1c2242f9e8c9c9d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33647386"
---
# <a name="character-data-types-visual-basic"></a>Types de données caractères (Visual Basic)
Visual Basic fournit *types de données caractère* afin de traiter les caractères imprimables et peut être affichée. Les caractères Unicode, alors que les deux `Char` contient un caractère tandis que `String` contient un nombre indéfini de caractères.  
  
 Pour une table qui affiche une comparaison côte-à-côte des types de données Visual Basic, consultez [des Types de données](../../../../visual-basic/language-reference/data-types/data-type-summary.md).  
  
## <a name="char-type"></a>Char (Type)  
 Le `Char` type de données est un caractère de Unicode (16 bits) sur deux octets. Si une variable stocke toujours exactement un caractère, déclarez-le en tant que `Char`. Par exemple :  
  
 [!code-vb[VbVbalrCharTypes#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrchartypes/vb/module1.vb#1)]
  
 Chaque valeur possible dans un `Char` ou `String` variable est un *point de code*, ou le code de caractère, dans le jeu de caractères Unicode. Les caractères Unicode incluent le jeu de caractères ASCII base, divers autres lettres de l’alphabet, les accents, les symboles monétaires, fractions, signes diacritiques et symboles mathématiques et techniques.  
  
> [!NOTE]
>  Les points de code D800 à DFFF (55 296 à 55 551 décimal) pour les réserves de ressources de jeu de caractères Unicode *paires de substitution*, qui requièrent deux valeurs de 16 bits pour représenter un seul point de code. A `Char` variable ne peut pas contenir une paire de substitution et un `String` utilise deux positions pour contenir une telle paire.  
  
 Pour plus d’informations, consultez [Type de données Char](../../../../visual-basic/language-reference/data-types/char-data-type.md).  
  
## <a name="string-type"></a>Type de chaîne  
 Le `String` type de données est une séquence de zéro ou plusieurs caractères Unicode à deux octets (16 bits). Si une variable peut contenir un nombre indéfini de caractères, déclarez-le en tant que `String`. Par exemple :  
  
 [!code-vb[VbVbalrCharTypes#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrchartypes/vb/module1.vb#2)]
  
 Pour plus d’informations, consultez [Type de données String](../../../../visual-basic/language-reference/data-types/string-data-type.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Types de données élémentaires](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)  
 [Types de données composites](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)  
 [Types génériques en Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)  
 [Types valeur et types référence](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)  
 [Conversions de type dans Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)  
 [Dépannage des types de données](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 [Caractères de type](../../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)
