---
title: Limitations du composant Timer Windows Forms&#39;s propriété d’intervalle
ms.date: 03/30/2017
helpviewer_keywords:
- timers [Windows Forms], event intervals
- Interval property [Windows Forms], limitations
- timers [Windows Forms], Windows-based
- Timer component [Windows Forms], limitations of Interval property
ms.assetid: 7e5fb513-77e7-4046-a8e8-aab94e61ca0f
ms.openlocfilehash: e5b9e7e43369913f0cdc9c7f2111bd4fe58675e6
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43465653"
---
# <a name="limitations-of-the-windows-forms-timer-component39s-interval-property"></a>Limitations du composant Timer Windows Forms&#39;s propriété d’intervalle
Les formulaires Windows <xref:System.Windows.Forms.Timer> composant possède un <xref:System.Windows.Forms.Timer.Interval%2A> propriété qui spécifie le nombre de millisecondes qui s’écouler entre deux événements de minuterie suivant. Sauf si le composant est désactivé, une minuterie continue à recevoir le <xref:System.Windows.Forms.Timer.Tick> événement à intervalles réguliers à peu près égales.  
  
 Ce composant est conçu pour un environnement Windows Forms. Si vous avez besoin d’un minuteur adapté à un environnement de serveur, consultez l’article [Introduction aux minuteurs serveur](https://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).  
  
## <a name="the-interval-property"></a>La propriété d’intervalle  
 Le <xref:System.Windows.Forms.Timer.Interval%2A> propriété présente quelques limitations à prendre en compte lorsque vous programmez un <xref:System.Windows.Forms.Timer> composant :  
  
-   Si votre application ou une autre application effectue des demandes importantes sur le système, telles que les boucles longues, calculs complexes, ou le lecteur, réseau ou accès de port, votre application ne peut pas obtenir des événements de minuterie aussi souvent que le <xref:System.Windows.Forms.Timer.Interval%2A> propriété spécifie.  
  
-   L’intervalle n’est pas garanti s’écouler exactement le moment. Pour garantir l’exactitude, la minuterie doit vérifier l’horloge système en fonction des besoins, plutôt que d’essayer de suivre en interne le temps écoulé.  
  
-   La précision de la <xref:System.Windows.Forms.Timer.Interval%2A> propriété est exprimée en millisecondes. Certains ordinateurs fournissent un compteur haute résolution qui a une résolution supérieure aux millisecondes. La disponibilité de ce compteur varie selon le matériel de processeur de votre ordinateur. Pour plus d’informations, consultez l’article 172338, « Comment à utiliser QueryPerformanceCounter à temps Code », dans la Base de connaissances Microsoft à http://support.microsoft.com.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.Timer>  
 [Timer, composant](../../../../docs/framework/winforms/controls/timer-component-windows-forms.md)  
 [Vue d’ensemble du composant Timer](../../../../docs/framework/winforms/controls/timer-component-overview-windows-forms.md)
