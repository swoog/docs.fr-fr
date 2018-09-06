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
ms.openlocfilehash: 3b031c6e3dc04637128f95ca8e922d3298981287
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863201"
---
# <a name="character-data-types-visual-basic"></a>Types de données caractères (Visual Basic)
Visual Basic fournit *les types de données character* à gérer avec des caractères imprimables et affichables. Reconnaissent les caractères Unicode, `Char` contient un caractère tandis que `String` contient un nombre indéfini de caractères.  
  
 Pour une table qui affiche une comparaison côte à côte des types de données Visual Basic, consultez [Types de données](../../../../visual-basic/language-reference/data-types/index.md).  
  
## <a name="char-type"></a>Char, Type  
 Le `Char` type de données est un caractère de Unicode sur deux octets (16 bits) unique. Si une variable stocke toujours exactement un caractère, déclarez-le en tant que `Char`. Exemple :  
  
 [!code-vb[VbVbalrCharTypes#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrchartypes/vb/module1.vb#1)]
  
 Chaque valeur possible dans un `Char` ou `String` variable est un *point de code*, ou code de caractère, dans le jeu de caractères Unicode. Les caractères Unicode incluent le jeu de caractères ASCII base, différents autres lettres de l’alphabet, les accents, les symboles monétaires, fractions, les signes diacritiques et symboles mathématiques et techniques.  
  
> [!NOTE]
>  Les points de code D800 à DFFF (55 296 à 55 551 décimal) pour les réserves de ressources de jeu de caractères Unicode *paires de substitution*, qui requiert des deux valeurs 16 bits pour représenter un seul point de code. Un `Char` variable ne peut pas contenir une paire de substitution et un `String` utilise deux positions pour contenir une paire.  
  
 Pour plus d’informations, consultez [Type de données Char](../../../../visual-basic/language-reference/data-types/char-data-type.md).  
  
## <a name="string-type"></a>Type de chaîne  
 Le `String` type de données est une séquence de zéro ou plusieurs caractères Unicode à deux octets (16 bits). Si une variable peut contenir un nombre indéfini de caractères, déclarez-le en tant que `String`. Exemple :  
  
 [!code-vb[VbVbalrCharTypes#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/vbvbalrchartypes/vb/module1.vb#2)]
  
 Pour plus d’informations, consultez [Type de données String](../../../../visual-basic/language-reference/data-types/string-data-type.md).  
  
## <a name="see-also"></a>Voir aussi  
 [Types de données élémentaires](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)  
 [Types de données composites](../../../../visual-basic/programming-guide/language-features/data-types/composite-data-types.md)  
 [Types génériques en Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)  
 [Types valeur et types référence](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)  
 [Conversions de type en Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)  
 [Dépannage des types de données](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 [Caractères de type](../../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)
