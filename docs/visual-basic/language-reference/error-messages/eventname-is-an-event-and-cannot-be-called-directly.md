---
title: '&#39;&lt;nom_événement&gt; &#39; est un événement et ne peut pas être appelée directement'
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: 4d8a7d716d2b7c52d1d027a1e7959d981bb0857e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33587330"
---
# <a name="39lteventnamegt39-is-an-event-and-cannot-be-called-directly"></a>&#39;&lt;nom_événement&gt; &#39; est un événement et ne peut pas être appelée directement
' <`eventname`>' est un événement et ne peut donc pas être appelé directement. Utilisez un `RaiseEvent` instruction pour déclencher un événement.  
  
 Un appel de procédure spécifie un événement pour le nom de la procédure. Un gestionnaire d’événements est une procédure, mais l’événement lui-même est un dispositif de signalisation qui doit être déclenché et géré.  
  
 **ID d’erreur :** BC32022  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Utilisez un `RaiseEvent` instruction pour signaler un événement et appeler les procédures qui le gèrent.  
  
## <a name="see-also"></a>Voir aussi  
 [RaiseEvent (instruction)](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
