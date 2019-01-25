---
title: 'Procédure : Déclarer des événements personnalisés pour éviter les blocages (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- declaring events [Visual Basic], custom
- events [Visual Basic], custom
- custom events [Visual Basic]
ms.assetid: 998b6a90-67c5-4d2c-8b11-366d3e355505
ms.openlocfilehash: e1fed68f4abffb0e20230f55b0ddeffc63f7c78d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691539"
---
# <a name="how-to-declare-custom-events-to-avoid-blocking-visual-basic"></a>Procédure : Déclarer des événements personnalisés pour éviter les blocages (Visual Basic)
Il existe plusieurs circonstances quand il est important de ce gestionnaire d’un événements ne bloquent pas les gestionnaires d’événements suivants. Événements personnalisés permettent à l’événement à appeler ses gestionnaires d’événements de façon asynchrone.  
  
 Par défaut, le champ de magasin de stockage pour une déclaration d’événement est un délégué multicast qui associe en série tous les gestionnaires d’événements. Cela signifie que si un gestionnaire met beaucoup de temps, il bloque les autres gestionnaires jusqu'à la fin. (Les gestionnaires d’événements valides doivent jamais exécuter les opérations de longue durée ou de blocage potentiellement).  
  
 Au lieu d’utiliser l’implémentation par défaut d’événements Visual Basic, vous pouvez utiliser un événement personnalisé à exécuter de façon asynchrone les gestionnaires d’événements.  
  
## <a name="example"></a>Exemple  
 Dans cet exemple, le `AddHandler` accesseur ajoute le délégué pour chaque gestionnaire de la `Click` événement à un <xref:System.Collections.ArrayList> stockés dans le `EventHandlerList` champ.  
  
 Lorsque le code déclenche le `Click` événement, le `RaiseEvent` accesseur appelle tous les délégués de gestionnaire d’événements de façon asynchrone à l’aide de la <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A> (méthode). Cette méthode appelle chaque gestionnaire sur un thread de travail et retourne immédiatement, afin de gestionnaires ne peut pas se bloquer mutuellement.  
  
 [!code-vb[VbVbalrEvents#27](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-custom-events-to-avoid-blocking_1.vb)]  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Collections.ArrayList>
- <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A>
- [Événements](../../../../visual-basic/programming-guide/language-features/events/index.md)
- [Guide pratique pour Déclarer des événements personnalisés pour économiser la mémoire](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-conserve-memory.md)
