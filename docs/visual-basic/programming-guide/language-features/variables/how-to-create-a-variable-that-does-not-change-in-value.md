---
title: 'Procédure : Créer une Variable qui ne Change pas de valeur (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- variables [Visual Basic], read-only
- variables [Visual Basic], constant value
ms.assetid: 86b59266-25df-4635-ae15-9b59c411d036
ms.openlocfilehash: 3a9fa93b69c9abb42b2dd7eae623048f3628999e
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64663571"
---
# <a name="how-to-create-a-variable-that-does-not-change-in-value-visual-basic"></a>Procédure : Créer une Variable qui ne Change pas de valeur (Visual Basic)
La notion d’une variable qui ne change pas sa valeur peut sembler contradictoire. Mais il existe des situations lors d’une constante n’est pas possible et il est utile de disposer d’une variable avec une valeur fixe. Dans ce cas, vous pouvez définir une variable membre avec le [ReadOnly](../../../../visual-basic/language-reference/modifiers/readonly.md) mot clé.  
  
 Vous ne pouvez pas utiliser le [instruction Const](../../../../visual-basic/language-reference/statements/const-statement.md) pour déclarer et affecter une valeur constante dans les circonstances suivantes :  
  
- La `Const` instruction n’accepte pas le type de données que vous souhaitez utiliser  
  
- Vous ne connaissez pas la valeur au moment de la compilation  
  
- Vous ne parvenez pas à calculer la valeur de constante au moment de la compilation  
  
### <a name="to-create-a-variable-that-does-not-change-in-value"></a>Pour créer une variable qui ne change pas de valeur  
  
1. Au niveau du module, déclarez une variable de membre avec le [instruction Dim](../../../../visual-basic/language-reference/statements/dim-statement.md)et incluent la [ReadOnly](../../../../visual-basic/language-reference/modifiers/readonly.md) mot clé.  
  
    ```  
    Dim ReadOnly timeStarted  
    ```  
  
     Vous pouvez spécifier `ReadOnly` uniquement sur une variable membre. Cela signifie que vous devez définir la variable au niveau du module, en dehors de toute procédure.  
  
2. Si vous pouvez calculer la valeur dans une seule instruction au moment de la compilation, utilisez une clause d’initialisation dans le `Dim` instruction. Suivez le [comme](../../../../visual-basic/language-reference/statements/as-clause.md) clause avec un signe égal (`=`), suivi par une expression. Assurez-vous que le compilateur peut évaluer cette expression à une valeur constante.  
  
    ```  
    Dim ReadOnly timeStarted As Date = Now  
    ```  
  
     Vous pouvez affecter une valeur à une `ReadOnly` variable une seule fois. Une fois que vous procédez ainsi, aucun code ne peut modifier jamais sa valeur.  
  
     Si vous ne connaissez pas la valeur au moment de la compilation, ou ne peut pas calculer au moment de la compilation dans une seule instruction, vous pouvez l’affecter au moment de l’exécution dans un constructeur. Pour ce faire, vous devez déclarer le `ReadOnly` variable au niveau de la classe ou structure. Dans le constructeur de cette classe ou structure, calculer la valeur fixe de la variable et affecter à la variable avant de retourner à partir du constructeur.  
  
## <a name="see-also"></a>Voir aussi

- [WriteOnly](../../../../visual-basic/language-reference/modifiers/writeonly.md)
- [Const (instruction)](../../../../visual-basic/language-reference/statements/const-statement.md)
