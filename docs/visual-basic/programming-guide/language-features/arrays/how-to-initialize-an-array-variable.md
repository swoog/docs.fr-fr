---
title: 'Procédure : Initialiser une Variable tableau en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], initializing
- arrays [Visual Basic], variables
- arrays [Visual Basic], initializing
- arrays [Visual Basic], declaring
ms.assetid: aadd7a60-7ca4-4608-b986-091f19e7fc10
ms.openlocfilehash: 4aa783d6179c72760a12d0259d587b5b38bb9140
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58832240"
---
# <a name="how-to-initialize-an-array-variable-in-visual-basic"></a>Procédure : Initialiser une Variable tableau en Visual Basic
Vous initialisez une variable tableau en incluant un littéral de tableau dans un `New` clause et en spécifiant les valeurs initiales du tableau. Vous pouvez spécifier le type ou pouvoir être déduit à partir des valeurs du littéral de tableau. Pour plus d’informations sur la façon dont le type est déduit, consultez « Remplissage d’un tableau avec des valeurs initiales » dans [tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md).  
  
### <a name="to-initialize-an-array-variable-by-using-an-array-literal"></a>Pour initialiser une variable de tableau à l’aide d’un littéral de tableau  
  
-   Dans le `New` clause, ou lorsque vous affectez la valeur de tableau, fournissez les valeurs d’élément à l’intérieur des accolades (`{}`). L’exemple suivant montre plusieurs façons de déclarer, créer et initialiser une variable destinée à contenir un tableau qui comporte des éléments de type `Char`.  
  
     [!code-vb[VbVbalrArrays#16](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#16)]  
  
     Après l’exécution de chaque instruction, le tableau créé a une longueur de 3, avec des éléments à l’index 0 à l’index 2 contenant les valeurs initiales. Si vous fournissez à la fois la limite supérieure et les valeurs, vous devez inclure une valeur pour chaque élément de l’index 0 jusqu'à la limite supérieure.  
  
     Notez que vous n’êtes pas obligé de spécifier la limite supérieure d’index si vous fournissez des valeurs d’éléments dans un littéral de tableau. Si aucune limite supérieure n’est spécifié, la taille du tableau est déduite selon le nombre de valeurs dans le littéral de tableau.  
  
### <a name="to-initialize-a-multidimensional-array-variable-by-using-array-literals"></a>Pour initialiser une variable de tableau multidimensionnel à l’aide de littéraux de tableau  
  
-   Imbriquez des valeurs à l’intérieur des accolades (`{}`) entre accolades. Vérifiez que les littéraux de tableau imbriqué que tous déduits en tant que tableaux du même type et de longueur. L’exemple de code suivant montre plusieurs exemples d’initialisation de tableau multidimensionnel.  
  
     [!code-vb[VbVbalrArrays#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#17)]  
  
-   Vous pouvez explicitement spécifier les limites du tableau, ou les ignorer et que le compilateur déduire les limites du tableau en fonction des valeurs du littéral de tableau. Si vous fournissez à la fois les limites supérieures et les valeurs, vous devez inclure une valeur pour chaque élément de l’index 0 jusqu'à la limite supérieure dans chaque dimension. L’exemple suivant montre plusieurs façons de déclarer, créer et initialiser une variable destinée à contenir un tableau à deux dimensions qui comporte des éléments de type `Short`  
  
     [!code-vb[VbVbalrArrays#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#18)]  
  
     Après l’exécution de chaque instruction, le tableau créé contient six éléments initialisés ayant les index `(0,0)`, `(0,1)`, `(0,2)`, `(1,0)`, `(1,1)`, et `(1,2)`. Chaque emplacement de tableau contient la valeur `10`.  
  
-   L’exemple suivant effectue une itération dans un tableau multidimensionnel. Dans une application de console Windows qui est écrit en Visual Basic, collez le code à l’intérieur de la `Sub Main()` (méthode). Les derniers commentaires illustrent la sortie.  
  
     [!code-vb[VbVbalrArrays#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#31)]  
  
### <a name="to-initialize-a-jagged-array-variable-by-using-array-literals"></a>Pour initialiser une variable tableau en escalier à l’aide de littéraux de tableau  
  
-   Imbriquez des valeurs d’objet à l’intérieur des accolades (`{}`). Bien que vous pouvez également imbriquer des littéraux de tableaux qui spécifient des tableaux de longueurs différentes, dans le cas d’un tableau en escalier, assurez-vous que les littéraux de tableaux imbriqués soient placés entre parenthèses (`()`). Les parenthèses forcent l’évaluation des littéraux de tableaux imbriqués et les tableaux obtenus sont utilisés comme valeurs initiales du tableau en escalier. L’exemple de code suivant montre deux exemples d’initialisation de tableau en escalier.  
  
     [!code-vb[VbVbalrArrays#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#19)]  
  
-   L’exemple suivant effectue une itération dans un tableau en escalier. Dans une application de console Windows qui est écrit en Visual Basic, collez le code à l’intérieur de la `Sub Main()` (méthode).  Les derniers commentaires dans le code affichent la sortie.  
  
     [!code-vb[VbVbalrArrays#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrArrays/VB/Class1.vb#32)]  
  
## <a name="see-also"></a>Voir aussi

- [Tableaux](../../../../visual-basic/programming-guide/language-features/arrays/index.md)
- [Dépannage des tableaux](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)
