---
title: 'Comment : créer une variable (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- Dim statement [Visual Basic]
- variables [Visual Basic], creating
ms.assetid: 35300be3-77b0-4bef-a156-034d3cdedde0
ms.openlocfilehash: f2e6a97e78bc42ebea9519eb0aa4411e9aec24cf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-create-a-new-variable-visual-basic"></a>Comment : créer une variable (Visual Basic)
Vous créez une variable avec un [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md).  
  
### <a name="to-create-a-new-variable"></a>Pour créer une variable  
  
1.  Déclarez la variable dans un `Dim` instruction.  
  
    ```  
    Dim newCustomer  
    ```  
  
2.  Inclure les spécifications pour les caractéristiques de la variable, tel que [privé](../../../../visual-basic/language-reference/modifiers/private.md), [statique](../../../../visual-basic/language-reference/modifiers/static.md), [ombres](../../../../visual-basic/language-reference/modifiers/shadows.md), ou [WithEvents](../../../../visual-basic/language-reference/modifiers/withevents.md). Pour plus d’informations, consultez [caractéristiques de l’élément déclaré](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md).  
  
    ```  
    Public Static newCustomer  
    ```  
  
     Vous n’avez pas besoin du `Dim` mot clé si vous utilisez d’autres mots clés dans la déclaration.  
  
3.  Suivez les spécifications de nom de la variable qui doit respecter les conventions et les règles de Visual Basic. Pour plus d’informations, consultez [noms d’élément déclaré](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md).  
  
    ```  
    Public Static newCustomer  
    ```  
  
4.  Suivre le nom de la [comme](../../../../visual-basic/language-reference/statements/as-clause.md) clause pour spécifier le type de données de la variable.  
  
    ```  
    Public Static newCustomer As Customer  
    ```  
  
     Si vous ne spécifiez pas le type de données, il utilise la valeur par défaut : `Object`.  
  
5.  Suivez les `As` clause avec un signe égal (`=`) et suivez le signe égal, la valeur de la variable initiale.  
  
     Visual Basic assigne la valeur spécifiée à la variable à chaque fois qu’il exécute la `Dim` instruction. Si vous ne spécifiez pas une valeur initiale, Visual Basic assigne la valeur initiale de la valeur par défaut pour le type de données de la variable lorsqu’il entre d’abord dans le code qui contient la `Dim` instruction.  
  
     Si la variable est un type référence, vous pouvez créer une instance de la classe en incluant le [nouvel opérateur](../../../../visual-basic/language-reference/operators/new-operator.md) mot clé dans le `As` clause. Si vous n’utilisez pas `New`, la valeur initiale de la variable est [rien](../../../../visual-basic/language-reference/nothing.md).  
  
    ```  
    Public Static newCustomer As New Customer  
    ```  
  
## <a name="see-also"></a>Voir aussi  
 [Variables](../../../../visual-basic/programming-guide/language-features/variables/index.md)  
 [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)  
 [Noms d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)  
 [Caractéristiques d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md)  
 [Types valeur et types référence](../../../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md)  
 [Instructions](../../../../visual-basic/language-reference/statements/index.md)  
 [Inférence de type local](../../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)  
 [Option Infer (instruction)](../../../../visual-basic/language-reference/statements/option-infer-statement.md)
