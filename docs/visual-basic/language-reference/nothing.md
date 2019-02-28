---
title: Nothing (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- Nothing
- vb.Nothing
helpviewer_keywords:
- Nothing keyword [Visual Basic]
- Nothing keyword [Visual Basic], syntax
ms.assetid: 06176e2d-bbf7-4a37-afaa-a86ad21ee99f
ms.openlocfilehash: b8dfc166681dbadf1d2f4ba5a985011f5427f50a
ms.sourcegitcommit: 40364ded04fa6cdcb2b6beca7f68412e2e12f633
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/28/2019
ms.locfileid: "56981424"
---
# <a name="nothing-visual-basic"></a>Nothing (Visual Basic)
Représente la valeur par défaut de n’importe quel type de données. Pour les types référence, la valeur par défaut est le `null` référence. Pour les types de valeur, la valeur par défaut varie selon que le type de valeur est nullable.  
  
> [!NOTE]
>  Pour les types de valeur non nullable, `Nothing` en Visual Basic diffère `null` dans C#. En Visual Basic, si vous définissez une variable d’un type valeur non nullable à `Nothing`, la variable est définie sur la valeur par défaut pour son type déclaré. Dans C#, si vous assignez une variable d’un type valeur non nullable à `null`, une erreur de compilation se produit.  
  
## <a name="remarks"></a>Notes  
 `Nothing` représente la valeur par défaut d’un type de données. La valeur par défaut varie selon que la variable est d’un type valeur ou d’un type référence.  
  
 Une variable d’un *type valeur* directement contient sa valeur. Valeur incluent tous les types de données numérique, `Boolean`, `Char`, `Date`, toutes les structures et toutes les énumérations. Une variable d’un *type référence* stocke une référence à une instance de l’objet en mémoire. Types référence comprennent les classes, les tableaux, les délégués et les chaînes. Pour plus d'informations, consultez [Value Types and Reference Types](../../visual-basic/programming-guide/language-features/data-types/value-types-and-reference-types.md).  
  
 Si une variable est d’une valeur de type, le comportement de `Nothing` varie selon que la variable est un type nullable. Pour représenter un type valeur nullable, ajoutez un `?` modificateur au nom de type. Affectation `Nothing` à une variable nullable définit la valeur sur `null`. Pour plus d’informations et des exemples, consultez [des Types valeur Nullable](../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md).  
  
 Si une variable est d’un type valeur qui n’est pas nullable, affectez `Nothing` à elle lui affecte la valeur par défaut pour son type déclaré. Si ce type contient des variables membres, ils sont prêts à leurs valeurs par défaut. L’exemple suivant illustre cela pour les types scalaires.  
  
 [!code-vb[VbVbalrKeywords#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class2.vb#7)]  
  
 Si une variable est de type référence, affectez `Nothing` à la variable lui affecte un `null` référence de type de la variable. Une variable qui est définie sur une `null` référence n’est pas associée à n’importe quel objet. Cela est illustré par l'exemple suivant.  
  
 [!code-vb[VbVbalrKeywords#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/class3.vb#8)]  
  
 Lors de la vérification si une référence (ou un type de valeur nullable) est variable `null`, n’utilisez pas `= Nothing` ou `<> Nothing`. Utilisez toujours `Is Nothing` ou `IsNot Nothing`.  
  
 Pour les chaînes en Visual Basic, la chaîne vide est égal à `Nothing`. Par conséquent, `"" = Nothing` a la valeur true.  
  
 L’exemple suivant montre les comparaisons qui utilisent la `Is` et `IsNot` opérateurs.  
  
 [!code-vb[VbVbalrKeywords#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrKeywords/VB/Class4.vb#9)]  
  
 Si vous déclarez une variable sans utiliser un `As` clause et affectez-lui la valeur `Nothing`, la variable a un type de `Object`. Est un exemple `Dim something = Nothing`. Une erreur de compilation se produit dans ce cas lorsque `Option Strict` se trouve sur et `Option Infer` est désactivé.  
  
 Lorsque vous assignez `Nothing` à une variable objet, il ne fait plus référence à une instance d’objet. Si la variable se rapportait précédemment à une instance, configurez-la sur `Nothing` n’arrête pas l’instance elle-même. L’instance est arrêtée, et les ressources mémoire et système associées sont libérées uniquement une fois que le garbage collector (GC) détecte qu’il n’y a aucune référence active restante.  
  
 `Nothing` diffère la <xref:System.DBNull> objet qui représente un variant non initialisé ou une colonne de base de données qui n’existe pas.  
  
## <a name="see-also"></a>Voir aussi
- [Dim (instruction)](../../visual-basic/language-reference/statements/dim-statement.md)
- [Durée de vie d’objet : Comment les objets sont créés et détruits](../../visual-basic/programming-guide/language-features/objects-and-classes/object-lifetime-how-objects-are-created-and-destroyed.md)
- [Durée de vie en Visual Basic](../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)
- [Is (opérateur)](../../visual-basic/language-reference/operators/is-operator.md)
- [IsNot (opérateur)](../../visual-basic/language-reference/operators/isnot-operator.md)
- [Types valeur Nullable](../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
