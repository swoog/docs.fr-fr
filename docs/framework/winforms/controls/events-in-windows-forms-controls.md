---
title: Événements dans les contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: 41ad95de7a65dbd0cb3a0d1af8f5c8cb00c1ccdd
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59215884"
---
# <a name="events-in-windows-forms-controls"></a>Événements dans les contrôles Windows Forms
Un contrôle Windows Forms hérite plus de soixante événements de <xref:System.Windows.Forms.Control?displayProperty=nameWithType>. Ceux-ci incluent le <xref:System.Windows.Forms.Control.Paint> événement, ce qui provoque un contrôle est dessiné, les événements liés à l’affichage d’une fenêtre, comme le <xref:System.Windows.Forms.Control.Resize> et <xref:System.Windows.Forms.Control.Layout> événements et les événements de souris et clavier de bas niveau. Certains événements de bas niveau sont synthétisés par <xref:System.Windows.Forms.Control> en événements de sémantique comme <xref:System.Windows.Forms.Control.Click> et <xref:System.Windows.Forms.Control.DoubleClick>. Pour plus d’informations sur les événements hérités, consultez <xref:System.Windows.Forms.Control>.  
  
 Si votre contrôle personnalisé doit remplacer des fonctionnalités d’événements héritées, remplacez la méthode `On`*EventName* plutôt que d’attacher un délégué. Si le modèle d’événement dans le .NET Framework ne vous est pas familier, consultez la page [Déclencher des événements à partir d’un composant](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).  
  
## <a name="see-also"></a>Voir aussi

- [Remplacer la méthode OnPaint](overriding-the-onpaint-method.md)
- [Gestion des entrées utilisateur](handling-user-input.md)
- [Définition d’un événement](defining-an-event-in-windows-forms-controls.md)
- [Événements](../../../standard/events/index.md)
