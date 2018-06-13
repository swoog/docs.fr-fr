---
title: remove (Référence C#)
ms.date: 07/20/2015
f1_keywords:
- remove_CSharpKeyword
helpviewer_keywords:
- remove event accessor [C#]
ms.assetid: c8223426-c17b-4fe2-8406-01564cf1dd2b
ms.openlocfilehash: 16a169ce1a0ef5dbc29739b2d808acb19737669e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33269117"
---
# <a name="remove-c-reference"></a>remove (Référence C#)
Le mot clé contextuel `remove` est utilisé pour définir un accesseur d’événement personnalisé qui est appelé quand le code client annule son abonnement à votre événement ([event](../../../csharp/language-reference/keywords/event.md)). Si vous fournissez un accesseur `remove` personnalisé, vous devez également fournir un accesseur [add](../../../csharp/language-reference/keywords/add.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre un événement qui a des accesseurs [add](../../../csharp/language-reference/keywords/add.md) et `remove` personnalisés. Pour obtenir l’exemple complet, consultez [Guide pratique pour implémenter des événements d’interface](../../../csharp/programming-guide/events/how-to-implement-interface-events.md).  
  
 [!code-csharp[csrefKeywordsContextual#15](../../../csharp/language-reference/keywords/codesnippet/CSharp/remove_1.cs)]  
  
 En général, vous n’avez pas besoin de fournir vos propres accesseurs d’événements personnalisés. Les accesseurs générés automatiquement par le compilateur quand vous déclarez un événement sont suffisants pour la plupart des scénarios.  
  
## <a name="see-also"></a>Voir aussi  
 [Événements](../../../csharp/programming-guide/events/index.md)
