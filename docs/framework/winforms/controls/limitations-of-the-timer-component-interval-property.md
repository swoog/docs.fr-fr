---
title: Restrictions relatives à la propriété Interval du composant Timer Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- timers [Windows Forms], event intervals
- Interval property [Windows Forms], limitations
- timers [Windows Forms], Windows-based
- Timer component [Windows Forms], limitations of Interval property
ms.assetid: 7e5fb513-77e7-4046-a8e8-aab94e61ca0f
ms.openlocfilehash: a9c4fda179e45ad2cf2ee2183e5881e97b763cdc
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64644940"
---
# <a name="limitations-of-the-windows-forms-timer-components-interval-property"></a>Restrictions relatives à la propriété Interval du composant Timer Windows Forms
Les formulaires Windows <xref:System.Windows.Forms.Timer> composant possède un <xref:System.Windows.Forms.Timer.Interval%2A> propriété qui spécifie le nombre de millisecondes qui s’écouler entre deux événements de minuterie suivant. Sauf si le composant est désactivé, une minuterie continue à recevoir le <xref:System.Windows.Forms.Timer.Tick> événement à intervalles réguliers à peu près égales.  
  
 Ce composant est conçu pour un environnement Windows Forms. Si vous avez besoin d’un minuteur adapté à un environnement de serveur, consultez l’article [Introduction aux minuteurs serveur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).  
  
## <a name="the-interval-property"></a>La propriété d’intervalle  
 Le <xref:System.Windows.Forms.Timer.Interval%2A> propriété présente quelques limitations à prendre en compte lorsque vous programmez un <xref:System.Windows.Forms.Timer> composant :  
  
- Si votre application ou une autre application effectue des demandes importantes sur le système, telles que les boucles longues, calculs complexes, ou le lecteur, réseau ou accès de port, votre application ne peut pas obtenir des événements de minuterie aussi souvent que le <xref:System.Windows.Forms.Timer.Interval%2A> propriété spécifie.  
  
- L’intervalle n’est pas garanti s’écouler exactement le moment. Pour garantir l’exactitude, la minuterie doit vérifier l’horloge système en fonction des besoins, plutôt que d’essayer de suivre en interne le temps écoulé.  
  
- La précision de la <xref:System.Windows.Forms.Timer.Interval%2A> propriété est exprimée en millisecondes. Certains ordinateurs fournissent un compteur haute résolution qui a une résolution supérieure aux millisecondes. La disponibilité de ce compteur varie selon le matériel de processeur de votre ordinateur.
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Timer>
- [Timer, composant](timer-component-windows-forms.md)
- [Vue d’ensemble du composant Timer](timer-component-overview-windows-forms.md)
