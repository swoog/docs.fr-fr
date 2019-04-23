---
title: Vue d'ensemble du composant Timer (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- Timer
helpviewer_keywords:
- Timer component [Windows Forms], about Timer components
- timers [Windows Forms], about timers
ms.assetid: e672c05b-a8b6-4b26-9e4d-9223aa9e3873
ms.openlocfilehash: 5bef0ba87d6a496acf7575965128be2b20b437ab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59074207"
---
# <a name="timer-component-overview-windows-forms"></a>Vue d'ensemble du composant Timer (Windows Forms)
<xref:System.Windows.Forms.Timer> est un composant Windows Forms qui déclenche un événement à intervalles réguliers. Ce composant est conçu pour un environnement Windows Forms. Si vous avez besoin d’un minuteur adapté à un environnement de serveur, consultez l’article [Introduction aux minuteurs serveur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).  
  
## <a name="key-properties-methods-and-events"></a>Événements, méthodes et propriétés de clé  
 La durée des intervalles est définie par le <xref:System.Windows.Forms.Timer.Interval%2A> propriété, dont la valeur est exprimée en millisecondes. Lorsque le composant est activé, le <xref:System.Windows.Forms.Timer.Tick> événement est déclenché chaque intervalle. Voici où vous devez ajouter le code qui doit être exécuté. Pour plus d'informations, voir [Procédure : Exécuter des procédures à intervalles définis avec le composant Timer Windows Forms](run-procedures-at-set-intervals-with-wf-timer-component.md). Les principales méthodes de la <xref:System.Windows.Forms.Timer> composant sont <xref:System.Windows.Forms.Timer.Start%2A> et <xref:System.Windows.Forms.Timer.Stop%2A>, lequel activer le minuteur et désactiver. Lorsque la minuterie est désactivée, elle est réinitialisée ; Il n’existe aucun moyen pour suspendre un <xref:System.Windows.Forms.Timer> composant.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Timer>
- [Timer, composant](timer-component-windows-forms.md)
- [Restrictions relatives à la propriété Interval du composant Timer Windows Forms](limitations-of-the-timer-component-interval-property.md)
