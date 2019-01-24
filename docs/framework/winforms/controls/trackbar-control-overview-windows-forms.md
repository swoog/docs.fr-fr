---
title: Vue d'ensemble du contrôle TrackBar (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- TrackBar
helpviewer_keywords:
- sliders [Windows Forms], about sliders
- TrackBar control [Windows Forms], about TrackBar control
- slider controls [Windows Forms], about slider controls
ms.assetid: 95910ecb-8a4c-4776-89fa-206c89ed6973
ms.openlocfilehash: 27a43befd69bc3fb33f8027bd32fc4d66414951c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54711997"
---
# <a name="trackbar-control-overview-windows-forms"></a>Vue d'ensemble du contrôle TrackBar (Windows Forms)
Les formulaires Windows <xref:System.Windows.Forms.TrackBar> contrôle (parfois appelé un contrôle « curseur ») est utilisé pour naviguer dans une grande quantité d’informations ou d’ajuster visuellement un paramètre numérique. Le <xref:System.Windows.Forms.TrackBar> contrôle comporte deux parties : le curseur de défilement, également appelé un curseur et les graduations. Le curseur est la partie qui peut être ajustée. Sa position correspond à la <xref:System.Windows.Forms.TrackBar.Value%2A> propriété. Les graduations sont des indicateurs visuels sont espacés à intervalles réguliers. La barre de suivi se déplace dans les incréments que vous spécifiez. Par exemple, vous pouvez utiliser la barre de suivi pour contrôler la vitesse ou la souris clignotement du curseur pour un système.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Les propriétés de clé de la <xref:System.Windows.Forms.TrackBar> contrôle sont <xref:System.Windows.Forms.TrackBar.Value%2A>, <xref:System.Windows.Forms.TrackBar.TickFrequency%2A>, <xref:System.Windows.Forms.TrackBar.Minimum%2A>, et <xref:System.Windows.Forms.TrackBar.Maximum%2A>. <xref:System.Windows.Forms.TrackBar.TickFrequency%2A> est l’espacement des graduations. <xref:System.Windows.Forms.TrackBar.Minimum%2A> et <xref:System.Windows.Forms.TrackBar.Maximum%2A> sont les valeurs minimale et maximale pouvant être représentées sur la barre de suivi.  
  
 Deux autres propriétés importantes sont <xref:System.Windows.Forms.TrackBar.SmallChange%2A> et <xref:System.Windows.Forms.TrackBar.LargeChange%2A>. La valeur de la <xref:System.Windows.Forms.TrackBar.SmallChange%2A> propriété est le nombre de positions le curseur se déplace en réponse à avoir la touche gauche ou flèche droite. La valeur de la <xref:System.Windows.Forms.TrackBar.LargeChange%2A> propriété est le nombre de positions le curseur se déplace en réponse à avoir la touche Pg préc ou Pg suiv enfoncée, ou en réponse à la souris clique sur la barre de suivi de chaque côté du curseur de défilement.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Windows.Forms.TrackBar>
- [TrackBar, contrôle](../../../../docs/framework/winforms/controls/trackbar-control-windows-forms.md)
