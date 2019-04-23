---
title: Valeurs de retour de référence (Visual Basic)
ms.date: 04/28/2017
helpviewer_keywords:
- variables [Visual Basic]
- ref return values [Visual Basic]
- ref returns [Visual Basic]
ms.assetid: 5ef0cc69-eb3a-4a67-92a2-78585f223cb5
ms.openlocfilehash: d0600f7d9030324160343e800c37e0f5e68bff61
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59133976"
---
# <a name="support-for-reference-return-values-visual-basic"></a>Prise en charge des valeurs de retour de référence (Visual Basic)

En commençant par C# 7.0, le C# prend en charge du langage *référencer des valeurs de retour*. Pour comprendre les valeurs de retour de référence est qu’ils sont le contraire des arguments qui sont passés par référence à une méthode. Lorsqu’un argument passé par référence est modifié, les modifications sont répercutées dans la valeur de la variable sur l’appelant. Lorsqu’une méthode fournit une valeur de retour de référence à un appelant, les modifications apportées à la valeur de retour de référence par l’appelant sont reflétées dans les données de la méthode appelée.

Visual Basic n’autorise pas les valeurs de retour vous permettent de créer des méthodes avec référence, mais il vous autorise à utiliser les valeurs de retour de référence. En d’autres termes, vous pouvez appeler une méthode avec une valeur de retour de référence et modifier cette valeur de retour, et les modifications apportées à la valeur de retour de référence sont répercutées dans les données de la méthode appelée.

## <a name="modifying-the-ref-return-value-directly"></a>Modification directe de la valeur de retour ref

Pour les méthodes qui réussissent et n’ont pas toujours `ByRef` paramètres, vous pouvez modifier directement la valeur de retour de référence. Pour cela, affectez la nouvelle valeur pour les expressions qui retourne la valeur de retour de référence. 

Ce qui suit C# exemple définit un `NumericValue.IncrementValue` valeur de retour de méthode qui incrémente une valeur interne et le retourne en tant que référence. 

[!code-csharp[Ref-Return](../../../../../samples/snippets/visualbasic/programming-guide/language-features/procedures/ref-returns1.cs)]

La référence de retourner la valeur est ensuite modifiée par l’appelant dans l’exemple Visual Basic suivant. Notez que la ligne avec la `NumericValue.IncrementValue` appel de méthode n’affecte pas une valeur à la méthode. Au lieu de cela, il attribue une valeur à la valeur de retour de référence retournée par la méthode.

[!code-vb[Ref-Return](../../../../../samples/snippets/visualbasic/programming-guide/language-features/procedures/use-ref-returns1.vb)]

## <a name="using-a-helper-method"></a>À l’aide d’une méthode d’assistance

Dans d’autres cas, modifier la valeur de retour de référence d’un appel de méthode directement toujours peut-être pas souhaitable. Par exemple, une méthode de recherche qui retourne une chaîne peut trouver pas toujours une correspondance. Dans ce cas, vous souhaitez modifier la valeur de retour de référence uniquement si la recherche est réussie.

Ce qui suit C# exemple illustre ce scénario. Il définit un `Sentence` classe écrite dans C# inclut un `FindNext` méthode qui recherche le mot suivant dans une phrase qui commence par une sous-chaîne spécifiée. La chaîne est retournée comme valeur de retour de référence et une variable `Boolean` passée par référence à la méthode indique si la recherche a réussi. La valeur de retour de référence indique que l’appelant peut uniquement pas de lire la valeur retournée ; il ou elle peut également la modifier, et cette modification est répercutée dans les données contenues en interne dans le `Sentence` classe.

[!code-csharp[Ref-Return](../../../../../samples/snippets/visualbasic/getting-started/ref-returns.cs)]

Modifier directement la référence de retourner la valeur dans ce cas n’est pas fiable, étant donné que l’appel de méthode peut échouer rechercher une correspondance et de retourner le premier mot dans la phrase. Dans ce cas, l’appelant sera modifier par inadvertance le premier mot de la phrase. Cela pourrait être bloqué par l’appelant retournant un `null` (ou `Nothing` en Visual Basic). Mais dans ce cas, la tentative de modifier une chaîne dont la valeur est `Nothing` lève un <xref:System.NullReferenceException>. Si peut également être évitée en l’appelant retournant <xref:System.String.Empty?displayProperty=nameWithType>, mais cela requiert que l’appelant définir une variable de chaîne dont la valeur est <xref:System.String.Empty?displayProperty=nameWithType>. Bien que l’appelant peut modifier cette chaîne, la modification elle-même n’a aucune utilité, étant donné que la chaîne modifiée n’a aucune relation avec les mots dans la phrase stockée par le `Sentence` classe.

La meilleure façon de gérer ce scénario consiste à passer la valeur de retour de référence par référence à une méthode d’assistance. La méthode d’assistance contient alors la logique pour déterminer si l’appel de méthode a réussi et, si elle le faisait, pour modifier la retour de référence valeur. L’exemple suivant fournit une implémentation possible.

[!code-vb[Ref-Return](../../../../../samples/snippets/visualbasic/getting-started/ref-return-helper.vb#1)]

## <a name="see-also"></a>Voir aussi

- [Passage des arguments par valeur et par référence](passing-arguments-by-value-and-by-reference.md)
- [Procédures dans Visual Basic](index.md)
