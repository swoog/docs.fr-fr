---
title: '&#39;&lt;EventName&gt; &#39; est un événement et ne peut pas être appelée directement'
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: 3efd8c18497ce288e16659db4ca4693d5a3e6acc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54581992"
---
# <a name="39lteventnamegt39-is-an-event-and-cannot-be-called-directly"></a>&#39;&lt;EventName&gt; &#39; est un événement et ne peut pas être appelée directement
' <`eventname`>' est un événement et ne peut donc pas être appelé directement. Utilisez un `RaiseEvent` instruction pour déclencher un événement.  
  
 Un appel de procédure spécifie un événement pour le nom de la procédure. Un gestionnaire d’événements est une procédure, mais l’événement lui-même est un dispositif de signalisation, qui doit être déclenché et géré.  
  
 **ID d’erreur :** BC32022  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Utilisez un `RaiseEvent` instruction pour signaler un événement et appeler les procédures qui le gèrent.  
  
## <a name="see-also"></a>Voir aussi
- [RaiseEvent (instruction)](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
