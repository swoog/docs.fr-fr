---
title: L'objet ou la classe ne prend pas en charge le jeu d'événements
ms.date: 07/20/2015
f1_keywords:
- vbrID459
ms.assetid: 785df3f3-2aae-4a25-af36-1f9879d4e5fd
ms.openlocfilehash: 4a6f1f59f43cdb351d49fbcbfd18362db888586e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593202"
---
# <a name="object-or-class-does-not-support-the-set-of-events"></a>L'objet ou la classe ne prend pas en charge le jeu d'événements
Vous avez essayé d’utiliser un `WithEvents` variable avec un composant qui ne peut pas fonctionner en tant que source d’événements pour le jeu d’événements spécifié. Par exemple, vous souhaitez recevoir les événements d’un objet, puis créer un autre objet qui `Implements` le premier objet. Même si vous pensez que vous pouvez recevoir les événements de l’objet implémenté, ce n’est pas toujours le cas. `Implements` implémente uniquement une interface pour les méthodes et propriétés. `WithEvents` n’est pas prise en charge privé `UserControls`, car les informations de type nécessaires pour déclencher le `ObjectEvent` n’est pas disponible au moment de l’exécution.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Vous ne pouvez pas recevoir d’événements pour un composant qui ne fournit pas d’événements.  
  
## <a name="see-also"></a>Voir aussi  
 [WithEvents](../../../visual-basic/language-reference/modifiers/withevents.md)  
 [Implements (instruction)](../../../visual-basic/language-reference/statements/implements-statement.md)
