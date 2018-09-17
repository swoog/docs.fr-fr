---
title: add (Référence C#)
ms.date: 07/20/2015
f1_keywords:
- add_CSharpKeyword
helpviewer_keywords:
- add event accessor [C#]
ms.assetid: faf30b99-10e8-45cd-ab9a-57585d4d1d8d
ms.openlocfilehash: b55827b60a89da2569fad9da135c84571a24b094
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2018
ms.locfileid: "45592995"
---
# <a name="add-c-reference"></a>add (Référence C#)
Le mot clé contextuel `add` est utilisé pour définir un accesseur d’événement personnalisé qui est appelé quand le code client s’abonne à votre événement ([event](../../../csharp/language-reference/keywords/event.md)). Si vous fournissez un accesseur `add` personnalisé, vous devez également fournir un accesseur [remove](../../../csharp/language-reference/keywords/remove.md).  
  
## <a name="example"></a>Exemple  
 L’exemple suivant illustre un événement qui a des accesseurs `add` et [remove](../../../csharp/language-reference/keywords/remove.md) personnalisés. Pour obtenir l’exemple complet, consultez [Guide pratique pour implémenter des événements d’interface](../../../csharp/programming-guide/events/how-to-implement-interface-events.md).  
  
[!code-csharp[csrefKeywordsContextual#15](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#15)]
  
 En général, vous n’avez pas besoin de fournir vos propres accesseurs d’événements personnalisés. Les accesseurs générés automatiquement par le compilateur quand vous déclarez un événement sont suffisants pour la plupart des scénarios.  
  
## <a name="see-also"></a>Voir aussi  
- [Événements](../../../csharp/programming-guide/events/index.md)
