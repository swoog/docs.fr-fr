---
title: L'objet ou la classe ne prend pas en charge le jeu d'événements
ms.date: 07/20/2015
f1_keywords:
- vbrID459
ms.assetid: 785df3f3-2aae-4a25-af36-1f9879d4e5fd
ms.openlocfilehash: ad9176b5332a75f03968e742501c3fce541055de
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59342880"
---
# <a name="object-or-class-does-not-support-the-set-of-events"></a>L'objet ou la classe ne prend pas en charge le jeu d'événements
Vous avez essayé d’utiliser un `WithEvents` variable avec un composant qui ne peut pas fonctionner comme une source d’événement pour le jeu d’événements spécifié. Par exemple, vous souhaitez recevoir les événements d’un objet, puis créer un autre objet qui `Implements` le premier objet. Même si vous pensez que pouvoir recevoir les événements de l’objet implémenté, ce n’est pas toujours le cas. `Implements` implémente uniquement une interface pour les méthodes et propriétés. `WithEvents` n’est pas pris en charge pour private `UserControls`, car les informations de type nécessaires pour déclencher le `ObjectEvent` n’est pas disponible au moment de l’exécution.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1. Vous ne pouvez pas recevoir d’événements pour un composant qui ne fournit pas d’événements.  
  
## <a name="see-also"></a>Voir aussi

- [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md)
- [Implements, instruction](../../../visual-basic/language-reference/statements/implements-statement.md)
