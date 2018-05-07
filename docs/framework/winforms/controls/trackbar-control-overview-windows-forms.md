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
ms.openlocfilehash: d0a0cbbcc618e2fa52b3719bcc8f0135a1e0752e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="trackbar-control-overview-windows-forms"></a>Vue d'ensemble du contrôle TrackBar (Windows Forms)
Windows Forms <xref:System.Windows.Forms.TrackBar> contrôle (parfois également appelé contrôle « slider ») est utilisé pour naviguer dans une grande quantité d’informations ou d’ajuster visuellement un paramètre numérique. Le <xref:System.Windows.Forms.TrackBar> contrôle comporte deux parties : le curseur de défilement, également appelé un curseur et les marques de graduation. Le curseur est la partie qui peut être ajustée. Sa position correspond à la <xref:System.Windows.Forms.TrackBar.Value%2A> propriété. Les graduations sont des indicateurs visuels qui sont exécutées à intervalles réguliers. La barre de suivi se déplace dans les incréments que vous spécifiez. Par exemple, vous pouvez utiliser la barre de suivi pour contrôler la souris ou le taux de clignotement du curseur pour un système.  
  
## <a name="key-properties"></a>Propriétés de clé  
 Les propriétés de clé de la <xref:System.Windows.Forms.TrackBar> contrôle sont <xref:System.Windows.Forms.TrackBar.Value%2A>, <xref:System.Windows.Forms.TrackBar.TickFrequency%2A>, <xref:System.Windows.Forms.TrackBar.Minimum%2A>, et <xref:System.Windows.Forms.TrackBar.Maximum%2A>. <xref:System.Windows.Forms.TrackBar.TickFrequency%2A> correspond à l’espacement des graduations. <xref:System.Windows.Forms.TrackBar.Minimum%2A> et <xref:System.Windows.Forms.TrackBar.Maximum%2A> sont les valeurs minimale et maximale pouvant être représentées sur la barre de suivi.  
  
 Deux autres propriétés importantes sont <xref:System.Windows.Forms.TrackBar.SmallChange%2A> et <xref:System.Windows.Forms.TrackBar.LargeChange%2A>. La valeur de la <xref:System.Windows.Forms.TrackBar.SmallChange%2A> propriété est le nombre de positions le curseur se déplace en réponse à disposer de la touche gauche ou droite. La valeur de la <xref:System.Windows.Forms.TrackBar.LargeChange%2A> propriété est le nombre de positions le curseur se déplace en réponse lorsque la PAGE précédente ou PAGE suivante touche ou en réponse à la souris clique sur la barre de suivi de chaque côté du curseur.  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.Windows.Forms.TrackBar>  
 [TrackBar, contrôle](../../../../docs/framework/winforms/controls/trackbar-control-windows-forms.md)
