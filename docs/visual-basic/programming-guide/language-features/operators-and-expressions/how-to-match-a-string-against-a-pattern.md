---
title: 'Procédure : Faire correspondre une chaîne à un modèle (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- comparison operators [Visual Basic], comparing strings
- pattern matching
- strings [Visual Basic], comparing
- string comparison [Visual Basic], operators
- Visual Basic code, operators
- pattern matching [Visual Basic], string comparison
- string comparison [Visual Basic]
- Like operator [Visual Basic], pattern matching
- pattern matching, empty strings
- operators [Visual Basic], comparison
ms.assetid: 19a83804-b5af-4739-928b-ac93e64e457f
ms.openlocfilehash: ca6537d81f080120fcbea0cf083f450dce4e9f62
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58826013"
---
# <a name="how-to-match-a-string-against-a-pattern-visual-basic"></a>Procédure : Faire correspondre une chaîne à un modèle (Visual Basic)
Si vous souhaitez savoir si une expression de la [Type de données String](../../../../visual-basic/language-reference/data-types/string-data-type.md) satisfait à un modèle, vous pouvez ensuite utiliser le [opérateur Like](../../../../visual-basic/language-reference/operators/like-operator.md).  
  
 `Like` accepte deux opérandes. L’opérande gauche est une expression de chaîne, et l’opérande de droite est une chaîne contenant le modèle à utiliser pour la correspondance. `Like` Retourne un `Boolean` valeur indiquant si l’expression de chaîne est conforme au modèle.  
  
 Vous pouvez faire correspondre chaque caractère de l’expression de chaîne avec un caractère spécifique, un caractère générique, une liste de caractères ou une plage de caractères. Les positions des spécifications dans la chaîne de modèle correspondent vers les positions des caractères à mettre en correspondance dans l’expression de chaîne.  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-specific-character"></a>Pour mettre en correspondance un caractère de l’expression de chaîne avec un caractère spécifique  
  
-   Placez le caractère spécifique directement dans la chaîne de modèle. Certains caractères spéciaux doivent être entourés de crochets (`[ ]`). Pour plus d’informations, consultez [opérateur Like](../../../../visual-basic/language-reference/operators/like-operator.md).  
  
     L’exemple suivant teste si `myString` se compose exactement du caractère `H`.  
  
     [!code-vb[VbVbalrOperators#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#70)]  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-wildcard-character"></a>Pour mettre en correspondance un caractère de l’expression de chaîne avec un caractère générique  
  
-   Placez un point d’interrogation (`?`) dans la chaîne de modèle. N’importe quel caractère valide dans cette position rend une correspondance.  
  
     L’exemple suivant teste si `myString` se compose du caractère `W` suivi exactement deux caractères de toutes les valeurs.  
  
     [!code-vb[VbVbalrOperators#71](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#71)]  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-list-of-characters"></a>Pour mettre en correspondance un caractère dans l’expression de chaîne par rapport à une liste de caractères  
  
-   Placez les crochets (`[ ]`) dans la chaîne de modèle et à l’intérieur de crochets, mettez la liste de caractères. Ne séparez pas les caractères par des virgules ou tout autre séparateur. N’importe quel caractère unique dans la liste est en correspondance réussite.  
  
     L’exemple suivant teste si `myString` se compose de n’importe quel caractère valid, suivi par une seule des caractères `A`, `C`, ou `E`.  
  
     [!code-vb[VbVbalrOperators#72](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#72)]  
  
     Notez que cette correspondance respecte la casse.  
  
### <a name="to-match-a-character-in-the-string-expression-against-a-range-of-characters"></a>Pour mettre en correspondance un caractère de l’expression de chaîne avec une plage de caractères  
  
-   Placez les crochets (`[ ]`) dans la chaîne de modèle et à l’intérieur de crochets, mettez les caractères les plus élevés dans la plage, séparés par un trait d’union (`–`). N’importe quel caractère unique dans la plage effectue une correspondance.  
  
     L’exemple suivant teste si `myString` se compose des caractères `num` suivie exactement un des caractères `i`, `j`, `k`, `l`, `m`, ou `n`.  
  
     [!code-vb[VbVbalrOperators#73](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#73)]  
  
     Notez que cette correspondance respecte la casse.  
  
## <a name="matching-empty-strings"></a>Correspondance des chaînes vides  
 `Like` traite la séquence `[]` comme une chaîne de longueur nulle (`""`). Vous pouvez utiliser `[]` pour tester si l’expression de chaîne entière est vide, mais vous ne pouvez pas l’utiliser pour tester si une position particulière dans l’expression de chaîne est vide. Si une position vide est une des options que vous devez tester, vous pouvez utiliser `Like` plusieurs fois.  
  
#### <a name="to-match-a-character-in-the-string-expression-against-a-list-of-characters-or-no-character"></a>Pour mettre en correspondance un caractère dans l’expression de chaîne par rapport à une liste de caractères ou aucun caractère  
  
1.  Appelez le `Like` opérateur deux fois sur la même expression de chaîne et connectez les deux appels avec la [ou opérateur](../../../../visual-basic/language-reference/operators/or-operator.md) ou le [OrElse Operator](../../../../visual-basic/language-reference/operators/orelse-operator.md).  
  
2.  Dans la chaîne de modèle pour la première `Like` clause, incluent la liste de caractères placés entourée crochets (`[ ]`).  
  
3.  Dans la chaîne de modèle pour le deuxième `Like` clause, ne placez pas n’importe quel caractère à la position en question.  
  
     L’exemple suivant teste le numéro de téléphone à sept chiffres `phoneNum` pour exactement trois chiffres, suivis d’un espace, un trait d’union (`–`), une période (`.`), ou aucun caractère, ne suivi par exactement quatre chiffres.  
  
     [!code-vb[VbVbalrOperators#74](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#74)]  
  
## <a name="see-also"></a>Voir aussi

- [Opérateurs de comparaison](../../../../visual-basic/language-reference/operators/comparison-operators.md)
- [Opérateurs et expressions](../../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
- [Like (opérateur)](../../../../visual-basic/language-reference/operators/like-operator.md)
- [String (type de données)](../../../../visual-basic/language-reference/data-types/string-data-type.md)
