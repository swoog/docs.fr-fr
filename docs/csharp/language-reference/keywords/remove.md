---
title: remove, mot clé contextuel - Référence C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- remove_CSharpKeyword
helpviewer_keywords:
- remove event accessor [C#]
ms.assetid: c8223426-c17b-4fe2-8406-01564cf1dd2b
ms.openlocfilehash: b5c604cbb0fef158750b0fa487374ab293795fc7
ms.sourcegitcommit: 8699383914c24a0df033393f55db3369db728a7b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65633718"
---
# <a name="remove-c-reference"></a>remove (Référence C#)

Le mot clé contextuel `remove` est utilisé pour définir un accesseur d’événement personnalisé qui est appelé quand le code client annule son abonnement à votre événement ([event](event.md)). Si vous fournissez un accesseur `remove` personnalisé, vous devez également fournir un accesseur [add](add.md).

## <a name="example"></a>Exemple

L’exemple suivant illustre un événement qui a des accesseurs [add](add.md) et `remove` personnalisés. Pour voir l’exemple complet, consultez [Guide pratique pour  implémenter des événements d’interface](../../programming-guide/events/how-to-implement-interface-events.md).

 [!code-csharp[csrefKeywordsContextual#15](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#15)]

En général, vous n’avez pas besoin de fournir vos propres accesseurs d’événements personnalisés. Les accesseurs générés automatiquement par le compilateur quand vous déclarez un événement sont suffisants pour la plupart des scénarios.

## <a name="see-also"></a>Voir aussi

- [Événements](../../programming-guide/events/index.md)
