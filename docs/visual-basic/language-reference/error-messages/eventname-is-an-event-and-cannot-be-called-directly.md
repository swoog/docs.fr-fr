---
title: "'<eventname>' est un événement. Il ne peut donc pas être appelé directement"
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: bf900566bdb4ecf8d8961a12b5dd67ba426caf27
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59305596"
---
# <a name="eventname-is-an-event-and-cannot-be-called-directly"></a>'\<nom_événement >' est un événement et ne peut pas être appelée directement
' <`eventname`>' est un événement et ne peut donc pas être appelé directement. Utilisez un `RaiseEvent` instruction pour déclencher un événement.  
  
 Un appel de procédure spécifie un événement pour le nom de la procédure. Un gestionnaire d’événements est une procédure, mais l’événement lui-même est un dispositif de signalisation, qui doit être déclenché et géré.  
  
 **ID d’erreur :** BC32022  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Utilisez un `RaiseEvent` instruction pour signaler un événement et appeler les procédures qui le gèrent.  
  
## <a name="see-also"></a>Voir aussi

- [RaiseEvent (instruction)](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
