---
title: Événements (Guide de programmation C#)
ms.date: 07/20/2015
helpviewer_keywords:
- classes [C#], events
- C# language, events
- events [C#]
ms.assetid: a8e51b22-d294-44fb-9539-0072f06c4cb3
ms.openlocfilehash: 5b844b20ac62b4cbc2a73931eecab95f22b4b1de
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33339915"
---
# <a name="events-c-programming-guide"></a>Événements (Guide de programmation C#)
Les événements permettent à une [classe](../../../csharp/language-reference/keywords/class.md) ou à un objet de notifier d’autres classes ou objets quand quelque chose de significatif se produit. La classe qui envoie (ou *déclenche*) l’événement est appelée *publieur* et les classes qui reçoivent (ou *gèrent*) l’événement sont appelées *abonnés*.  
  
 Dans une application C# Windows Forms ou web classique, vous vous abonnez à des événements déclenchés par des contrôles, comme des boutons et des zones de liste. Vous pouvez utiliser l’IDE Visual C# pour parcourir les événements publiés par un contrôle et sélectionner ceux que vous voulez gérer. L’IDE ajoute automatiquement une méthode de gestionnaire d’événements vide et le code pour vous abonner à l’événement. Pour plus d’informations, consultez [Guide pratique pour s’abonner et annuler l’abonnement à des événements](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md).  
  
## <a name="events-overview"></a>Vue d'ensemble des événements  
 Les événements ont les propriétés suivantes :  
  
-   Le publieur détermine quand un événement est déclenché ; les abonnés déterminent l’action entreprise en réponse à l’événement.  
  
-   Un événement peut avoir plusieurs abonnés. Un abonné peut gérer plusieurs événements provenant de plusieurs publieurs.  
  
-   Les événements qui n’ont aucun abonné ne sont jamais déclenchés.  
  
-   Les événements sont généralement utilisés pour signaler des actions de l’utilisateur, comme les clics de bouton ou les sélections de menu dans les interfaces utilisateur graphiques.  
  
-   Quand un événement a plusieurs abonnés, les gestionnaires d’événements sont appelées de façon synchrone quand un événement est déclenché. Pour appeler des événements de façon asynchrone, consultez [Calling Synchronous Methods Asynchronously](../../../../docs/standard/asynchronous-programming-patterns/calling-synchronous-methods-asynchronously.md).  
  
-   Dans la bibliothèque de classes [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] , les événements sont basés sur le délégué <xref:System.EventHandler> et la classe de base <xref:System.EventArgs> .  
  
## <a name="related-sections"></a>Rubriques connexes  
 Pour plus d'informations, voir :  
  
-   [Guide pratique pour s’abonner et se désabonner d’événements](../../../csharp/programming-guide/events/how-to-subscribe-to-and-unsubscribe-from-events.md)  
  
-   [Comment : publier des événements conformes aux indications du .NET Framework](../../../csharp/programming-guide/events/how-to-publish-events-that-conform-to-net-framework-guidelines.md)  
  
-   [Comment : déclencher les événements de la classe de base dans les classes dérivées](../../../csharp/programming-guide/events/how-to-raise-base-class-events-in-derived-classes.md)  
  
-   [Guide pratique d’implémentation d’événements d’interface](../../../csharp/programming-guide/events/how-to-implement-interface-events.md)  
  
-   [Synchronisation des threads](../../../csharp/programming-guide/concepts/threading/thread-synchronization.md)  
  
-   [Comment : utiliser un dictionnaire pour stocker des instances d’événements](../../../csharp/programming-guide/events/how-to-use-a-dictionary-to-store-event-instances.md)  
  
-   [Comment : implémenter des accesseurs d’événement personnalisés](../../../csharp/programming-guide/events/how-to-implement-custom-event-accessors.md)  
  
## <a name="c-language-specification"></a>Spécification du langage C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="featured-book-chapters"></a>Chapitres proposés  
 [Delegates, Events, and Lambda Expressions](https://msdn.microsoft.com/library/orm-9780596516109-03-09.aspx) (Délégués, événements et expressions lambda) dans [C# 3.0 Cookbook, Third Edition: More than 250 solutions for C# 3.0 programmers](https://msdn.microsoft.com/library/orm-9780596516109-03.aspx)  
  
 [Delegates and Events](https://msdn.microsoft.com/library/orm-9780596521066-01-17.aspx) dans [Learning C# 3.0: Master the fundamentals of C# 3.0](https://msdn.microsoft.com/library/orm-9780596521066-01.aspx)  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.EventHandler>  
 [Guide de programmation C#](../../../csharp/programming-guide/index.md)  
 [Délégués](../../../csharp/programming-guide/delegates/index.md)  
 [Création de gestionnaires d’événements dans les Windows Forms](../../../../docs/framework/winforms/creating-event-handlers-in-windows-forms.md)  
 [Programmation multithread avec le modèle asynchrone basé sur les événements](../../../../docs/standard/asynchronous-programming-patterns/multithreaded-programming-with-the-event-based-asynchronous-pattern.md)
